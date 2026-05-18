# TryHackMe: Cybersecurity 101 – Core Takeaways & Lab Notes
A curated summary of foundational concepts, methodology, and hands-on tooling covered during my comprehensive dive into cybersecurity fundamentals.

# 1. Core Security Principles & Career Landscapes
- The CIA Triad: Grounded all security decisions in ensuring Confidentiality (restricting data access), Integrity (preventing/detecting unauthorized alterations), and Availability (ensuring systems are up when needed).
- Defense in Depth: Understood that security relies on layered protections (physical, technical, administrative) rather than a single point of failure.

 # 2. Offensive Security Tools & Methodologies
- Reconnaissance & Directory Brute-Forcing: Mastered utilizing dirb and Gobuster to discover hidden directories, unlinked pages, and exposed sensitive endpoints via wordlists.
- Online Authentication Attacks: Leveraged Hydra to perform high-speed, automated brute-force attacks against network and web login protocols (SSH, FTP, HTTP-POST).
- Database Exploitation: Utilized SQLMap to automate the detection and exploitation of SQL injection vulnerabilities, extracting database structures, tables, and credentials.
- The Metasploit Framework: Gained hands-on experience using msfconsole to search for exploits, configure payloads (like Meterpreter), and establish reverse shells on vulnerable systems.
- Credential Cracking: Used specialized parsing scripts like ssh2john and rar2john to extract password hashes from protected files, subsequently cracking them using John the Ripper with the rockyou.txt wordlist.

# 3. Web Hacking Foundations & OWASP Top 10
- HTTP/Web Architecture: Analyzed HTTP requests/responses, tracking how methods (GET, POST), headers, and status codes dictate client-server interactions.
- Intercepting Proxies: Utilized Burp Suite Proxy to capture, analyze, and manipulate live HTTP traffic on-the-fly before it reaches the web application server.
- Cross-Site Scripting (XSS): Executed reflected XSS payloads (<script>alert()</script>) to understand how input sanitization failures allow attackers to run malicious JavaScript in a user's browser.
- IAAA Failures: Evaluated critical breakdowns in Identity, Authentication, Authorization, and Accountability, mapping out how weak implementation leads to Broken Access Control (OWASP A01).
- Insecure Deserialization: Performed practical deserialization attacks in Python using the pickle module to construct payloads capable of arbitrary remote code execution.
- Credential Leakage: Explored critical vulnerabilities like the Moniker Link (CVE-2024-21413) to analyze how flawed URL handling in email clients can automatically leak user NTLM hashes to rogue servers.

# 4. Defensive Security, SOC, & Architecture
- Proactive vs. Reactive Security: Differentiated Red Team (offensive simulation/penetration testing) from Blue Team (preventing, detecting, and mitigating active intrusions).
- Security Solutions Architecture: Explored how Firewalls filter traffic, IDS/IPS monitor network anomalies, and SIEM systems aggregate diverse log data.
- The Role of SIEM: Learned how a SIEM normalizes and correlates massive streams of isolated logs from endpoints, servers, and routers to alert analysts to malicious activity.
- Vulnerability Management: Used OpenVAS (Greenbone) to perform automated asset scans, interpret CVSS severity scores, and prioritize remediation strategies.

# 5. Digital Forensics & Incident Response (DFIR)
- Manual Log Analysis: Developed terminal-based log parsing skills using Linux utilities (cat, grep, awk) to track specific attacker patterns (e.g., filtering out specific malicious POST requests by timestamp or IP address).
- Data Decoding & Manipulation: Used CyberChef to build modular "recipes" for rapidly decoding Base64, performing XOR operations, and analyzing obfuscated data strings.
- Malware Analysis Environments: Utilized FlareVM to safely explore tools built for incident response, reverse engineering, and analyzing windows portable executables.
- Static Executable Analysis: Leveraged PEStudio and CFF Explorer to inspect anomalies in executable headers, import tables, and embedded strings without executing the malware.
- Dynamic Monitoring: Utilized Process Monitor (ProcMon) and Process Explorer to track live system alterations, monitoring how suspicious processes interact with the registry and file system.
- Network Forensics: Analyzed packet captures (.pcap) within Wireshark, applying display filters (ip.addr == <IP>) to isolate Command and Control (C2) callback traffic and determine target destination ports (e.g., tracking Cobalt Strike traffic).
