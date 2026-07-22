# Splunk Universal Forwarder Installation

## Objective

Install and configure the Splunk Universal Forwarder on the Windows 10 virtual machine to send Windows Event Logs and Sysmon logs to Splunk Enterprise running on the Windows 11 host.

---

## Lab Environment

| Component | Details |
|----------|---------|
| Host Machine | Windows 11 |
| Target Machine | Windows 10 Home |
| SIEM | Splunk Enterprise |
| Log Collector | Splunk Universal Forwarder |
| Port | 9997 |

---

## What is the Universal Forwarder?

The Splunk Universal Forwarder (UF) is a lightweight agent that collects logs from a machine and securely forwards them to a Splunk Enterprise server.

In this lab, the UF sends:

- Windows Security Logs
- System Logs
- Application Logs
- Sysmon Logs
- PowerShell Logs

---

## Installation Steps

### Step 1: Download

Download the Universal Forwarder from the official Splunk website.

---

### Step 2: Install

Run the installer as an Administrator.

Select:

- Universal Forwarder
- Local System Account
- Default Installation Directory

---

### Step 3: Configure the Receiving Server

During installation, specify the Splunk Enterprise server.

Example:

```
Host IP: <Windows 11 Host IP>
Port: 9997
```

---

### Step 4: Start the Service

Open **Services** and verify that:

```
SplunkForwarder
```

is in the **Running** state.

---

## Verify Forwarding

Open Command Prompt as Administrator:

```cmd
cd "C:\Program Files\SplunkUniversalForwarder\bin"

splunk list forward-server
```

Expected output:

```
Active forwards:
    <Host-IP>:9997
```

---

## Splunk Configuration

On the Windows 11 host:

Settings

↓

Forwarding and Receiving

↓

Configure Receiving

↓

Enable TCP Port

```
9997
```

---

## Troubleshooting

### Problem 1

No logs appeared in Splunk.

**Cause**

The Universal Forwarder was configured with an old host IP address after the host received a new IP from DHCP.

**Solution**

Remove the old forwarding server:

```cmd
splunk remove forward-server <Old-IP>:9997
```

Add the new forwarding server:

```cmd
splunk add forward-server <New-IP>:9997
```

Restart the service:

```cmd
net stop splunkforwarder
net start splunkforwarder
```

---

### Problem 2

Command Output

```
Active forwards:
None
```

**Cause**

The Universal Forwarder could not communicate with Splunk Enterprise.

**Checks Performed**

- Verified Splunk Enterprise was running
- Verified TCP port 9997 was enabled
- Verified Windows Firewall settings
- Verified network connectivity
- Updated the host IP address

---

## Verification

- Universal Forwarder service is running
- `splunk list forward-server` shows an active connection
- Windows Event Logs appear in Splunk
- Sysmon events appear in Splunk
- New events are searchable

---

## Lessons Learned

During this project, the Windows 11 host received a different IP address through DHCP. Because the Universal Forwarder still pointed to the old IP address, log forwarding stopped.

Updating the forwarding server configuration restored log collection successfully.

---

## Skills Demonstrated

- Splunk Universal Forwarder Installation
- Windows Log Forwarding
- Network Troubleshooting
- Splunk Administration
- Windows Services
- Command Line Administration
