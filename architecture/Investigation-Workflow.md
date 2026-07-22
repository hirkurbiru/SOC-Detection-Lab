# Log Flow

## Objective

Explain how logs travel through the lab.

---

## Flow

Windows Event

↓

Sysmon Event

↓

Universal Forwarder

↓

TCP Port 9997

↓

Splunk Enterprise

↓

Indexer

↓

Search Head

↓

Dashboard

↓

SOC Analyst

---

## Logs Collected

- Security
- System
- Application
- Sysmon
- PowerShell

---

## Result

Logs become searchable inside Splunk.
