# Hardware Requirements

## Overview

Before building the SOC Detection Lab, ensure your computer meets the minimum hardware requirements. Since multiple virtual machines will run simultaneously, sufficient CPU, memory, and storage are essential.

---

## Minimum Requirements

| Component | Requirement |
|-----------|-------------|
| Processor | Intel Core i5 (4 cores) or AMD Ryzen 5 |
| RAM | 8 GB |
| Storage | 80 GB Free Space |
| Operating System | Windows 10/11 64-bit |
| Virtualization | Intel VT-x / AMD-V Enabled |

---

## Recommended Requirements

| Component | Recommendation |
|-----------|----------------|
| Processor | Intel Core i7 (6+ cores) or AMD Ryzen 7 |
| RAM | 16 GB or more |
| Storage | 250 GB SSD |
| Operating System | Windows 11 |
| Internet | Stable Broadband Connection |

---

## Virtual Machines Used

### Windows 10 VM

Purpose:
- Target machine
- Generate Windows Event Logs
- Install Sysmon
- Install Splunk Universal Forwarder

Recommended Resources:

- CPU: 2 Cores
- RAM: 4 GB
- Disk: 50 GB

---

### Kali Linux VM

Purpose:
- Attack machine
- Security testing
- Network scanning
- Simulate attacks

Recommended Resources:

- CPU: 2 Cores
- RAM: 2–4 GB
- Disk: 30 GB

---

### Host Machine

Purpose:
- Run VirtualBox
- Host Splunk Enterprise
- Receive and analyze logs

Recommended Resources:

- CPU: 4+ Cores
- RAM: 8 GB available for host
- SSD storage preferred

---

## Why These Requirements?

Running Windows 10, Kali Linux, VirtualBox, and Splunk Enterprise simultaneously requires significant system resources. Insufficient RAM or CPU may cause virtual machines to become slow or unresponsive.

Using an SSD instead of an HDD significantly improves VM performance and reduces boot times.

---

## Notes

- Enable virtualization (Intel VT-x or AMD-V) in the BIOS/UEFI before creating virtual machines.
- Keep at least 20 GB of free disk space for logs, snapshots, and future investigations.
- A stable internet connection is required to download software updates and installation packages.
