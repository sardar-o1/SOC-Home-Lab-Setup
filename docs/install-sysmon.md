# Install Microsoft Sysmon on Windows 10

Sysmon enhances log monitoring by providing detailed insights into system activity—such as process creation, network connections, and file changes - giving more granular control over logs.

Sysmon requires a config file in order to tell the binary how to analyze the events that it is receiving. You can create your own Sysmon config or download one created by SwiftOnSecurity.

### Open the Windows 10 VM and ensure it has an active internet connection.

1. Download Sysmon from the official website - https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon 

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/14f62a451dda4c2b48d54c1a014c9eb6d1eb12a9/Screenshots/sysmon1.png)

2. Download the Sysmon configuration file. Click "Code," then select "Download ZIP."

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/14f62a451dda4c2b48d54c1a014c9eb6d1eb12a9/Screenshots/sysmon2.png)

3. Extract the ZIP and copy its contents into the Sysmon installation folder so the configuration is available when Sysmon is installed.
   
![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/14f62a451dda4c2b48d54c1a014c9eb6d1eb12a9/Screenshots/sysmon3.png)

4. Open Command Prompt with administrator privileges and change to the directory containing your extracted Sysmon folder.

Run the install command: sysmon64.exe -accepteula -i sysmonconfig-export.xml

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/14f62a451dda4c2b48d54c1a014c9eb6d1eb12a9/Screenshots/sysmon4.png)


### To verify Sysmon installed successfully, open Event Viewer → Applications and Services Logs → Microsoft → Windows → Sysmon.
