# SMB (Server Message Block)

## Summary & Key Concepts

### What is SMB?

-   **Server Message Block (SMB)** is a client-server, request-response protocol used for sharing access to files, printers, serial ports, and other resources on a network.
-   It can also handle inter-process communication.
-   Primarily used by Windows operating systems, but available on Linux/Unix via **Samba**.
-   Operates over TCP/IP, typically using port 445. Older implementations might use NetBIOS over TCP/IP on ports 137-139.

### Samba & CIFS

-   **Samba**: A free software re-implementation of the SMB networking protocol that allows Linux/Unix systems to integrate and communicate with Windows networks.  
    -   [Samba `smb.conf` Man Page](https://www.samba.org/samba/docs/current/man-html/smb.conf.5.html)  
    -   [Samba `rpcclient` Man Page](https://www.samba.org/samba/docs/current/man-html/rpcclient.1.html)
-   **CIFS (Common Internet File System)**: A specific dialect of SMB, created by Microsoft. It is often considered synonymous with **SMBv1**. Modern systems use newer, more secure versions of SMB.

### SMB Versions

| **SMB Version** | **Supported In**                   | **Key Features**                                                        |
| --------------- | ---------------------------------- | ----------------------------------------------------------------------- |
| CIFS / SMB 1.0  | Windows NT 4.0 / Windows 2000      | Communication via NetBIOS; direct connection via TCP. (Outdated)        |
| SMB 2.0         | Windows Vista, Windows Server 2008 | Performance upgrades, improved message signing, caching.                |
| SMB 2.1         | Windows 7, Windows Server 2008 R2  | Locking mechanisms.                                                     |
| SMB 3.0         | Windows 8, Windows Server 2012     | Multichannel connections, end-to-end encryption, remote storage access. |
| SMB 3.1.1       | Windows 10, Windows Server 2016    | Pre-authentication integrity checking, AES-128-GCM encryption.          |

### NetBIOS & Workgroups

-   **Workgroup**: A logical grouping of computers on a network for organizational purposes.
-   **NetBIOS (Network Basic Input/Output System)**: An API that provides services allowing applications on separate computers to communicate over a local area network. It handles name registration and resolution on the network.
-   **NBNS (NetBIOS Name Server) / WINS (Windows Internet Name Service)**: Used for name registration and resolution in a NetBIOS environment.

---

## SMB Enumeration Methodology

A step-by-step approach to enumerating and interacting with SMB services.

### 1. Port Scanning & Service Identification

-   **Goal**: Discover open SMB ports and identify the service version.
-   **Tools**: [`nmap`](https://nmap.org/)
-   **Method**:
    ```bash
    # Scan for SMB ports (139, 445) and run default scripts (-sC) and version detection (-sV)
    sudo nmap -sV -sC -p139,445 <TARGET_IP>
    ```
-   **What to look for**: OS version, SMB version, computer name, domain/workgroup name, and message signing status.

### 2. Basic Share Enumeration (Anonymous/Null Session)

-   **Goal**: List available shares without credentials.
-   **Tools**: [`smbclient`](https://www.samba.org/samba/docs/current/man-html/smbclient.1.html), [`smbmap`](https://github.com/ShawnDEvans/smbmap), [`crackmapexec`](https://github.com/byt3bl33d3r/CrackMapExec)
-   **Method**:

    ```bash
    # List shares with smbclient (Null Session)
    smbclient -N -L //<TARGET_IP>

    # List shares with smbmap
    smbmap -H <TARGET_IP>

    # List shares with CrackMapExec
    crackmapexec smb <TARGET_IP> --shares -u '' -p ''
    ```

-   **What to look for**: Share names, comments, and access permissions (Read/Write).

### 3. Deep Enumeration with RPC

-   **Goal**: Gather detailed information about the domain, users, and system configuration.
-   **Tools**: [`rpcclient`](https://www.samba.org/samba/docs/current/man-html/rpcclient.1.html), [`enum4linux-ng`](https://github.com/cddmp/enum4linux-ng)
-   **Method**:

    ```bash
    # Connect with rpcclient (Null Session)
    rpcclient -U "" -N <TARGET_IP>

    # Once connected, run queries:
    rpcclient $> srvinfo        # Server info
    rpcclient $> enumdomains    # List domains
    rpcclient $> querydominfo   # Domain details
    rpcclient $> netshareenumall# List all shares
    rpcclient $> enumdomusers   # Enumerate domain users
    ```

-   **What to look for**: Usernames, RIDs, domain info, detailed share paths, and OS details.

### 4. User and Group Enumeration

-   **Goal**: Systematically find all users and groups on the system.
-   **Tools**: [`rpcclient`](https://www.samba.org/samba/docs/current/man-html/rpcclient.1.html), [`samrdump.py`](https://github.com/SecureAuthCorp/impacket/blob/master/examples/samrdump.py) (Impacket), [`enum4linux-ng`](https://github.com/cddmp/enum4linux-ng)
-   **Method**:

    ```bash
    # Brute-force RIDs with a bash loop
    for i in $(seq 500 1100); do rpcclient -N -U "" <TARGET_IP> -c "queryuser 0x$(printf '%x\n' $i)" | grep "User Name"; done

    # Use Impacket's samrdump.py for automation
    samrdump.py <TARGET_IP>

    # Use enum4linux-ng for comprehensive enumeration
    ./enum4linux-ng.py <TARGET_IP> -A
    ```

-   **What to look for**: Valid usernames, their RIDs, group memberships, and password policy details.

### 5. Interacting with Shares

-   **Goal**: Connect to accessible shares to explore, download, or upload files.
-   **Tools**: [`smbclient`](https://www.samba.org/samba/docs/current/man-html/smbclient.1.html)
-   **Method**:

    ```bash
    # Connect to a specific share (will prompt for password for anonymous login)
    smbclient //<TARGET_IP>/<SHARE_NAME>

    # Inside smbclient:
    smb: \> help      # List available commands
    smb: \> ls        # List files and directories
    smb: \> get <FILENAME> # Download a file
    smb: \> put <FILENAME> # Upload a file (if writable)
    smb: \> recurse ON # Turn on recursion for mget/mput
    smb: \> mget *    # Download all files
    smb: \> !<CMD>    # Execute a local shell command
    ```

-   **What to look for**: Sensitive files, configuration files, user data, or writable directories for potential exploits.

---

## Cheatsheet: Tools & Commands

### [`nmap`](https://nmap.org/)

-   **Purpose**: Initial discovery and service scanning.
-   **Command**:
    ```bash
    sudo nmap -sV -sC -p139,445 <TARGET_IP>
    ```
-   **Useful NSE Scripts**: `smb-os-discovery`, `smb-enum-shares`, `smb-enum-users`, `smb2-security-mode`.

### [`smbclient`](https://www.samba.org/samba/docs/current/man-html/smbclient.1.html)

-   **Purpose**: The primary command-line tool for interacting with SMB shares.
-   **Commands**:

    ```bash
    # List shares (anonymous null session)
    smbclient -N -L //<TARGET_IP>

    # Connect to a share (anonymous)
    smbclient -N //<TARGET_IP>/<SHARE_NAME>

    # Connect to a share (with user)
    smbclient -U <USERNAME> //<TARGET_IP>/<SHARE_NAME>
    ```

### [`rpcclient`](https://www.samba.org/samba/docs/current/man-html/rpcclient.1.html)

-   **Purpose**: Perform MS-RPC functions to query for detailed system information.
-   **Commands**:

    ```bash
    # Connect anonymously
    rpcclient -U "" -N <TARGET_IP>

    # Common queries
    srvinfo, enumdomains, querydominfo, netshareenumall, enumdomusers, queryuser <RID>, querygroup <RID>
    ```

### [`enum4linux-ng`](https://github.com/cddmp/enum4linux-ng)

-   **Purpose**: An automated, all-in-one enumeration tool that wraps many of the manual `rpcclient` and `smbclient` queries.
-   **Command**:
    ```bash
    # Run all enumeration checks
    ./enum4linux-ng.py <TARGET_IP> -A
    ```

### [`samrdump.py`](https://github.com/SecureAuthCorp/impacket/blob/master/examples/samrdump.py) (Impacket)

-   **Purpose**: A script from the [Impacket](https://github.com/SecureAuthCorp/impacket) suite to enumerate users and system information via SAMR.
-   **Command**:
    ```bash
    samrdump.py <TARGET_IP>
    ```

### [`SMBMap`](https://github.com/ShawnDEvans/smbmap)

-   **Purpose**: A handy tool to enumerate share permissions across a host or network.
-   **Command**:

    ```bash
    # Enumerate shares and permissions anonymously
    smbmap -H <TARGET_IP>

    # Enumerate with credentials
    smbmap -u <USER> -p <PASS> -d <DOMAIN> -H <TARGET_IP>
    ```

### [`CrackMapExec`](https://github.com/byt3bl33d3r/CrackMapExec) (CME)

-   **Purpose**: A powerful post-exploitation tool that excels at network-wide SMB enumeration and command execution.
-   **Command**:
    ```bash
    # Enumerate shares anonymously
    crackmapexec smb <TARGET_IP> --shares -u '' -p ''
    ```

---

## Samba Configuration (`smb.conf`)

### Dangerous Settings

Misconfigurations in `/etc/samba/smb.conf` can lead to serious vulnerabilities.

| **Setting**                | **Description**                                                   | **Risk**                                                                                              |
| -------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `guest ok = yes`           | Allows connection without a password (anonymous access).          | Attackers can access the share without credentials, leading to information disclosure or file access. |
| `writable = yes`           | Allows users to create and modify files in the share.             | Combined with `guest ok = yes`, allows anyone to write files, potentially leading to RCE.             |
| `browseable = yes`         | Makes the share visible in the list of available shares.          | Helps attackers easily discover potentially sensitive shares.                                         |
| `create mask = 0777`       | Sets full read/write/execute permissions for newly created files. | Uploaded scripts or binaries will have execute permissions, facilitating code execution.              |
| `logon script = script.sh` | Executes a script upon user login.                                | If an attacker can write to this script, they can execute code when a legitimate user logs in.        |

### Practical Tips & Troubleshooting

-   **Always check for anonymous/null sessions first.** This is the most common and easiest misconfiguration to exploit.
-   **Don't rely on a single tool.** One tool might miss something another finds. For example, `enum4linux-ng` is great for automation, but `rpcclient` gives you granular control for manual queries.
-   **Correlate information.** Usernames found via `enumdomusers` can be used to check for access to shares listed by `smbmap`.
-   **Check share permissions carefully.** `READ` access can leak sensitive data. `WRITE` access is a high-impact finding and could lead to Remote Code Execution (RCE), especially if the share is a web root or contains executable scripts.
-   **Remember RIDs.** User RIDs (Relative Identifiers) often start at 1000 (`0x3e8`). Group RIDs for domain users are often 513 (`0x201`). This is useful for brute-force guessing.

---

## References and Tools

### Official Documentation

-   **[Microsoft SMB Protocol Specification](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-smb/f210069c-7086-4dc2-885e-861d837df688)**
-   **[Microsoft CIFS Protocol Specification](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cifs/934c2faa-54af-4526-ac74-6a24d126724e)**
-   **[Samba `smb.conf` Man Page](https://www.samba.org/samba/docs/current/man-html/smb.conf.5.html)**
-   **[Samba `rpcclient` Man Page](https://www.samba.org/samba/docs/current/man-html/rpcclient.1.html)**

### Further Reading

-   **[SMB Protocol Examples](https://web.archive.org/web/20240815212710/https://winprotocoldoc.blob.core.windows.net/productionwindowsarchives/MS-SMB2/%5BMS-SMB2%5D.pdf#%5B%7B%22num%22%3A920%2C%22gen%22%3A0%7D%2C%7B%22name%22%3A%22XYZ%22%7D%2C69%2C738%2C0%5D)**
-   **[NetBIOS Name Server (NBNS)](https://networkencyclopedia.com/netbios-name-server-nbns/)**
-   **[Windows Internet Name Service (WINS)](https://networkencyclopedia.com/windows-internet-name-service-wins/)**
-   **[Remote Procedure Call (RPC)](https://www.geeksforgeeks.org/remote-procedure-call-rpc-in-operating-system/)**

