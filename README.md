# Hyper-V Active Directory Lab

## Introduction

This project documents the enterprise-style Hyper-V lab environment I built to strengthen my Windows Server and Active Directory administration skills.

The lab was designed to simulate a real-world enterprise environment and includes multiple domain controllers, Active Directory Domain Services (AD DS), DNS, Organizational Units (OUs), Security Groups, FSMO Role Management, Active Directory Replication, and domain-joined client machines.

The objective of this lab was to gain hands-on experience with Windows Server administration, Active Directory infrastructure management, and troubleshooting in a controlled virtual environment.

## Lab Architecture Diagram

```text
                 +------------------+
                 |      DC01        |
                 | Primary Domain   |
                 | Controller       |
                 +--------+---------+
                          |
            Active Directory / DNS
                          |
                 +--------+---------+
                 |      BDC01       |
                 | Additional DC    |
                 | Replication      |
                 +--------+---------+
                          |
          --------------------------------
          |                              |
 +--------+--------+            +--------+--------+
 |    CLIENT01     |            |    CLIENT02     |
 | Domain Joined   |            | Domain Joined   |
 +-----------------+            +-----------------+
```

---

# Lab Environment

## Hypervisor

* Microsoft Hyper-V

## Operating Systems

### Servers

* Windows Server 2019

### Clients

* Windows 10

---

# Virtual Machines

## DC01 (Primary Domain Controller)

Responsibilities:

* Active Directory Domain Services (AD DS)
* DNS Server
* Authentication Services
* User Management
* Group Management
* Group Policy Management

---

## BDC01 (Additional Domain Controller)

Responsibilities:

* Additional Domain Controller
* Active Directory Replication
* High Availability
* Backup Authentication Services

Key Activities Performed:

* Promoted server to Additional Domain Controller
* Configured Active Directory replication
* Verified replication health
* Tested replication between domain controllers

---

## CLIENT01

Responsibilities:

* Domain-Joined Workstation
* User Login Testing
* Active Directory Validation
* Group Policy Testing

---

## CLIENT02

Responsibilities:

* Domain-Joined Workstation
* User Access Testing
* Permission Validation
* Group Policy Verification

---

# Active Directory Configuration

## Domain Deployment

Configured Active Directory Domain Services and created the lab domain.

### Components Configured

* Forest
* Domain
* DNS Integration
* Domain Controllers

---

## Organizational Unit (OU) Structure

Created Organizational Units for administrative management.

Examples:

* Users
* Computers
* Groups
* IT
* HR
* Administration

---

## User Management

Performed:

* User Creation
* Password Management
* Account Unlock Operations
* User Administration
* Account Verification

---

## Group Management

Created and managed security groups for access control and administration.

Configured:

* Security Groups
* Group Memberships
* Administrative Groups

---

# DNS Configuration

Configured and validated:

* Forward Lookup Zones
* DNS Records
* Name Resolution
* Client DNS Configuration

Performed testing to verify successful communication between all systems.

---

# Active Directory Replication

Implemented Active Directory replication between:

* DC01
* BDC01

Validation Tasks:

* Replication Verification
* Replication Monitoring
* Synchronization Testing

Benefits:

* High Availability
* Redundancy
* Improved Reliability

---

# FSMO Role Management

Performed FSMO role administration and testing.

FSMO Roles:

* Schema Master
* Domain Naming Master
* RID Master
* PDC Emulator
* Infrastructure Master

Activities:

* Identified FSMO Role Holders
* Verified FSMO Role Ownership
* Performed FSMO Role Transfer Testing
* Validated Successful Role Changes

---

# Client Domain Integration

Successfully joined:

* CLIENT01
* CLIENT02

to the Active Directory domain.

Validation Performed:

* Domain Authentication
* DNS Resolution
* User Logon Testing
* Group Policy Processing

---

# Group Policy Management

Configured and tested:

* Password Policies
* Security Policies
* User Configuration Policies
* Computer Configuration Policies

Verified policy application on domain-joined clients.

---

# Skills Demonstrated

* Hyper-V Administration
* Windows Server 2019
* Active Directory Domain Services
* DNS Administration
* Domain Controller Deployment
* Active Directory Replication
* FSMO Role Management
* Organizational Unit Management
* User Administration
* Group Management
* Group Policy Administration
* Client Domain Integration
* Windows Troubleshooting

---

# Challenges Faced

### Active Directory Replication

Learned how replication works between multiple domain controllers and verified synchronization status.

### FSMO Role Transfer

Performed role transfer testing and validated ownership changes between domain controllers.

### DNS Troubleshooting

Resolved name resolution issues during domain join and replication testing.

### Client Domain Join Issues

Verified DNS configuration and domain connectivity before successfully joining client systems to the domain.

---

# Lessons Learned

This project significantly improved my understanding of:

* Active Directory Infrastructure
* Domain Controller Deployment
* Multi-Domain Controller Environments
* Active Directory Replication
* FSMO Roles
* DNS Administration
* Group Policy Management
* Enterprise Windows Server Administration
* Troubleshooting Active Directory Environments

---

# Screenshots

Screenshots to be added:

* Hyper-V Virtual Machines
* DC01 Configuration
* BDC01 Configuration
* Active Directory Users and Computers
* DNS Manager
* Active Directory Sites and Services
* FSMO Role Verification
* Replication Status
* CLIENT01 Domain Join
* CLIENT02 Domain Join
* Group Policy Management
