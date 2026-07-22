# Sysmon Installation

## Objective

Install Microsoft Sysmon on the Windows 10 virtual machine to generate detailed system activity logs for security monitoring and investigation.

---

# What is Sysmon?

System Monitor (Sysmon) is a Microsoft Sysinternals tool that records detailed information about system activity.

Unlike the default Windows Event Logs, Sysmon provides enhanced visibility into:

- Process Creation
- Network Connections
- File Creation
- Driver Loading
- Registry Changes
- Image Loading
- DNS Queries
- Process Termination

These events help security analysts detect malicious activity and investigate incidents.

---

# Lab Environment

| Component | Value |
|-----------|-------|
| Operating System | Windows 10 Home |
| Tool | Sysmon |
| Log Source | Microsoft-Windows-Sysmon/Operational |
| SIEM | Splunk Enterprise |

---

# Installation Steps

## Step 1

Download Sysmon from the Microsoft Sysinternals website.

---

## Step 2

Extract the downloaded ZIP file.

Example:

```
C:\Tools\Sysmon\
```

---

## Step 3

Open Command Prompt as Administrator.

---

## Step 4

Install Sysmon.

Example:

```cmd
sysmon64.exe -accepteula -i sysmonconfig.xml
```

---

# Verify Installation

Open Event Viewer.

Navigate to:

```
Applications and Services Logs

↓

Microsoft

↓

Windows

↓

Sysmon

↓

Operational
```

You should see Sysmon events being generated.

---

# Important Event IDs

| Event ID | Description |
|-----------|-------------|
| 1 | Process Creation |
| 2 | File Creation Time Changed |
| 3 | Network Connection |
| 5 | Process Terminated |
| 7 | Image Loaded |
| 8 | Create Remote Thread |
| 11 | File Created |
| 12 | Registry Object Created |
| 13 | Registry Value Set |
| 22 | DNS Query |

---

# Events Used in This Project

During this lab the following Sysmon events were investigated:

- Event ID 1 (Process Creation)
- Event ID 11 (File Creation)

These events were forwarded to Splunk and analyzed using SPL queries.

---

# Splunk Verification

Example SPL:

```spl
index=* sourcetype="XmlWinEventLog:Microsoft-Windows-Sysmon/Operational"
```

Expected Result:

Sysmon events should appear in Splunk.

---

# Troubleshooting

## No Sysmon Events

Possible Causes

- Sysmon service not installed
- Incorrect configuration file
- Universal Forwarder not collecting Sysmon logs

---

## Events Not Visible in Splunk

Verify:

- Sysmon Operational Log exists
- Universal Forwarder inputs are configured
- Splunk receiving port (9997) is enabled
- Forwarder service is running

---

# Lessons Learned

Sysmon provided detailed telemetry that was not available in the default Windows Event Logs. It enabled the investigation of process creation, file creation, and PowerShell activity, significantly improving visibility into system behavior.

---

# Skills Demonstrated

- Sysmon Installation
- Windows Event Logging
- Event ID Analysis
- Splunk Log Collection
- Security Monitoring
