# Lab Verification

## Objective

Verify that all components of the SOC Detection Lab are installed, configured, and functioning correctly.

---

# Verification Checklist

| Component | Status |
|-----------|--------|
| Windows 11 Host | ✅ |
| VirtualBox | ✅ |
| Windows 10 VM | ✅ |
| Kali Linux VM | ✅ |
| Splunk Enterprise | ✅ |
| Universal Forwarder | ✅ |
| Sysmon | ✅ |
| Network Connectivity | ✅ |
| Event Forwarding | ✅ |

---

# Splunk Verification

Search:

```spl
index=*
```

Expected Result:

Events from Windows 10 should appear.

---

# Sysmon Verification

Search:

```spl
sourcetype="XmlWinEventLog:Microsoft-Windows-Sysmon/Operational"
```

Expected Result:

Sysmon events are displayed.

---

# Security Log Verification

Search:

```spl
EventCode=4624 OR EventCode=4625
```

Expected Result:

Successful and failed login events appear.

---

# Process Creation Verification

Search:

```spl
EventCode=1
```

Expected Result:

Sysmon Process Creation events appear.

---

# File Creation Verification

Search:

```spl
EventCode=11
```

Expected Result:

Sysmon File Creation events appear.

---

# PowerShell Verification

Execute a PowerShell command on Windows 10 and verify that related events are collected in Splunk.

---

# Result

The SOC Detection Lab is fully operational and ready for attack simulation, log analysis, threat hunting, and incident investigation.
