# 🚀 SOC Analyst Lab – Nmap Scanning & Enumeration

## 📌 Overview
This project demonstrates practical network scanning and vulnerability assessment using Nmap in Termux (Android).

---

## 🛠 Tools Used
- Nmap
- Termux (Android Linux)

---

## 🎯 Target
scanme.nmap.org (authorized test target)

---

## 🔍 Basic Scan
Command:
nmap -Pn scanme.nmap.org

Result:
- Host is up
- Open ports:
  - 22 (SSH)
  - 80 (HTTP)
  - 9929 (Nping)
  - 31337 (Filtered)

---

## 🔎 Service Scan
Command:
nmap -sV scanme.nmap.org

Result:
- SSH: OpenSSH (Ubuntu)
- HTTP: Apache (Ubuntu)

---

## 🧠 Advanced Scan
Command:
nmap -A scanme.nmap.org

Result:
- OS detected: Linux
- Service versions identified

---

## 🚨 Vulnerability Scan
Command:
nmap --script vuln scanme.nmap.org

Result:
- Possible CSRF found
- No XSS detected

---

## 🌐 Web Enumeration
Command:
nmap --script http-enum -p 80 scanme.nmap.org

Result:
- /images/ directory exposed

---

## 🛡️ Key Takeaways
- Open ports increase risk
- Services reveal system details
- Enumeration is critical in security testing

---

## ⚠️ Disclaimer
This scan was performed on an authorized target (scanme.nmap.org)
