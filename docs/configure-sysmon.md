# Configure Sysmon to Send Logs to Splunk via Universal Forwarder

1. After completing the setup of the Ubuntu Splunk server, installing the Splunk Universal Forwarder, and installing Sysmon on Windows 10, open File Explorer and navigate to: C:\Program Files\SplunkUniversalForwarder\etc\system\local

If you do not see an inputs.conf file in this directory, create a new file named inputs.conf.

Next, add the Sysmon log collection configuration to the file. You can copy the configuration from the config/sysmon directory in this repository.


![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/0f65ace570d2de2cfcaee8a91a2f54edc53cce10/Screenshots/sys_config1.png)
![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/0f65ace570d2de2cfcaee8a91a2f54edc53cce10/Screenshots/sys_config2.png)
![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/0f65ace570d2de2cfcaee8a91a2f54edc53cce10/Screenshots/sys_config3.png)
![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/0f65ace570d2de2cfcaee8a91a2f54edc53cce10/Screenshots/sys_config4.png)
![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/0f65ace570d2de2cfcaee8a91a2f54edc53cce10/Screenshots/sys_config5.png)
