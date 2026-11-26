# 🖥️ Windows Server 2016 – Enterprise IT Infrastructure Lab

![Windows Server](https://img.shields.io/badge/Windows_Server-2016-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Active Directory](https://img.shields.io/badge/Active_Directory-AD_DS-0078D4?style=for-the-badge)
![VMware](https://img.shields.io/badge/VMware-Workstation-607078?style=for-the-badge&logo=vmware&logoColor=white)
![IT Support](https://img.shields.io/badge/IT_Support-28A745?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-In_Progress-orange?style=for-the-badge)

## 📖 About This Project

This repository documents my hands-on Windows Server 2016
laboratory studies, focusing on IT Support, System
Administration, and Enterprise IT Infrastructure.

The project simulates a corporate IT environment using
virtual machines, centralized user management, network
services, security policies, and resource management.

It includes theoretical knowledge, practical configuration
steps, technical documentation, screenshots, and
troubleshooting scenarios.

## 🖥️ Lab Environment

| Component | Technology |
|---|---|
| Virtualization | VMware Workstation |
| Server Operating System | Windows Server 2016 |
| Client Operating System | Windows 10 |
| Directory Services | Active Directory Domain Services |
| Network Services | DNS & DHCP |
| Policy Management | Group Policy |
| File Management | SMB & NTFS |
| Resource Management | FSRM |
| Printer Management | Print Server |

## 🏗️ Lab Architecture

```text
Virtual Lab Environment
│
├── Domain Controller
│   ├── Active Directory Domain Services
│   ├── DNS Server
│   └── Group Policy Management
│
├── File and Print Server
│   ├── SMB File Shares
│   ├── NTFS Permissions
│   ├── File Server Resource Manager
│   └── Print Services
│
├── DHCP Service
│   └── IP Address Management
│
└── Windows 10 Client
    ├── Domain Authentication
    ├── Network Drives
    ├── Group Policy
    └── Shared Resources
```

## 📚 Lab Modules

### 01 — Lab Environment

- Windows Server initial configuration
- Virtual laboratory environment
- Member server management

### 02 — Active Directory

- Domain and Domain Controller concepts
- Logical and physical structures of Active Directory
- Forest, Tree, Domain, OU and Sites
- Workgroup vs. Domain
- Active Directory Domain Services installation
- User and group management
- Organizational Unit configuration
- Domain Join
- Domain users vs. Local users
- User logon restrictions

### 03 — File Server

- IPv4 and DNS configuration
- Member server domain integration
- SMB file and folder sharing
- Accessing shared network resources
- Hidden shares and administrative shares
- Network drive configuration
- File Server installation and management

### 04 — Access and Permissions

- NTFS permissions
- Share permissions
- Effective permissions
- Group-based access management
- Permission inheritance

### 05 — File Server Resource Manager (FSRM)

- Quota management
- File screening management
- File type restrictions
- Storage resource management

### 06 — Group Policy (GPO)

- Group Policy creation and management
- User restrictions
- Centralized network drive mapping
- GPO inheritance and precedence
- Enforced policies
- Group Policy reporting
- Starter GPO
- Remote software deployment (MSI)
- Folder redirection
- Desktop wallpaper deployment
- Domain password policy configuration

### 07 — Print Server

- Print Server installation
- Centralized printer management
- Printer deployment through Group Policy
- Printer access permissions
- Print Server security configuration

### 08 — DHCP Server

- DHCP fundamentals
- DHCP role installation
- Scope configuration
- IP address ranges
- Exclusion ranges
- Automatic IP address assignment

### 09 — Troubleshooting

- Domain Join issues
- DNS configuration issues
- Network connectivity problems
- Group Policy processing errors
- Printer deployment issues

## 🎯 Learning Objectives

- Build and manage a virtual enterprise IT environment.
- Configure centralized user and computer management.
- Manage organizational units and security groups.
- Configure file sharing and access permissions.
- Implement centralized Group Policy configurations.
- Manage network services and shared resources.
- Develop practical IT troubleshooting skills.
- Improve technical documentation skills.

## 🔐 Security Considerations

- Role-based access management
- Principle of least privilege
- Group-based resource permissions
- Centralized security policies
- Secure file and printer access
- Password policy management

All configurations are performed in a controlled
laboratory environment for educational purposes.

## 📸 Screenshots & Documentation

Each lab module will include relevant configuration
steps, technical explanations, and screenshots
from the virtual laboratory environment.

Technical documentation is primarily written in Turkish.

## 📈 Project Status

🟡 In Progress

This repository is being developed and updated
as part of my ongoing IT Support and System
Administration learning journey.

## 💼 Career Focus

- IT Support
- IT Specialist
- System Administration
- Enterprise IT Infrastructure
- Network Services

---

Built through hands-on practice, continuous learning,
technical documentation, and problem-solving.
