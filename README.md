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

### Account Lockout Policy and Lockout Simulations
<img width="1919" height="1079" alt="Lockout Policy" src="https://github.com/user-attachments/assets/414c3956-e987-4da9-9545-f2ed990dbae9" />

<img width="1919" height="1079" alt="LockoutLog" src="https://github.com/user-attachments/assets/ee45f6f8-3050-4be8-9407-66fc0b63a479" />

<img width="1919" height="1079" alt="UserLockout2" src="https://github.com/user-attachments/assets/5e59b964-f6d1-41e3-becd-98182ea38b15" />

### Password Policy and Password Reset

<img width="1919" height="1079" alt="Password Policy" src="https://github.com/user-attachments/assets/b1fb685e-c8d0-458e-97a8-378b5a17c055" />

<img width="1919" height="1079" alt="Unlocking" src="https://github.com/user-attachments/assets/ff749729-4bcd-48dd-9356-935fd9b959b7" />

<img width="1919" height="1079" alt="Password Change" src="https://github.com/user-attachments/assets/fd2e46ab-c556-4e45-b967-c4a799bf41a6" />

<img width="1919" height="1079" alt="User Logged In" src="https://github.com/user-attachments/assets/05e810c5-880a-482d-b9a5-b912fa45e16b" />

### GPO Creation and Simulation

<img width="1919" height="1079" alt="GPO Creation" src="https://github.com/user-attachments/assets/fd8b77e2-8302-4935-9449-237a6efccb4e" />

<img width="1919" height="1079" alt="GPO Details" src="https://github.com/user-attachments/assets/9f3b492e-8fa0-41cf-930f-9921a3e61e9c" />

<img width="1919" height="1079" alt="GPO Console" src="https://github.com/user-attachments/assets/8c512c02-d1cd-4a03-be7c-0149d8ca934c" />

<img width="1919" height="1079" alt="GPO Working" src="https://github.com/user-attachments/assets/6593bcd6-72ea-4338-a26b-69483872995c" />


## Future Expansion
- NTFS permissions
- File share management
- Drive mapping via GPO
- PowerShell Automation
- Domain trust lifecycle management


