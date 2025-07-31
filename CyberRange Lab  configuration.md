# Getting Started with Kali Linux on Windows using VirtualBox

This guide will walk you through downloading, installing, extracting, and running **Kali Linux** in a **Windows 10/11** environment using **Oracle VirtualBox**. It has been structured specifically for cybersecurity and ethical hacking learners who want to create a secure, isolated lab setup.

---

## ☑ Prerequisites: Setup Virtualization Environment

### 1. Install VirtualBox

* Visit [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
* Choose **Windows hosts** if your system runs Windows 10 or 11
* Download the installer and run it

  * Locate the file in `Downloads`
  * Right-click and **Run as Administrator**
  * Follow the installer wizard: Click **Next**, **Install**, and **Finish**
  * A **reboot is recommended** after installation

### 2. Enable Windows Virtualization Features

* Open **Start Menu** → search for `Turn Windows features on or off`
* Enable the following checkboxes:

  * `Hyper-V`
  * `Virtual Machine Platform`
  * `Windows Hypervisor Platform`
  * `Windows Subsystem for Linux`
* Click **OK** and **Reboot** your system

---

## ☑ Install 7-Zip (for extracting .7z files)

### 1. Download 7-Zip

* Visit [https://www.7-zip.org/](https://www.7-zip.org/)
* Download the appropriate version for your system (64-bit recommended)

### 2. Install 7-Zip

* Locate the downloaded installer
* Right-click → **Run as Administrator**
* Click **Next**, **Install**, and **Finish**

---

## ☑ Download & Extract Kali Linux for VirtualBox

### 1. Download Kali Linux VM

* Go to [https://www.kali.org/get-kali/#kali-virtual-machines](https://www.kali.org/get-kali/#kali-virtual-machines)
* Choose the **VirtualBox Image** under "Kali Linux Virtual Machines"

  * Prefer the **standard release**, not the weekly build (avoid dev/debugging versions)

### 2. Extract the .7z File

* Locate the file: `kali-linux-2025.2-virtualbox-amd64.7z`
* Right-click → 7-Zip → **Extract Here**
* Wait for 2–5 minutes
* You will get a folder named: `kali-linux-2025.2-virtualbox-amd64`

This folder contains the **Kali VM image** and configuration for VirtualBox.

---

## ☑ Open Kali Linux in VirtualBox

### 1. Locate & Open VM

* Open the extracted folder
* Locate a file named `kali-linux-2025.2-virtualbox-amd64.vbox`
* Double-click this `.vbox` file

  * This action will auto-import the VM into **VirtualBox**

### 2. Verify VM is Loaded

* VirtualBox will display the Kali VM in the sidebar

---

## ☑ Configure Kali Linux VM (Safe + Optimized)

### Edit VM Settings:

* Right-click on the Kali VM → **Settings**

**System Settings:**

* Base Memory: **2048 MB** (2 GB RAM)
* Processor(s): **2 CPUs**

**Network:**

* Adapter 1: **NAT** (for internet access)

**Shared Folders (Optional):**

* Add shared folders between host and guest for easy file transfer

---

## ☑ Start Kali Linux

### 1. Power On the VM

* Click **Start** or double-click the VM name

### 2. Login Credentials

* Username: `kali`
* Password: `kali`

---

## ☑ First Things to Do After Boot

### 1. Update and Upgrade System

```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Reboot System

```bash
sudo reboot
```

### 3. (Optional) Change Password

```bash
sudo passwd
# Enter new password twice
```

### 4. Install a Better Terminal

The default terminal may be slow or unresponsive. Install **Terminator**:

```bash
sudo apt install -y terminator
```

---

## ☑ Summary Checklist

| Step                         | Status |
| ---------------------------- | ------ |
| VirtualBox Installed         | ☑      |
| Hypervisor Enabled           | ☑      |
| 7-Zip Installed              | ☑      |
| Kali VM Downloaded           | ☑      |
| Kali VM Extracted            | ☑      |
| Kali VM Opened in VirtualBox | ☑      |
| VM Configured (RAM/CPU/NAT)  | ☑      |
| Kali Updated & Ready         | ☑      |

---

## 📚 Additional Recommendations

* Always **update Kali** before starting new labs
* **Snapshot** the VM state after initial setup (optional but recommended)
* Keep a backup of the `.vbox` and `.vdi` files
* Avoid using Kali Linux VM for general browsing
* Use it strictly as a **sandbox** for ethical hacking practices

---

## 💼 Intended Audience

This document is tailored for **Cybersecurity & Ethical Hacking** students aiming to:

* Practice hands-on penetration testing
* Learn security tools in a virtual lab
* Build real-world ethical hacking experience

---

For any issues or improvements, raise a ticket or contact your course instructor.

---

**Author**: Vaishnavu C V
**Role**: Principal CyberSecurity Engineer, Mentor & Ethical Hacker
**Code Name**: `@hackwithvyshu`
