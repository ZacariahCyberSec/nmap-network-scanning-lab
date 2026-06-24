🚀 SOC Analyst Lab – Nmap Network Scanning & Vulnerability Assessment

📌 Overview

This project demonstrates a hands-on cybersecurity lab focused on network reconnaissance, service enumeration, and vulnerability assessment using Nmap in a Termux (Android Linux) environment.

The goal of this lab is to simulate real-world SOC analysis workflows by identifying open ports, services, and potential vulnerabilities on a target system.

---

🛠 Tools & Environment

- Nmap
- Termux (Android Linux environment)
- Linux command-line

---

🎯 Target

- scanme.nmap.org (authorized testing target)

---

🔍 Phase 1: Network Reconnaissance

nmap -Pn scanme.nmap.org

Key Findings:

- Host is active
- Multiple open ports identified:
  - 22 (SSH)
  - 80 (HTTP)
  - 9929 (Nping)
  - 31337 (Filtered)

---

🔎 Phase 2: Service & Version Detection

nmap -sV scanme.nmap.org

Key Findings:

- SSH: OpenSSH (Ubuntu)
- HTTP: Apache Web Server

---

🧠 Phase 3: Advanced Enumeration

nmap -A scanme.nmap.org

Key Findings:

- OS detected: Linux
- Service versions identified
- HTTP headers exposed

---

🚨 Phase 4: Vulnerability Assessment

nmap --script vuln scanme.nmap.org

Key Findings:

- Potential CSRF vulnerability detected
- No XSS vulnerabilities found
- SQL injection test inconclusive

---

🌐 Phase 5: Web Enumeration

nmap --script http-enum -p 80 scanme.nmap.org

Key Findings:

- Exposed directory: "/images/"
- Indicates possible misconfiguration

---

📸 Screenshots

🔍 Full Scan

"Scan" (screenshots/scan.png)

🚨 Vulnerability Scan

"Vuln" (screenshots/vuln.png)

🌐 Web Enumeration

"Enum" (screenshots/enum.png)

---

🛡️ Security Analysis

From a SOC Analyst perspective, this activity represents:

- Network reconnaissance behavior
- Service enumeration attempts
- Vulnerability scanning activity
- Web probing for exposed directories

Potential Risks Identified:

- Open services increase attack surface
- Outdated services may expose vulnerabilities
- Directory exposure may lead to information disclosure

---

🎯 Skills Demonstrated

- Network scanning & reconnaissance
- Service enumeration
- Vulnerability assessment
- Web application enumeration
- Security analysis & interpretation

---

📊 Conclusion

This lab simulates the early stages of a cyber attack and demonstrates how attackers gather intelligence before exploitation.

It also highlights how SOC analysts detect and analyze suspicious scanning activity in real-world environments.

---

⚠️ Disclaimer

All scans were performed on an authorized testing target: scanme.nmap.org
