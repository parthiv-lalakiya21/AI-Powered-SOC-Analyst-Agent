# AI-Powered SOC Analyst Agent

## Overview

AI-Powered SOC Analyst Agent is a cybersecurity automation project that combines Python, Airia AI, Tshark, Kali Linux, and Ubuntu to simulate Security Operations Center (SOC) workflows. The solution captures network traffic, detects suspicious activities, generates structured security alerts, and leverages AI to perform automated threat triage and incident analysis.

## Features

* Detects ICMP Flood / Network Volume Attacks
* Detects Network Reconnaissance and Port Scanning Activities
* Detects SSH Brute Force Attempts
* Automated Packet Capture using Tshark
* Alert Generation in Structured JSON Format
* AI-Powered Threat Analysis using Airia AI
* MITRE ATT&CK Mapping
* Risk Scoring and Severity Classification
* Automated Incident Response Recommendations
* Real-World Attack Simulation using Kali Linux

---

## Technologies Used

* Python 3
* Airia AI
* Tshark / Wireshark
* Kali Linux
* Ubuntu 22.04
* Nmap
* Hydra
* Hping3
* JSON
* Requests Library

---

## Project Architecture

```text
Kali Linux (Attacker)
        |
        |  ICMP Flood / Nmap Scan / Hydra Attack
        v
Ubuntu Server
        |
        |  Tshark Packet Capture
        v
Python SOC Agent
        |
        |  Alert Generation (JSON)
        v
Airia AI
        |
        |  Threat Classification
        |  Risk Scoring
        |  MITRE ATT&CK Mapping
        v
SOC Triage Report
```

---

## Detection Capabilities

| Attack Type     | Detection                         |
| --------------- | --------------------------------- |
| ICMP Flood      | Suspicious Network Volume         |
| Port Scanning   | Network Reconnaissance / Scanning |
| SSH Brute Force | Brute Force Attempt               |

---

## Attack Simulation

### ICMP Flood Detection

```bash
sudo hping3 --icmp --flood <TARGET_IP>
```

### Port Scanning Detection

```bash
nmap -p- <TARGET_IP>
```

### SSH Brute Force Detection

```bash
hydra -l root -P /usr/share/wordlists/rockyou.txt ssh://<TARGET_IP>
```

---

## Sample Alert

```json
{
  "alert_id": "SOC-12345678",
  "alert_type": "Brute Force Attempt",
  "indicator_type": "ip",
  "indicator_value": "192.168.1.20",
  "destination_ip": "192.168.1.8",
  "evidence": {
    "packet_count": 150,
    "time_window_seconds": 60
  }
}
```

---

## Sample AI Analysis

```json
{
  "threat_classification": "Brute Force Attempt",
  "risk_score": 85,
  "risk_level": "Critical",
  "confidence_level": "High",
  "mitre_mapping": {
    "technique_id": "T1110",
    "technique_name": "Brute Force"
  }
}
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/ai-soc-analyst-agent.git

cd ai-soc-analyst-agent
```

### Install Dependencies

```bash
sudo apt update

sudo apt install tshark -y

pip3 install requests
```

---
 ## Screenshots

### Wazuh Dashboard
![Wazuh Dashboard](screenshots/wazuh1.jpg)

### Active Agents
![Active Agents](screenshots/wazuh2.jpg)

### Security Alerts
![Security Alerts](screenshots/wazuh3.jpg)

---

## Project Workflow

1. Capture network traffic using Tshark.
2. Convert captured packets into CSV format.
3. Analyze traffic patterns and security events.
4. Detect attacks based on predefined thresholds.
5. Generate structured security alerts.
6. Send alerts to Airia AI.
7. Receive AI-generated threat analysis and response recommendations.

---

## Learning Outcomes

* Network Traffic Analysis
* Security Monitoring
* SOC Operations
* Threat Detection
* Incident Response
* MITRE ATT&CK Framework
* AI-Assisted Security Analysis
* Packet Capture and Inspection
* Cybersecurity Automation

---

## Author

Parthiv Lalakiya

Cybersecurity & SOC Analyst Enthusiast
