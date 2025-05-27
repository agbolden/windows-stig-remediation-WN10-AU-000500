# Windows 10 STIG Remediation – WN10-AU-000500

This project demonstrates manual and automated remediation of a DISA STIG finding: `WN10-AU-000500` – *The Application event log size must be configured to 32768 KB or greater.*

## 🛠 Tools Used
- Azure-hosted Windows 10 VM
- Tenable.io (Advanced Scan)
- PowerShell (Registry Edit)

---

## 🔍 Overview of Remediation Workflow

1. Scan VM for STIGs using Tenable.io
2. Identify failed finding: `WN10-AU-000500`
3. Apply manual fix via registry
4. Verify success, then revert and rescan
5. Automate the fix using PowerShell
6. Rescan to confirm final remediation
7. Document process + upload screenshots and scripts

---

## 🧪 Screenshots

### 🔴 Initial Failure
![Baseline Failed](./screenshots/1_baseline_failed.png)

### ✅ Manual Remediation Pass
![Manual Pass](./screenshots/2_manual_fix_passed.png)

### 🔁 Reverted Manual Fix (Fails Again)
![Reverted Fail](./screenshots/3_reverted_fix_failed.png)

### ⚙️ PowerShell Fix Pass
![PowerShell Fix Pass](./screenshots/4_powershell_fix_passed.png)

### 🧾 PowerShell Script
![Script](./screenshots/5_powershell_script.png)

### 📊 STIG Reference Page
![STIG Reference](./screenshots/7_stig_reference_page.png)

---

## 💻 PowerShell Script

See `scripts/WN10-AU-000500_Remediation.ps1`.

---

## 📄 Documentation

See `STIG_Remediation_Report_WN10-AU-000500.md` for full breakdown.
