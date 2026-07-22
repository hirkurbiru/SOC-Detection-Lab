# Windows 10 Virtual Machine Installation

## Objective

Create and configure the Windows 10 virtual machine used as the target endpoint in the SOC Detection Lab.

---

## Purpose

The Windows 10 VM simulates an enterprise workstation.

It generates:

- Windows Security Events
- Sysmon Events
- PowerShell Logs
- Authentication Logs
- File Activity
- Process Creation Events

---

## Virtual Machine Configuration

| Setting | Value |
|---------|------|
| Operating System | Windows 10 Home |
| Memory | 4 GB |
| CPU | 2 Cores |
| Disk | 50 GB |
| Network | Bridged Adapter |

---

## Installation Steps

1. Create a new virtual machine in VirtualBox.
2. Attach the Windows 10 ISO.
3. Complete the Windows installation.
4. Install Guest Additions (optional).
5. Configure networking.
6. Install Windows updates.

---

## Post Installation

Install:

- Sysmon
- Splunk Universal Forwarder
- Windows Defender Updates

---

## Verification

- Windows boots successfully.
- Internet connectivity is available.
- Host machine is reachable.
- Splunk Universal Forwarder installed.
- Sysmon installed.

---

## Troubleshooting

| Issue | Solution |
|--------|----------|
| No Internet | Check Bridged Adapter settings |
| Cannot ping host | Verify firewall and network configuration |
| Logs not forwarding | Check Universal Forwarder service |
