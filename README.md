# 🔥 Security Wordlists & Payloads

> **Comprehensive security wordlists & exploit payloads for penetration testers and security researchers.**

This repository provides categorized wordlists and payloads for security assessments, including **sensitive paths, exploit payloads, fuzzing wordlists, WAF bypass techniques, and more**. Compatible with security tools like **Burp Suite, FFUF, Dirsearch, Nuclei, SQLmap, etc.**

---

## 📁 Directory Structure

```
security-lists/
│── sensitive_paths/            # Sensitive file and directory paths
│   ├── admin_panels.txt
│   ├── login_pages.txt
│   ├── api_endpoints.txt
│   ├── error_pages.txt
│   ├── backups.txt
│   ├── config_files.txt
│── technology_fingerprints/    # Fingerprints for CMS, frameworks, and servers
│   ├── cms/
│   │   ├── wordpress.txt
│   │   ├── joomla.txt
│   │   ├── drupal.txt
│   ├── frameworks/
│   │   ├── django.txt
│   │   ├── laravel.txt
│   ├── servers/
│   │   ├── apache.txt
│   │   ├── nginx.txt
│── exploit_payloads/           # Exploitation payloads
│   ├── xss/
│   ├── sqli/
│   ├── other/
│── unauthorized_access/        # Default credentials, common users & passwords
│── fuzzing_wordlists/          # Wordlists for fuzzing directories, params, headers, etc.
│── waf_bypass/                 # Techniques to bypass Web Application Firewalls (WAFs)
│── misconfig_information_disclosure/ # Lists for exposed sensitive files and misconfigurations
│── README.md                   # This file
```

---

## 🚀 How to Use

### **🛠️ Directory & File Enumeration**
Use **FFUF**, **Dirsearch**, or similar tools to scan directories and files:
```sh
ffuf -w sensitive_paths/admin_panels.txt -u https://target.com/FUZZ
```

### **💉 Exploit Payloads (XSS, SQLi, etc.)**
Use these payloads with security tools like **Burp Suite**, **SQLmap**, or manually:
```sh
sqlmap -u "https://target.com/index.php?id=1" --batch --file-read="exploit_payloads/sqli/union_based.txt"
```

### **🔍 Subdomain & Parameter Fuzzing**
Use wordlists for discovering subdomains, headers, and parameters:
```sh
wfuzz -w fuzzing_wordlists/parameters.txt -u "https://target.com/page.php?FUZZ=value"
```

---

## 🔥 Features
✔️ **Structured & Organized** – Easy to navigate and use
✔️ **Compatible with Popular Tools** – Burp Suite, FFUF, SQLmap, etc.
✔️ **Regularly Updated** – Contributions and improvements welcome
✔️ **Optimized for Security Researchers & Pentesters**

---

## 📢 Contribution
We welcome contributions! To contribute:
1. Fork the repository
2. Create a new branch (`feature/update-wordlist`)
3. Commit your changes
4. Submit a pull request 🚀

---

## ⚠️ Disclaimer
This repository is intended **for educational and ethical penetration testing purposes only**. Misuse of this information **may lead to legal consequences**. The author assumes **no responsibility for any misuse or damage**.

---

## ⭐ Support
If you find this project useful, feel free to ⭐ star this repository and share it!

