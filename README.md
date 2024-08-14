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
12. 
[Contribution guidelines for this project](docs/CONTRIBUTING.md)

# Create a new virtual machine
1. [1] Select **File** > [2] **New Virtual Machine Wizard**.

  ![ Image 1. ](/img/1_1.png)

2. Click **Next**.

  ![ Image 2. ](/img/1_2.png)

3. Continue to select **Next**.

  ![ Image 3. ](/img/1_3.png)

4. Select **Install the operating system later**, then click **Next**.

  ![ Image 4. ](/img/1_4.png)

5. [1] Select **Guest Operating System** and [2] **Version**, [2] click **Next**.

  ![ Image 5. ](/img/1_5.png)

6. [1] Name the Virtual Machine, [2] Select **Browse...** to change location, [3] then click **Next**.

  ![ Image 6. ](/img/1_6.png)

7. Select a firmware type and click **Next**.

  ![ Image 7. ](/img/1_7.png)

8. [1] Processor configuration, [2] click **Next**.

  ![ Image 8. ](/img/1_8.png)
 
9. [1] Specify the amount of memory, [2] click **Next**.

  ![ Image 9. ](/img/1_9.png)

10. [1] Select the type of network you want to add, [2] click **Next**.

  ![ Image 10. ](/img/1_10.png)

11. Select I/O Controller types and click **Next**.

  ![ Image 11. ](/img/1_11.png)

12. [1] Select a Disk type, [2] then click **Next**.

  ![ Image 12. ](/img/1_12.png)

13. [1] Select a Disk, [2] click **Next**.

  ![ Image 13. ](/img/1_13.png)

14. [1] Specify Disk capacity, [2] then click **Next**.

  ![ Image 14. ](/img/1_14.png)

15. [1] Select **Browse..** to change the file save folder, [2] Click **Next**.

  ![ Image 15. ](/img/1_15.png)

16. Click **Finish**.

  ![ Image 16. ](/img/1_16.png)

 



