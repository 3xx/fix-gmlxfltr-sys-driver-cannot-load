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

## ⚠️ CRITICAL WARNING

Before starting the fix, you MUST completely disconnect the **Attack Shark Mouse** and remove all related devices, including the USB dongle, wireless receiver, or any connected accessory.

If you do not disconnect the device first, the driver may reinstall automatically during the removal process, and the fix may fail.

---

## 💥 Solution (Permanent Fix)

> ⚠️ This method completely removes the driver from your system.

### 🧾 Requirements

- Administrator privileges
- Command Prompt (Run as Administrator)

---

## ⚙️ Fix Commands

> ⚠️ `oemXXX.inf` is NOT fixed and will be different on each system.  
> First run the detection command below, find the matching `Published Name`, then replace `oemXXX.inf` with the exact value shown on your system.

```bash
sc.exe delete GMLXDFltr
del C:\Windows\System32\drivers\GMLXDFltr.sys
pnputil /enum-drivers | findstr /i GMLXDFltr
pnputil /delete-driver oemXXX.inf /uninstall /force
shutdown /r /t 0
