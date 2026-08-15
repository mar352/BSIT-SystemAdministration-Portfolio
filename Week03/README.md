# Week 03: Virtual Machine Setup and Boot Process Documentation

## Project Overview
This repository documents the installation, configuration, and verification of a Linux virtual machine environment, alongside a technical breakdown of system firmware architectures (BIOS vs. UEFI) and boot process execution sequences. The goal is to establish a working virtualized system administration environment and analyze hardware-to-OS execution paths.

---

## Learning Objectives
* Successfully configure and deploy a virtualized Operating System (OS) using VirtualBox/VMware.
* Understand system firmware execution paths, specifically comparing Legacy BIOS (MBR) and UEFI (GPT/ESP).
* Map out the step-by-step System Boot Sequence from hardware POST to user shell invocation.
* Document system configurations, technical challenges, and verification procedures for system administration standards.

---

## Virtual Machine Specifications

| Parameter | Specification |
| :--- | :--- |
| **Hypervisor** | Oracle VM VirtualBox / VMware Workstation |
| **Guest OS** | Ubuntu Desktop 22.04 LTS / Debian 12 |
| **Base Memory (RAM)** | 4096 MB (4 GB) |
| **Processors (vCPU)** | 2 Cores |
| **Virtual Disk Size** | 25 GB (Dynamically Allocated) |
| **Storage Controller** | VDI / SATA |
| **Graphics Controller** | VMSVGA (3D Acceleration Enabled) |
| **Network Adapter** | NAT / Bridged Adapter |

---

## Installation Summary
1. **Hypervisor Setup:** Installed and verified VirtualBox on the host machine.
2. **Media Mounting:** Downloaded the official ISO image and mounted it to the VM virtual optical drive.
3. **Partitioning:** Allocated disk space using standard GUID Partition Table (GPT) layout with an EFI System Partition (ESP) and root `/` filesystem.
4. **User & System Configuration:** Configured system hostname, root credentials, administrative user accounts, and timezone settings.
5. **OS Deployment:** Executed base package installation, kernel setup, and bootloader configuration.

---

## Configuration Summary
* **Package Updates:** Executed `sudo apt update && sudo apt upgrade -y` to update repository packages.
* **Guest Additions / Tools:** Installed hypervisor integrations (`virtualbox-guest-utils` / `open-vm-tools`) for display scaling and shared clipboard support.
* **Network Settings:** Configured static/DHCP interface parameters and verified internet connectivity via `ping`.
* **Administrative Privileges:** Added the primary user to the `sudo` group for administrative access.

---

## Verification Results
System deployment was validated through the following terminal verifications:

* **Kernel & Architecture Check:**
  ```bash
  uname -r
  # Output: Verified active Linux Kernel version (6.x.x)