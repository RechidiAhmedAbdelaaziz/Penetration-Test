## Key Concepts

-   **IMAP (Internet Message Access Protocol)**

    -   Ports: 143 (unencrypted), 993 (SSL/TLS)
    -   Server-side email management: folders, multiple clients, synchronization
    -   Text-based protocol, supports concurrent connections
    -   Emails remain on server until deleted

-   **POP3 (Post Office Protocol v3)**

    -   Ports: 110 (unencrypted), 995 (SSL/TLS)
    -   Downloads emails to client, minimal server-side management
    -   Simpler protocol, less functionality than IMAP

-   **Security**
    -   Credentials sent in plaintext unless SSL/TLS is used
    -   Use SSL/TLS (ports 993/995) for secure communication
    -   Misconfigurations can expose sensitive data or allow unauthorized access

---

## Cheatsheet: Enumeration & Interaction

### Nmap Service Detection

```bash
nmap -sV -p110,143,993,995 <target>
```

-   Detects IMAP/POP3 services and versions
-   Use `-sC` for default scripts to enumerate capabilities and SSL cert info

### IMAP Commands (Manual Interaction)

| Command                 | Description             |
| ----------------------- | ----------------------- |
| `1 LOGIN <user> <pass>` | Authenticate user       |
| `1 LIST "" *`           | List all mailboxes      |
| `1 SELECT INBOX`        | Select INBOX for access |
| `1 FETCH <ID> all`      | Retrieve message data   |
| `1 LOGOUT`              | Close connection        |

### POP3 Commands (Manual Interaction)

| Command           | Description             |
| ----------------- | ----------------------- |
| `USER <username>` | Specify username        |
| `PASS <password>` | Specify password        |
| `STAT`            | Get mailbox statistics  |
| `LIST`            | List messages and sizes |
| `RETR <id>`       | Retrieve message by ID  |
| `DELE <id>`       | Delete message by ID    |
| `QUIT`            | Close connection        |

### SSL/TLS Encrypted Interaction

-   **IMAP (993):**
    ```bash
    openssl s_client -connect <target>:993
    ```
-   **POP3 (995):**
    ```bash
    openssl s_client -connect <target>:995
    ```

### cURL for IMAP

```bash
curl -k 'imaps://<target>' --user <user>:<pass>
curl -k 'imaps://<target>' --user <user>:<pass> -v
```

---

## Attack & Defense Procedures

### Enumeration

-   Scan for open ports (110, 143, 993, 995)
-   Use Nmap scripts to enumerate capabilities and SSL certs
-   Identify server software/version and supported authentication methods

### Exploitation

-   Test for weak/default credentials (e.g., username = password)
-   Attempt login via IMAP/POP3 using tools or manual commands
-   Enumerate mailboxes and retrieve messages if access is gained

### Post-Exploitation

-   Download and analyze emails for sensitive data
-   Attempt to send emails (if permitted)
-   Check for configuration weaknesses (e.g., anonymous login, verbose logging)

### Defense & Mitigation

-   Enforce SSL/TLS for all connections
-   Disable plaintext authentication
-   Use strong, unique passwords
-   Limit login attempts and monitor logs
-   Regularly update and patch mail server software

---

## Practical Examples

-   **Nmap scan:**
    ```bash
    nmap -sV -p110,143,993,995 -sC <target>
    ```
-   **Manual IMAP login:**
    ```bash
    openssl s_client -connect <target>:993
    1 LOGIN user password
    1 LIST "" *
    ```
-   **Manual POP3 login:**
    ```bash
    openssl s_client -connect <target>:995
    USER user
    PASS password
    LIST
    ```

---

## Troubleshooting Tips

-   If SSL/TLS fails, try unencrypted ports (143/110) for testing (never in production)
-   Use `-v` with cURL or `-d` with Nmap for verbose/debug output
-   Check for self-signed certificates and certificate warnings

---

## Best Practices & Common Pitfalls

-   Always use encrypted connections in production
-   Avoid default or weak credentials
-   Regularly audit server configurations for dangerous settings (e.g., `auth_debug`, `auth_anonymous_username`)
-   Monitor for unauthorized access attempts

---

## Checklist for Hands-On Labs

-   [ ] Scan target for IMAP/POP3 ports
-   [ ] Enumerate service banners and capabilities
-   [ ] Attempt login with known/weak credentials
-   [ ] Retrieve and analyze mailbox contents
-   [ ] Document findings and recommend mitigations

---
