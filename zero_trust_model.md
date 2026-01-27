# 🏢 Zero Trust Model

**Zero Trust** is a cybersecurity model based on one simple principle:  
> **Never trust anyone by default, even internal employees.**

Every user and system must **continuously authenticate and be explicitly authorized** before accessing any resource, regardless of their location (inside or outside the network).

---

## 🔹 Why Zero Trust?

Traditionally:
- Security relied on a **perimeter firewall**
- Once inside the network, users were **implicitly trusted**
- Problem: stolen credentials could grant full access to the network  

Zero Trust fixes this by **verifying every request**, even from internal users.

---

## 🔹 Real-World Analogy

- Network = **office building**  
- Firewall = **front door guard** → checks identity once  
- Old model: after passing the guard, users access every room  
- Issue: identity theft lets attackers bypass security  
- Zero Trust: **every room requires verification**, even after entering the building

---

## 🔹 Core Principles

1. **Continuous Authentication & Authorization**
   - Every action and access request is validated
2. **Assume internal threats exist**
   - Internal users/devices can be compromised
3. **Encrypt traffic internally**
   - Protects data even within the network
4. **Multi-Factor Authentication (MFA)**
   - Uses multiple factors to calculate a **Trust Score** for access
5. **Context-Aware / Conditional Access**
   - Access can be restricted based on:
     - Device
     - Geolocation
     - Time/date
     - User behavior

---

## 🔹 Example: Trust Score

- Username/password correct → +1  
- Usual device → +1  
- Expected geolocation → +1  
- MFA passed → +2  

> Access granted only if **total trust score** meets the policy threshold

---

## 🔹 Conditional Access (Azure Example)

- Uses **Ruleset-Based Access Control**
- Conditional rules evaluate:
  - Time & date  
  - Device type & location  
  - User trust score  
- Allows granular access policies and reduces risk

---

## ✅ Key Takeaways

- **Zero Trust = continuous verification** for all users and devices  
- Prevents attackers from exploiting stolen credentials  
- Supports multi-layered security:
Perimeter Security → Network Segmentation → Zero Trust Policies
- Essential for protecting modern networks from both internal and external threats

🔐 **Remember:** Even internal traffic is treated as untrusted until verified.
