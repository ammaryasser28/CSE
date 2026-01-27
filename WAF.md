# 🌐 WAF (Web Application Firewall)

**Web Application Firewall (WAF)** is a security control that sits in front of web applications to **inspect HTTP/HTTPS traffic at Layer 7**. It detects and blocks malicious requests before they reach the application.

---

## 🔹 Traditional Firewall vs WAF

### 🖥️ Traditional Firewall
- Works at **Layer 3 & Layer 4**  
- Focuses on:
  - IP addresses  
  - Ports  
  - Protocols  

**Example:**
- TCP Port 443 → ALLOWED
> The firewall sees only that the HTTPS connection is allowed; it does not inspect the content.

---

### 🛡️ WAF
- Works at **Layer 7 (Application Layer)**  
- Understands:
  - HTTP methods (GET, POST, etc.)  
  - URLs and parameters  
  - Cookies and request bodies  

**Example:**
- GET /login.php?user=admin' OR '1'='1 → BLOCK
> WAF detects an **SQL Injection attempt** and blocks it before it reaches the web application.


<img width="729" height="289" alt="image" src="https://github.com/user-attachments/assets/0f3e9e31-2d25-45a9-8180-e486ac85a659" />

---

## 🚨 Why WAF is Important

- Modern attacks target **applications**, not just the network  
- Traditional firewalls **cannot detect application-level attacks**  
- WAF protects against:
  - SQL Injection  
  - Cross-Site Scripting (XSS)  
  - Command Injection  
  - File Inclusion  
  - Other OWASP Top 10 attacks  

---

## 🎯 WAF in Defense in Depth

WAF acts as an **additional layer of defense** in a multi-layered security strategy:

```
Firewall (L3/L4)
↓
WAF (L7)
↓
Web Application
```

- Traffic passes through the firewall  
- WAF inspects content and blocks malicious behavior  
- Reduces the risk of application compromise  

---

## ✅ Summary

- **Firewall** controls access to the network  
- **WAF** controls the behavior of requests at the application level  
- Using both together provides **strong protection for web applications**  

🔐 **Any public-facing web application without a WAF is an easy target for modern attacks.**
