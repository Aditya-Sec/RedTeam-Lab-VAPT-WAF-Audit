# 🔍 Web Application Vulnerability Assessment & Penetration Testing (VAPT)

This project documents a complete VAPT assessment of a sample or real-world web application using industry-standard tools and methodologies. The goal was to identify security flaws, simulate exploitation where safe, and recommend mitigation strategies.

---

## 🧪 Scope of Assessment

- **Target**: Sample vulnerable web app (e.g., DVWA / Juice Shop / Custom test app)
- **Testing Type**: Black Box / Grey Box (Mention what you used)
- **Focus Areas**:
  - Input validation
  - Authentication
  - Session management
  - Authorization
  - Sensitive data exposure

---

## 🛠️ Tools Used

| Tool         | Purpose                      |
|--------------|-------------------------------|
| Burp Suite   | Manual testing, fuzzing       |
| Nmap         | Service & port discovery      |
| Nikto        | Web server vulnerability scan |
| OWASP ZAP    | Automated scanning            |
| WAFW00F      | WAF detection                 |
| Dirb / Gobuster | Directory brute forcing   |
| WhatWeb      | Web technology fingerprinting |

---

## 📊 Vulnerabilities Found

| Vulnerability             | Severity | Status   |
|---------------------------|----------|----------|
| Reflected XSS             | Medium   | Exploited|
| SQL Injection (Login)     | High     | Exploited|
| Directory Traversal       | Medium   | Verified |
| Information Disclosure    | Low      | Verified |
| Admin Panel Exposed       | High     | Verified |
| Outdated JS Libraries     | Low      | Reported |

---

## 🧠 Key Findings

### 1. 🔓 SQL Injection (Login Bypass)
- Parameter: `username`
- Payload: `' OR 1=1--`
- Impact: Unauthenticated access to admin dashboard.

### 2. 🧼 Reflected XSS
- Parameter: `search`
- Payload: `<script>alert('xss')</script>`
- Impact: JavaScript execution in user browser.

### 3. 🗂️ Directory Traversal
- URL: `/download?file=../../../../etc/passwd`
- Impact: Local file disclosure (Linux)

---

## 🔐 Mitigation Recommendations

- Use parameterized queries / ORM to avoid SQLi
- Sanitize all input/output using allow-lists
- Implement Content Security Policy (CSP)
- Hide sensitive endpoints via authentication + obscurity
- Keep libraries and frameworks up to date
- Deploy WAF with custom rules for application layer

---

## 📸 Screenshots

| Screenshot                        | Description                         |
|----------------------------------|-------------------------------------|
| login-bypass-sqli.png            | SQLi payload bypassing login        |
| reflected-xss-poc.png            | XSS alert popup example             |
| wafw00f-scan-result.png          | WAF detection result (optional)     |
| dirb-hidden-paths.png            | Directory enumeration results       |

---

## 📚 Learning Outcome

- Manual VAPT flow and OWASP Top 10 familiarity
- Crafting and testing payloads safely
- Using Burp Suite & ZAP efficiently
- Reporting findings in a professional format

---

## 🗂 Folder Structure

WebApp-VAPT/
├── README.md
├── screenshots/
│ ├── login-bypass-sqli.png
│ ├── reflected-xss-poc.png
│ ├── dirb-hidden-paths.png
├── payloads-used.txt
├── report.pdf (optional)
└── notes.md


---

## 🙋 About Me

I'm a Blue Team SOC Analyst transitioning into Red Teaming. This lab is part of my hands-on journey into offensive security, web testing, and threat simulation.

📌 Connect on [LinkedIn]( www.linkedin.com/in/aditya-kumar-goswami)

