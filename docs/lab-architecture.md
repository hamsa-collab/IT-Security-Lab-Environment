Mini Enterprise IT & Security Lab
Project Overview
This project is a small virtual enterprise environment for practising Windows Server administration, Active Directory, PowerShell automation, and basic security validation.

Host System
Host OS: Windows 11
Virtualization platform: Oracle VirtualBox 7.2.12
Host RAM: 8 GB
CPU: Intel Core i5-10210U
Planned Architecture
Virtual Machine 1 — Windows Server 2025
Operating system: Windows Server 2025 Evaluation
Planned roles: Active Directory Domain Services (AD DS) and DNS
Administration: PowerShell
Monitoring: Windows Event Viewer and security logs
Network and Security
Use a dedicated lab network where practical.
Avoid exposing lab services to the public internet.
Use strong lab-only passwords.
Record configuration changes and test results.
Project Goals
Build a functional Windows Server lab.
Practise basic server administration.
Automate selected administration and security checks with PowerShell.
Apply basic security hardening.
Document findings, screenshots, and lessons learned.


## 1. Host Machine Specifications

| Component | Specification |
|---|---|
| Laptop | HP 15s-du1xxx |
| System SKU | 1V842PA#UUF |
| Operating System | Windows 11 |
| Processor | Intel Core i5-10210U @ 1.60 GHz |
| CPU Cores | 4 cores |
| Logical Processors | 8 |
| Installed RAM | 8 GB |
| Memory Speed | 2667 MT/s |
| Memory Slots Used | 2 of 2 |
| Available Storage (C:) | 251 GB |
| Virtualization Software | Oracle VirtualBox 7.2.12 r1743 |

### Hardware Considerations

The virtual machine will use conservative resource allocations to ensure that the host operating system remains responsive.

Only one virtual machine will initially be operated at a time.

---

## 2. Virtual Machine General Settings

| Setting | Configuration |
|---|---|
| VM Name | Windows Server 2025 |
| Type | Microsoft Windows |
| Version | Windows Server 2025 (64-bit), if available |
| Installation Media | Windows Server 2025 Evaluation ISO |
| Unattended Installation | Disabled (manual installation) |

---

## 3. System Configuration

### 3.1 Motherboard

| Setting | Configuration |
|---|---|
| Base Memory | 4096 MB (4 GB) |
| Boot Order | Optical, Hard Disk |
| Chipset | PIIX3 |
| Pointing Device | USB Tablet |
| Enable EFI | Enabled |

**Purpose:** Allocate sufficient memory for Windows Server while reserving resources for the host operating system.

### 3.2 Processor

| Setting | Configuration |
|---|---|
| Processor Allocation | 2 CPUs |
| Execution Cap | 100% |
| Enable PAE/NX | Enabled |

**Purpose:** Provide sufficient processing resources for basic server administration and Active Directory exercises without allocating all available CPU cores.

### 3.3 Acceleration

| Setting | Configuration |
|---|---|
| Paravirtualization Interface | Default |
| Hardware Virtualization | VT-x/AMD-V enabled |
| Nested Paging | Enabled |

**Note:** Some settings may be automatically managed by VirtualBox or unavailable depending on the host configuration.

---

## 4. Display Configuration

| Setting | Configuration |
|---|---|
| Video Memory | 128 MB |
| Graphics Controller | VBoxSVGA |
| Enable 3D Acceleration | Disabled |

**Purpose:** Provide adequate display resources for the Windows Server graphical interface.

---

## 5. Storage Configuration

| Setting | Configuration |
|---|---|
| Storage Controller | SATA |
| Virtual Hard Disk Format | VDI |
| Virtual Disk Capacity | 60–80 GB |
| Disk Allocation | Dynamically Allocated |
| Optical Drive | Windows Server 2025 Evaluation ISO |

**Purpose:** Provide sufficient storage for the operating system, server roles, administrative tools and project exercises.

**Important:** Verify that the virtual hard disk is attached before starting the installation. Do not delete or detach existing virtual disks.

---

## 6. Network Configuration

### Adapter 1

| Setting | Configuration |
|---|---|
| Enable Network Adapter | Enabled |
| Attached To | NAT |
| Cable Connected | Enabled |

**Purpose:** NAT provides internet connectivity for initial setup and Windows updates.

### Future Network Configuration

An isolated or host-only network will be considered for security testing and Active Directory exercises.

The objective is to prevent test services from being unnecessarily exposed to the public internet.

---

## 7. Planned Server Roles and Activities

The Windows Server virtual machine will be used to practise:

1. Windows Server installation and initial configuration.
2. Active Directory Domain Services (AD DS).
3. Domain user and group management.
4. DNS configuration.
5. User access and privilege administration.
6. PowerShell administration and automation.
7. Windows Event Viewer and security log analysis.
8. Basic Windows Server security hardening.
9. Security configuration validation.

A second Windows client virtual machine may be introduced later if the laptop's available resources permit.

---

## 8. Configuration Summary

| Component | Target Configuration |
|---|---|
| RAM | 4096 MB |
| CPU | 2 cores |
| Virtual Disk | 60–80 GB |
| Video Memory | 128 MB |
| Graphics Controller | VBoxSVGA |
| EFI | Enabled |
| Network | NAT |
| Installation Media | Windows Server 2025 ISO |

---

## 9. Verification Checklist

The following items must be verified during VM configuration.

- [ ] Virtual machine created.
- [ ] Windows Server 2025 ISO attached.
- [ ] RAM allocation verified.
- [ ] Processor allocation verified.
- [ ] EFI configuration verified.
- [ ] Hardware acceleration verified.
- [ ] Virtual hard disk attached.
- [ ] Virtual hard disk capacity verified.
- [ ] Network adapter configured.
- [ ] Windows Server installation completed.
- [ ] Successful first boot confirmed.

---

## 10. Evidence Collection

The following screenshots will be collected as project evidence:

| Evidence | Description |
|---|---|
| Screenshot 1 | VirtualBox VM general settings |
| Screenshot 2 | Motherboard and RAM configuration |
| Screenshot 3 | Processor configuration |
| Screenshot 4 | Display configuration |
| Screenshot 5 | Storage configuration |
| Screenshot 6 | Network configuration |
| Screenshot 7 | Windows Server installation |
| Screenshot 8 | Successful Windows Server boot |

All screenshots will reflect the actual configuration and activities performed.

Sensitive information such as passwords and licence keys must not be included in published screenshots.

---

## 11. Project Progress

### Completed

- [x] Oracle VirtualBox installed.
- [x] VirtualBox version verified.
- [x] Windows Server 2025 Evaluation ISO downloaded.
- [x] GitHub repository created.
- [x] Lab architecture documentation committed.

### In Progress

- [ ] Virtual machine configuration.
- [ ] Windows Server installation.
- [ ] Initial server configuration.

### Upcoming Activities

- [ ] Configure Active Directory Domain Services.
- [ ] Configure DNS.
- [ ] Practise user and group administration.
- [ ] Develop PowerShell automation scripts.
- [ ] Apply basic security hardening.
- [ ] Review Windows security event logs.
- [ ] Document findings and publish project evidence.

---

**Project Objective:**

To develop practical IT infrastructure administration and cybersecurity skills through the deployment, configuration, administration and security validation of a simulated enterprise Windows Server environment.
