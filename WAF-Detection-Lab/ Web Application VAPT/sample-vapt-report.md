# 📝 Web Application VAPT Report

**Target:** DVWA  
**Test Date:** June 2025  
**Tester:** Aditya

---

## 🔍 1. Reconnaissance

- Open ports: 80 (HTTP)
- Technologies: PHP, Apache 2.4
- Directory brute force: `/uploads`, `/phpmyadmin`

---

## 🛠 2. Vulnerabilities Discovered

| # | Vulnerability | Risk | CVSS | Tool Used |
|---|---------------|------|------|-----------|
| 1 | SQL Injection (Login) | High | 9.8 | Burp Suite + SQLmap |
| 2 | Reflected XSS | Medium | 6.1 | Burp Suite |
| 3 | Insecure File Upload | High | 8.6 | Manual |
| 4 | Directory Listing | Low | 3.1 | Dirb |

---

## 🔐 3. Sample Exploit

**Vuln:** SQL Injection in login  
**Payload:** `' OR '1'='1`  
**Impact:** Auth bypass to admin panel

---

## 📉 4. CVSS Example

CVSS (SQLi):  
- Base Score: **9.8**
- Attack Vector: Network  
- Confidentiality Impact: High  
→ [CVSS Calculator](https://www.first.org/cvss/calculator/3.1)

---

## 📷 5. Screenshots

- `screenshots/sql-login-bypass.png`
- `screenshots/xss-alert.png`
- `screenshots/file-upload.png`

---

## ✅ 6. Recommendations

- Sanitize input (prepared statements)
- Enable Web Application Firewall
- Restrict file types
- Remove unnecessary directories

---

## 📌 Summary

This test demonstrates how common vulnerabilities like SQLi and XSS can compromise the app when unprotected. It reinforces the need for layered defenses and code audits.

---

## 🔗 Tools Used

- SQLmap
- OWASP ZAP
- Burp Suite
- Nmap
- Nikto
