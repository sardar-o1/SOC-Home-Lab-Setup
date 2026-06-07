# Configure Sysmon to Send Logs to Splunk via Universal Forwarder

1. After completing the setup of the Ubuntu Splunk server, installing the Splunk Universal Forwarder, and installing Sysmon on Windows 10, open File Explorer and navigate to: C:\Program Files\SplunkUniversalForwarder\etc\system\local

    If you do not see an inputs.conf file in this directory, create a new file named inputs.conf.

    Next, add the Sysmon log collection configuration to the file. You can copy the configuration from the configs/splunk/inputs.conf directory in this repository.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/0f65ace570d2de2cfcaee8a91a2f54edc53cce10/Screenshots/sys_config1.png)

2. Open PowerShell as an Administrator and restart the Splunk Universal Forwarder service.

First, navigate to the Splunk Universal Forwarder bin directory: cd "C:\Program Files\SplunkUniversalForwarder\bin"

Then restart the Universal Forwarder by running: .\splunk.exe restart

After the service restarts successfully, the Universal Forwarder will begin collecting Sysmon events based on the configuration specified in inputs.conf.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/0f65ace570d2de2cfcaee8a91a2f54edc53cce10/Screenshots/sys_config2.png)

3. Log in to the Splunk Web interface on your Ubuntu server. From the Splunk home page, select Search & Reporting. Then, click Data Summary to view the data currently being indexed by Splunk.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/0f65ace570d2de2cfcaee8a91a2f54edc53cce10/Screenshots/sys_config3.png)

4. You should now see your Windows host listed in the Data Summary page, indicating that the Splunk Universal Forwarder is successfully sending data to the Splunk server.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/0f65ace570d2de2cfcaee8a91a2f54edc53cce10/Screenshots/sys_config4.png)

5. Click Sources next to the host entry. You should see Sysmon events listed among the available sources or sourcetypes. This confirms that the Splunk Universal Forwarder is successfully collecting and forwarding Sysmon logs to the Splunk server.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/0f65ace570d2de2cfcaee8a91a2f54edc53cce10/Screenshots/sys_config5.png)


