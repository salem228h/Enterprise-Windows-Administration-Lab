# 💻 Windows Enterprise Workstation Deployment

> Simulated Week 1 Desktop Support scenario:
> configure the first standardized Windows 11 Enterprise image
> for a 20-laptop corporate rollout.

![](https://img.shields.io/badge/OS-Windows%2011%20Enterprise-blue)
![](https://img.shields.io/badge/Role-Desktop%20Support%20Technician-lightgrey)
![](https://img.shields.io/badge/Platform-VMware%20Workstation-orange)
![](https://img.shields.io/badge/Progress-3%20of%2010%20Complete-yellow)

---

## Overview

A hands-on IT support project simulating real-world Desktop Support tasks.
Starting from a clean Windows 11 install, this project covers
security hardening, user management, networking, and system administration —
using only native Windows tools and CMD.

**Role simulated:** Desktop Support Technician / IT Support Specialist

---

## Progress

| Phase | Topic | Status |
|-------|-------|--------|
| 1 | Baseline Documentation | ✅ Complete |
| 2 | Workstation Standardization | ✅ Complete |
| 3 | Local Users & Groups | ✅ Complete |
| 4 | Windows Security Hardening | ⏳ In Progress |
| 5 | Windows Defender | ⏳ Pending |
| 6 | BitLocker | ⏳ Pending |
| 7 | Windows Firewall | ⏳ Pending |
| 8 | Networking Tools | ⏳ Pending |
| 9 | Event Viewer & Performance Monitor | ⏳ Pending |
| 10 | Final Documentation & Validation | ⏳ Pending |

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
- Applied initial Windows Updates to bring system to current patch level

### Phase 3 — Local Users & Groups ✅
- Created Administrator and Standard User accounts
- Verified group membership and permission levels
- Tested login behavior for each account type

### Phase 4 — Windows Security Hardening ⏳
- Configure Windows Security baseline settings
- Disable unnecessary services and features
- Apply CIS Benchmark recommendations

### Phase 5 — Windows Defender ⏳
- Verify real-time protection and cloud-delivered protection
- Run full system scan and review results
- Configure exclusions and scheduled scans

### Phase 6 — BitLocker ⏳
- Enable BitLocker on the OS drive
- Save and document recovery key securely
- Verify encryption status

### Phase 7 — Windows Firewall ⏳
- Review Domain / Private / Public firewall profiles
- Create custom inbound and outbound rules
- Test and validate rule behavior

### Phase 8 — Networking Tools ⏳
- Configure static IP addressing
- Verify connectivity using `ipconfig /all` · `ping` · `nslookup`
- Document network configuration

### Phase 9 — Event Viewer & Performance Monitor ⏳
- Investigate System and Application logs
- Identify and document warning and error events
- Track CPU, RAM, and Disk usage via Performance Monitor

### Phase 10 — Final Documentation & Validation ⏳
- Complete all docs: checklist · lessons learned · troubleshooting
- Final screenshot evidence for all phases
- Validate against deployment checklist

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

**2. Windows 11 hardware requirements blocked the install**
TPM 2.0 and Secure Boot must be enabled before starting the install —
not something you can fix after the fact.

**3. Static IP broke DNS resolution**
After setting a static IP, `ping google.com` failed
but `ping 8.8.8.8` worked.
Fix: manually set preferred DNS to `8.8.8.8`.

**4. sfc /scannow requires elevated CMD**
Must right-click → Run as administrator.
Exactly the kind of thing a help desk call is about.

**5. Firewall rule order matters**
A broader allow rule higher in the list was overriding
my custom block rule. Moved the block rule above it — fixed.
Firewall rules evaluate top-down. Order is everything.

---

## Author

**Mohammad Salem Hassani**
IT Support Specialist · 2026
