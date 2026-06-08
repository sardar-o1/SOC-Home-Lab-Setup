# SOC-Home-Lab-Setup
## Overview 
This repository documents the setup and configuration of my SOC (Security Operations Center) Home Lab. The lab is built using virtual machines and security tools to create a hands-on environment for learning security monitoring, log management, and SIEM operations.

Throughout this project, I installed, configured, and integrated tools such as Splunk, Sysmon, and Splunk Universal Forwarders to collect and centralize security events from multiple systems. The repository includes step-by-step installation guides, configuration files, network architecture diagrams, and documentation covering the complete setup process.

The goal of this project is to gain practical experience with log collection, system monitoring, and SOC workflows while building a foundation for future threat detection and security analysis projects.

# Currently, the lab consists of:

| Virtual Machine | Operating System | Role |
| :--- | :--- | :--- |
| **Adversary Node** | Kali Linux | Attack Simulation | 
| **Endpoint Target** | Windows 10 Enterprise | Victim Machine / Telemetry Source | 
| **SIEM Engine** | Ubuntu Server | Splunk Enterprise Log Indexer | 

# Lab Architecture

```text
[ Kali Linux (Attacker VM) ]
           │
           │ (Simulated Attacks / Malware Execution)
           ▼
[ Windows 10 (Victim VM) ]
           │
           │ (Generates: Security, System, Application, & Sysmon Logs)
           ▼
[ Splunk Universal Forwarder ]
           │
           │ (Sends Encrypted Event Data via Port 9997)
           ▼
[ Ubuntu Server (Splunk Enterprise) ]
           │
(Ingests, Parses, & Indexes Log Data)
```

# Installation Guide

### 1. Install [virtual box](docs/install-virtualbox.md)

### 2. Install [kali linux](docs/install-kali-linux.md)

### 3. Install [windows 10](docs/install-windows10.md)

### 4. Install [sysmon](docs/install-sysmon.md)

### 5. Install [ubuntu server](docs/install-ubuntu.md)

### 6. Install [splunk enterprise](docs/install-splunk.md)

### 7. Install & Configure [splunk universal forwarder](docs/install-universal-forwarder.md)

### 8. Configure [Universal Forwarder to Collect Sysmon Logs](docs/forward-sysmon-logs-to-splunk.md)


# Troubleshooting Guide

#### - Universal Forwarder not connecting to Splunk:

Verify network connectivity between the Windows host and the Splunk server using the ping command. Ensure both machines can communicate with each other. Confirm that port 9997 is open on the Splunk indexer and not blocked by any firewall. Also verify that the Splunk Universal Forwarder service is running. If connectivity issues persist, review the VirtualBox network mode configuration (e.g., NAT, Internal Network, or Bridged Adapter) based on your lab setup.

#### - No Sysmon events appearing in Splunk:

Ensure the Sysmon service is installed and actively running on the Windows host. Verify that the Splunk Universal Forwarder inputs.conf is correctly configured to collect Sysmon logs. Also confirm that events are being generated in Event Viewer under Microsoft-Windows-Sysmon/Operational.

