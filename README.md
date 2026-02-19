Active Directory Homelab – User & Group Policy Management
Overview

A Windows Active Directory environment built using Oracle VirtualBox to simulate real-world Help Desk and junior system administrator tasks. This lab focuses on user lifecycle management, password policy enforcement, account lockouts, and Group Policy configuration and troubleshooting.

## Environment Configuration
Windows Server 2022 (DC01 – Domain Controller)
Windows 11 Pro (Client01 – Domain-Joined Workstation)
Domain: lab.local
Internal network configuration
DNS hosted on the Domain Controller

### Active Directory Implementation

## Organizational Structure
Created Organizational Units (OUs) for Users and Workstations
Managed domain-based object placement for proper Group Policy scope
Validated OU-based policy processing (User vs Computer configuration)

## User Lifecycle Management
Created and managed domain user accounts
Created and assigned security groups
Added and removed users from groups and verified membership
Enforced password change at first logon
Configured domain password and account lockout policies
Simulated account lockout scenarios
Unlocked and reset user accounts
Disabled and re-enabled user accounts
Verified authentication behavior from domain-joined client

## Group Policy Configuration
Account Lockout Policy (Default Domain Policy)
Lockout threshold: 5 invalid attempts
Lockout duration: 15 minutes
Reset counter after: 15 minutes

## Workstation Baseline GPO
Created and linked a workstation baseline Group Policy Object (GPO)
Configured both Computer and User policy settings including:
Machine inactivity timeout
Control Panel access restriction
Desktop configuration settings
Linked GPOs to appropriate OUs
Identified and corrected OU scoping issue affecting User policy processing
Verified policy enforcement using gpupdate and gpresult

## Troubleshooting & Validation
Diagnosed and resolved GPO scope misconfiguration (User vs Computer OU placement)
Verified DNS configuration and domain connectivity
Confirmed secure channel status between client and domain controller
Tested domain authentication and policy processing from client machine

## Skills Demonstrated
Active Directory Users and Computers (ADUC)
Group Policy Management Console (GPMC)
OU scoping and policy processing
Account lockout and password policy enforcement
Domain join and authentication troubleshooting
Basic Windows Server administration

## Screenshots

### ADUC Console
![ADUC](Screenshots/ADUC-Console%2001.png)

## Future Expansion
- Security groups and NTFS permissions
- File share management
- Drive mapping via GPO
- PowerShell Automation
- Domain trust lifecycle management


