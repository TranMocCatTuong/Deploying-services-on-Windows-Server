# Resources to prepare.
- Tools: VMware Workstation Pro (Version 15).
- File ISO: windows server 2022, windows 10.

# Parameters.
| Name         | OS                | IP          | Subnet mask   | Default Gateway | DNS Server    |
|:--------------:|:-------------------:|:-------------:|:---------------:|:-----------------:|:---------------:|
| WS2K22-DC01  | Windows server 2022 | 192.168.1.2 | 255.255.255.0 | 192.168.1.1 | 192.168.1.2 |
| WS2K22-SRV01  | Windows server 2022 | 192.168.1.3 | 255.255.255.0 | 192.168.1.1 | 192.168.1.2 |
| WS2K22-SRV02  | Windows server 2022 | 192.168.1.4 | 255.255.255.0 | 192.168.1.1 | 192.168.1.2 |
| WIN10-CL01  | Windows 10 | 192.168.1.16 | 255.255.255.0 | 192.168.1.1 | 192.168.1.2 |
| WIN10-CL02  | Windows 10 | 192.168.1.17 | 255.255.255.0 | 192.168.1.1 | 192.168.1.2 |

# Services deployed.
1. Active Directory Domain Services (AD DS)
2. Domain Name System (DNS).
3. Dynamic Host Configuration Protocol (DHCP).
4. File and Storage Services.
5. Hyper-V.
6. Networking Services (VPN, Routing, và Remote Access).
7. Print and Document Services.
8. Web Services (IIS).
9. Windows Deployment Services (WDS).
10. Windows Server Update Services (WSUS).
11. 2FA.


