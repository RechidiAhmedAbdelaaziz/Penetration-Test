# Nmap Performance Notes

## Key Performance Options

- **Timing template:** `-T <0-5>` (0=paranoid, 5=insane)
- **Parallelism:** `--min-parallelism <num>`
- **Timeouts:** `--initial-rtt-timeout <time>`, `--max-rtt-timeout <time>`
- **Rate:** `--min-rate <num>`
- **Retries:** `--max-retries <num>`

---

## Timeouts

- RTT = Round-Trip-Time (response wait time)
- Default: `--min-rtt-timeout 100ms`
- Lowering timeouts speeds up scans but may miss hosts.

**Example:**
```bash
sudo nmap 10.129.2.0/24 -F --initial-rtt-timeout 50ms --max-rtt-timeout 100ms
```

---

## Max Retries

- Default: `--max-retries 10`
- Lower = faster, but may miss open ports.

**Example:**
```bash
sudo nmap 10.129.2.0/24 -F --max-retries 0
```

---

## Packet Rate

- `--min-rate <num>`: minimum packets/sec
- Useful when bandwidth is known/whitelisted.

**Example:**
```bash
sudo nmap 10.129.2.0/24 -F --min-rate 300
```

---

## Timing Templates

- `-T 0`: paranoid
- `-T 1`: sneaky
- `-T 2`: polite
- `-T 3`: normal (default)
- `-T 4`: aggressive
- `-T 5`: insane

**Example:**
```bash
sudo nmap 10.129.2.0/24 -F -T 5
```

---

## Notes

- Faster scans = higher chance of missing hosts/ports.
- Aggressive scans may trigger security systems.
- More: [Nmap Performance Docs](https://nmap.org/book/man-performance.html)
