# 🔑 IAM (Identity and Access Management)

**IAM** is a framework that ensures the right people, services, and applications have the **appropriate access** to the right resources at the right times.

IAM answers three core questions:  
1. **Who are you?** → Authentication  
2. **What are you allowed to do?** → Authorization  
3. **How do we prove and track this?** → Auditing  

---

## 🛡️ Authenticator Assurance Levels (AAL)

**Authenticator Assurance Levels (AAL)** define the strength of the authentication used to verify a user.  
These levels are standardized by **NIST (National Institute for Standards and Technology)**.

### 🔹 Levels:

- **AAL1 – Basic Level**  
  - Single-factor authentication (e.g., username + password)  
  - Suitable for non-critical services  

- **AAL2 – Medium Level**  
  - Two different authentication factors required:  
    1. Something you know (password)  
    2. Something you have (OTP, authenticator app, or hardware key)  

- **AAL3 – High Level**  
  - Strongest level, resistant to phishing  
  - Requires:  
    1. Hardware-based authenticator  
    2. Authenticator with verifier impersonation resistance  
  - Used for **highly sensitive services** like databases  

> Understanding AAL helps identify standards and compliance responsibilities, which is part of a **GRC (Governance, Risk, Compliance) role**.

---

## 🔐 Single Sign-On (SSO)

**SSO** allows users to **authenticate once** using a single set of credentials and access **multiple resources** without re-entering passwords.

### 🔹 Example: Active Directory
- Acts as a **central directory service**  
- Users are created once and can access multiple services  
- Prevents each application from performing separate authentication  

### 🔹 Federation & Protocols
- Users can authenticate with **one identity provider** and access multiple systems  
- Common protocols: **SAML, OAuth, OIDC**  

### 🔹 Benefits of SSO
- **Improved Security:** fewer passwords to manage  
- **Better User Experience:** authenticate once, access multiple applications  

---

## ✅ Key Takeaways

- **IAM** ensures proper authentication, authorization, and auditing  
- **AAL levels** define authentication strength based on service sensitivity  
- **SSO** improves security and usability by centralizing authentication  
- Standards like NIST help organizations implement IAM consistently and securely
