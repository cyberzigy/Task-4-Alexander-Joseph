# Project 4 - Audited Systems

## A Framework for Blue Team Defense

This project is a local system security audit performed on a Windows 11 Pro workstation.

The audit followed a structured vulnerability checklist covering:

* Password and account security
* Software and patch management
* Firewall configuration
* Disk encryption
* Administrative privileges
* Outdated and unsupported software
* System hardening and verification

## Findings

The audit identified:

1. An unencrypted Windows operating-system drive
2. An outdated Java 8 Update 192 installation
3. End-of-life Microsoft Silverlight software

The system was subsequently hardened by enabling BitLocker encryption and removing obsolete software.

## Security Checks

The following PowerShell tools were used during the audit:

```powershell
Get-NetFirewallProfile
Get-BitLockerVolume
Get-LocalGroupMember -Group "Administrators"
Get-ItemProperty HKLM:\Software\Microsoft\Windows\CurrentVersion\Uninstall\*
Get-HotFix
```

## Evidence

The `evidence` directory contains screenshots documenting the initial audit, identified findings, remediation actions, and final hardened state.

## Skills Demonstrated

* System security auditing
* Vulnerability identification
* Risk assessment
* PowerShell security checks
* Patch and software management
* Disk encryption
* Security remediation
* Verification and documentation

**Project:** Cybersecurity Project 4
**Type:** Blue Team / Defensive Security Audit
