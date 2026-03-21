# Active-Directory-Home-Lab

## Overview
This project demontrates the setup and configuration of an Active Directory environment using a virtualized lab. The goal was to simulate a real-world corporate network and practice common IT Help Desk and system administration tasks.

## Technologies Used
- Windows Server 2022
- Windows 10 Pro
- VirtualBox
- Active Directory Domain Services (AD DS)

---

## Lab Setup
 
### 1. Virtual Machine Setup
- Created a Domain Controller VM (DC01)
- Installed Windows Server 2022
- Allocated system resources (CPU, RAM, storage)

### 2. Network Configuration
- Assigned a static IP address
- Configured DNS to point to the Domain Contoller

### 3. Active Directory Installation
- Installed AD DS role
- Promoted server to Domain Controller
- Created domain: home.local

### 4. User Management
- Created test users
  - josh.admin
  - test.user
- Configured basic password policies

### 5. Client Machine Setup
- Installed Windows 10 Pro VM
- Connected client to the same virtual network
- Successfully joined the home.local domain
- Verified domain authentication using test.user

### 6. Group Policy Implementation
- Created Group Policy Object (GPO)
  - "Disable Command Prompt"
- Linked the GPO within the domain
- Applied the policy to a standard user account

---

## Results
- Successfully deployed a functional domain environment
- Verified domain user authentication on a client machine
- Confirmed DNS resolution between client and server
- Validated Group Policy enforcement:
  "The command prompt has been disabled by your administrator"

---

## Help Desk Scenarios Simulated
- Password Reset
- Account lock/unlock
- Domain login troubleshooting
- Network connectivity issues
- Group Policy enforcement testing

---

## Troubleshooting

### PXE Boot Issue
- Problem: VM booted into network (iPXE) instead of OS
- Solution: Corrected boot order in VirtualBox to prioritize the hard disk

---

### Domain Join Issue
- Problem: Unable to join domain
- Cause: Windows Home Edition does not support domain join
- Solution: Reinstalled Windows 10 Pro and successfully joined the domain

---

## What I Learned

- How enterprise environments use Microsoft Active Directory for centralized management
- The critical role of DNS in domain functionality
- User and access control within a domain
- How Group Policy enforces system-wide restrictions
- Real-world troubleshooting and problem-solving techniques

---

## Next Steps

- Implement additional Microsoft Group Policy configurations (Control Panel restrictions, password policies)
- Configure shared network drives and permissions
- Create Organizational Units (OUs) for structured management
- Expand lab with additional client machines
