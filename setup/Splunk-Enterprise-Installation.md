# Splunk Enterprise Installation

## Objective

Install Splunk Enterprise on the Windows 11 host machine to collect, search, and analyze security logs.

---

## Purpose

Splunk Enterprise acts as the Security Information and Event Management (SIEM) platform.

It is responsible for:

- Collecting logs
- Indexing events
- Searching logs
- Creating dashboards
- Performing investigations

---

## Installation Steps

### Step 1

Download Splunk Enterprise.

### Step 2

Run the installer as Administrator.

### Step 3

Create an administrator account.

### Step 4

Launch Splunk.

Default Web Interface

```
http://localhost:8000
```

---

## Initial Configuration

### Enable Receiving Port

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

## Verification

- Splunk starts successfully
- Web interface loads
- Administrator login works
- TCP Port 9997 is enabled

---

## Troubleshooting

### Splunk Service Won't Start

Restart the service.

### Cannot Access Web Interface

Verify that port 8000 is not blocked by the firewall.

### Universal Forwarder Cannot Connect

Verify TCP Port 9997 is enabled.

---

## Result

Splunk Enterprise is successfully configured to receive logs from the Universal Forwarder.
