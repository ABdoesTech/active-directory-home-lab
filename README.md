# active-directory-home-lab

📌 Project Overview

This project simulates a small business IT environment using Windows Server 2022 and Windows 11 virtual machines.  
The goal was to deploy and manage a domain environment similar to what is used in real-world enterprise IT support roles.

---

## 🏗️ Lab Environment

**Hypervisor:** VirtualBox  
**Domain Controller:** Windows Server 2022  
**Client Machine:** Windows 11  
**Network Type:** Internal Network (LABNET)

### Network Configuration

- Domain Controller IP: 192.168.10.10 (Static)
- Client IP: 192.168.10.20
- Subnet Mask: 255.255.255.0
- DNS Server: 192.168.10.10

---

## ⚙️ Server Configuration Steps

### 1️⃣ Installed Roles & Features
- Active Directory Domain Services (AD DS)
- DNS Server
- DHCP Server

### 2️⃣ Promoted Server to Domain Controller
- Created domain: `lab.local`
- Configured forest & domain functional level
- Verified SYSVOL and NETLOGON shares

### 3️⃣ DNS Configuration
- Verified forward lookup zone
- Tested name resolution from client machine
- Used `nslookup` to confirm proper DNS functionality

### 4️⃣ DHCP Configuration
- Created DHCP scope
- Assigned IP range for client machines
- Verified lease assignment

---

## 👥 Active Directory Management

### Organizational Units Created:
- IT
- HR
- Sales
- Workstations

### User & Group Management:
- Created multiple test users
- Created security groups
- Assigned group memberships
- Applied NTFS permissions to shared folders

---

## 🛡️ Group Policy Implementation

Created and applied GPOs to simulate real business policies:

- Password complexity enforcement
- Account lockout threshold
- Desktop wallpaper restriction
- Disabled Control Panel access (test OU)

Verified GPO application using:
- `gpresult /r`
- Group Policy Management Console

---

## 🔐 Account Lockout Troubleshooting Simulation

Scenario:
A user account was locked due to multiple failed login attempts.

Troubleshooting Steps:
- Verified lockout in Active Directory Users & Computers
- Reviewed security logs in Event Viewer
- Unlocked account
- Reset password
- Confirmed login success

---

## 🖥️ Client Machine Testing

- Joined Windows 11 machine to domain
- Logged in with domain user accounts
- Tested GPO enforcement
- Verified shared folder access

---

## 📊 Real-World Skills Demonstrated

- Domain environment deployment
- Active Directory administration
- DNS & DHCP configuration
- Group Policy management
- User account troubleshooting
- Network configuration fundamentals
- IT documentation practices

---

## 🎯 What I Learned

- Importance of DNS in domain environments
- How Group Policy impacts enterprise systems
- How to troubleshoot account and authentication issues
- Best practices for organizing OUs and applying policies

---

## 🚀 Future Improvements

- Implement file server with access-based enumeration
- Simulate multi-site replication
- Add backup domain controller
- Integrate Microsoft 365 hybrid environment
