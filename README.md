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
We need to properly configure our virtual machines to safely run testing tools and prevent any external access to the host system. VirtualBox provides several network configuration modes. For this lab, I chose the Internal Networking option to create a fully isolated environment for hands-on practice.

To learn more about VirtualBox network modes, go to the official website : (https://docs.oracle.com/en/virtualization/virtualbox/6.0/user/networkingmodes.html)
# 
Download VirtualBox: (https://www.virtualbox.org/wiki/Downloads)
