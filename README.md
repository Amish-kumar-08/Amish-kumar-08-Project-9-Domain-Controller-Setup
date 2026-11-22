# **Project 9: Domain Controller Setup**

## **Overview**

Configured a Windows Server as an Active Directory Domain Controller to practice centralized authentication and user management.

## **Objectives**

- Install Active Directory Domain Services (AD DS).
- Configure a new Active Directory forest.
- Promote Windows Server to Domain Controller.
- Install and configure DNS.
- Create and manage domain users.
- Verify domain user accounts using PowerShell.

## **Environment**

- **Operating System:** Windows Server 2022 Datacenter
- **Server IP:** `10.5.3.141`
- **Server Name:** `AZ-LKM-JAV-01`
- **Domain Name:** `amish.local`
- **DNS:** Installed with AD DS

## **Implementation**

1. Installed Active Directory Domain Services (AD DS).
2. Configured a new forest named `amish.local`.
3. Promoted Windows Server to Domain Controller.
4. Installed and configured DNS.
5. Created two domain users:
   - `amish.admin`
   - `amish.user`
6. Verified both accounts using PowerShell `Get-ADUser`.
7. Confirmed that both domain user accounts are enabled.

## **Technologies Used**

- Windows Server 2022
- Active Directory Domain Services (AD DS)
- DNS
- PowerShell
- Oracle VirtualBox

## **Deliverables**

- AD DS installation screenshot
- Domain Controller configuration screenshot
- Active Directory Users and Computers screenshot showing both domain users
- PowerShell user verification screenshot
- Domain authentication testing screenshot (pending)

## **PowerShell Verification**

Command used to verify both domain user accounts:

```powershell
Get-ADUser -Filter * |
Where-Object {$_.SamAccountName -in @("amish.admin","amish.user")} |
Select-Object Name, SamAccountName, Enabled
```

**Verification Result:**

Both `amish.admin` and `amish.user` were successfully created and verified with their Enabled status set to `True`.

## **Outcome**

Successfully configured an Active Directory Domain Controller, established a new forest named `amish.local`, configured DNS, and created two enabled domain user accounts for centralized authentication and user management practice.
