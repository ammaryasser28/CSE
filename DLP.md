# 🔐 Data Loss Prevention (DLP)

## Overview
**Data Loss Prevention (DLP)** is a set of tools and policies designed to protect sensitive data from:

- Unauthorized access  
- Accidental exposure  
- Intentional or unintentional data leakage  

**Primary Goal:** Protect data confidentiality and prevent sensitive information from leaving the organization.

---

## 1. Attacker Objectives
When an attacker gains access to a network, objectives may include:

### Service Disruption
Disabling systems or services.  
**Examples:**
- DDoS attacks  
- System shutdowns  

### Data Corruption
Modifying, deleting, or encrypting data to make it unusable.

### Data Leakage
Stealing sensitive information and transferring it outside the organization.  

**Modern ransomware often uses Double Extortion:**
1. Data exfiltration  
2. Data encryption  
3. Threaten to publish the data if ransom is not paid  

---

## 2. Data Corruption vs Data Leakage

| Type | Description | Security Impact |
|------|------------|----------------|
| Data Corruption | Data is altered, damaged, or encrypted | Integrity |
| Data Leakage | Data is exposed to unauthorized parties | Confidentiality |

**Examples**

**Data Corruption**
- Database encrypted by ransomware  
- Files modified or damaged  

**Data Leakage**
- Employee sends customer data to personal email  
- Sensitive files uploaded to external cloud storage  

---

## 3. Sources of Data Loss
Data loss is not always caused by attackers.

### External Attackers
- Network compromise  
- Data exfiltration  

### Insider Threats
- Uploading company files to personal cloud accounts  
- Sending sensitive data externally  
- Copying data to USB devices  

> Insider activity is one of the most common causes of data leakage.

### Accidental Actions
- Deleting important files  
- Sending data to the wrong recipient  

### Environmental Factors
- Fire or flood  
- Hardware or data center failure  

---

## 4. SOC Analyst Role in DLP
SOC analysts monitor user activity and investigate potential data leakage incidents.

### Cloud Activity Monitoring
Watch for traffic to external storage services such as:
- Google Drive  
- Dropbox  
- OneDrive  

**Purpose:** Detect unauthorized data uploads.

### Website Categorization
Security solutions categorize websites by type.  

**Example Rule:**
```text
If internal traffic goes to category: Cloud Storage
→ Generate Alert
This allows detection even if the specific site is unknown.
```
---

## 5. What DLP Tools Monitor

- **Email:** Detect or block sensitive data sent externally  
  *Example:* Credit card numbers

- **Cloud Services:** Monitor or block file uploads to external storage

- **Removable Media:** USB drives, external hard disks

---

## 6. Data Classification (Critical Requirement)

DLP effectiveness depends on proper data classification.

| Classification | Example |
|----------------|---------|
| Public | Website content |
| Internal | Internal documents |
| Confidential | Customer data |
| Restricted / Top Secret | Financial records, salaries |

> Without classification, DLP systems cannot determine what data needs protection.

---

## 7. DLP Policies

Policies define allowed or blocked actions.

**Examples:**
- Block sending credit card data via external email
- Prevent copying HR files to USB
- Generate alerts when files are uploaded to Dropbox

---

## 8. Integration with SIEM

DLP systems send alerts to a SIEM platform for centralized monitoring.

**Example Alert:**
```text
User: Ahmed
Action: File Upload
Destination: Google Drive
Content: Customer Data Detected
```
## SOC Analyst Responsibilities

- **Validate the activity**  
- **Determine if it is:**
  - Legitimate business use
  - Policy violation
  - Malicious activity
  - False positive

---

## 🎯 Interview Key Points

- DLP prevents data leakage  
- Data Corruption affects **Integrity**  
- Insider threats are a major risk  
- Data Classification is essential for DLP  
- DLP monitors:
  - Email
  - Cloud storage
  - USB devices  
- Alerts are analyzed through SIEM

---

## 🛠 Real SOC Investigation Scenario

**Alert:** A user uploaded a file containing customer data to Google Drive.

**Investigation Steps:**
1. Identify the user and department  
2. Verify business justification  
3. Check data sensitivity level  
4. Review user activity history  
5. Escalate if the action is unauthorized
