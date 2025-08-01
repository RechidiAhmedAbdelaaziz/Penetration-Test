
## Purpose
Passive domain info gathering helps understand a company's online presence, technologies, and structure without direct interaction.

## Key Steps

1. **Review Main Website**
    - Note offered services and implied technologies.

2. **Certificate Transparency**
    - Use [crt.sh](https://crt.sh/) to find subdomains via SSL certificates.
    - Example:  
      ```bash
      curl -s https://crt.sh/?q=domain.com&output=json | jq .
      ```

3. **Identify Company-Hosted Servers**
    - Resolve subdomains to IPs, filter out third-party hosts.
    - Example:  
      ```bash
      for i in $(cat subdomainlist); do host $i; done
      ```

4. **Shodan Lookup**
    - Investigate IPs for open ports/services.
    - Example:  
      ```bash
      for i in $(cat ip-addresses.txt); do shodan host $i; done
      ```

5. **DNS Records**
    - Use `dig` to find A, MX, NS, TXT, SOA records.
    - Example:  
      ```bash
      dig any domain.com
      ```

## What to Look For

- **A records:** Direct IPs for domains.
- **MX records:** Email providers (e.g., Google, Outlook).
- **NS records:** Name servers, hosting providers.
- **TXT records:** Verification keys, SPF/DMARC/DKIM info, third-party integrations (Atlassian, LogMeIn, Mailgun, etc.).

## Useful Links
- [crt.sh](https://crt.sh/)
- [Shodan](https://www.shodan.io/)
- [OSINT: Corporate Recon](https://academy.hackthebox.com/course/preview/osint-corporate-recon)

## Notes
- Focus on what is visible and implied.
- Document third-party services and technologies for further investigation.
- Skip testing third-party hosted assets without permission.
