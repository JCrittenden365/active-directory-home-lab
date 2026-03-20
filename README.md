# Active-Directory-Home-Lab

## Overview
This project demontrates the setup and configuration of an Active Directory environment using a virtualized lab. The goal was to simulate a real-world corporate network and practice common IT Help Desk tasks.

## Technologies Used
- Windows Server 2022
- Windows 10 Client
- VirtualBox
- Active Directory Domain Services (AD DS)

---

## Lab Setup
 
### 1. Virtual Machine Setup
- Created a Domain Name Controller VM (DC01)
- Installed Windows Server
- Configured system resources (CPU, RAM, storage)

### 2. Network Configuration
- Assigned static IP address
- Configured DNS to point to the Domain Contoller

### 3. Active Directory Installation
- Installed AD DS role
- Promoted server to Domain Controller
- Created domain: 'home.local'

### 4. User Management
- Created test users
  - josh.admin
  - test.user
- Configured password policies

### 5. Client Machine Setup
- Installed Windows 10 VM
- Connected to same network
- Joined domain successfully

---

## Help Desk Scenarios Simulated
- Password Reset
- Account lock/unlock
- Domain login testing
- Network Troubleshooting

---

## Troubleshooting

### PXE Boot Issue
- Problem: VM booted into network (iPXE) instead of OS
- Solution: Corrected boot order in VirtualBox to prioritize hard disk

---

## What I Learned

- How Active Directory environments are structured
- Importance of DNS in domain environments
- User and permission management
- Real-world troubleshooting techniques

---

## Next Steps

- Implement Group Policy (GPO)
- Add shared folders and permissions
- Expand lab with additional client machines
