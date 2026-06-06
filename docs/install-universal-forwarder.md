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

9. The deployment server is an optional Splunk component that centrally manages configurations and updates for multiple Universal Forwarders. Enter the Splunk server IP and the default deployment port (8089).

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/UF9.png)

10. The receiving server (the Splunk indexer) receives data from Universal Forwarders. Enter the Splunk server IP and the receiving port (default: 9997), which you configured earlier on the Splunk server.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/ffd23d05b27fad7d0945c44e60e9cb1704d18542/Screenshots/UF10.png)

11. Click "Finish" to complete the installation.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/bc3370c1db9036cd9ed2cc26c92506b32df2e5ab/Screenshots/UF11.png)

#

## Again, go to the Splunk server to ensure the Ubuntu Splunk server is receiving data from the Universal Forwarder

1. Log in to the Splunk server web interface and select "Search & Reporting".

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/bc3370c1db9036cd9ed2cc26c92506b32df2e5ab/Screenshots/splunk_conf4.png)

2. Click "Data Summary".

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/bc3370c1db9036cd9ed2cc26c92506b32df2e5ab/Screenshots/splunk_conf5.png)

3. We see our Windows host listed. Click a host, then view Source or Sourcetype to verify the selected log sources.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/bc3370c1db9036cd9ed2cc26c92506b32df2e5ab/Screenshots/splunk_conf6.png)

4. When you click the host, all events appear. Select Verbose mode — Splunk prioritizes completeness by discovering and extracting all available fields.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/bc3370c1db9036cd9ed2cc26c92506b32df2e5ab/Screenshots/splunk_conf7.png)


