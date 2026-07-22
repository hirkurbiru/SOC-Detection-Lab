# SOC Lab Architecture

## Objective

This document explains the overall architecture of the SOC Detection Lab.

---

## Components

### Windows 11 Host

Role:

- Hosts VirtualBox
- Runs Splunk Enterprise
- Receives forwarded logs

---

### Windows 10 VM

Role:

- Target endpoint
- Generates Windows Events
- Runs Sysmon
- Runs Splunk Universal Forwarder

---

### Kali Linux VM

Role:

- Attack machine
- Generates attack activity
- Performs reconnaissance

---

### Splunk Enterprise

Role:

- Collects logs
- Indexes events
- Searches events
- Creates dashboards

---

### Sysmon

Role:

Provides enhanced endpoint telemetry.

---

### Universal Forwarder

Role:

Transfers Windows Event Logs securely to Splunk Enterprise.

---

## Architecture Summary

The Windows 10 endpoint generates security events. Sysmon enhances these logs, and the Universal Forwarder sends them to Splunk Enterprise. Kali Linux is used to simulate attacker behavior for testing and investigations.
