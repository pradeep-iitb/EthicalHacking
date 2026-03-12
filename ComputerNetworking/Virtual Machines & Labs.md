# Configuring the Network of VM Labs 
## Side by Side Comparison

| Mode | Internet Access | Talk to Host | Talk to Other VMs | Visible on Network |
|---|---|---|---|---|
| **NAT** | ✅ | ❌ | ❌ | ❌ |
| **Bridged** | ✅ | ✅ | ✅ | ✅ |
| **Host-Only** | ❌ | ✅ | ❌ | ❌ |
| **Internal** | ❌ | ❌ | ✅ | ❌ |
| **NAT Network** | ✅ | ❌ | ✅ | ❌ |

---

## For Your Cybersecurity Labs Specifically

| Scenario | Best Mode |
|---|---|
| Just setting up Kali, installing tools | **NAT** |
| Kali attacking Metasploitable | **Internal Network** or **NAT Network** |
| Running a honeypot | **Host-Only** |
| Network scanning lab | **Bridged** |
| Multi-VM pentest lab with internet | **NAT Network** |

---

## What Happens Physically

When you install VirtualBox or VMware, it creates **virtual network adapters** on your laptop — you can actually see them:

- On Windows → `ipconfig` → you'll see `VirtualBox Host-Only Adapter`
- On Linux → `ip a` → you'll see `vboxnet0` or `vmnet1`

These are fake network cards your laptop creates to communicate with VMs.

