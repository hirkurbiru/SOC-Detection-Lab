# Windows 11 Host Configuration

## Objective

Configure the Windows 11 host machine to support the SOC Detection Lab.

---

## System Information

| Component | Value |
|----------|-------|
| Operating System | Windows 11 |
| Role | Host Machine |
| Main Software | Splunk Enterprise, VirtualBox |

---

## Host Responsibilities

The Windows 11 host is responsible for:

- Running Splunk Enterprise
- Hosting VirtualBox
- Running Windows 10 VM
- Running Kali Linux VM
- Receiving logs from the Universal Forwarder

---

## Configuration Steps

### Step 1 – Install Windows Updates

Ensure Windows is fully updated before installing software.

---

### Step 2 – Enable Virtualization

Verify Intel VT-x or AMD-V is enabled in BIOS/UEFI.

---

### Step 3 – Install VirtualBox

Install Oracle VirtualBox.

---

### Step 4 – Install Splunk Enterprise

Install Splunk Enterprise on the host machine.

---

### Step 5 – Configure Receiving Port

Enable TCP Port **9997** for receiving logs from the Universal Forwarder.

---

### Step 6 – Verify Connectivity

Confirm the Windows 10 virtual machine can communicate with the host using:

```powershell
ping <Host-IP>
```

---

## Verification Checklist

- Windows updated
- Virtualization enabled
- VirtualBox installed
- Splunk Enterprise installed
- Receiving port enabled
- VM connectivity verified

---

## Troubleshooting

### Problem

Virtual machine cannot reach the host.

**Possible Causes**

- Windows Firewall
- Incorrect network adapter
- IP address changed
- Wrong forwarding configuration

---

## Lessons Learned

During this project, the host IP address changed due to DHCP. This caused the Splunk Universal Forwarder to stop forwarding logs until the forwarding server configuration was updated.
