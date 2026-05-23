# SOC-Home-Lab-Setup
I built a simple and beginner-friendly SOC (Security Operations Center) home lab designed to provide an environment for hands-on practice in defensive cybersecurity. This project is part of my cybersecurity learning journey, where I practice blue team operations, basic threat detection, log analysis, and attack simulation in an isolated lab setup.

I plan to continuously upgrade and expand this home lab in the future as part of my cybersecurity learning journey.

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


