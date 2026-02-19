Active Directory Homelab – User & Group Policy Management
Overview

A Windows Active Directory environment built using Oracle VirtualBox to simulate real-world Help Desk and junior system administrator tasks. This lab focuses on user lifecycle management, password policy enforcement, account lockouts, and Group Policy configuration and troubleshooting.

## Environment Configuration
Windows Server 2022 (DC01 – Domain Controller)
Windows 11 Pro (Client01 – Domain-Joined Workstation)
Domain: lab.local
Internal network configuration
DNS hosted on the Domain Controller

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

### ADUC Console and Users
<img width="1919" height="1079" alt="LablocalOUS" src="https://github.com/user-attachments/assets/79e1d138-9305-4af8-8e04-d9ec45d77953" />

<img width="1919" height="1079" alt="Lablocalusers" src="https://github.com/user-attachments/assets/4573fd78-b293-4c74-9d06-d32e22df661d" />


## Future Expansion
- NTFS permissions
- File share management
- Drive mapping via GPO
- PowerShell Automation
- Domain trust lifecycle management


