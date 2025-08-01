# Firewall and IDS/IPS Evasion (Nmap)

## Firewalls
- Block/allow network traffic based on rules.
- **Dropped** packets: ignored, no response.
- **Rejected** packets: RST flag or ICMP error (e.g., Net/Host/Port Unreachable).

## IDS/IPS
- **IDS**: Detects and reports suspicious activity.
- **IPS**: Blocks/prevents attacks automatically.
- Detection is harder than firewalls; use multiple VPS/IPs to test.

## Nmap Evasion Techniques

### Scanning Methods
- **SYN Scan (`-sS`)**: Standard, easily detected/blocked.
- **ACK Scan (`-sA`)**: Sends ACK packets, harder for firewalls/IDS to filter.
- **Decoys (`-D RND:5`)**: Spoofs source IPs to hide real one.
- **Source IP (`-S <ip>`)**: Specify source IP for scan.
- **Source Port (`--source-port 53`)**: Use trusted ports (e.g., DNS 53) to bypass filters.

### Useful Nmap Options
| Option                | Description                                 |
|-----------------------|---------------------------------------------|
| `-p <ports>`          | Scan specific ports                         |
| `-sS`                 | SYN scan                                    |
| `-sA`                 | ACK scan                                    |
| `-Pn`                 | No ping                                     |
| `-n`                  | No DNS resolution                           |
| `--disable-arp-ping`  | Disable ARP ping                            |
| `--packet-trace`      | Show sent/received packets                  |
| `-D RND:5`            | Use 5 random decoy IPs                      |
| `-O`                  | OS detection                                |
| `-S <ip>`             | Use specific source IP                      |
| `-e <iface>`          | Use specific network interface              |
| `--source-port <port>`| Use specific source port                    |

### Example Scenarios

#### SYN vs ACK Scan
- SYN scan: Open ports reply with SYN-ACK; filtered ports may not reply.
- ACK scan: Open/closed ports reply with RST; filtered ports may not reply.

#### Decoy Scan
```bash
sudo nmap <target> -p 80 -sS -Pn -n --disable-arp-ping --packet-trace -D RND:5
```
- Hides your real IP among decoys.

#### Source IP/Port Scan
```bash
sudo nmap <target> -n -Pn -p 445 -O -S <spoofed-ip> -e <iface>
sudo nmap <target> -p50000 -sS -Pn -n --disable-arp-ping --packet-trace --source-port 53
```
- Use trusted IP/port to bypass filters.

#### Netcat Example (Bypass with Source Port)
```bash
ncat -nv --source-port 53 <target> <port>
```

## DNS Proxying
- Nmap does reverse DNS by default.
- Use `--dns-server <ns>` to specify DNS server.
- Use `--source-port 53` to mimic DNS traffic and bypass firewalls.

---

**Tip:** Always monitor responses (flags, ICMP errors) to infer filtering and evasion success.