# Nmap Host Discovery Notes

## Overview

-   **Purpose:** Identify live hosts on a network before further testing.
-   **Tools:** Nmap with various host discovery options.
-   **Best Practice:** Save all scan results for documentation and comparison.

---

## Common Nmap Options

| Option               | Description                        |
| -------------------- | ---------------------------------- |
| `-sn`                | Host discovery only (no port scan) |
| `-oA <name>`         | Save results in all formats        |
| `-iL <file>`         | Scan IPs from a file               |
| `-PE`                | Use ICMP Echo requests             |
| `--packet-trace`     | Show sent/received packets         |
| `--reason`           | Show reason for host status        |
| `--disable-arp-ping` | Disable ARP ping, use ICMP only    |

---

## Scanning Methods

### 1. Scan Entire Network Range

| Command                                | Description                                                      |
| -------------------------------------- | ---------------------------------------------------------------- |
| `sudo nmap 10.129.2.0/24 -sn -oA tnet` | Scan all hosts in the subnet, host discovery only, save results. |
| `grep for \| cut -d" " -f5`            | Extract live IPs from output.                                  |

---

### 2. Scan from IP List

Prepare a file `hosts.lst`:

```
10.129.2.4
10.129.2.10
...
```

| Command                                | Description                                            |
| -------------------------------------- | ------------------------------------------------------ | ----------------------------- |
| `sudo nmap -sn -oA tnet -iL hosts.lst` | Scan IPs from file, host discovery only, save results. |
| `grep for                              | cut -d" " -f5`                                         | Extract live IPs from output. |

---

### 3. Scan Multiple IPs

| Command                                                      | Description                                           |
| ------------------------------------------------------------ | ----------------------------------------------------- |
| `sudo nmap -sn -oA tnet 10.129.2.18 10.129.2.19 10.129.2.20` | Scan specific IPs, host discovery only, save results. |
| `sudo nmap -sn -oA tnet 10.129.2.18-20`                      | Scan IP range, host discovery only, save results.     |

---

### 4. Scan Single IP

| Command                              | Description                                        |
| ------------------------------------ | -------------------------------------------------- |
| `sudo nmap 10.129.2.18 -sn -oA host` | Scan single IP, host discovery only, save results. |

---

## Advanced Options

### ICMP Echo Request (Ping Scan)

| Command                                                 | Description                                |
| ------------------------------------------------------- | ------------------------------------------ |
| `sudo nmap 10.129.2.18 -sn -oA host -PE --packet-trace` | Use ICMP Echo requests, show packet trace. |

### Show Reason for Host Status

| Command                                           | Description                  |
| ------------------------------------------------- | ---------------------------- |
| `sudo nmap 10.129.2.18 -sn -oA host -PE --reason` | Show reason for host status. |

### Disable ARP Ping

| Command                                                                    | Description                                         |
| -------------------------------------------------------------------------- | --------------------------------------------------- |
| `sudo nmap 10.129.2.18 -sn -oA host -PE --packet-trace --disable-arp-ping` | Use ICMP only, disable ARP ping, show packet trace. |
