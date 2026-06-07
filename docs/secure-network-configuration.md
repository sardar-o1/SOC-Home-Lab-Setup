# Network Configuration

When analyzing malware, avoid using Bridged Adapter mode. For maximum isolation, you can disable network connectivity entirely by selecting Not Attached.

For this lab, Internal Networking in VirtualBox is used to create a fully isolated environment between Kali Linux and Windows 10 for hands-on practice. If internet access is required, the default NAT mode can be used.

This setup helps demonstrate how to configure virtual machine networking based on specific requirements for security analysis.

#

Let’s configure our network as an internal network. In this network configuration, we will set up a static IP to ensure that both machines can communicate with each other.

 
1. Open VirtualBox > select Kali Linux > go to Settings > and then select Network. You will see that the default network adapter is set to NAT.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%201.png)

2. Now select the Internal Network option and give it any name you like.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%202.png)

3. Next, go to the Windows network settings, select the Internal Network option, and choose the name you created earlier.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%203.png)

4. Now power on your Kali Linux machine. Right-click the Ethernet icon and go to “Edit Connections.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%204.png)

5. Then select the wired connection 1 and click the settings icon.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%205.png)

6. Next, go to IPv4 settings > choose the method as Manual > then click Add to enter your static IP address and netmask, and save it.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%206.png)

7. Now open a terminal on Kali, run the 'ifconfig' command, and check to confirm that the IP address has been successfully added.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%207.png)

8. Open the Windows machine, right-click the Ethernet icon in the bottom-right corner, and open Network Settings.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%208.png)

9. Select the “Change adapter options” option.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%209.png)

10. Right-click Ethernet and go to Properties. In the Properties window, select Internet Protocol Version 4 (TCP/IPv4) and click OK.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%2010.png)

11. Here, select “Use the following IP address” and enter your Windows static IP address and subnet mask.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%2011.png)

12. Again, check the IP address by opening Command Prompt and running the ipconfig command.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%2012.png)

13. To ensure both machines can communicate with each other, run the command 'ping 192.198.10.1' on the Windows machine. However, before running the ping command on kali machine, make sure the firewall is disabled on the Windows virtual machine.

![network](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/54fa6495032844fd2154b48e3a623a5a49ec0c0f/Images/network%20img%2013.png)
