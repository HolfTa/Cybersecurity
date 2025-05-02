# 🔌 Network Ports Cheat Sheet

## 📘 What Are Ports?

Ports are logical endpoints used by operating systems to manage multiple network services on a single IP address. They act like "doors" through which data flows between a computer and external devices or services on the internet or a local network.

Each port is identified by a number ranging from **0 to 65535**, divided into three main categories:

- **Well-known ports (0–1023):** Used by core services like HTTP, FTP, and DNS.
- **Registered ports (1024–49151):** Used by software vendors for specific applications.
- **Dynamic/private ports (49152–65535):** Used for temporary or private connections, often dynamically assigned.

When a client wants to connect to a server, it specifies both the **IP address** and the **port number**. For example:

---

## 📌 Essential and Well-Known Port Numbers

| Port | Protocol | Service Name         | Description |
|------|----------|----------------------|-------------|
| 20   | TCP      | FTP (Data)           | Transfers data for FTP in active mode |
| 21   | TCP      | FTP (Control)        | Controls FTP connection commands |
| 22   | TCP      | SSH                  | Secure Shell for encrypted remote login |
| 23   | TCP      | Telnet               | Remote login (unencrypted) |
| 25   | TCP      | SMTP                 | Sends emails (Simple Mail Transfer Protocol) |
| 53   | TCP/UDP  | DNS                  | Domain Name System (resolves domain names) |
| 67   | UDP      | DHCP (Server)        | Dynamic Host Configuration Protocol – server |
| 68   | UDP      | DHCP (Client)        | DHCP client request port |
| 69   | UDP      | TFTP                 | Trivial File Transfer Protocol |
| 80   | TCP      | HTTP                 | HyperText Transfer Protocol (web traffic) |
| 110  | TCP      | POP3                 | Post Office Protocol v3 (retrieve email) |
| 123  | UDP      | NTP                  | Network Time Protocol (sync clocks) |
| 137  | UDP      | NetBIOS Name Service | Name resolution in Windows networks |
| 138  | UDP      | NetBIOS Datagram     | Connectionless communication in Windows |
| 139  | TCP      | NetBIOS Session      | Session layer communication in Windows |
| 143  | TCP      | IMAP                 | Internet Message Access Protocol |
| 161  | UDP      | SNMP                 | Simple Network Management Protocol |
| 162  | UDP      | SNMP Trap            | Receives SNMP trap messages |
| 389  | TCP/UDP  | LDAP                 | Lightweight Directory Access Protocol |
| 443  | TCP      | HTTPS                | Secure web traffic (HTTP over SSL/TLS) |
| 445  | TCP      | SMB                  | Server Message Block (file sharing) |
| 465  | TCP      | SMTPS                | Secure SMTP (deprecated, but still used) |
| 514  | UDP      | Syslog               | Logging messages over network |
| 587  | TCP      | SMTP (Submission)    | Sending mail (modern submission port) |
| 636  | TCP      | LDAPS                | Secure LDAP over SSL |
| 993  | TCP      | IMAPS                | Secure IMAP |
| 995  | TCP      | POP3S                | Secure POP3 |
| 1433 | TCP      | MS SQL Server        | Microsoft SQL database service |
| 1521 | TCP      | Oracle DB            | Oracle database default port |
| 3306 | TCP      | MySQL                | MySQL database service |
| 3389 | TCP      | RDP                  | Remote Desktop Protocol |
| 5432 | TCP      | PostgreSQL           | PostgreSQL database service |
| 5900 | TCP      | VNC                  | Virtual Network Computing (remote desktop) |
| 6379 | TCP      | Redis                | Redis in-memory data store |
| 8080 | TCP      | HTTP (Alt)           | Alternative HTTP port (commonly used in testing/dev) |

---