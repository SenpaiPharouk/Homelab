# Findings Table: Metasploitable 2 (192.168.100.20)

Scope: authorized testing of my own isolated lab only.
Tool: Nmap 7.99 from Kali Linux. Risk ratings are my own assessment.

**Evidence:** "Confirmed" means an Nmap script reported it. "Version-based" means the service version is known to be risky, but I did not exploit it.

| Port | Service / version | Risk | Evidence | Fix |
|---|---|---|---|---|
| 21 | vsftpd 2.3.4 | Critical | Confirmed: ftp-vsftpd-backdoor (CVE-2011-2523), command ran as uid=0 | Upgrade vsftpd or remove FTP |
| 6667 | UnrealIRCd | Critical | Confirmed: irc-unrealircd-backdoor flagged a trojaned version | Reinstall from a trusted source, or remove IRC |
| 1099 | Java RMI (GNU Classpath) | Critical | Confirmed: rmi-vuln-classloader, remote code execution | Disable RMI or restrict access |
| 1524 | "Metasploitable root shell" | Critical | Version scan identified a bindshell | Remove the service, block the port |
| 3632 | distccd v1 | High | Version-based: exposed distributed compiler | Disable it or restrict to trusted hosts |
| 23 | Linux telnetd | High | Version-based: plain-text logins | Replace with SSH |
| 512-514 | rexecd, rlogind, rshd | High | Version-based: legacy r-services, weak authentication | Disable, use SSH |
| 25, 5432 | Postfix, PostgreSQL 8.3 | High | Confirmed: weak Diffie-Hellman; POODLE (CVE-2014-3566) on both; CCS injection (CVE-2014-0224) on PostgreSQL | Update OpenSSL, disable SSLv3 and export ciphers |
| 80, 8180 | Apache 2.2.8, Tomcat | Medium | Confirmed: Slowloris "likely vulnerable" (CVE-2007-6750); TRACE enabled; admin paths found | Upgrade, disable TRACE, restrict /admin and /manager |
| 3306 | MySQL 5.0.51a | Medium | Version-based: old database exposed to the network | Bind to localhost, upgrade |
| 2049, 111 | NFS, rpcbind | Medium | Version-based: network file shares exposed | Restrict exports, firewall |
| 5900, 6000 | VNC, X11 | Medium | Version-based: remote desktop and display exposed | Firewall, strong passwords |

## Not verified
Three scripts failed to run (sslv2-drown, http-sql-injection, smb-vuln-regsvc-dos). Those services are untested, not proven safe.
