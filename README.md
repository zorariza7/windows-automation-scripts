# windows-automation-scripts
Simple automation scripts for Windows troubleshooting and maintenance.
# Windows Automation Scripts

A collection of simple Windows automation scripts for IT Support tasks.  
These scripts are designed to speed up routine troubleshooting, maintenance, and diagnostics.

All scripts are safe, lightweight, and created for educational and practical IT Support use.

---

## 1. System Cleanup Script (Batch)
Clears temporary files and frees storage space.

**File:** `cleanup_temp.bat`

del /q/f/s %TEMP%* del /q/f/s C:\Windows\Temp*

---

## 2. Network Adapter Reset (Batch)
Resets network configs to fix connectivity issues.

**File:** `reset_network.bat`

ipconfig /flushdns ipconfig /release ipconfig /renew netsh winsock reset

---

## 3. Basic System Info (PowerShell)
Shows essential system information for troubleshooting.

**File:** `system_info.ps1`

Get-ComputerInfo | Select-Object WindowsVersion, CsTotalPhysicalMemory, CsName, OsArchitecture

---

## 4. Installed Apps Report (PowerShell)
Lists installed software (useful for audits or malware checks).

**File:** `installed_apps.ps1`

Get-WmiObject -Class Win32_Product | Select-Object Name, Version

---

## 5. Windows Update Trigger (Batch)
Forces Windows to search for updates manually.

**File:** `force_update.bat`

wuauclt /detectnow wuauclt /updatenow

---

## Future Plans
- Automate printer troubleshooting
- Auto-backup script
- Local account audit script
- Event Viewer log extractor


---
