# Software Requirements

## Overview

This document lists all software used to build the SOC Detection Lab and explains the purpose of each component.

---

## Software List

| Software | Purpose |
|----------|---------|
| Windows 11 | Host Operating System |
| Oracle VirtualBox | Virtualization Platform |
| Windows 10 Home | Target Machine |
| Kali Linux | Attack Machine |
| Splunk Enterprise | SIEM Platform |
| Splunk Universal Forwarder | Log Collection |
| Sysmon | Advanced Windows Logging |
| PowerShell | Administration & Investigation |
| Windows Defender | Endpoint Protection |

---

## Software Details

### Windows 11

**Purpose**

- Host Operating System
- Runs Splunk Enterprise
- Hosts the virtual machines

---

### Oracle VirtualBox

**Purpose**

- Create virtual machines
- Run Windows 10 and Kali Linux simultaneously
- Manage virtual networking

---

### Windows 10 Home

**Purpose**

- Simulate an enterprise endpoint
- Generate Windows Security Events
- Install Sysmon
- Install Universal Forwarder

---

### Kali Linux

**Purpose**

- Perform attack simulations
- Network scanning
- Security testing

---

### Splunk Enterprise

**Purpose**

- Collect logs
- Search events
- Build dashboards
- Perform investigations

Default Port

8000 (Web Interface)

Receiving Port

9997

---

### Splunk Universal Forwarder

**Purpose**

- Forward Windows Event Logs
- Send Sysmon logs
- Send Security logs to Splunk

---

### Sysmon

**Purpose**

Sysmon provides detailed Windows telemetry such as:

- Process Creation
- Network Connections
- File Creation
- Registry Changes
- Driver Loading
- DNS Queries

---

### Windows Defender

**Purpose**

- Endpoint protection
- Malware detection
- Security event generation

---

## Notes

All software versions should be kept up to date whenever possible. Ensure compatibility between Splunk Enterprise, the Universal Forwarder, and the Sysmon configuration used in the lab.
