# Network Topology

## Objective

Explain communication between all machines in the SOC Lab.

---

## Machines

| Machine | Purpose |
|----------|---------|
| Windows 11 | Splunk Server |
| Windows 10 | Endpoint |
| Kali Linux | Attacker |

---

## Communication

Kali Linux

↓

Windows 10

↓

Universal Forwarder

↓

Splunk Enterprise

---

## Network Mode

VirtualBox Bridged Adapter

---

## Ports

| Port | Purpose |
|------|---------|
|8000|Splunk Web|
|9997|Splunk Forwarding|

---

## Verification

- Ping Host
- Ping Windows VM
- Verify Forwarder Connection
