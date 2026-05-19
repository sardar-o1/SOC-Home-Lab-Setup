# SOC-Home-Lab-Setup
I built a simple and beginner-friendly SOC (Security Operations Center) home lab designed to provide an environment for hands-on practice in defensive cybersecurity. This project is part of my cybersecurity learning journey, where I practice blue team operations, basic threat detection, log analysis, and attack simulation in an isolated lab setup.

# Virtualization
Virtualization is a technology that allows a single physical computer to run multiple isolated virtual machines (VMs), each with its own operating system and applications simultaneously.

There are several free virtualization platforms available, such as VirtualBox, VMware Workstation, and Microsoft Hyper-V. For this project, I chose VirtualBox because it is beginner-friendly, lightweight, and widely used for cybersecurity labs.

# Currently, the lab consists of:
| Virtual Machine | Purpose |
|------------------|---------|
| Kali Linux       | Attacking & testing |
| Windows 10       | Monitoring & detection |

# Secure Network Configuration
We need to properly configure our virtual machines to safely run testing tools and prevent any external access to the host system. VirtualBox provides several network configuration modes. For this lab, I chose the Internal Networking option to create a fully isolated environment for hands-on practice. If you need internet access for testing tools, you can use the default NAT mode. 

However, if you are analyzing malware and looking for additional indicators of compromise on a virtual machine, I highly recommend that the VM does not have internet connectivity and does not use a bridged network adapter. Instead, it should be placed on its own isolated network, or you can simply use the “Not Attached” mode.

![network diagram](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/55f2e7b4613283948cf5af5f72d3ef7476a5df14/Images/Network%20diagram.png)

To learn more about VirtualBox network modes, go to the official website : (https://docs.oracle.com/en/virtualization/virtualbox/6.0/user/networkingmodes.html)

# Download VirtualBox: (https://www.virtualbox.org/wiki/Downloads)

1. Download VirtualBox for your operating system.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/0593b54799dcfe2a59949410efec5d88dc1f0739/Images/virtualbox%20img%201.png)

1.1 Now verify the SHA256 checksum provided by the website to ensure that the downloaded file has not been modified.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/e37c7f091e848618da06ca95ff8b5a17b58ce22d/Images/virtualbox%20img%202.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/e37c7f091e848618da06ca95ff8b5a17b58ce22d/Images/virtualbox%20img%203.png)

1.2 Now open PowerShell and navigate to the directory where your downloaded file is located. Then enter the command shown in the screenshot below.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/e37c7f091e848618da06ca95ff8b5a17b58ce22d/Images/virtualbox%20img%204.png)

1.3 Now we are ready to install VirtualBox. Double-click the `.exe` file to begin the installation.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/e37c7f091e848618da06ca95ff8b5a17b58ce22d/Images/virtualbox%20img%205.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/e37c7f091e848618da06ca95ff8b5a17b58ce22d/Images/virtualbox%20img%206.png)

1.4 If you face any missing dependencies, install them and continue.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/e37c7f091e848618da06ca95ff8b5a17b58ce22d/Images/virtualbox%20img%207.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/e37c7f091e848618da06ca95ff8b5a17b58ce22d/Images/virtualbox%20img%208.png)

# Now download Kali Linux from the official website: https://www.kali.org/get-kali/#kali-virtual-machines

2. There are multiple ways to download Kali Linux, but I prefer downloading the prebuilt virtual machine because it can be easily imported into VirtualBox.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/99ae5b2fb7c2c80b7aae1236c46e8bdaf3cfb7f7/Images/kali%201.png)

2.1 Now extract the downloaded file. You will need 7-Zip for extraction. If it is not installed on your system, download the version compatible with your operating system from the official website. https://www.7-zip.org/download.html

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/99ae5b2fb7c2c80b7aae1236c46e8bdaf3cfb7f7/Images/kali%202.png)

2.2 Now head over to the extracted folder. All you need to do is double-click the `.vbox` file, and it should automatically import into VirtualBox.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/99ae5b2fb7c2c80b7aae1236c46e8bdaf3cfb7f7/Images/kali%204.png)

2.3 If you cannot see the `.vbox` file extension, open File Explorer > go to the View tab > enable File name extensions.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/99ae5b2fb7c2c80b7aae1236c46e8bdaf3cfb7f7/Images/kali%203.png)

2.4 Log in with the default username and password: `kali/kali`.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/99ae5b2fb7c2c80b7aae1236c46e8bdaf3cfb7f7/Images/kali%205.png)

# Now download Windows 10 from the official website: https://www.microsoft.com/en-in/software-download/windows10

3. Download Windows 10 and create your own Windows 10 ISO image.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%201.png)

3.1 After downloading Windows 10, double-click the downloaded file. It will help you generate an ISO image file.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%202.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%203.png)

3.2 Now check the “Create installation media” option.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%204.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%205.png)

3.3 Choose the ISO file option because we want to create and download an ISO image for VirtualBox.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%206.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%207.png)

3.4 Now start creating your Windows 10 virtual machine. Open VirtualBox and click on “New.” Enter a name for the virtual machine, whatever you want, and select the ISO image from its location on your device.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%208.png)

3.5 I will leave the virtual machine configuration settings as default.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%209.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%2010.png)

3.6 Let’s start the Windows virtual machine by clicking the Start button, and then configure the Windows 10 setup.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%2011.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%2012.png)

3.7 Click on “Install now.”

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%2013.png)

3.8 Go ahead and select “I don’t have a product key,” then continue.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%2014.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%2015.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%2016.png)

3.9 I prefer to go with the custom setup.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%2017.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%2018.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%2019.png)

3.10 Sign in with your Outlook email ID, and you’re all set to start using Windows.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/b829c3ead2cfbd087ed38456b226ca8cc68765b8/Images/windows10%20img%2020.png)

# Let’s configure our network as an internal network


