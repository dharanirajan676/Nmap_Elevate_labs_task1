# Nmap_Elevate_labs_task1
 🛡️ Cyber Security Internship - Task 1

Objective: To perform a network scan to discover devices and their open ports on the local network using **Nmap**, and assess potential security risks.

Tools Used:  Nmap – for scanning ports (TCP SYN scan) - Command Prompt (CMD) – to find IP and subnet

nmap downloaded from https://nmap.org/download.html

steps taken for port (TCP) Scanning
1. using command ipconfig to collect system info including ip address and their ranges
2. using command nmap -sS 10.24.56.0/24 for open port scanning in configred system with their ip ranges (10.24.56.0/24: Scans IPs from 10.24.56.1 to 10.24.56.254)

Scan Findings:
Host: 10.24.56.180
Open Port: 53/tcp — domain (DNS)
Risk:
DNS services are often targets for DNS spoofing, DDoS amplification, or data exfiltration.
If the DNS server is misconfigured, attackers may exploit it to reroute traffic.

Host: 10.24.56.38
Open Ports:
135/tcp — msrpc (Microsoft RPC)
139/tcp — netbios-ssn (NetBIOS Session Service)
445/tcp — microsoft-ds (SMB file sharing)
3306/tcp — mysql (MySQL database)
Risks:
Ports 135, 139, 445 (Windows Services): Frequently exploited by malware like WannaCry and NotPetya. Can allow remote code execution, lateral movement, or unauthorized file access.
Port 3306 (MySQL): If the database is externally exposed and credentials are weak, it’s vulnerable to SQL injection, data theft, or remote access.

Recommendations:
>. Close unused ports or restrict them with firewall rules.
>. Disable SMB v1, NetBIOS, or unused Windows services.
>. Secure MySQL with strong passwords and local-only access.
>. Regularly patch and update all running services.
>. Monitor the network for suspicious connections.

________________________________________________________________________ THANK YOU __________________________________________________________________________________________________________________________________

