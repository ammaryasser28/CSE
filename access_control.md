# 🔒 Access Control

**Access Control** ensures that individuals or systems can access only the resources necessary to perform their job, and nothing more.

### 🔹 Principle of Least Privilege
- Grants **minimum access** needed for a task  
- Reduces risk of accidental or malicious misuse  

### 🔹 Separation of Duties
- Divides sensitive tasks among multiple people  
- Prevents a single person from completing a critical action alone  
- Example: If all critical tasks are assigned to one skilled person, compromising their credentials puts the system at risk ⚠️

---

## 🛡️ Access Control Techniques

### 1️⃣ Discretionary Access Control (DAC)
- **Definition:** Resource owner decides who can access it  
- **Example:** File permissions on your computer  
  - You create a file → decide who can read/edit it  
  - If you give full control, the other person can share it further  
- **Pros:** Flexible, intuitive  
- **Cons:** Access can spread uncontrolled  
- **Real-world examples:** Windows NTFS, Linux file permissions, Google Drive sharing

---

### 2️⃣ Mandatory Access Control (MAC)
- **Definition:** System enforces access rules based on security classifications  
- Users **cannot override** the policy  
- Common in **military or government systems**  
  - Documents classified as Top Secret, Secret, Confidential, Unclassified  
  - Users can access only documents at or below their clearance  
- **Pros:** High security  
- **Cons:** Less flexible  

---

### 3️⃣ Role-Based Access Control (RBAC)
- **Definition:** Permissions are assigned to roles → users are assigned to roles  
- Easier to manage than individual permissions  
- **Example in a hospital:**
  - **Doctor:** read/write patient records, prescribe medications  
  - **Nurse:** read records, update vitals, cannot prescribe medications  
  - **Receptionist:** schedule appointments, view basic info, no access to medical history  

---

## ✅ Key Takeaways
- **Least privilege** reduces risk  
- **Separation of duties** prevents abuse of power or accidental breaches  
- **DAC** is flexible but less controlled  
- **MAC** is strict and highly secure  
- **RBAC** simplifies management by assigning permissions to roles  

> Proper access control is essential for protecting sensitive data and ensuring security compliance in organizations.
