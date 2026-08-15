# Active-Directory-Lab


## Overview

This project documents a hands-on Windows Server and Active Directory home lab built using VMware Workstation. The lab simulates a small corporate environment where I performed common Help Desk and IT administration tasks, including managing users, security groups, passwords, account status, DNS, Group Policy, and domain-joined computers.

## Lab Objectives

The objectives of this lab were to:

* [x] Deploy a Windows Server virtual machine
* [x] Configure a static IP address
* [x] Install Active Directory Domain Services (AD DS)
* [x] Configure a new Active Directory domain
* [x] Configure DNS services
* [x] Create Organizational Units (OUs)
* [x] Create and manage user accounts
* [x] Create security groups and assign users
* [x] Perform password resets
* [x] Disable and enable user accounts
* [x] Configure an account lockout policy
* [x] Unlock a locked user account
* [x] Deploy a Windows 11 client VM
* [x] Configure client DNS
* [x] Join a Windows client to the domain
* [x] Verify domain user authentication

## Lab Environment

| Component              | Configuration                    |
| ---------------------- | -------------------------------- |
| Hypervisor             | VMware Workstation               |
| Domain Controller      | Windows Server                   |
| Client Machine         | Windows 11 Enterprise Evaluation |
| Domain                 | `corp.lab`                       |
| Domain Controller Name | `DC01`                           |
| Client Name            | `CLIENT01`                       |
| Domain Controller IP   | `192.168.83.129`                 |
| Client IP              | `192.168.83.130`                 |
| Subnet Mask            | `255.255.255.0`                  |
| Default Gateway        | `192.168.83.2`                   |

## Active Directory Structure

The following Organizational Unit structure was created:

```text
corp.lab
├── Employees
│   ├── IT
│   ├── HR
│   └── Finance
└── Groups
```

## User Accounts

Six fictional employee accounts were created and organized by department.

### IT Department

* John Smith (`jsmith`)
* Sarah Johnson (`sjohnson`)

### HR Department

* Michael Brown (`mbrown`)
* Emily Davis (`edavis`)

### Finance Department

* David Wilson (`dwilson`)
* Lisa Martinez (`lmartinez`)

## Security Groups

The following Global Security Groups were created:

* `IT-Support`
* `HR-Staff`
* `Finance-Staff`

Users were assigned to their corresponding department security groups.

## Help Desk Tasks Performed

### Password Reset

Simulated a Help Desk ticket where a user forgot their password. The user's password was reset through Active Directory Users and Computers, and the account was configured to require a password change at the next login.

### Account Disable and Enable

Simulated an employee taking extended leave. The user's Active Directory account was temporarily disabled and later re-enabled.

### Account Lockout and Unlock

Configured an Account Lockout Policy using Group Policy Management. A user account was locked after multiple failed login attempts and then unlocked through Active Directory Users and Computers.

### DNS Configuration and Troubleshooting

Configured the Windows 11 client to use the Domain Controller as its preferred DNS server. Initially, DNS requests failed because the Domain Controller VM was powered off. After starting the server, DNS resolution for `corp.lab` was successfully verified.

### Domain Join

Configured the Windows 11 client to use the Domain Controller for DNS and successfully joined `CLIENT01` to the `corp.lab` domain.

### Domain User Authentication

Successfully authenticated to `CLIENT01` using an Active Directory domain user account and verified the session using:

```text
whoami
hostname
```

## Screenshots

### Server Renamed

![Server Renamed](screenshots/01-server-renamed.png)

### Static IP Configuration

![Static IP Configuration](screenshots/02-static-ip-configuration.png)

### AD DS Installed

![AD DS Installed](screenshots/03-adds-installed.png)

### Domain Controller

![Domain Controller](screenshots/04-domain-controller.png)

### Organizational Units

![Organizational Units](screenshots/05-organizational-units.png)

### Active Directory Users

![Active Directory Users](screenshots/06-active-directory-users.png)

### Security Group Membership

![Security Group Membership](screenshots/07-security-group-members.png)

### Password Reset

![Password Reset](screenshots/08-password-reset.png)

### DNS Resolution

![DNS Resolution](screenshots/09-dns-resolution.png)

### Client Joined to Domain

![Client Joined to Domain](screenshots/10-client-domain-joined.png)

### Domain User Login

![Domain User Login](screenshots/11-domain-user-login.png)

### Account Lockout Policy

![Account Lockout Policy](screenshots/12-account-lockout-policy.png)

### Account Unlock

![Account Unlock](screenshots/13-account-unlock.png)

## Skills Demonstrated

* Windows Server Administration
* Active Directory Administration
* Active Directory Domain Services (AD DS)
* DNS Configuration and Troubleshooting
* User Account Management
* Security Group Management
* Password Reset and Account Recovery
* Account Enable/Disable Management
* Group Policy Management
* Account Lockout Troubleshooting
* Windows Domain Joining
* Domain User Authentication
* Basic Network Troubleshooting
* VMware Virtualization

## Key Takeaways

This lab provided hands-on experience managing a Windows Server Active Directory environment and performing common Help Desk administration tasks. I gained practical experience configuring a Domain Controller, managing users and groups, troubleshooting DNS connectivity, applying account security policies, joining Windows clients to a domain, and authenticating users within a domain environment.
