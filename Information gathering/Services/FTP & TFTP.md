# FTP & TFTP - Pentest Notes

## FTP (File Transfer Protocol)
- Runs on TCP ports **21** (control) and **20** (data).
- **Active vs Passive mode**: Passive helps bypass client firewalls.
- **Clear-text protocol**: Credentials and data can be sniffed.
- **Anonymous FTP**: Sometimes enabled, allows access without credentials.
- Useful FTP commands: `ls`, `get`, `put`, `status`, `debug`, `trace`.
- **Directory listing** and file manipulation possible.
- **Recursive listing** (`ls -R`) for full directory structure.
- **Upload/Download**: Can exploit LFI/RCE if web server syncs files.
- **FTP Banner**: Reveals service/version info.
- **Config files**:
    - `/etc/vsftpd.conf`: Main config, check for dangerous settings.
    - `/etc/ftpusers`: Users denied FTP access.
- **Dangerous settings**:
    - `anonymous_enable=YES`
    - `anon_upload_enable=YES`
    - `anon_mkdir_write_enable=YES`
    - `no_anon_password=YES`
    - `write_enable=YES`
    - `hide_ids=YES` (hides real usernames)
    - `ls_recurse_enable=YES`
- **FTP logs**: Can be abused for RCE.
- **SSL/TLS**: Use `openssl s_client` to inspect certificates for hostnames/emails.

## TFTP (Trivial File Transfer Protocol)
- Runs on **UDP** (unreliable, no authentication).
- No user authentication, limited to globally shared files.
- **Commands**: `connect`, `get`, `put`, `quit`, `status`, `verbose`.
- No directory listing.
- Only use in local/protected networks.

## Enumeration & Footprinting
- **Nmap**:
    - Scan FTP: `nmap -sV -p21 -sC -A <target>`
    - NSE scripts: `/usr/share/nmap/scripts/ftp-*`
        - `ftp-anon.nse`: Checks anonymous access.
        - `ftp-brute.nse`: Brute-force credentials.
        - `ftp-syst.nse`: Server status/version.
        - `ftp-vsftpd-backdoor.nse`: Checks for known backdoor.
    - Script trace: `--script-trace` for detailed interaction.
- **Other tools**: `nc`, `telnet`, `wget -m` (mirror/download all files).

## Pentest Actions
- Check for **anonymous login** and **write permissions**.
- **Download all files** for offline analysis.
- **Upload files** to test for LFI/RCE/webshell possibilities.
- **Enumerate users** (unless `hide_ids=YES`).
- **Inspect FTP banners** for version/service info.
- **Check SSL certs** for hostnames/emails.
- Use **Nmap NSE scripts** for vulnerability checks.
- **Review config files** for misconfigurations.
- **Monitor FTP logs** for possible attack vectors.

---
**Always check for misconfigurations, weak permissions, and exposed sensitive data.**