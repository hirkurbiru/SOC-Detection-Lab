# SOC Investigations

This directory contains the security investigations completed during the SOC Detection Lab project.

Each investigation demonstrates how Windows events were collected using Sysmon and Windows Event Logs, forwarded to Splunk Enterprise, and analyzed using SPL (Search Processing Language).

## Objectives

- Investigate Windows security events
- Analyze Sysmon logs
- Practice incident investigation
- Develop detection engineering skills
- Understand Windows Event IDs
- Improve Splunk search skills

## Completed Investigations

| No. | Investigation | Status |
|-----|---------------|--------|
| 01 | Process Creation | ✅ |
| 02 | Failed Login | ✅ |
| 03 | Successful Login | ✅ |
| 04 | File Creation | ✅ |
| 05 | PowerShell Activity | ✅ |

## Investigation Summary

### Process Creation

- Event ID: Sysmon Event ID 1
- Objective: Monitor newly created processes.

### Failed Login

- Event ID: 4625
- Objective: Detect failed authentication attempts.

### Successful Login

- Event ID: 4624
- Objective: Monitor successful user logins.

### File Creation

- Event ID: Sysmon Event ID 11
- Objective: Detect newly created files.

### PowerShell Activity

- Event Source: Sysmon & PowerShell
- Objective: Investigate PowerShell command execution.

## Skills Demonstrated

- Splunk SPL
- Windows Event Analysis
- Sysmon Investigation
- Incident Response
- Detection Engineering
- Blue Team Operations
- Windows Administration

## Future Investigations

The repository will continue to grow with additional investigations, including:

- Brute Force Detection
- RDP Login Detection
- Registry Monitoring
- Network Connection Monitoring
- Scheduled Task Detection
- Windows Defender Alerts
- Service Creation Detection
- Active Directory Investigations
