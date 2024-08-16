# Preface

This repository is a report documenting my journey of researching Windows Server. My goal is to create a comprehensive guide to assist readers who may be encountering difficulties in learning about Windows Server. Additionally, this repository will serve as a testament to my skills, providing potential employers with a clear assessment of my capabilities.

# Commitment Statement

I hereby declare that this report is my own work, created through my own research and analysis. The content of this document is a result of my independent study, and all sources used are properly cited.

# Required Preparations.

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

Active Directory Domain Services (AD DS) are fundamental components of Active Directory that handle the management of users and computers, allowing system administrators to structure data into logical hierarchies.

AD DS supports features such as security certificates, Single Sign-On (SSO), LDAP, and rights management.

For Incident Response (IR) and cybersecurity professionals, understanding AD DS is crucial because any cyberattack will impact Active Directory. Knowing what to monitor and how to address attacks is essential for effective response and mitigation.

[How to create an Active Directory Domain With Windows Server 2022? ](docs/ADDS.md)

[How to create Group? ](docs/Create_Gr.md)

### User Permissions by Department.

| **Department**        | **User Group**                | **Permissions**                                                                          | **Description**                                                   |
|-----------------------|------------------------------|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| **IT Department**     | IT_Admins                     | - Full Control<br>- Manage Active Directory<br>- Deploy and manage network systems       | Administer the network, deploy, and maintain IT infrastructure    |
|                       | IT_Support                    | - Read/Write<br>- Install software<br>- Manage user accounts                             | Provide user support, install software, and manage basic accounts |
| **Finance Department**| Finance_Managers              | - Full Control in Finance folder<br>- Access to accounting systems                       | Manage financial operations, access accounting systems and reports|
|                       | Finance_Staff                 | - Read/Write in Finance folder<br>- Limited access to accounting systems                 | Perform daily financial tasks, such as data entry and reporting   |
| **HR Department**     | HR_Managers                   | - Full Control in HR folder<br>- Manage employee records                                 | Manage HR information, recruitment, training, and employee development |
|                       | HR_Staff                      | - Read/Write in HR folder<br>- Limited access to employee records                        | Support daily HR activities, manage employee records              |
| **Sales Department**  | Sales_Managers                | - Full Control in Sales folder<br>- Access to CRM systems                                | Manage sales teams, coordinate sales strategies                   |
|                       | Sales_Staff                   | - Read/Write in Sales folder<br>- Limited access to CRM systems                          | Perform sales activities, data entry, and manage customer information |
| **Marketing Department**| Marketing_Managers          | - Full Control in Marketing folder<br>- Access to advertising tools                      | Manage marketing campaigns and advertising                        |
|                       | Marketing_Staff               | - Read/Write in Marketing folder<br>- Limited access to advertising tools                | Execute daily marketing tasks, prepare content, and manage campaigns |


