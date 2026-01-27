# 🔀 Switch Attacks

Switches play a critical role in internal network communication by forwarding traffic based on MAC addresses. Compromising a switch can seriously impact network confidentiality and allow attackers to intercept traffic that was never intended for them.

---

## 🧠 How Switches Forward Traffic

Switches rely on the **CAM Table (Content Addressable Memory)** to map devices to ports:

- MAC Address → Switch Port


This allows the switch to forward traffic only to the intended destination port, preventing other devices from seeing the traffic.

---

## 🚨 MAC Flooding Attack

### 🔍 Attack Overview
In a **MAC Flooding** attack, an attacker sends a large number of frames with spoofed or fake MAC addresses to the switch.

The switch attempts to store these entries in the CAM table until it becomes full.

---

### ⚠️ Impact of MAC Flooding
Once the CAM table overflows:
- The switch can no longer map MAC addresses correctly  
- It starts behaving like a **hub**  
- Incoming traffic is broadcast to **all ports**

This allows the attacker to:
- Capture traffic not intended for them  
- Perform packet sniffing  
- Steal sensitive data or session information  

🛑 This attack breaks network segmentation and compromises confidentiality.

---

## 🛰️ CDP Information Disclosure Attack

### 🔎 What Is CDP?
**Cisco Discovery Protocol (CDP)** is a proprietary protocol used by Cisco devices to:
- Discover neighboring Cisco devices  
- Share device and network information  
- Simplify network management  

CDP packets are typically sent in plaintext and can be observed by any device on the same network segment.

---

### 🕵️ Information Exposure
By sniffing CDP packets, an attacker may learn:
- Device vendor and model  
- Device hostname  
- IP address  
- Operating system and version  
- Network topology details  

---

### 🎯 Why This Information Is Dangerous
Knowing the **operating system version** allows an attacker to:
- Identify known vulnerabilities  
- Select applicable exploits  
- Reduce reconnaissance time  
- Increase the likelihood of a successful attack  

In many cases, CDP unintentionally provides attackers with valuable intelligence about the network.

---

## 🔐 Security Implications

- **MAC Flooding** enables unauthorized traffic interception  
- **CDP Information Disclosure** exposes internal network details  
- Both attacks can be performed from within the local network  
- Switches are often trusted and insufficiently monitored  

---

## ✅ Conclusion

Switches are foundational components of internal network security. Attacks such as MAC Flooding and CDP information disclosure demonstrate how misconfigured or unsecured switches can be exploited to compromise confidentiality and assist further attacks.

🛡️ **Securing switch configurations and limiting unnecessary discovery protocols are essential practices for SOC and Blue Team operations.**
