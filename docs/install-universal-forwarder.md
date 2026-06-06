# Download and install the Splunk Universal Forwarder on Windows 10 — step by step


#### The Splunk Universal Forwarder collects logs, events, and metrics and forwards them to the Splunk server. This installation ensures the Ubuntu Splunk server receives data from the Universal Forwarder.


## Before downloading and installing the Universal Forwarder, enable the receiving port on the Ubuntu Splunk server.

1. Log in to the Splunk web interface, then click Settings and select Forwarding and Receiving.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/splunk_conf1.png)

2. Click the "+Add new".

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/splunk_conf2.png)

3. Now configure the receiving port (default: 9997) and save.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/splunk_conf3.png)

#

# Now download the Universal Forwarder


1. Open the Windows 10 VM, sign in to the Splunk website, then click "Trial & Download."

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/UF1.png)

2. Now you will see the Universal Forwarder download option — click the "Download" button.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/UF2.png)

3. Now select the Universal Forwarder for your OS — I have 64‑bit Windows, so I downloaded the 64‑bit .msi file.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/UF3.png)

4. Go to the folder containing the .msi file and double-click it to start the installer. Check "Accept the license agreement" and choose "Customized options".

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/UF4.png)

5. Next, leave the encryption settings at their default values.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/UF5.png)

6. Select "Local System" to send all local system data to the Splunk server.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/UF6.png)

7. Now select which logs to forward to the Splunk server.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/UF7.png)

8. Create a Universal Forwarder username and password.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/UF8.png)

9.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/UF9.png)
![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/UF10.png)
![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/bc3370c1db9036cd9ed2cc26c92506b32df2e5ab/Screenshots/UF11.png)

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/bc3370c1db9036cd9ed2cc26c92506b32df2e5ab/Screenshots/splunk_conf4.png)
![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/bc3370c1db9036cd9ed2cc26c92506b32df2e5ab/Screenshots/splunk_conf5.png)
![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/bc3370c1db9036cd9ed2cc26c92506b32df2e5ab/Screenshots/splunk_conf6.png)
![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/bc3370c1db9036cd9ed2cc26c92506b32df2e5ab/Screenshots/splunk_conf7.png)
