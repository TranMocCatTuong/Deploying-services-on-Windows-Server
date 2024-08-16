# Resources to prepare.
- Tools: VMware Workstation Pro (Version 15).
- File ISO: windows server 2022, windows 10.

# Services deployed.

> [!TIP]
> Think of this as a table of contents, where you can click on a service to quickly navigate to it.

### [1. Active Directory Domain Services (AD DS)](https://github.com/TranMocCatTuong/Deploying-services-on-Windows-Server/blob/main/README.md#1-active-directory-domain-services-ad-ds-1)
### 2. Domain Name System (DNS).
### 3. Dynamic Host Configuration Protocol (DHCP).
### 4. File and Storage Services.
### 5. Hyper-V.
### 6. Networking Services (VPN, Routing, và Remote Access).
### 7. Print and Document Services.
### 8. Web Services (IIS).
### 9. Windows Deployment Services (WDS).
### 10. Windows Server Update Services (WSUS).
### 11. 2FA.


# Create new virtual machines.

[How to create new virtual machine?](docs/Create_new_virtual_machine.md)

| Name         | Memory                | Processors          | Hard Disk   | Network Adapter | CD/DVD    | OS                |
|:--------------:|:-------------------:|:-------------:|:---------------:|:-----------------:|:---------------:|:-------------------:|
| WS2K22-DC01  | 4 GB | 2 | 60 GB (NVMe) | VMnet1, NAT | SATA | Windows server 2022 |
| WS2K22-SRV01  | 4 GB | 2 | 60 GB (NVMe) | VMnet1 | SATA | Windows server 2022 |
| WS2K22-SRV02  | 4 GB | 2 | 60 GB (NVMe) | VMnet1 | SATA | Windows server 2022 |
| WIN10-CL01  | 4 GB | 2 | 60 GB (NVMe) | VMnet1 | SATA | Windows 10 |
| WIN10-CL02  | 4 GB | 2 | 60 GB (NVMe) | VMnet1 | SATA | Windows 10 |

 # Network configuration for virtual machines.

 [How to configure network?](docs/Conf_Network.md)
 > [!NOTE]
> If you've configured the network for the virtual machines but still can't connect them to each other, try disabling the firewall.
 
| Name         | IP          | Subnet mask   | Default Gateway | DNS Server    |
|:--------------:|:-------------:|:---------------:|:-----------------:|:---------------:|
| WS2K22-DC01   | 192.168.1.2 | 255.255.255.0 | 192.168.1.1 | 192.168.1.2 |
| WS2K22-SRV01  | 192.168.1.3 | 255.255.255.0 | 192.168.1.1 | 192.168.1.2 |
| WS2K22-SRV02  | 192.168.1.4 | 255.255.255.0 | 192.168.1.1 | 192.168.1.2 |
| WIN10-CL01  | 192.168.1.16 | 255.255.255.0 | 192.168.1.1 | 192.168.1.2 |
| WIN10-CL02  | 192.168.1.17 | 255.255.255.0 | 192.168.1.1 | 192.168.1.2 |

## 1. Active Directory Domain Services (AD DS)



