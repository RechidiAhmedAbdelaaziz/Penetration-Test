# MySQL – Pentest Study & Application Notes

## Overview
- **MySQL**: Open-source relational database (RDBMS) by Oracle.
- **Client-server model**: MySQL server manages data; clients interact via SQL.
- **Common use**: Dynamic websites (e.g., WordPress), often as part of LAMP/LEMP stacks.
- **Files**: Databases often stored as `.sql` files.

---

## Key Concepts

### MySQL Clients
- Retrieve/edit data using SQL queries.
- Access via internal network or Internet.
- Example: WordPress stores posts, users, passwords in MySQL (usually localhost-only).

### MySQL Databases
- Used for dynamic content, user data, permissions, etc.
- Sensitive data (e.g., passwords) should be encrypted before storage.

### MariaDB
- Fork of MySQL, fully compatible, created after Oracle acquired MySQL.

---

## Default Configuration

```bash
sudo apt install mysql-server -y
cat /etc/mysql/mysql.conf.d/mysqld.cnf | grep -v "#" | sed -r '/^\s*$/d'
```

**Key config options:**
- `[client]`/`[mysqld]` sections: port, socket, user, datadir, etc.
- Default port: `3306`
- Config file: `/etc/mysql/mysql.conf.d/mysqld.cnf`

---

## Dangerous Settings

| Setting             | Description                                                        |
|---------------------|--------------------------------------------------------------------|
| `user`              | User MySQL runs as (should not be root).                           |
| `password`          | MySQL user password (avoid plain text, restrict file permissions). |
| `admin_address`     | IP for admin connections.                                          |
| `debug`             | Debugging info (can leak sensitive data).                          |
| `sql_warnings`      | Verbose error output (can aid attackers).                          |
| `secure_file_priv`  | Restricts import/export file locations.                            |

**Risks:**
- Plaintext credentials in config files.
- Overly verbose errors can leak info for attacks (e.g., SQLi).
- Misconfigured permissions can expose sensitive data.

---

## Footprinting & Enumeration

### Scanning for MySQL

```bash
sudo nmap <target-ip> -sV -sC -p3306 --script mysql*
```
- Detects open MySQL port, version, users, weak creds, etc.
- **Note**: Nmap results may have false positives (e.g., empty root password).

### Manual Login

```bash
mysql -u root -h <target-ip>
# If password required:
mysql -u root -p<password> -h <target-ip>
```
- No space between `-p` and password.

### Example: Database Enumeration

```sql
show databases;
use <database>;
show tables;
show columns from <table>;
select * from <table>;
select * from <table> where <column> = "<string>";
```

---

## Attack & Defense Procedures

### Attack Steps
1. **Port scan** for 3306/tcp.
2. **Nmap scripts** for user/password enumeration.
3. **Brute-force** or use found creds to login.
4. **Enumerate** databases/tables for sensitive data.
5. **Check for SQLi** in web apps using MySQL.

### Defense/Hardening
- Restrict MySQL to localhost unless needed.
- Use strong, unique passwords.
- Limit user privileges (principle of least privilege).
- Encrypt sensitive data before storage.
- Restrict config file permissions.
- Disable verbose error messages in production.
- Regularly update MySQL/MariaDB.

---

## Cheatsheet

| Command                                                      | Description                                 |
|--------------------------------------------------------------|---------------------------------------------|
| `mysql -u <user> -p<password> -h <ip>`                       | Connect to MySQL server                     |
| `show databases;`                                            | List all databases                          |
| `use <database>;`                                            | Switch to a database                        |
| `show tables;`                                               | List tables in current database             |
| `show columns from <table>;`                                 | List columns in a table                     |
| `select * from <table>;`                                     | Dump all rows from a table                  |
| `select * from <table> where <column> = "<string>";`         | Search for a value in a table               |

---

## Best Practices & Pitfalls

- **Best Practices**: Restrict network access, use encrypted connections, monitor logs, backup data.
- **Common Pitfalls**: Default/weak passwords, exposed config files, excessive privileges, verbose errors.

---

## Hands-on Checklist

- [ ] Install MySQL/MariaDB on a VM
- [ ] Configure secure user/password
- [ ] Restrict network access to 3306
- [ ] Enumerate databases/tables as attacker
- [ ] Test SQLi on a test web app
- [ ] Harden configuration and retest

---

## References

- [MySQL Security Best Practices](https://dev.mysql.com/doc/refman/8.0/en/general-security-issues.html)
- [MySQL Server System Variables](https://dev.mysql.com/doc/refman/8.0/en/server-system-variables.html)
- [SQL Injection Fundamentals (HTB)](https://academy.hackthebox.com/course/preview/sql-injection-fundamentals)
- [SQLMap Essentials (HTB)](https://academy.hackthebox.com/course/preview/sqlmap-essentials)
