
## ✅ Kali Linux Installation & VirtualBox Setup Summary

### 1. Downloaded Kali Linux VirtualBox Image

I visited the official Kali Linux website at [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/), scrolled down to the **“Virtual Machines”** section, and downloaded the Kali Linux VirtualBox.

---

### 2. Extracted Kali Image Using 7-Zip

After the download, I used **7-Zip** (I had previously downloaded and installed 7-Zip from https://www.7-zip.org) to extract the file by right-clicking it and choosing either **Extract Here** or **Extract to folder**. The extracted folder contained:

* A `.vbox` file (VirtualBox configuration)
* A `.vdi` file (virtual hard disk)
  <img width="800" height="406" alt="Screenshot 2025-07-22 011046" src="https://github.com/user-attachments/assets/cd4d7487-02fe-4ff6-8d3c-50513e31a72d" />


This meant I didn’t have to install Kali manually via ISO—it was a pre-configured virtual machine.

---

### 3. Installed VirtualBox (Faced Errors & Fixed Them)

I then downloaded and attempted to install **Oracle VirtualBox** from its [official site](https://www.virtualbox.org/). During installation, I encountered an error saying:

> “Microsoft Visual C++ 2015 or later is required”
<img width="800" height="406" alt="Screenshot 2025-07-22 014649" src="https://github.com/user-attachments/assets/c171e503-fae6-4f30-827f-a21ba9bfef01" />


At first, I installed the **Microsoft Visual C++ 2013 Redistributable**, but it did not work with VirtualBox. I realized it was outdated and incompatible.

To fix this, I downloaded and installed the correct **Microsoft Visual C++ 2015–2022 Redistributable (x64)**. Once installed, the VirtualBox setup ran successfully.

---

### 4. Imported Kali Linux into VirtualBox

After launching VirtualBox, I clicked **“Add”**, navigated to the extracted folder, and selected the `.vbox` file. The Kali virtual machine then appeared in the VirtualBox Manager with its configuration details like RAM and disk size.

---

### 5. Booted Up Kali VM

I started the Kali VM from the VirtualBox interface. The status showed as **Running**, confirming that the virtual machine was successfully booted. After a short wait, Kali’s desktop interface appeared.
<img width="800" height="406" alt="Screenshot 2025-07-22 013335" src="https://github.com/user-attachments/assets/8e10983c-788a-4ad3-85d0-b0bf6a93a7ad" />


---

### 6. Attempted Shared Folder Setup

I tried to set up a shared folder between my Windows system and the Kali VM by choosing a folder on my desktop. I enabled both **Auto-mount** and **Make Permanent** options.

However, the **OK** button was not clickable. This was because the virtual machine was already running. I learned that shared folder settings in VirtualBox can only be changed when the VM is powered off.

---
