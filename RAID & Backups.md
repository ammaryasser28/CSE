# 🗄️ RAID & Backups – Complete Guide

## Overview
RAID and Backups are essential for **data reliability, performance, and disaster recovery** in any organization.

---

## 1️⃣ RAID – Redundant Array of Independent Disks

RAID is a technology that combines multiple hard drives into a single logical unit to provide:

- **Performance** (speed)  
- **Fault Tolerance** (protection from drive failure)  
- Or both

### RAID Levels

| RAID Level | Description | Pros | Cons | Use Case |
|------------|------------|------|------|----------|
| RAID 0 🏎️ | Striping – data split across disks | Very fast | No protection, one disk fail → all lost | Video editing |
| RAID 1 🪞 | Mirroring – data copied on 2 disks | Full protection, simple | Uses 2x storage | HR/Finance data |
| RAID 5 ⚖️ | Striping + single parity | Balanced speed & protection | Can lose 1 disk only | Small/medium businesses |
| RAID 6 🛡️ | Striping + double parity | Can lose 2 disks | Slightly slower | Critical servers |
| RAID 10 👑 | RAID 1 + RAID 0 | High speed + high protection | Expensive, double storage | Enterprise databases |

> **Tip:** RAID is not a backup solution. It only improves availability and fault tolerance.

---

## 2️⃣ Backups – Protecting Your Data

Backups are **not just copy-paste**.  
Proper backups are critical to recover from accidental loss, hardware failure, or ransomware attacks.

### Types of Backups

#### Full Backup
- Copies **everything**  
- **Pros:** Easy restore  
- **Cons:** Time-consuming, large storage  
Source: [A][B][C][D][E]
Backup: [A][B][C][D][E]

#### Incremental Backup
- Copies **only changes** since last backup (Full or Incremental)  
- **Pros:** Fast, small storage  
- **Cons:** Restore requires all increments in order  
Sunday: FULL → [A][B][C][D][E]
Monday: INC → [F]
Tuesday: INC → [G][C*]
Wednesday: INC → [H]

#### Differential Backup
- Copies **all changes since last Full backup**  
- **Pros:** Easier restore than Incremental  
- **Cons:** Larger storage than Incremental  
Sunday: FULL → [A][B][C][D][E]
Monday: DIFF → [F]
Tuesday: DIFF → [F][G][C*]
Wednesday: DIFF → [F][G][C*][H]

---

### Comparison Table

| Backup Type | Size | Backup Speed | Restore Speed |
|-------------|------|--------------|---------------|
| Full        | Large | Slow        | Fast          |
| Incremental | Very Small | Fast    | Slow          |
| Differential| Medium | Medium     | Medium        |

---

## ⚠️ Backup Isolation
- If **Backup Storage is always connected** to the network, ransomware can encrypt backups too  
- **Best Practice:** Isolate backups from production network. Connect **only during backup**, then disconnect immediately.

---

## 🔒 Best Practices
1. **Verify Backups** – Check logs or SIEM to ensure backups completed successfully  
2. **Encrypt Data at Rest** – Protect data even if storage is compromised  
3. **Multi-Vendor Security** – Don’t rely on a single backup vendor  

---

## 💸 Why Companies Invest Millions?
- **GDPR Fines:** Up to 4% of annual global revenue for data breaches  
- **Reputational Damage:** Customers may leave  
- Backup & security are **investments, not expenses**  

---

## Summary
- **RAID** improves availability and speed  
- **Backups** are critical for disaster recovery  
- **Incremental vs Differential**: Incremental = smaller/faster backup, Differential = easier restore  
- **Isolation & verification** are crucial for ransomware protection  
- **Security compliance** (GDPR, etc.) drives investment  

