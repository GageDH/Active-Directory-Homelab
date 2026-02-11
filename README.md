# Active-Directory-Homelab

## Overview
A Window Active Directory environment created with Oracle VirtualBox. This lab simulates real-world help desk and junior system administrator tasks.

## Environment Configuration
- Windows Server 2022 (DC01)
- Windows 11 Pro (Client01)
- Domain: lab.local
- Internal Network configuration
- DNS hosten on a Domain Controller

## Active Directory Implementation

### Organizational Structure
- Created Organizational Unit: Lab_Users
- Managed domain-based object placement

### User Lifecycle Management
- Enforced password change at first logon
- Simulated account lockout scenarios
- Configured domain account policy
- Unlocked and reset user accounts

## Group Policy Configuration
Configured Account Lockout Policy via Default Domain Policy:
- Lockout threshold 5 invalid attempts
- Lockout duration: 15 minutes
- Resent counter: 15 minutes

## Skills Demonstrated
- Active Directory Users and Computers (ADUC)
- Group Policy Management
- Domain join & recovery workflow
- Authentication troubheshooting

## Screenshots

### ADUC Console
![ADUC]("Screenshots/ADUC-Console 01.png")

## Future Expansion
- Security groups and NTFS permissions
- File share management
- Drive mapping via GPO
- PowerShell Automation
- Domain trust lifecycle management


