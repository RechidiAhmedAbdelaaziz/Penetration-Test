# **DNS Footprinting & Enumeration - Pentesting Notes**

## **1. Key Concepts**
### **DNS Basics**
- Translates domain names (e.g., `example.com`) → IP addresses (e.g., `93.184.216.34`).
- Distributed system (no central database).
- Uses different server types:
  - **Root servers** (13 globally) → Manage TLDs (`.com`, `.net`).
  - **Authoritative servers** → Official source for a domain’s records.
  - **Recursive resolvers** (e.g., `8.8.8.8`) → Cache responses for faster queries.
  - **Forwarding servers** → Pass queries to another DNS server.

### **DNS Record Types**
| Record | Purpose | Example |
|--------|---------|---------|
| `A` | IPv4 address | `example.com → 192.0.2.1` |
| `AAAA` | IPv6 address | `example.com → 2606:2800:220:1:248:1893:25c8:1946` |
| `MX` | Mail servers | `mail.example.com` |
| `NS` | Nameservers for the domain | `ns1.example.com` |
| `TXT` | Arbitrary text (SPF, DKIM, verification) | `"v=spf1 include:_spf.google.com ~all"` |
| `CNAME` | Alias (points to another domain) | `www.example.com → example.com` |
| `PTR` | Reverse DNS (IP → domain) | `1.2.3.4 → example.com` |
| `SOA` | Zone authority (admin email, serial #) | `admin.example.com` |

---

## **2. DNS Footprinting Methodology**
### **Step 1: Basic DNS Queries**
```bash
# Get A record (IPv4)
dig example.com  
dig example.com @8.8.8.8  # Query specific DNS server

# Get all records (if allowed)
dig any example.com

# Get nameservers (NS)
dig ns example.com

# Get mail servers (MX)
dig mx example.com

# Get TXT records (SPF, verification)
dig txt example.com
```

### **Step 2: Check for Zone Transfer (AXFR)**
```bash
# Attempt zone transfer
dig axfr example.com @ns1.example.com

# If successful → Lists ALL records (subdomains, IPs, internal hosts)
```

### **Step 3: Brute-Force Subdomains**
```bash
# Using wordlist (SecLists)
for sub in $(cat subdomains.txt); do dig $sub.example.com +short; done

# Using dnsenum
dnsenum --dnsserver 8.8.8.8 -f subdomains.txt example.com
```

### **Step 4: Check DNS Server Version**
```bash
# BIND version leak (if enabled)
dig CH TXT version.bind @dns-server
```

---

## **3. Common Attacks & Misconfigurations**
### **Dangerous DNS Settings**
| Misconfiguration | Risk |
|------------------|------|
| `allow-transfer: any;` | Open zone transfer (AXFR) leaks all records |
| `allow-query: any;` | Allows public DNS queries (info disclosure) |
| No rate limiting | DNS amplification attacks possible |

### **Exploitable Scenarios**
1. **Open Zone Transfer** → Dump all DNS records (subdomains, internal IPs).
2. **Subdomain Takeover** → If a CNAME points to a deleted cloud service.
3. **Cache Poisoning** → Redirect users to malicious sites.
4. **DNS Tunneling** → Exfiltrate data via DNS queries.

---

## **4. Defensive Measures**
### **Secure DNS Best Practices**
- **Restrict zone transfers** (`allow-transfer: trusted-IP;`).
- **Disable version.bind** → Prevents DNS server version leaks.
- **Use DNSSEC** → Prevents DNS spoofing.
- **Enable rate limiting** → Mitigates DDoS attacks.
- **Monitor logs** → Detect unusual AXFR requests.

### **Encrypted DNS**
- **DoT (DNS over TLS)** → Encrypts DNS traffic (port 853).
- **DoH (DNS over HTTPS)** → Hides DNS in HTTPS traffic.

---

## **5. Practical Examples**
### **Lab Exercise: Find Subdomains**
```bash
# Using dig + wordlist
for sub in $(cat subdomains-top1000.txt); do 
  if dig $sub.example.com +short | grep -v "NXDOMAIN"; then 
    echo "[+] Found: $sub.example.com"; 
  fi; 
done
```

### **Real-World Pentest Scenario**
1. Find nameservers:  
   ```bash
   dig ns example.com
   ```
2. Check for AXFR:  
   ```bash
   dig axfr example.com @ns1.example.com
   ```
3. If AXFR fails → Brute-force subdomains:  
   ```bash
   dnsenum example.com
   ```
4. Check for SPF/DMARC misconfigurations:  
   ```bash
   dig txt example.com
   ```

---

## **6. Cheatsheet**
| Command | Purpose |
|---------|---------|
| `dig example.com` | Basic DNS lookup |
| `dig any example.com` | Get all available records |
| `dig ns example.com` | Find nameservers |
| `dig mx example.com` | Find mail servers |
| `dig axfr example.com @ns1` | Attempt zone transfer |
| `dig CH TXT version.bind @dns` | Check DNS server version |
| `dnsenum example.com` | Automated subdomain brute-forcing |

---

## **7. Checklist for Labs**
✅ Perform basic DNS queries (`A`, `MX`, `NS`, `TXT`).  
✅ Test for open zone transfers (`AXFR`).  
✅ Brute-force subdomains (`dnsenum`, `dig + wordlist`).  
✅ Check for DNS server version leaks (`version.bind`).  
✅ Verify SPF/DMARC records (`dig txt`).  

---

### **Final Notes**
- **DNS is a goldmine** for recon (subdomains, internal IPs, emails).
- **Always check AXFR** → Often misconfigured in internal networks.
- **Use multiple tools** (`dig`, `dnsenum`, `nslookup`).  

🚀 **Happy Hacking!** 🚀