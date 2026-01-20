# Windows 10 Home Hardening Project
This project documents the process of hardening a Windows 10 Home virtual machine
---

## 🔐 Hardening Steps Completed

## 1. Windows Defender Configuration
- Enabled real-time protection
- Enabled cloud-delivered protection
- Enabled automatic sample submission
- Enabled tamper protection

## 2. Firewall Hardening
- Verified all firewall profiles (Private/Public) were enabled
- Confirmed default inbound/outbound rules

## 3. Service Hardening
- Disabled unnecessary services such as:
   - Remote Registry
   - Xbox Services
   - Print Spooler (optional)
   - Remote Desktop Services (optional)

## 4. NTFS Permission Review
- Verified inheritance and permissions on key system folders

## 5. Registry-Based Security Policies
- Enabled "Do Not Display Last Username"
- Enforced NTLMv2 Authentication
- Enabled USB write protection

## 6. Password & Lockout Policies
Configured using 'net accounts':
- Minimum password length: 12
- Maximum password age: 60 days
- Lockout threshold: 5 attempts
- Lockout duration: 15 minutes

## 7. Audit Policies
- Enabled Success/Failure auditing for Logon events
- Created an auditabled folder and verified Security Log entries
- Confirmed audit settings using 'auditpol'

## 8. Windows Update Hardening
- Enabled Microsoft product updates
- Enabled restart notifications
- Enabled automatic update behavior

---

## 📂 Screenshots
All Screenshots for each step are included in the **Screenshots** folder.

---

## ✅ Validation
Validation was performed using:
- 'Get-MpComputerStatus'
- 'Get-NetFirewallProfile'
- 'net accounts'
- 'auditpol /get /category:*'
- Registry Editor checks
- Windows Update settings review

All hardening controls were confirmed to be active.

---

## 🧩 Skills Demonstrated
- Windows Security configuration
- Registry-based policy enforcement
- Audit policy configuration
- System hardening methodology
- Documentation and validation
- Troubleshooting Home edition limitations

---

## 📌 Summary
This projects demonstrates the ability to harden a Windows 10 Home system using manual and registry-based methods. Even without enterprise tools like Group Policy or Local Security Policy, strong security 
controls were successfully implemented and validated. 
