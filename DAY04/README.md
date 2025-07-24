### Basic File & Directory Operations

| Command | Example                  | Purpose                       |
| ------- | ------------------------ | ----------------------------- |
| `ls`    | `ls`                     | Lists files and directories   |
| `cd`    | `cd /var/log`            | Changes the current directory |
| `pwd`   | `pwd`                    | Shows current directory path  |
| `mkdir` | `mkdir test_dir`         | Creates a new directory       |
| `rmdir` | `rmdir test_dir`         | Deletes an empty directory    |
| `touch` | `touch file.txt`         | Creates a new empty file      |
| `rm`    | `rm file.txt`            | Deletes a file                |
| `cp`    | `cp file.txt /tmp/`      | Copies a file                 |
| `mv`    | `mv file.txt backup.txt` | Moves or renames a file       |

### File Permissions & Ownership

| Command | Example                    | Purpose                  |
| ------- | -------------------------- | ------------------------ |
| `chmod` | `chmod 755 script.sh`      | Changes file permissions |
| `chown` | `chown user:user file.txt` | Changes file ownership   |

### Help & Information

| Command | Example              | Purpose                             |
| ------- | -------------------- | ----------------------------------- |
| `man`   | `man ls`             | Opens the manual page for a command |
| `echo`  | `echo "Hello World"` | Prints a message to the terminal    |
| `cat`   | `cat file.txt`       | Displays file content               |

### File Editing

| Command       | Example         | Purpose                      |
| ------------- | --------------- | ---------------------------- |
| `nano` / `vi` | `nano file.txt` | Edits a file in the terminal |

### System Monitoring & Processes

| Command | Example     | Purpose                     |
| ------- | ----------- | --------------------------- |
| `ps`    | `ps aux`    | Lists active processes      |
| `kill`  | `kill 1234` | Terminates a process by PID |
| `top`   | `top`       | Real-time system monitoring |

### Disk & Usage Monitoring

| Command | Example        | Purpose                |
| ------- | -------------- | ---------------------- |
| `df`    | `df -h`        | Shows disk space usage |
| `du`    | `du -sh /etc/` | Shows directory size   |

### Other Commands

| Command | Example | Purpose                    |
| ------- | ------- | -------------------------- |
| `clear` | `clear` | Clears the terminal screen |
| `exit`  | `exit`  | Logs out from the terminal |

---

In **cybersecurity**, a **sandbox** is a **safe, isolated testing environment** used to run and analyze suspicious files, programs, or code without risking harm to the actual system or network.

### **Key Features of a Sandbox:**

* **Isolated:** Runs separately from your main system.
* **Safe Testing:** Lets you open unknown files or malware to see what they do.
* **Observation:** Allows monitoring of behavior like file changes, registry edits, or network activity.
* **No Real Damage:** Even if the program is malicious, it can’t affect the host machine.

### **Common Uses in Cybersecurity:**

1. **Malware analysis** – See how a virus behaves.
2. **Testing suspicious email attachments** – Prevent phishing attacks.
3. **Software testing** – Check how new applications behave.
4. **Digital forensics** – Analyze threats post-attack.

### **Real-World Examples:**

* **Windows Sandbox** – A built-in tool in Windows for safe app testing.
* **Firejail (Linux)** – Limits program access to system resources.
* **Cloud Sandboxes** – Used by antivirus companies to scan files in real-time.

---
In cybersecurity (and many other fields), two main kinds of analysis are often referred to as:

**1.Static Analysis**

Definition: Examining code, files, or software without running it.

Purpose: To find vulnerabilities, backdoors, or malicious code.

Used in: Malware analysis, code review, vulnerability detection.

Example:Analyzing a malware's code or file structure without executing it.

Tools: IDA Pro, PEStudio, strings command.

**2.Dynamic Analysis**

Definition: Observing the behavior of a program while it’s running, often in a sandbox.

Purpose: To detect real-time actions like system changes, file drops, or network calls.

Used in: Malware behavior analysis, intrusion detection.

Example:Running a suspicious file in a sandbox to watch what it does.

Tools: Cuckoo Sandbox, Process Monitor, Wireshark.

----
**Microsoft Advanced Threat Analytics (ATA)** is an on-premises platform that helps identify:

1.Malicious attacks
2.Suspicious user behavior
3.Known security issues in real time

**How It Works:**

1.ATA monitors network traffic and analyzes activities from domain controllers, using:
      i)Behavioral analytics
      ii)Security event logs
      iii)Deep packet inspection
      
2.It then alerts security teams about potential threats like:
           a. Pass-the-Ticket or Pass-the-Hash attacks
           b. Privilege escalation
           c. Lateral movement
           d. Reconnaissance attempts
           e. Brute-force attacks





