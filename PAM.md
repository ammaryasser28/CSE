# PAM - Privileged Access Management

## What is a Privileged Account?
A privileged account is a user or system account with elevated permissions capable of performing sensitive and potentially dangerous actions on systems.

**Examples:**
- `Administrator` in Windows
- `root` in Linux

**Privileges include:**
- Installing or removing software
- Changing system or security settings
- Creating, modifying, or deleting users
- Accessing sensitive data (logs, configs, databases)
- Controlling other systems or services

> Privileged accounts are often called **"Keys to the Kingdom"** because if compromised, an attacker can control the entire system.

---

## What is PAM?
**Privileged Access Management (PAM)** is a system used to manage, secure, and monitor privileged accounts in an organization.

---

## How PAM Works
- Instead of admins logging in directly to every server, they log in through a **PAM Portal**.
- All activities on servers are logged and monitored.
- Flow:
Admin → PAM → Server

---

## Key PAM Functions

### 1. Session Recording
- Logs all commands executed by admins
- Acts like a surveillance camera for privileged sessions

### 2. Password Management
- Enforces strong password policies:
  - Uppercase and lowercase letters
  - Numbers and symbols
- Can generate strong passwords automatically

### 3. Secure Password Storage
- Passwords are **not stored locally**
- Stored securely in a PAM vault

### 4. Password Rotation
- Automatically rotates passwords at set intervals
- Prevents reuse of the same password for extended periods

### 5. Access Control
- Restricts access to specific systems
- Can limit access to approved devices or specific times

---

## Practical Example
A company with 50 servers:

- **Without PAM:** Each admin has separate passwords for each server  
- **With PAM:** Admin logs into PAM Portal, which manages server access, and all activities are logged and controlled

---

## Summary
**PAM =**
- Managing privileged accounts  
- Storing passwords securely  
- Recording and monitoring admin sessions  
- Automatic password rotation  
- Controlling who can access what, where, and when

