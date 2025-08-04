# SMTP Penetration Testing Cheatsheet

## 1. Key Concepts

-   **SMTP (Simple Mail Transfer Protocol):** Protocol for sending emails over IP networks.
-   **Ports:** Default is TCP 25; others include 587 (submission, STARTTLS), 465 (SSL/TLS).
-   **Components:**
    -   **MUA:** Mail User Agent (client)
    -   **MSA:** Mail Submission Agent (relay)
    -   **MTA:** Mail Transfer Agent (server)
    -   **MDA:** Mail Delivery Agent (delivers to mailbox)
-   **Security Concerns:**
    -   Transmits data in plaintext unless SSL/TLS is used.
    -   Open relays can be abused for spam and spoofing.
    -   Lack of sender authentication by default.

## 2. Methodologies

### Enumeration

-   Identify open SMTP ports (25, 587, 465).
-   Use banner grabbing and command enumeration.
-   Test for open relay and user enumeration.

### Exploitation

-   Abuse open relay to send spoofed emails.
-   Enumerate valid users with VRFY/EXPN.
-   Attempt to intercept or manipulate email flow.

### Post-Exploitation

-   Analyze email headers for sensitive info.
-   Attempt lateral movement via phishing or credential reuse.

### Defense

-   Harden SMTP configuration.
-   Restrict relay access.
-   Enforce authentication and encryption.

## 3. SMTP Commands & Usage

| Command    | Description                          | Example Usage                 |
| ---------- | ------------------------------------ | ----------------------------- |
| HELO/EHLO  | Start session, identify client       | `HELO mail.example.com`       |
| MAIL FROM  | Specify sender                       | `MAIL FROM:<user@domain.tld>` |
| RCPT TO    | Specify recipient                    | `RCPT TO:<user@domain.tld>`   |
| DATA       | Begin email content                  | `DATA`                        |
| VRFY       | Verify if user exists                | `VRFY username`               |
| EXPN       | Expand mailing list                  | `EXPN listname`               |
| RSET       | Reset session                        | `RSET`                        |
| NOOP       | No operation, keep connection alive  | `NOOP`                        |
| QUIT       | End session                          | `QUIT`                        |
| AUTH PLAIN | Authenticate client (after STARTTLS) | `AUTH PLAIN <base64-creds>`   |

## 4. Tools & Commands

### Enumeration

```bash
# Nmap default scripts and version detection
nmap -sC -sV -p25 <target>

# Nmap SMTP command enumeration
nmap --script smtp-commands -p25 <target>

# Nmap open relay test
nmap --script smtp-open-relay -p25 <target> -v

# Banner grabbing with Netcat or Telnet
telnet <target> 25
nc <target> 25
```

### Manual Interaction

```bash
telnet <target> 25
EHLO test
VRFY root
MAIL FROM:<attacker@evil.com>
RCPT TO:<victim@target.com>
DATA
Subject: Test
This is a test.
.
QUIT
```

### Sending Email via Command Line

```bash
telnet <target> 25
EHLO domain.com
MAIL FROM:<attacker@evil.com>
RCPT TO:<victim@target.com>
DATA
From: attacker@evil.com
To: victim@target.com
Subject: Test
Date: <date>
Message body here.
.
QUIT
```

### Proxying SMTP via HTTP Proxy

```bash
CONNECT <target>:25 HTTP/1.0
```

## 5. Attack Procedures

### 1. Service Discovery

-   Scan for open SMTP ports (25, 587, 465).
-   Identify service and version.

### 2. Banner Grabbing & Command Enumeration

-   Connect via telnet/nc.
-   Use EHLO/HELO to enumerate supported commands.

### 3. User Enumeration

-   Use VRFY/EXPN to check for valid users.
-   Note: Some servers always return code 252 (cannot verify user).

### 4. Open Relay Testing

-   Attempt to send email from external to external address.
-   Use Nmap `smtp-open-relay` script for automated testing.

### 5. Exploitation

-   If open relay, send spoofed emails.
-   Attempt phishing or social engineering.

### 6. Post-Exploitation

-   Analyze mail headers for internal IPs, software, timestamps.
-   Look for sensitive info in mail content.

## 6. Defense Procedures

-   Restrict `mynetworks` to trusted IP ranges.
-   Require authentication for mail submission.
-   Enforce STARTTLS/SSL for encryption.
-   Disable VRFY/EXPN if not needed.
-   Implement SPF, DKIM, DMARC for sender validation.
-   Regularly audit SMTP configuration.
