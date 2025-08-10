# MSSQL Pentest Study & Application Notes

## Overview
- **MSSQL** (Microsoft SQL Server): Closed-source RDBMS, primarily on Windows, strong .NET integration.
- **Common Clients:**  
    - SQL Server Management Studio (SSMS)
    - mssql-cli
    - SQL Server PowerShell
    - HeidiSQL
    - SQLPro
    - Impacket's mssqlclient.py (useful for pentesters)

## Default System Databases

| Database   | Description                                                        |
|------------|--------------------------------------------------------------------|
| master     | Tracks all system info for SQL server instance                     |
| model      | Template for new databases                                         |
| msdb       | Used by SQL Server Agent for jobs & alerts                         |
| tempdb     | Stores temporary objects                                           |
| resource   | Read-only, contains system objects                                 |

## Default Configuration
- Service runs as `NT SERVICE\MSSQLSERVER`
- **Windows Authentication** is common (uses local SAM or AD)
- **Encryption not enforced by default**
- Saved credentials in SSMS may be found on admin/dev systems

## Dangerous Settings & Misconfigurations
- No encryption for client connections
- Use of spoofable self-signed certificates
- Named pipes enabled
- Weak/default `sa` credentials (often forgotten)

## Footprinting MSSQL

### Nmap Scripts
```bash
sudo nmap --script ms-sql-info,ms-sql-empty-password,ms-sql-xp-cmdshell,ms-sql-config,ms-sql-ntlm-info,ms-sql-tables,ms-sql-hasdbaccess,ms-sql-dac,ms-sql-dump-hashes \
    --script-args mssql.instance-port=1433,mssql.username=sa,mssql.password=,mssql.instance-name=MSSQLSERVER \
    -sV -p 1433 <target-ip>
```
- Reveals: hostname, instance name, version, named pipes, etc.

### Metasploit
```bash
use auxiliary/scanner/mssql/mssql_ping
set RHOSTS <target-ip>
run
```
- Reveals: ServerName, InstanceName, Version, TCP port, Named pipe

### Impacket mssqlclient.py
```bash
python3 mssqlclient.py <domain>/<user>@<target-ip> -windows-auth
# or
python3 mssqlclient.py <user>:<password>@<target-ip>
```
- Once connected, enumerate databases:
```sql
select name from sys.databases
```

## Cheatsheet

| Tool/Command                        | Purpose                        |
|------------------------------------- |--------------------------------|
| `locate mssqlclient`                 | Find Impacket client           |
| `nmap -p 1433 --script ...`          | MSSQL enumeration              |
| `msfconsole > mssql_ping`            | MSSQL info via Metasploit      |
| `mssqlclient.py`                     | Connect to MSSQL               |
| `select name from sys.databases`     | List databases                 |

## Attack & Defense Procedures

### Enumeration
- Scan with Nmap scripts for version, config, and weak creds
- Use Metasploit's `mssql_ping`
- Attempt connection with Impacket's mssqlclient.py

### Exploitation
- Try default/weak `sa` credentials
- Abuse misconfigurations (e.g., xp_cmdshell if enabled)

### Post-Exploitation
- Enumerate users, roles, and permissions
- Search for sensitive data in databases
- Attempt lateral movement if Windows Auth is used

### Defense/Mitigation
- Enforce encrypted connections
- Disable/rename `sa` account
- Use strong, unique passwords
- Restrict named pipes and unnecessary features
- Regularly audit permissions and configurations

## Practical Tips
- Always check for saved credentials in SSMS on compromised hosts
- Named pipes can be a lateral movement vector
- Default ports and settings are common in real-world targets

## Checklist

- [ ] Nmap MSSQL scripts run
- [ ] Metasploit mssql_ping scan
- [ ] Attempted connection with mssqlclient.py
- [ ] Enumerated databases and users
- [ ] Checked for xp_cmdshell and dangerous features
- [ ] Documented findings and recommended mitigations
