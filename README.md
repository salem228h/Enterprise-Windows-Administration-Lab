# 💻 Windows Enterprise Workstation Deployment

> Simulated Week 1 Desktop Support scenario:
> configure the first standardized Windows 11 Enterprise image
> for a 20-laptop corporate rollout.

![](https://img.shields.io/badge/OS-Windows%2011%20Enterprise-blue)
![](https://img.shields.io/badge/Role-Desktop%20Support%20Technician-lightgrey)
![](https://img.shields.io/badge/Platform-VMware%20Workstation-orange)
![](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## Overview

A hands-on IT support project simulating real-world Desktop Support tasks.
Starting from a clean Windows 11 install, this project covers
security hardening, user management, networking, and system administration —
using only native Windows tools and CMD.

**Role simulated:** Desktop Support Technician / IT Support Specialist

---

## Environment

| Component | Detail |
|-----------|--------|
| Virtualization | VMware Workstation |
| OS | Windows 11 Enterprise |
| Tools | Local Users & Groups · Windows Defender · BitLocker |
| | Windows Firewall · CMD · Event Viewer · Performance Monitor |

---

## Tasks Completed

### Phase 1 — Baseline Documentation ✅
- Documented system specifications and hardware inventory
- Captured baseline screenshots before any configuration
- Created deployment checklist for standardized rollout

### Phase 2 — Workstation Standardization ✅
- Clean install of Windows 11 Enterprise in VMware
- Configured computer name, region, time zone, and display settings
- Applied all pending Windows Updates

### Phase 3 — Local Users & Groups ✅
- Created Administrator and Standard User accounts
- Verified group membership and permission levels
- Tested login behavior for each account type

### Phase 4 — Windows Security Hardening ✅
- Applied Windows Security baseline settings
- Disabled unnecessary services and features
- Validated configuration against CIS Benchmark recommendations

### Phase 5 — Windows Defender ✅
- Verified real-time and cloud-delivered protection
- Ran full system scan — no threats detected
- Configured scheduled scans

### Phase 6 — BitLocker ✅
- Enabled BitLocker on the OS drive
- Recovery key saved and documented securely
- Verified encryption status — fully encrypted

### Phase 7 — Windows Firewall ✅
- Reviewed Domain / Private / Public profiles
- Created custom inbound rule and validated behavior
- Confirmed rule order and default-deny posture

### Phase 8 — Networking Tools ✅
- Configured static IP addressing
- Verified connectivity: `ipconfig /all` · `ping` · `nslookup`
- Documented full network configuration

### Phase 9 — Event Viewer & Performance Monitor ✅
- Investigated System and Application logs
- Identified and documented a sample warning event
- Tracked CPU, RAM, and Disk via Performance Monitor data collector set

### Phase 10 — Final Documentation & Validation ✅
- All phases documented with screenshot evidence
- Deployment checklist signed off
- Lessons learned and troubleshooting guide completed

---

## Key Commands

```cmd
:: System info
systeminfo
hostname
winver

:: Network diagnostics
ipconfig /all
ping 8.8.8.8
nslookup google.com
netstat -an

:: User management
net user
net localgroup administrators
lusrmgr.msc

:: System health
sfc /scannow
chkdsk C: /f
eventvwr.msc

:: Security
Get-BitLockerVolume
netsh advfirewall show all
```

---

## Repository Structure
Enterprise-Windows-Workstation/
├── README.md
├── screenshots/
│   ├── 01-baseline/
│   ├── 02-standardization/
│   ├── 03-users-groups/
│   ├── 04-security-hardening/
│   ├── 05-windows-defender/
│   ├── 06-bitlocker/
│   ├── 07-firewall/
│   ├── 08-networking/
│   └── 09-event-viewer-perfmon/
├── docs/
│   ├── Build-Checklist.md
│   ├── Lessons-Learned.md
│   └── Troubleshooting.md
├── scripts/
│   └── admin-commands.md
└── LICENSE

---

## Skills Demonstrated

`Windows 11 Deployment` `Local Account Management`
`Endpoint Security` `BitLocker Encryption`
`Firewall Configuration` `TCP/IP Networking`
`CMD Administration` `Event Log Analysis`
`Performance Monitoring` `System Troubleshooting`

---

## Lessons Learned

**1. BitLocker requires TPM — not enabled by default in VMware**
Had to enable virtual TPM in VM Settings → Security → Enable TPM
before BitLocker would activate.

**2. Windows 11 blocked install without TPM 2.0 and Secure Boot**
Both must be enabled before starting the OS install —
not something you can fix after the fact.

**3. Static IP broke DNS resolution**
After setting a static IP, `ping google.com` failed
but `ping 8.8.8.8` worked.
Fix: manually added `8.8.8.8` as preferred DNS.

**4. sfc /scannow requires elevated CMD**
Must right-click → Run as administrator.
Exactly the kind of mistake a help desk call is about.

**5. Firewall rule order matters**
A broader allow rule was overriding my custom block rule.
Moved the block rule above it — fixed immediately.
Rules evaluate top-down. Order is everything.

---

## Author

**Mohammad Salem Hassani**
IT Support Specialist · 2026
