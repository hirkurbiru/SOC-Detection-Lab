# Network Configuration

## Objective

Configure networking between the Windows 11 host, Windows 10 VM, and Kali Linux VM to enable communication and log forwarding.

---

# Network Topology

```
                    Internet
                         │
                    Home Router
                         │
                  Windows 11 Host
               (Splunk Enterprise)
                         │
          ┌──────────────┴──────────────┐
          │                             │
     Windows 10 VM               Kali Linux VM
(Sysmon + Universal            (Attack Machine)
     Forwarder)
```

---

# VirtualBox Network Mode

Network Adapter:

- Bridged Adapter

Purpose:

- Allow virtual machines to obtain IP addresses from the router.
- Enable communication between the host and virtual machines.

---

# Lab Components

| Machine | Purpose |
|----------|---------|
| Windows 11 | Host & Splunk Server |
| Windows 10 | Target Machine |
| Kali Linux | Attacker Machine |

---

# Communication Flow

Windows 10

↓

Universal Forwarder

↓

TCP Port 9997

↓

Splunk Enterprise

↓

Search & Dashboard

---

# Connectivity Tests

Verify communication using:

Windows:

```powershell
ping <Host-IP>
```

Kali:

```bash
ping <Windows10-IP>
```

---

# Ports Used

| Port | Service |
|------|---------|
| 8000 | Splunk Web |
| 9997 | Splunk Receiving |
| 3389 | Remote Desktop (Optional) |

---

# Problems Encountered

## Universal Forwarder Not Sending Logs

Reason:

The Windows 11 host IP changed because of DHCP.

Result:

Universal Forwarder continued sending logs to the old IP.

Solution:

Update the forwarding server with the new IP and restart the service.

---

# Verification

- Windows 10 can ping the host.
- Kali can ping Windows 10.
- Splunk receives new events.
- Universal Forwarder shows an active connection.
