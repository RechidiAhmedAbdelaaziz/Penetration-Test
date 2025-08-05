## Overview

-   **SNMP (Simple Network Management Protocol):** Used for monitoring and managing network devices (routers, switches, servers, IoT, etc.).
-   **Versions:**
    -   **SNMPv1:** No authentication or encryption.
    -   **SNMPv2c:** Community-based, still no encryption.
    -   **SNMPv3:** Adds authentication and encryption (recommended).
-   **Ports:**
    -   UDP 161 (queries/commands)
    -   UDP 162 (traps/notifications)
-   **MIB (Management Information Base):**
    -   Text files describing device objects in a tree structure.
    -   Each object has an OID (Object Identifier).

---

## Key Concepts

-   **Community Strings:** Act as passwords for SNMP access (`public`, `private` are common defaults).
-   **OIDs:** Numeric identifiers for SNMP objects (e.g., `.1.3.6.1.2.1.1.1.0`).
-   **Traps:** Unsolicited notifications from SNMP agents to managers.

---

## Common SNMP Daemon Config (`/etc/snmp/snmpd.conf`)

```bash
sysLocation    <location>
sysContact     <contact>
sysServices    <services>
agentaddress   127.0.0.1,[::1]
rocommunity    public default -V systemonly
rouser         authPrivUser authpriv -V systemonly
```

---

## Dangerous Settings

| Setting                        | Description                                |
| ------------------------------ | ------------------------------------------ |
| `rwuser noauth`                | Full OID tree access, no authentication    |
| `rwcommunity <string> <IPv4>`  | Full OID tree access from any IPv4 address |
| `rwcommunity6 <string> <IPv6>` | Same as above, but for IPv6                |

---

## Enumeration & Attack Methodology

### 1. Service Discovery

-   Scan for UDP 161/162 (e.g., with `nmap`):
    ```bash
    nmap -sU -p 161,162 <target>
    ```

### 2. Community String Brute-Force

-   Use `onesixtyone` with SecLists:
    ```bash
    onesixtyone -c /path/to/snmp.txt <target>
    ```

### 3. SNMP Data Extraction

-   **snmpwalk:** Enumerate SNMP data with known community string.
    ```bash
    snmpwalk -v2c -c public <target>
    ```
-   **braa:** Brute-force OIDs.
    ```bash
    braa <community>@<IP>:.1.3.6.*
    ```

### 4. Analyze Output

-   Look for:
    -   System info (OS, hostname, contact, location)
    -   Installed software/packages
    -   Network interfaces and routing info
    -   Usernames, process lists, running services

---

## Cheatsheet

| Tool        | Usage Example                      | Purpose                       |
| ----------- | ---------------------------------- | ----------------------------- |
| snmpwalk    | `snmpwalk -v2c -c public <target>` | Enumerate SNMP data           |
| onesixtyone | `onesixtyone -c snmp.txt <target>` | Brute-force community strings |
| braa        | `braa public@<target>:.1.3.6.*`    | Brute-force OIDs              |
| nmap        | `nmap -sU -p 161,162 <target>`     | Discover SNMP services        |

---

## Practical Example

```bash
# Discover SNMP service
nmap -sU -p 161 <target>

# Brute-force community strings
onesixtyone -c /usr/share/seclists/Discovery/SNMP/snmp.txt <target>

# Enumerate SNMP data
snmpwalk -v2c -c public <target>

# Brute-force OIDs
braa public@<target>:.1.3.6.*
```

---

## Troubleshooting Tips

-   SNMP may be firewalled or bound to localhost only.
-   Community strings may be non-standard; try custom wordlists.
-   SNMPv3 requires username/password and encryption keys.

---

## Best Practices & Mitigation

-   **Use SNMPv3** with authentication and encryption.
-   **Restrict access** to trusted IPs only.
-   **Change default community strings** (`public`, `private`).
-   **Disable SNMP if not needed.**
-   **Monitor SNMP logs** for unauthorized access attempts.

---

## Common Pitfalls

-   Relying on default or weak community strings.
-   Exposing SNMP to the internet.
-   Not upgrading to SNMPv3.

---

## Not Applicable to Real-World/Certs

-   Brute-forcing SNMPv3 credentials is rarely practical due to complexity.

---

## Hands-On Checklist

-   [ ] Scan for SNMP (UDP 161/162)
-   [ ] Brute-force community strings
-   [ ] Enumerate SNMP data (snmpwalk, braa)
-   [ ] Identify sensitive info (users, software, configs)
-   [ ] Document findings and recommend mitigations

---

## References

-   [SNMP RFC1157](https://datatracker.ietf.org/doc/html/rfc1157)
-   [Net-SNMP Documentation](http://www.net-snmp.org/docs/man/snmpd.conf.html)
-   [Object Identifier Registry](https://www.alvestrand.no/objectid/)
-   [SecLists SNMP Wordlists](https://github.com/danielmiessler/SecLists)
