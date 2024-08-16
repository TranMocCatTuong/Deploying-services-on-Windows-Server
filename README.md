# Preface

This repository is a report documenting my journey of researching Windows Server. My goal is to create a comprehensive guide to assist readers who may be encountering difficulties in learning about Windows Server. Additionally, this repository will serve as a testament to my skills, providing potential employers with a clear assessment of my capabilities.

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

1. Open **Server Manager**, [1] On the toolbar select **Manage**. [2] Choose **Add Roles and Features**.

  ![ Image 1. ](/img/3_1.png)

2. Click **Next**.

  ![ Image 2. ](/img/3_2.png)

3. Click **Next**.

  ![ Image 3. ](/img/3_3.png)

4. Click **Next**.

  ![ Image 4. ](/img/3_4.png)

5. In the **Roles** list, check the box for **Active Directory Domain Services**.

  ![ Image 5. ](/img/3_5.png)

6. Click **Add Features**.

  ![ Image 6. ](/img/3_6.png)

7. Continue press **Next**.

  ![ Image 7. ](/img/3_7.png)

8. Click **Next**.

  ![ Image 8. ](/img/3_8.png)

9. Click **Next**.

  ![ Image 9. ](/img/3_9.png)

10. Check the box Restart the destination server automatically if required.

  ![ Image 10. ](/img/3_10.png)

11. Click **Yes**.

  ![ Image 11. ](/img/3_11.png)

12. Click **Install** to finish and **Restart** Windows Server.

  ![ Image 12. ](/img/3_12.png)

13. When restarting the Windows Server, click on the icon as shown in the image.
    
  ![ Image 13. ](/img/3_13.png)

15. Double-click **Promote this server to a domain controller**.

  ![ Image 14. ](/img/3_14.png)

15. Check **Add a new forest**, then set the root domain name. Click **Next**.

  ![ Image 15. ](/img/3_15.png)

16. 

  ![ Image 16. ](/img/3_16.png)

17. 

  ![ Image 17. ](/img/3_17.png)

18. 

  ![ Image 18. ](/img/3_18.png)

19. 

  ![ Image 19. ](/img/3_19.png)

20. 

  ![ Image 20. ](/img/3_20.png)

21. 

  ![ Image 21. ](/img/3_21.png)
