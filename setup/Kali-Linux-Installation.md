# Kali Linux Installation

## Objective

Install Kali Linux as the attacker machine used to simulate attacks against the Windows 10 virtual machine.

---

## Purpose

Kali Linux is used for:

- Network Scanning
- Port Scanning
- Attack Simulation
- Security Testing
- Generating logs for investigation

---

## Virtual Machine Configuration

| Setting | Value |
|----------|-------|
| Operating System | Kali Linux |
| RAM | 2 GB |
| CPU | 2 Cores |
| Disk | 30 GB |
| Network | Bridged Adapter |

---

## Installation Steps

### Step 1

Create a new VirtualBox virtual machine.

### Step 2

Attach the Kali Linux ISO.

### Step 3

Complete the installation.

### Step 4

Update the operating system.

```bash
sudo apt update
sudo apt upgrade -y
```

### Step 5

Verify the IP address.

```bash
ip a
```

### Step 6

Verify connectivity.

```bash
ping <Windows10-IP>
```

---

## Verification Checklist

- Kali boots successfully
- Internet access works
- Can ping Windows 10
- Can ping Host Machine

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| No Internet | Verify Bridged Adapter |
| Wrong IP Address | Renew DHCP lease |
| Cannot Ping Windows | Check Windows Firewall |

---

## Result

Kali Linux is ready for attack simulation and security testing.
