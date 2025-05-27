# STIG Remediation Report – WN10-AU-000500

**Title:** The Application event log size must be configured to 32768 KB or greater  
**STIG ID:** WN10-AU-000500  
**Severity:** Medium  
**Vuln ID:** V-220779  
**Registry Path:** `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\EventLog\Application`  
**Value Name:** MaxSize  
**Required Value:** `32768` (decimal)  

---

## 🔎 Summary

A Tenable scan identified that the `MaxSize` registry value was not set properly for the Application Event Log. This could result in logs filling up quickly, leading to loss of audit data and compliance violations.

---

## 🛠 Manual Remediation Steps

1. Open `regedit`
2. Navigate to:  
   `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\EventLog\Application`
3. Add or update `MaxSize` as a `REG_DWORD` with value `32768`

✅ Verified in Tenable: STIG passed after manual fix.

---

## 🔁 Reverted Manual Fix

The change was undone to test detection again.

🔴 Result: STIG failed as expected.

---

## ⚙️ PowerShell Remediation

See [`scripts/WN10-AU-000500_Remediation.ps1`](./scripts/WN10-AU-000500_Remediation.ps1)

✅ Ran PowerShell script → rescanned → STIG passed.

---

## ✅ Final Result

STIG `WN10-AU-000500` remediated and verified through automated scripting.

Screenshots available in `/screenshots` folder.
