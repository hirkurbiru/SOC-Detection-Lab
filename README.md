# 🛡️ SOC Detection Lab

A complete Security Operations Center (SOC) Home Lab built using **Splunk Enterprise**, **Sysmon**, **Windows Event Logs**, **VirtualBox**, **Windows 10**, and **Kali Linux**.

This project demonstrates how to build a SOC lab from scratch, collect and analyze Windows logs, simulate attacks, investigate security events, and create detections using Splunk.

---

## 📌 Project Overview

The purpose of this lab is to gain practical experience in:

- Windows Security Monitoring
- Splunk Log Analysis
- Sysmon Event Monitoring
- Attack Simulation
- Incident Investigation
- Detection Engineering
- Blue Team Operations

---

## 🎯 Objectives

- Build a functional SOC home lab
- Configure centralized log collection
- Monitor Windows Event Logs
- Simulate attacker activities
- Investigate security events
- Create Splunk searches and dashboards
- Learn SOC analyst workflows

---

## 🖥️ Lab Architecture

```
                    Internet
                        │
                  Home Router
                        │
                Windows 11 Host
              (Splunk Enterprise)
                        │
        ┌───────────────┴───────────────┐
        │                               │
 Windows 10 VM                   Kali Linux VM
(Sysmon + Universal             (Attack Machine)
    Forwarder)
```

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Windows 11 | Host Machine |
| Windows 10 | Target Machine |
| Kali Linux | Attack Simulation |
| VirtualBox | Virtualization |
| Splunk Enterprise | SIEM Platform |
| Splunk Universal Forwarder | Log Collection |
| Sysmon | Advanced Event Logging |
| Windows Event Viewer | Security Logs |
| PowerShell | Administration & Investigation |

---

## 📂 Repository Structure

```
SOC-Detection-Lab/
│
├── docs/
├── setup/
├── architecture/
├── investigations/
├── detections/
├── dashboards/
├── screenshots/
├── scripts/
└── README.md
```

---

## 🔍 Investigations Completed

- Failed Login Investigation (Event ID 4625)
- Successful Login Investigation (Event ID 4624)
- Process Creation Monitoring
- File Creation Monitoring
- PowerShell Activity Investigation

---

## 📊 Skills Demonstrated

- Windows Administration
- Splunk Search Processing Language (SPL)
- Windows Event Analysis
- Sysmon Configuration
- Security Log Investigation
- Detection Engineering
- MITRE ATT&CK Mapping
- Incident Response
- Blue Team Operations

---

## 🚀 Future Improvements

- Active Directory Integration
- Sysmon Custom Configuration
- Sigma Rules
- Splunk Dashboards
- Splunk Alerts
- Brute Force Detection
- RDP Monitoring
- Malware Simulation
- Threat Hunting Scenarios

---

## 📜 License

This project is licensed under the MIT License.
