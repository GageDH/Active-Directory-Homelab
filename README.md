Active Directory Homelab – User & Group Policy Management
Overview

A Windows Active Directory environment built using Oracle VirtualBox to simulate real-world Help Desk and junior system administrator tasks. This lab focuses on user lifecycle management, password policy enforcement, account lockouts, incorporating file share management, role-based access control (RBAC), drive mapping, DHCP network confirguration, and Group Policy configuration and troubleshooting.

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

An image of the basic Account lockout policy.

<img width="1919" height="1079" alt="LockoutLog" src="https://github.com/user-attachments/assets/ee45f6f8-3050-4be8-9407-66fc0b63a479" />



<img width="1919" height="1079" alt="UserLockout2" src="https://github.com/user-attachments/assets/5e59b964-f6d1-41e3-becd-98182ea38b15" />



Log details showing a user that was locked out due to entering too many incorrect passwords.



<img width="1919" height="1079" alt="Disabled User" src="https://github.com/user-attachments/assets/cca9fceb-d67b-40c3-a5fa-7278deb029ba" />



<img width="1919" height="1079" alt="User Disabled" src="https://github.com/user-attachments/assets/69216f41-4d07-4cd8-87c5-b31563345e41" />



Creation of a disabled user OU for isolating and archiving purposes and disabling the user.



### Password Policy and Password Reset

<img width="1919" height="1079" alt="Password Policy" src="https://github.com/user-attachments/assets/b1fb685e-c8d0-458e-97a8-378b5a17c055" />



An image of the server's password policy currently in effect.



<img width="1919" height="1079" alt="Unlocking" src="https://github.com/user-attachments/assets/ff749729-4bcd-48dd-9356-935fd9b959b7" />



<img width="1919" height="1079" alt="Password Change" src="https://github.com/user-attachments/assets/fd2e46ab-c556-4e45-b967-c4a799bf41a6" />



<img width="1919" height="1079" alt="User Logged In" src="https://github.com/user-attachments/assets/05e810c5-880a-482d-b9a5-b912fa45e16b" />



Images showing how the account locked out due to too many incorrect password entries is unlocked and password is reset followed by the user sucessfully logging in afterwards.



### GPO Creation and Simulation

<img width="1919" height="1079" alt="GPO Creation" src="https://github.com/user-attachments/assets/fd8b77e2-8302-4935-9449-237a6efccb4e" />



<img width="1919" height="1079" alt="GPO Details" src="https://github.com/user-attachments/assets/9f3b492e-8fa0-41cf-930f-9921a3e61e9c" />



Images showing the creation of the GPO in the server.

<img width="1919" height="1079" alt="GPO Console" src="https://github.com/user-attachments/assets/8c512c02-d1cd-4a03-be7c-0149d8ca934c" />



<img width="1919" height="1079" alt="GPO Working" src="https://github.com/user-attachments/assets/6593bcd6-72ea-4338-a26b-69483872995c" />

Images showing the GPO working within the server.

## File Share Configuration

Created shared directory: C:\CompanyData and departmental folders (IT, HR). Configured share permissions (Authenticated Users → Full Control) and NTFS permissions based on department. Implemented role-based access using security groups (IT_Share_Access, HR_Share_Access). Assigned permissions to groups instead of individual users.

<img width="1914" height="1079" alt="Screenshot_19" src="https://github.com/user-attachments/assets/77e10d9e-d79e-4b64-a758-487cc1b02187" />

<img width="1919" height="1058" alt="Screenshot_20" src="https://github.com/user-attachments/assets/60e609d1-5f04-4e73-a987-09ab3650f9a3" />

Images of created shared directory along with the departmental folders and file permissions.

<img width="1920" height="1062" alt="Screenshot_21" src="https://github.com/user-attachments/assets/833f70f4-5759-40d7-9592-b20378d1a55b" />

<img width="1919" height="1063" alt="Screenshot_22" src="https://github.com/user-attachments/assets/634e708c-2ead-4a34-8f22-b3559d0ad5e1" />

<img width="1917" height="1059" alt="Screenshot_23" src="https://github.com/user-attachments/assets/82a53fd7-f973-48b4-896a-378c8bd39bb5" />

<img width="1920" height="1065" alt="Screenshot_24" src="https://github.com/user-attachments/assets/12d7429e-3dd7-49e0-bc5b-2f411876e63b" />

Creation of the file security groups and assigning them accordingly.

<img width="1919" height="1079" alt="Screenshot_25" src="https://github.com/user-attachments/assets/b5ca6b5b-e1ba-43b9-b1b9-32c6f49338f3" />

<img width="1919" height="1079" alt="Screenshot_26" src="https://github.com/user-attachments/assets/e602985a-6b61-4ff9-899e-856f3e204a4a" />

Demonstration of an IT user attempting to access a file in the HR Folder and an HR user attempting to access the IT folder.

## Drive Mapping via GPO

Configured drive mapping using Group Policy Preferences. Mapped departmental drives: IT → I: and HR → H:. Used Item-Level Targeting based on security group membership. Verified drive mapping from domain-joined client

<img width="1916" height="1079" alt="Screenshot_27" src="https://github.com/user-attachments/assets/5b2b62d5-9cb8-4e6a-8569-24762bacab94" />

<img width="1919" height="1079" alt="Screenshot_28" src="https://github.com/user-attachments/assets/95981ae3-c9d3-4a7f-bdf6-d5c0dc54e2eb" />

<img width="1919" height="1079" alt="Screenshot_29" src="https://github.com/user-attachments/assets/66701599-7cc4-4c96-a870-eb5d95b620c8" />

Creation and demonstration of an IT user accessing their departmental drive.

## DHCP Configuration

Installed DHCP Server role on Domain Controller. Created scope: 10.0.0.100 – 10.0.0.200. Configured DNS settings to point to Domain Controller. Verified client lease assignment using ipconfig /all. Tested end-to-end network configuration from client machine

<img width="1918" height="1063" alt="Screenshot_14" src="https://github.com/user-attachments/assets/feba71cd-f557-4d62-af00-e6a11a09d01a" />

<img width="1918" height="1059" alt="Screenshot_15" src="https://github.com/user-attachments/assets/e9d01359-17d7-4172-b1e4-eab3cfb1461e" />

<img width="1918" height="1003" alt="Screenshot_16" src="https://github.com/user-attachments/assets/6799c6ad-2e31-490f-a428-cf9229b0937e" />

Creation of the DHCP Server with the scope 10.0.0.100 - 10.0.0.200.

<img width="1919" height="1064" alt="Screenshot_17" src="https://github.com/user-attachments/assets/af0af0d9-ac1d-488c-860b-b272788b9004" />

<img width="1920" height="1060" alt="Screenshot_18" src="https://github.com/user-attachments/assets/3d55e7dc-5e86-4250-9436-109ee9492840" />

Test of the end-to-end network configuration on the client machine.
