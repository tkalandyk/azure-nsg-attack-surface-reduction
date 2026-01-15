
<img width="1536" height="1024" alt="ChatGPT Image Jan 14, 2026, 08_40_40 PM" src="https://github.com/user-attachments/assets/5036c536-50b9-476d-82a4-c2259cb68d27" />


# 🔐 Azure NSG Attack Surface Reduction  
### *RDP Hardening with Least Privilege Access*

---

## 🧠 Overview
This project demonstrates how a **small, targeted network control** can significantly reduce cloud breach risk.  
By tightening Azure Network Security Group (NSG) rules, unnecessary public exposure was eliminated while preserving required administrative access.

This mirrors real-world cloud security work where **speed, precision, and risk reduction** matter more than complexity.

---

## 🏗️ Environment
- ☁️ **Cloud Platform:** Microsoft Azure  
- 🖥️ **Asset:** Windows Virtual Machine  
- 🔒 **Security Control:** Network Security Group (NSG)  
- 🌍 **Region:** East US 2  

---

## ⚠️ Risk Identified
The virtual machine required RDP for administration.  
However, allowing inbound management access from broad sources increases exposure to:

- 🔓 Brute-force login attempts  
- 🤖 Automated internet scanning  
- 🔑 Credential stuffing attacks  

Management ports such as RDP (TCP 3389) are **high-value targets** for attackers.

---

## 🛠️ Remediation
Inbound RDP access (TCP 3389) was **restricted to a single trusted public IP address**, applying a **least-privilege** network policy.

All other inbound traffic remained **explicitly denied** by default.

---

## 📸 Evidence — NSG Hardening Applied
<img width="940" height="788" alt="Untitled design (1)" src="https://github.com/user-attachments/assets/52eb2dc6-24dc-4e5b-a1ac-089ca5e7fa7e" />


## 🎯 Outcome
- 🔽 Reduced the VM’s external attack surface  
- 🔐 Prevented unauthorized internet-based access attempts  
- ⚙️ No service interruption or downtime  
- 🚀 Immediate security posture improvement  

This change required **minutes**, not days, and delivered immediate risk reduction.

---

## 💡 Key Takeaway
Effective security is often about **intentional simplicity**.  
Restricting management access is one of the fastest, most reliable ways to reduce cloud breach risk.

> Small changes, when applied correctly, can prevent large incidents.

---


## 🧭 Framework Alignment

### MITRE ATT&CK
This control helps mitigate common attacker techniques associated with exposed management services:

- **T1133 – External Remote Services**  
  Restricting RDP access reduces exposure to internet-facing remote services commonly targeted for initial access.

- **T1078 – Valid Accounts**  
  Limiting access to trusted sources lowers the risk of credential-based abuse against remote management interfaces.

This change focuses on **preventing initial access**, rather than detecting malicious activity after compromise.

---


## 🧩 Real-World Note
In production environments, this control is commonly paired with:
- Azure Bastion  
- Just-In-Time (JIT) VM access  

These approaches further reduce exposure while maintaining operational flexibility.

---

## ✅ Why This Matters
This project demonstrates:
- Cloud security fundamentals  
- Least-privilege access control  
- Risk-based decision making  
- Business-focused security improvements  

It reflects how security teams **actually operate** in modern cloud environments.
