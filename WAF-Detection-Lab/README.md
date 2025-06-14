# 🛡️ WAF Detection and Bypass Lab

This lab demonstrates techniques to detect and bypass Web Application Firewalls (WAFs) using tools like **wafw00f** and **Burp Suite**.

---

## 🧰 Tools Used:
- **WAFW00F** - for WAF fingerprinting
- **Burp Suite** - for manual injection & testing
- **DVWA/BWAPP** - vulnerable web app
- **ModSecurity WAF** - protection layer

---

## 🔍 Detection Result

```bash
wafw00f http://target-site
Result: ModSecurity WAF Detected
