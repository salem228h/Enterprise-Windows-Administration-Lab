# 💻 Windows Enterprise Workstation Deployment

> Simulated Week 1 Desktop Support scenario:
> configure the first standardized Windows 11 Enterprise image
> for a 20-laptop corporate rollout.

![](https://img.shields.io/badge/OS-Windows%2011%20Enterprise-blue)
![](https://img.shields.io/badge/Role-Desktop%20Support%20Technician-lightgrey)
![](https://img.shields.io/badge/Platform-VMware%20Workstation-orange)
![](https://img.shields.io/badge/Series-Part%201%20of%208-brightgreen)

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
|  | Windows Firewall · CMD · Event Viewer · Performance Monitor |

---

## Tasks Completed

### 1. 🖥️ Windows 11 Installation & Configuration
- Clean install in VMware Workstation
- Configured computer name, region, time zone, and initial settings

### 2. 👤 Local User & Group Management
- Created Administrator and Standard User accounts
- Verified group membership and access permissions

### 3. 🛡️ Windows Security Configuration
- Verified Windows Defender real-time protection
- Applied all pending Windows Updates

### 4. 🔐 BitLocker Drive Encryption
- Enabled BitLocker on the OS drive
- Recovery key saved and documented securely

### 5. 🔥 Windows Firewall Configuration
- Reviewed Domain / Private / Public firewall profiles
- Created a custom inbound rule

### 6. 🌐 Networking Configuration
- Configured static IP addressing
- Verified connectivity: `ipconfig /all` · `ping` · `nslookup`

### 7. ⌨️ Command Line Administration
```cmd
systeminfo          → hardware and OS details
tasklist            → running processes
netstat -an         → active connections and listening ports
sfc /scannow        → system file integrity check
```

### 8. 📋 Event Viewer
- Investigated System and Application logs
- Identified and documented a sample warning / error event

### 9. 📊 Performance Monitoring
- Tracked CPU, RAM, and Disk usage via Resource Monitor
- Created a Performance Monitor data collector set

---

## Key Commands Used

```cmd
:: System info
systeminfo
hostname
winver

:: Network diagnostics
ipconfig /all
ping 8.8.8.8 -t
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
Get-BitLockerVolume          (PowerShell)
netsh advfirewall show all
```

---

## Skills Demonstrated

`Windows 11 Deployment` `Local Account Management`
`Endpoint Security` `BitLocker Encryption`
`Firewall Configuration` `TCP/IP Networking`
`CMD Administration` `Event Log Analysis`
`Performance Monitoring` `System Troubleshooting`


---




---

## Author

**Mohammad Salem Hassani**
IT Support Specialist
