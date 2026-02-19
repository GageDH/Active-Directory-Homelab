A Windows Active Directory environment created using Oracle VirtualBox. This lab simulates real-world Help Desk and junior system administrator tasks including user lifecycle management, password policy enforcement, and Group Policy configuration and troubleshooting.

Environment Configuration
Windows Server 2022 (DC01 – Domain Controller)
Windows 11 Pro (Client01 – Domain-Joined Workstation)
Domain: lab.local
Internal network configuration
DNS hosted on the Domain Controller

Active Directory Implementation

Organizational Structure
Created Organizational Units (OUs) for Users and Workstations
Managed domain-based object placement for proper Group Policy scope
Validated OU-based policy processing (User vs Computer configuration)

User Lifecycle Management
Created and managed domain user accounts
Added and removed users from security groups
Enforced password change at first logon
Configured domain password policy and account lockout policy
Simulated account lockout scenarios
Unlocked and reset user accounts
Disabled and re-enabled user accounts
Verified authentication behavior from domain-joined client

Group Policy Configuration
Configured Account Lockout Policy via Default Domain Policy:

Lockout threshold: 5 invalid attempts

Lockout duration: 15 minutes

Reset counter after: 15 minutes

Created and linked a workstation baseline Group Policy Object (GPO)
Configured both Computer and User policy settings including:

Machine inactivity timeout

Control Panel access restriction

Desktop configuration settings

Linked GPOs to appropriate OUs and corrected policy scoping issues
Verified policy enforcement using gpupdate and gpresult

Troubleshooting & Validation
Diagnosed and corrected OU scoping issue affecting User policy application
Verified DNS configuration and domain connectivity
Confirmed secure channel status between client and domain controller
Tested domain authentication and policy processing from client machine

Skills Demonstrated
Active Directory Users and Computers (ADUC)
Group Policy Management Console (GPMC)
User and Computer OU scoping
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


