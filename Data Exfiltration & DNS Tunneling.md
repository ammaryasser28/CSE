# 🕵️ Data Exfiltration & DNS Tunneling

## 📌 Data Leakage vs Data Corruption

| Type | Description | Detection Difficulty |
|------|------------|--------------------|
| Data Corruption / Destruction | Hacker deletes or encrypts data | Relatively easy |
| Data Exfiltration (Leakage) | Hacker transfers data outside the network without being detected | Very hard, requires extra effort |

---

## 🚀 Hacker's Journey Inside a Network

1. Compromise a single machine.
2. **Reconnaissance**: Identify critical files and servers.
3. **Aggregation**: Collect all important files in one folder.
4. **Archiving / Encryption**: Compress and encrypt files to reduce size and avoid detection.
5. **Exfiltration**: Send data outside without being noticed.

**Simplest (but rare) method: Insider Threat**  
- Employee physically moves data via USB or Hard Drive.  
- No logs, no network traffic, no detection.

---

## 🎯 DNS Tunneling: The Smart Way

### Why DNS?
- DNS is almost always allowed outbound.
- Required for Internet functionality.
- Rarely blocked or deeply monitored.

---

### How DNS Tunneling Works

1. **Register a domain**
evil.com

Set up a DNS Server controlled by the attacker.

2. **Encrypt the data**
- Convert files to Base64:
"This is stolen data" → "dGhpcy1pcy1zdG9sZW4tZGF0YQ"


3. **Split the data**
- DNS Label max: 63 characters
- Divide data into chunks:
chunk1.evil.com
chunk2.evil.com


4. **Send the data**
- Compromised host performs DNS queries for each chunk.

5. **Attacker receives the data**
- DNS Server extracts the Subdomain
- Reassembles chunks
- Decodes → original data ✅

---

### 🔧 Command & Control via DNS

1. Attacker sends a command:
whoami

2. Compromised host executes → result:
corp\administrator

3. Result is Base64 encoded → sent as DNS Query:
mnxw24dmmuwwk3tbnr2a.attacker-domain.com

4. Attacker decodes → sees output

---

## ⚠️ Why It's Dangerous

- Bypasses Firewalls (DNS usually allowed)
- Bypasses IDS/IPS (DNS not always monitored)
- No direct connection needed
- Hard to detect in normal logs

---

## 🔎 How to Detect

Monitor DNS traffic for:
- Long and unusual Subdomains
- Excessive DNS queries to a single domain
- Base64 encoded strings in DNS queries

---

## 🛡️ Prevention

- Use DNS Filtering Solutions
- Monitor DNS logs in SIEM
- Restrict DNS queries to trusted servers only
- Integrate with DLP tools

---

## 📚 Summary

> DNS Tunneling is a technique to exfiltrate data or control devices by hiding information inside DNS queries, as DNS traffic is typically allowed and hard to monitor.


