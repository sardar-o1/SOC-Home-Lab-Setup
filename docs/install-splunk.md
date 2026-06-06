# Install Splunk Enterprise on Ubuntu VM


1. Open a browser on the Ubuntu VM and go to the Splunk Enterprise download page: https://www.splunk.com/en\_us/download/splunk-enterprise.html. Create a Splunk account if you don't already have one.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/5faf5e354124b78cb6f2ae869bb9d0d467cf6a26/Screenshots/splunk1.png)

2. Sign in to your Splunk account using the credentials you created.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/5faf5e354124b78cb6f2ae869bb9d0d467cf6a26/Screenshots/splunk2.png)

3. Splunk offers installers for multiple operating systems; download the latest Splunk Enterprise .deb package for Linux. Click "Download Now" or copy the direct wget link.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/5faf5e354124b78cb6f2ae869bb9d0d467cf6a26/Screenshots/splunk3.png)

4. After clicking "Download Now," select the command-line (wget) option and copy that command.
   
![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/5faf5e354124b78cb6f2ae869bb9d0d467cf6a26/Screenshots/splunk4.png)

5. Open Terminal on Ubuntu and paste the previously copied wget link.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/5faf5e354124b78cb6f2ae869bb9d0d467cf6a26/Screenshots/splunk5.png)


6. Within the download directory, install Splunk on Ubuntu, run: sudo dpkg -i splunk*.deb
   
![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/5faf5e354124b78cb6f2ae869bb9d0d467cf6a26/Screenshots/splunk6.png)


7. Switch to the root user with sudo su, then change to Splunk’s bin directory (/opt/splunk/bin) because that directory contains the executable programs and startup scripts. Start Splunk and accept the license.
run: ./splunk start --accept-license

You will be prompted to create the Splunk admin username and password.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/5faf5e354124b78cb6f2ae869bb9d0d467cf6a26/Screenshots/splunk7.png)


9. Now the Splunk web interface is ready—open http://127.0.0.1:8000 in your browser or copy the provided link and log in to start using Splunk.

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/5faf5e354124b78cb6f2ae869bb9d0d467cf6a26/Screenshots/splunk8.png)

10. Enable Splunk to start at boot run: ./splunk enable boot-start or /opt/splunk/bin/splunk enable boot-start.

For official documentation, see: https://help.splunk.com/en/splunk-enterprise/get-started/install-and-upgrade/10.4/install-splunk-enterprise-on-linux-or-macos/install-on-linux

![img](https://github.com/sardar-o1/SOC-Home-Lab-Setup/blob/5faf5e354124b78cb6f2ae869bb9d0d467cf6a26/Screenshots/splunk9.png)


