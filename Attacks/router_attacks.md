# 🛜 Router Attacks

During network penetration testing and security assessments, routers and switches are often overlooked compared to servers and endpoints. However, compromising these devices can have a severe impact, as routers act as critical gateways for all network traffic.

---

## 🚨 Denial of Service (DoS) and Distributed DoS (DDoS)

### 🔴 Denial of Service (DoS)
A **DoS attack** is launched from a single host and a single IP address with the goal of disrupting the availability of a router.

Router availability is critical—especially for **perimeter routers**—because taking them offline can impact the entire organization.

### 📌 Impact Example
- Attacking a single public service → Only that service is affected  
- Attacking the perimeter router →  
  - Complete internet outage  
  - All internal and external services disrupted  

This makes routers a highly attractive target for attackers.

---

## ⚙️ Planned Downtime as Self‑Inflicted DoS

Applying operating system updates and security patches to routers is essential for mitigating vulnerabilities. However, these updates often require:
- Device reboot  
- Temporary service interruption  

This downtime can be considered a **planned, self‑inflicted denial of service**. Despite the short‑term disruption, failing to apply updates may result in long‑term security risks and significant financial losses that can reach millions of dollars.

---

## 🧱 Mitigating DoS vs DDoS Attacks

### 🟢 DoS Mitigation
DoS attacks are relatively easier to mitigate because they originate from a limited number of sources.

Common mitigation techniques include:
- Access Control Lists (ACLs)  
- Rate limiting  
- Request filtering  
- Coordination with the ISP (e.g., Orange)

---

### 🔴 DDoS Challenges
Unlike DoS attacks, **DDoS attacks** originate from thousands or even millions of IP addresses simultaneously.

This makes them:
- More difficult to detect  
- Harder to block using traditional filtering  
- Dependent on advanced mitigation strategies such as ISP‑level filtering or traffic scrubbing services  

---

## 🕵️ Packet Sniffing on Routers

There is no better place for packet sniffing than a router. Every packet that requires routing passes through it, making routers ideal monitoring points.

### ⚠️ Security Risk
If an attacker gains control of a router, they may:
- Capture unencrypted traffic  
- Intercept credentials and sessions  
- Monitor sensitive communications  

This highlights the importance of securing router access and configurations.

---

## 🔄 Routing Table Poisoning

### 🎯 What Is Routing Table Poisoning?
Routing table poisoning involves manipulating routing information to alter the path of network traffic.

### 🚨 Attack Scenarios
- **Man‑in‑the‑Middle (MITM):**  
  Traffic is redirected through the attacker’s network for interception and then forwarded to the original destination to avoid detection.

- **Traffic Blackholing:**  
  Traffic is routed to a non‑existent network, causing service disruption and freezing network operations.

Both scenarios can severely impact network availability and confidentiality.

---

## ✅ Conclusion

Routers are not just networking devices—they are critical control points for all traffic flowing through the network. Compromising them can lead to:
- DoS and DDoS attacks  
- Packet sniffing and data interception  
- Man‑in‑the‑Middle attacks  
- Complete network outages  

🔐 **Securing network devices is just as important as securing servers and endpoints and is a key responsibility for SOC and Blue Team operations.**
