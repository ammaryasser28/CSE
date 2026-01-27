# 🛡️ Defense in Depth

**Defense in Depth** is a cybersecurity strategy that protects systems using **multiple, independent layers of security**.  
If one layer fails, another can stop or slow an attacker, reducing the overall risk.

---

## 🎯 Why Defense in Depth?

- Historically, organizations relied on **a single perimeter firewall** to protect public assets.  
- Modern networks and applications are **complex**, and one security control is no longer sufficient.  
- Defense in Depth ensures that multiple layers work together to protect critical assets.

**Example Layers:**
Firewall + IDS + EDR + Hardening + IAM + Logging + Backups + Training + Network Segmentation


---

## 🧱 Layers of Defense

### 1️⃣ Perimeter Security 🌐
- Focus: Protect network borders  
- Devices: Firewalls, Proxy Servers, Anti-DDoS appliances  
- Purpose: Mitigate threats from the Internet or untrusted networks  

### 2️⃣ Network Security 🔗
- Focus: Protect internal network  
- Techniques: Network segmentation, VLANs, Network Access Control (NAC)  
- Purpose: Limit lateral movement of attackers  

### 3️⃣ Host Security 💻
- Focus: Secure endpoints and servers  
- Techniques: System hardening, vulnerability scanning, application control, anti-malware  
- Purpose: Reduce risk of compromise at the system level  

### 4️⃣ Application Security 🖥️
- Focus: Secure software and applications  
- Techniques: Authentication mechanisms, input validation, buffer overflow protection, secure coding  
- Purpose: Prevent application-level attacks  

### 5️⃣ Data Security 🔐
- Focus: Protect sensitive data  
- Techniques: Encryption, data classification, access policies  
- Purpose: Ensure confidentiality and integrity even if other layers are breached  

---

## ✅ Summary

**Defense in Depth** = Multiple, independent security layers protecting the same asset:
Perimeter Security → Network Security → Host Security → Application Security → Data Security


- Each layer increases attack complexity  
- Reduces impact of any single security failure  
- Essential for SOC analysts and cybersecurity professionals to safeguard networks and assets  

🔐 **Goal:** Make compromising any part of the network difficult and minimize potential damage.

