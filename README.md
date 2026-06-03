# PowerShell System Administration Scripts

## Introduction

This repository contains PowerShell scripts that I use and develop while learning and performing Windows Server administration tasks.

As a Junior System Administrator, I work with Active Directory, Windows Server, file permissions, user management, and system administration tasks. The purpose of this repository is to document PowerShell commands and scripts that help automate repetitive administrative work, improve efficiency, and strengthen my PowerShell skills.

The scripts included in this repository focus on real-world administration scenarios such as user management, group management, reporting, system monitoring, and file server administration.

---

## Objectives

The main objectives of this repository are:

* Learn PowerShell scripting for Windows administration
* Automate repetitive administrative tasks
* Improve operational efficiency
* Reduce manual errors
* Build reusable administration tools
* Document PowerShell learning progress

---

## Environment

### Technologies Used

* Windows Server 2019
* Active Directory Domain Services (AD DS)
* PowerShell
* DNS
* DHCP
* NTFS Permissions
* File Services

---

## Script Categories

### Active Directory User Management

Scripts related to:

* User creation
* User account management
* Password resets
* Account unlock operations
* User information reporting

### Active Directory Group Management

Scripts related to:

* Security group reporting
* Group membership verification
* User-to-group mapping
* Permission-related group management

### Reporting and Auditing

Scripts used for:

* User reports
* Computer reports
* Group reports
* Service status reports
* Administrative auditing

### Windows Server Administration

Scripts related to:

* Service management
* Server information gathering
* Health monitoring
* Event log review
* System administration tasks

### File Server Administration

Scripts used for:

* NTFS permission verification
* Folder permission auditing
* Shared folder administration
* Access management

---

## Sample Scripts

### List All Active Directory Users

```powershell
Get-ADUser -Filter * | Select Name, SamAccountName
```

Purpose:
Retrieve all Active Directory user accounts and display basic user information.

---

### List All Active Directory Groups

```powershell
Get-ADGroup -Filter *
```

Purpose:
Display all Active Directory groups available in the domain.

---

### List Domain Computers

```powershell
Get-ADComputer -Filter *
```

Purpose:
Retrieve all computer objects joined to the domain.

---

### View Running Services

```powershell
Get-Service
```

Purpose:
Display service information and verify service status.

---

## Challenges and Learning Experience

While building these scripts, I gained practical experience in:

* Understanding PowerShell syntax
* Working with Active Directory cmdlets
* Automating administration tasks
* Generating reports
* Troubleshooting script errors
* Improving efficiency through automation

---

## Future Enhancements

Planned additions include:

* Bulk user creation scripts
* Password expiration reports
* Disabled user reports
* Group membership reports
* NTFS permission reporting
* DNS administration scripts
* DHCP administration scripts
* Server health monitoring scripts

---

## Lessons Learned

This repository has helped strengthen my understanding of:

* PowerShell fundamentals
* Windows Server administration
* Active Directory management
* Automation concepts
* Troubleshooting techniques
* System administration best practices

---

## Disclaimer

The scripts in this repository are created for learning, lab, and administrative automation purposes. Any production use should be tested and validated before deployment.
