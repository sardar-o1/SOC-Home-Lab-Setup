# SOC-Home-Lab-Setup
## Overview 
This repository documents the development of my SOC (Security Operations Center) Home Lab, a hands-on cybersecurity environment built to practice and strengthen defensive security skills. The lab simulates a small enterprise network using virtualized systems and security tools, providing a controlled environment for monitoring, log analysis, threat detection, and incident investigation.

The primary goal of this project is to gain practical experience with Blue Team operations by deploying and configuring security technologies such as SIEM solutions, endpoint monitoring tools, and network services. Through this lab, I perform attack simulations, analyze security events, investigate alerts, and improve my understanding of security monitoring workflows.

This project is continuously evolving as I expand the lab with new technologies, security use cases, and detection capabilities to further develop my cybersecurity knowledge and practical SOC experience.

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
           │ (Ingests, Parses, & Indexes Log Data)
           ▼
[ Dashboards / Alerts / Detection Rules ]
```

# Installation Guide

### 1. Install [virtual box](docs/install-virtualbox.md)

### 2. Install [kali linux](docs/install-kali-linux.md)

### 3. Install [windows 10](docs/install-windows10.md)

### 4. Install [sysmon](docs/install-sysmon.md)

### 5. Install [ubuntu server](docs/install-ubuntu.md)

### 6. Install [splunk enterprise](docs/install-splunk.md)

### 7. Install [splunk universal forwarder](docs/install-universal-forwarder.md)





