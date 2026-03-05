# Windows Server 2025 Domain Setup

## Environment

- Hypervisor: VirtualBox
- Domain Controller: Windows Server 2025
- Client: Windows 11
- Network: Internal Network (LABNET)

## Server Configuration Steps

1. Installed Windows Server 2025
2. Assigned static IP (192.168.10.10)
3. Installed Roles:
   - Active Directory Domain Services
   - DNS Server
   - DHCP Server
4. Promoted server to Domain Controller
5. Created domain: lab.local

## Domain Join

- Configured client DNS to 192.168.10.10
- Joined Windows 11 machine to lab.local
- Verified domain authentication

## Verification Tools Used

- nslookup
- ipconfig /all
- dcdiag
- gpresult /r
