# 🖧 VLANs (Virtual LANs)

**VLANs (Virtual Local Area Networks)** are logical network segments created on the same physical network to separate devices and control communication. VLANs are primarily configured by network administrators but provide significant security benefits that SOC and Blue Team analysts should understand.

---

## 🎯 Purpose of VLANs

The main purposes of VLANs are:

- **Network Segmentation:** Separates devices into isolated groups  
- **Policy Management:** Applies specific rules and access controls per group  
- **Security:** Limits lateral movement of attackers across the network  

---

## 🔹 How VLAN Segmentation Works

Without VLANs, all devices are on the same network. If a single device is compromised, the attacker can move freely to any other device.  

With VLANs:
- Different departments or device types are isolated:
  - HR → VLAN1  
  - IT → VLAN2  
  - IoT Devices → VLAN3  
  - Servers → VLAN4  

**Result:** An attacker inside one VLAN cannot directly access devices in another VLAN without additional exploitation.

---

## 🔹 Policy Enforcement with VLANs

VLANs make it easier to enforce network policies:
- Restrict access to only authorized devices and users per VLAN  
- Apply Quality of Service (QoS) or monitoring per VLAN  
- Control traffic flow for different teams or functions

**Example:**
- Finance Team → VLAN with access only to finance servers  
- Marketing Team → VLAN with access only to marketing resources  

---

## 🧠 Importance for SOC Analysts

For SOC and Blue Team operations, VLANs provide:
- A logical map of network communication  
- Insight into normal vs abnormal traffic between VLANs  
- Detection of attacks such as **VLAN hopping**, which are indicators of lateral movement attempts  

---

## ✅ Conclusion

- VLANs are a critical tool for **network segmentation and security**  
- They reduce the potential for lateral movement by attackers  
- Simplify policy application and monitoring for different teams  
- SOC Analysts should understand VLAN structure to detect abnormal activity effectively  

🔐 **Understanding VLANs is essential for improving internal network security and monitoring.**
