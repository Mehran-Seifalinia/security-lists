# 🔥 Security Wordlists & Payloads

> **Comprehensive security wordlists & exploit payloads for penetration testers and security researchers.**

This repository provides categorized wordlists and payloads for security assessments, including **sensitive paths, exploit payloads, fuzzing wordlists, WAF bypass techniques, and more**. Compatible with security tools like **Burp Suite, FFUF, Dirsearch, Nuclei, SQLmap, etc.**

---

## 📁 Directory Structure


# Security Lists Directory Structure

| Directory/File Path                            | Description                                                      |
|------------------------------------------------|------------------------------------------------------------------|
| `security-lists/`                              | Main directory for security lists                                |
| ├── `sensitive_paths/`                         | Sensitive file and directory paths                               |
| │   ├── [admin_panels.txt](https://github.com/Mehran-Seifalinia/security-lists/blob/main/sensitive_paths/admin_panels.txt) | List of admin panel paths                                        |
| │   ├── `login_pages.txt`                      | List of login page paths                                         |
| │   ├── `api_endpoints.txt`                    | List of API endpoints                                            |
| │   ├── `error_pages.txt`                      | List of error page paths                                         |
| │   ├── `backups.txt`                          | List of backup file paths                                        |
| │   ├── `config_files.txt`                     | List of configuration files                                      |
| ├── `technology_fingerprints/`                 | Fingerprints for CMS, frameworks, and servers                    |
| │   ├── `cms/`                                 | List of CMS technologies                                          |
| │   │   ├── `wordpress.txt`                    | List of WordPress-specific fingerprints                           |
| │   │   ├── `joomla.txt`                       | List of Joomla-specific fingerprints                             |
| │   │   ├── `drupal.txt`                       | List of Drupal-specific fingerprints                             |
| │   ├── `frameworks/`                          | List of frameworks                                              |
| │   │   ├── `django.txt`                       | List of Django-specific fingerprints                             |
| │   │   ├── `laravel.txt`                      | List of Laravel-specific fingerprints                            |
| │   ├── `servers/`                             | List of server technologies                                       |
| │   │   ├── `apache.txt`                       | List of Apache-specific fingerprints                             |
| │   │   ├── `nginx.txt`                        | List of Nginx-specific fingerprints                              |
| ├── `exploit_payloads/`                        | Exploitation payloads                                            |
| │   ├── `xss/`                                 | XSS payloads                                                     |
| │   ├── `sqli/`                                | SQL Injection payloads                                           |
| │   ├── `other/`                               | Other exploit payloads                                           |
| ├── `unauthorized_access/`                     | Default credentials, common users & passwords                    |
| ├── `fuzzing_wordlists/`                       | Wordlists for fuzzing directories, params, headers, etc.         |
| ├── `waf_bypass/`                              | Techniques to bypass Web Application Firewalls (WAFs)            |
| ├── `misconfig_information_disclosure/`       | Lists for exposed sensitive files and misconfigurations          |
| └── `README.md`                                | This file                                                       |



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

