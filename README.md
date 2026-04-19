# 🛠 GMLXDFltr.sys Driver Fix


<p align="center">
  <img src="https://img.shields.io/badge/Windows-10%20%7C%2011-blue?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Status-Stable-success?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Fix-Permanent-critical?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge"/>
</p>

---

## 📸 Preview

<p align="center">
  <img width="582" height="320" src="https://github.com/user-attachments/assets/85653b54-499d-483b-9bbd-9606976713a6"/>
</p>

---

## 🚨 Issue

Windows may block the following driver:

**GMLXDFltr.sys**

---

## ⚠️ CRITICAL WARNING (READ BEFORE FIX)

Before starting the fix:

- You MUST completely disconnect **Attack Shark Mouse**
- Remove:
  - USB dongle  
  - Wireless receiver  
  - Any related device  

Failure to do this may cause:
- Driver reinstall during removal  
- Fix not working properly  

---

## 💥 Solution (Permanent Fix)

> ⚠️ This method completely removes the driver from your system

### 🧾 Requirements

- Administrator privileges  
- Command Prompt (Run as Administrator)  

---

## ⚙️ Fix Commands

Run the following commands in **Command Prompt (Admin):**

```bash
sc.exe delete GMLXDFltr
del C:\Windows\System32\drivers\GMLXDFltr.sys
pnputil /delete-driver oem77.inf /uninstall /force
shutdown /r /t 0
