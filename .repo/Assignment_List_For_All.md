# Ethical Hacking Assignments - Semester 5, 2025

## Assignment Instructions

* **Duration**: 2 hours maximum
* **Report**: 1-page report per assignment
* **Repository**: Create a GitHub repository named `EH_sem5_2025_Notes`
* **Directory**: Submit all assignments in the `1st Assignment` directory
* **Deadline**: Submit by next Friday

---

## Student Assignments

### Assignment 1: TCP and UDP Port Discovery

* Use `nmap` to scan both TCP and UDP ports on `scanme.nmap.org`.
* Save the results and summarize open services.
* **Report**: Explain TCP vs UDP ports + screenshot of the scan.

### Assignment 2: Full Port Scan

* Use `nmap -p-` to scan all 65535 ports on `testphp.vulnweb.com`.
* **Script**: Save the command as a `.sh` file and automate output saving.

### Assignment 3: DNS and IP Discovery

* Use `nmap -sL` and `dig` to find IPs, DNS info of `zero.webappsecurity.com`.
* Create a flowchart: DNS resolution process.

### Assignment 4: Create Low-Privilege User

* In Kali VM, create a user `student01` with no sudo access.
* Use `adduser`, `usermod`, and confirm permissions.
* **Evidence**: Screenshot of commands + `/etc/passwd` snippet.

### Assignment 5: File Creation and Permission

* Create a file using `touch`. Change permission to `751`.
* Use `chmod`, `ls -l`, and explain octal notation.

### Assignment 6: What is Shodan?

* Visit [Shodan.io](https://shodan.io), search for `scanme.nmap.org`.
* Document what data is visible and its use for attackers and defenders.

### Assignment 7: Explain Core Network Terms

* Create a 1-page illustrated document:

  * NAT, ARP, MAC, IPv4, IPv6
  * One-line explanation and diagram each.

### Assignment 8: Directory Monitoring Bash Script

* Write a 15-line bash script to monitor changes in `/home/student/Downloads`.
* Log the change type (file created/deleted/modified).

### Assignment 9: Mini Port Scanner Script

* Write a bash script that:

  * Takes IP as input
  * Scans top 1000 ports
  * Saves results in `scan_<date>.log`

### Assignment 10: Linux AI Help Chat using Groq API

* Use Groq’s free API to create a CLI chatbot.
* Input: Any Linux command.
* Output: Easy explanation.
* **Limit**: ≤ 15 lines Python code.

### Assignment 11: Ncat Chat Terminal

* Create a script with 10 lines to simulate chat using `ncat`.
* Terminal A: Listener
* Terminal B: Connects and sends message

### Assignment 12: Serve a Directory using Python

* Use `python3 -m http.server 8080` in a directory.
* Screenshot server + browser result + terminal command.

### Assignment 13: VirusTotal API Usage

* Register for [VirusTotal](https://virustotal.com) API key.
* Use Python or bash with `curl` to check hash details of a test file.
* **Code limit**: 10-15 lines.

### Assignment 14: Sudo Usage Logging

* Create a Python/Bash script that monitors `/var/log/auth.log` every 30s.
* If `sudo` success/fail found, log username + time.

### Assignment 15: System Hack Timeline

* Pick any past real-life attack (e.g., Equifax breach).
* Document a 6-step timeline (initial access → data exfiltration).

### Assignment 16: Detect Service Version with Nmap

* Use `nmap -sV` on `testphp.vulnweb.com`.
* Summarize at least 3 detected services with versions and known CVEs.

### Assignment 17: Bash Script for Auto Ping and Log

* Create a script that:

  * Pings a domain every 5 mins
  * Logs response time in a CSV file with timestamp

### Assignment 18: Discover Hidden Directories

* Use `dirb` or `gobuster` on `testphp.vulnweb.com`.
* Document at least 5 discovered directories.

### Assignment 19: Python Socket Port Scanner

* Create a script that scans ports 1–100 on a given domain.
* Limit: 15 lines
* Add sleep between scans and proper output formatting.

### Assignment 20: Check Internet Exposure via Shodan

* Search your public IP on Shodan.
* Document what services are visible (mask IP in report).
* Reflect on what to do to harden your system.

---

## Submission Guidelines

1. **Repository Setup**: Create `EH_sem5_2025_Notes` repository
2. **Directory Structure**: Create `1st Assignment` folder
3. **Report Format**:

   * 1-page maximum
   * Include screenshots where applicable
   * Document your methodology
   * Explain findings and conclusions
4. **Code Submission**: Include all scripts and configurations
5. **Deadline**: Submit by next Friday

## Assessment Criteria

* **Technical Implementation** (40%)
* **Report Quality** (30%)
* **Security Analysis** (20%)
* **Documentation** (10%)

---

**Note**: All assignments are designed for educational purposes. Use only authorized systems and follow ethical hacking principles. Remember to respect privacy and legal boundaries in all activities.
