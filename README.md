# NTFS Permissions Management and Access-Based Enumeration (ABE)

## Introduction

This project demonstrates how I implemented secure shared folder access management using Active Directory Security Groups, NTFS Permissions, and Access-Based Enumeration (ABE) in a Windows Server environment.

The objective was to ensure that users could only access and view folders relevant to their department or project. This approach improved security, reduced unauthorized access, simplified permission management, and provided a cleaner file-sharing experience for end users.

---
## Automation Areas

```text
PowerShell
│
├── Active Directory Administration
├── User Reporting
├── Group Reporting
├── Server Monitoring
├── File Server Management
└── Administrative Automation
```
## Key Skills Demonstrated

* Active Directory Administration
* Security Group Management
* NTFS Permission Management
* Access-Based Enumeration (ABE)
* Windows Server Administration
* PowerShell Administration
* Group-Based Access Control
* File Server Administration
* Permission Troubleshooting
* Access Management

---

## Group-Based Folder Access Management

To simplify permission management and improve security, I implemented a group-based access control model using Active Directory Security Groups.

### Security Groups Created

The following security groups were created:

* GG_TeklaStructure_RW
* GG_RevitStructure_RW
* GG_Algisa_Tekla_RW
* GG_KOL_ACS_RW

Naming convention:

* GG = Global Group
* Project/Department Name
* RW = Read/Write Access

### Permission Assignment Strategy

Instead of assigning NTFS permissions directly to individual users, permissions were assigned to Active Directory Security Groups.

Users were added to the appropriate security groups based on their project requirements.

This approach provided:

* Centralized permission management
* Easier user onboarding and offboarding
* Reduced administrative effort
* Improved security and scalability

### Folder Access Configuration

Each project folder was mapped to its corresponding security group.

| Project Folder | Security Group       |
| -------------- | -------------------- |
| TeklaStructure | GG_TeklaStructure_RW |
| RevitStructure | GG_RevitStructure_RW |
| Algisa_Tekla   | GG_Algisa_Tekla_RW   |
| KOL_ACS        | GG_KOL_ACS_RW        |

Users assigned to a specific security group could access only the folders related to their work.

### Access-Based Enumeration (ABE)

After configuring NTFS permissions, Access-Based Enumeration (ABE) was enabled on the shared folders.

With ABE enabled:

* Users can only see folders they have permission to access.
* Unauthorized folders remain hidden.
* Users see only project folders relevant to their role.

For example:

A user who is a member of GG_TeklaStructure_RW can access and view only the TeklaStructure folder.

The same user cannot view:

* RevitStructure
* Algisa_Tekla
* KOL_ACS

unless additional permissions are granted.

### Permission Optimization

To achieve the required access model:

* Inherited permissions were reviewed and adjusted.
* Unnecessary permissions were removed.
* Security group memberships were validated.
* Folder access was tested using user accounts.
* NTFS and Share permissions were verified.

### Results

After implementation:

* Users could access only project folders relevant to their work.
* Unauthorized folders remained hidden.
* Permission management became centralized through Active Directory groups.
* Administrative overhead was reduced.
* The file-sharing environment became more secure and organized.

---

## Environment

### Server Environment

* Windows Server 2019
* Active Directory Domain Services (AD DS)
* File Server Role
* Access-Based Enumeration (ABE)
* NTFS Permissions
* PowerShell

### Tools Used

* Active Directory Users and Computers (ADUC)
* Server Manager
* File and Storage Services
* PowerShell
* icacls

---

## PowerShell and Permission Automation

PowerShell and icacls were used to assist with permission verification, administration, and automation tasks.

Areas of automation included:

* Permission validation
* Security group verification
* Folder permission auditing
* Administrative reporting

---

## Challenges Faced

### Permission Inheritance Issues

Some folders inherited permissions from parent directories, resulting in unexpected access behavior.

This required reviewing inheritance settings and applying the correct permission structure.

### Folder Visibility Issues

Certain users could not see folders even after being added to the correct security group.

Troubleshooting involved validating:

* Group membership
* NTFS permissions
* Share permissions
* ABE configuration

### Permission Conflicts

Several scenarios required verification of effective permissions due to conflicts between Share Permissions and NTFS Permissions.

---

## Lessons Learned

This project strengthened my understanding of:

* Active Directory Security Groups
* NTFS Permissions
* Access-Based Enumeration (ABE)
* Windows File Server Administration
* Group-Based Access Control
* PowerShell Administration
* Permission Troubleshooting
* Enterprise Security Best Practices

---

## Screenshots

Screenshots of:

* Active Directory Security Groups
* NTFS Permission Configuration
* Shared Folder Settings
* Access-Based Enumeration Configuration
* Permission Validation Testing

will be added in future updates.
