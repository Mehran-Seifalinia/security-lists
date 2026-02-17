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
| │   ├── [Admin panel](https://github.com/Mehran-Seifalinia/security-lists/blob/main/sensitive_paths/admin_panels.txt)               | List of admin panel paths                            |
| │   ├── [Login page](https://github.com/Mehran-Seifalinia/security-lists/blob/main/sensitive_paths/login_pages.txt)                 | List of login page paths                             |
| │   ├── [API endpoint](https://github.com/Mehran-Seifalinia/security-lists/blob/main/sensitive_paths/api_endpoints.txt)             | List of API endpoints                                |
| │   ├── [Errors](https://github.com/Mehran-Seifalinia/security-lists/blob/main/sensitive_paths/error_pages.txt)                 | List of error page paths                             |
| │   ├── [Backups](https://github.com/Mehran-Seifalinia/security-lists/blob/main/sensitive_paths/backups.txt)                         | List of backup file paths                            |
| │   ├── [Config files](https://github.com/Mehran-Seifalinia/security-lists/blob/main/sensitive_paths/config_files.txt)               | List of configuration files                          |
| │   ├── [Database files](https://github.com/Mehran-Seifalinia/security-lists/blob/main/sensitive_paths/database_files.txt)           | List of databases paths                              |
| ├── `technology_fingerprints/ `                | Fingerprints for CMS, frameworks, and servers        |
| │   ├── `cms/`                                 | List of CMS technologies                             |
| │   │   ├── [Wordpress](https://github.com/Mehran-Seifalinia/security-lists/blob/main/technology_fingerprints/cms/wordpress.txt)     | List of WordPress-specific fingerprints              |
| │   │   ├── [Joomla](https://github.com/Mehran-Seifalinia/security-lists/blob/main/technology_fingerprints/cms/joomla.txt)           | List of Joomla-specific fingerprints                 |
| │   │   ├── [Drupal](https://github.com/Mehran-Seifalinia/security-lists/blob/main/technology_fingerprints/cms/drupal.txt)           | List of Drupal-specific fingerprints                 |
| │   ├── `frameworks/`                          | List of frameworks                                   |
| │   │   ├── [Django](https://github.com/Mehran-Seifalinia/security-lists/blob/main/technology_fingerprints/frameworks/django.txt)    | List of Django-specific fingerprints                 |
| │   │   ├── [Laravel](https://github.com/Mehran-Seifalinia/security-lists/blob/main/technology_fingerprints/frameworks/laravel.txt)  | List of Laravel-specific fingerprints                |
| │   ├── `servers/`                             | List of server technologies                          |
| │   │   ├── [Apache](https://github.com/Mehran-Seifalinia/security-lists/blob/main/technology_fingerprints/servers/apache.txt)       | List of Apache-specific fingerprints                 |
| │   │   ├── [Nginx](https://github.com/Mehran-Seifalinia/security-lists/blob/main/technology_fingerprints/servers/nginx.txt)         | List of Nginx-specific fingerprints                  |
| ├── `exploit_payloads/`                        | Exploitation payloads                 |
| │   ├── `xss/`                                 | XSS payloads                          |
| │   │   ├── [Basic](https://github.com/Mehran-Seifalinia/security-lists/blob/main/exploit_payloads/xss/basic.txt)                        | Simple basic XSS payloads                        |
| │   │   ├── [DOM](https://github.com/Mehran-Seifalinia/security-lists/blob/main/exploit_payloads/xss/dom.txt)                            | Simple DOM XSS payloads                          |
| │   │   ├── [Bypass](https://github.com/Mehran-Seifalinia/security-lists/blob/main/exploit_payloads/xss/bypass.txt)                      | Simple Bypass for XSS                            |
| │   ├── `sqli/`                                | SQL Injection payloads                |
| │   ├── `Command injection/`                   | OS command Injection payloads         |
| │   │   ├── [Basic(Linux)](https://github.com/Mehran-Seifalinia/security-lists/blob/main/exploit_payloads/Command%20injection/basic(Linux).txt)         | Simple basic commands for Linux      |
| │   │   ├── [Basic(Windows)](https://github.com/Mehran-Seifalinia/security-lists/blob/main/exploit_payloads/Command%20injection/Blind(Windows).txt)     | Simple basic commands for windows    |
| │   │   ├── [Blind(Linux)](https://github.com/Mehran-Seifalinia/security-lists/blob/main/exploit_payloads/Command%20injection/Blind(Linux).txt)         | Blind basic commands for Linux       |
| │   │   ├── [Blind(Windows)](https://github.com/Mehran-Seifalinia/security-lists/blob/main/exploit_payloads/Command%20injection/Blind(Windows).txt)     | Blind basic commands for windows     |
| │   │   ├── [OOB(Linux)](https://github.com/Mehran-Seifalinia/security-lists/blob/main/exploit_payloads/Command%20injection/OOB(Linux).txt)             | OOB basic commands for Linux         |
| │   │   ├── [OOB(Windows)](https://github.com/Mehran-Seifalinia/security-lists/blob/main/exploit_payloads/Command%20injection/OOB(Windows).txt)         | OOB basic commands for windows       |
| │   ├── `other/`                               | Other exploit payloads                                           |
| ├── `unauthorized_access/`                     | Default credentials, common users & passwords                    |
| ├── `fuzzing_wordlists/`                       | Wordlists for fuzzing directories, params, headers, etc.         |
| ├── `waf_bypass/`                              | Techniques to bypass Web Application Firewalls (WAFs)            |
| ├── `misconfig_information_disclosure/`        | Lists for exposed sensitive files and misconfigurations          |
| └── `README.md`                                | This file                                                        |



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

