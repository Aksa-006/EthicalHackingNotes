# Ethical Hacking Assignments - Semester 3, 2025 (Complete Student Mapping)

## Assignment Instructions

* **Duration**: 2 hours maximum
* **Report**: 1-page report per assignment
* **Repository**: Create a GitHub repository named `EH_sem3_2025_Notes`
* **Directory**: Submit all assignments in the `1st Assignment` directory
* **Deadline**: Submit by next Friday

---

## Student Assignments - Round 1 (Students 1-20)

### Assignment 1: TCP and UDP Port Discovery
**Assigned to: [SankaraNarayananS18](https://github.com/SankaraNarayananS18)**

**🎯 What to do:** Scan a website to find open doors (ports) using two different methods
**📋 Scenario:** You're a security analyst checking what services are running on a target system
**🔧 How:** Use `nmap` tool to scan both TCP and UDP ports on `scanme.nmap.org`
**❓ Why:** TCP and UDP work differently - TCP is like a phone call (reliable), UDP is like shouting (fast but unreliable)
**📊 Report:** Explain the difference between TCP/UDP, show screenshot of scan results, list what services you found running

* Use `nmap` to scan both TCP and UDP ports on `scanme.nmap.org`.
* Save the results and summarize open services.
* **Report**: Explain TCP vs UDP ports + screenshot of the scan.

### Assignment 2: Full Port Scan
**Assigned to: [Aaron-VS](https://github.com/Aaron-VS)**

**🎯 What to do:** Check every single door (all 65,535 ports) on a website to find hidden services
**📋 Scenario:** You're doing a comprehensive security audit - no stone left unturned
**🔧 How:** Use `nmap -p-` command to scan all ports on `testphp.vulnweb.com`
**❓ Why:** Some services hide on unusual ports to avoid detection - we need to find them all
**📊 Report:** Show your script file, explain what unusual ports you found, why full scans are important for security

* Use `nmap -p-` to scan all 65535 ports on `testphp.vulnweb.com`.
* **Script**: Save the command as a `.sh` file and automate output saving.

### Assignment 3: DNS and IP Discovery
**Assigned to: [Umeshwarkumar](https://github.com/Umeshwarkumar)**

**🎯 What to do:** Find the real address (IP) of a website and understand how the internet finds websites
**📋 Scenario:** You're investigating how websites are located on the internet
**🔧 How:** Use `nmap -sL` and `dig` commands to get IP addresses and DNS information of `zero.webappsecurity.com`
**❓ Why:** DNS is like a phone book for the internet - understanding it helps in network reconnaissance
**📊 Report:** Show the IP addresses you found, create a simple flowchart showing how DNS works, explain what each tool revealed

* Use `nmap -sL` and `dig` to find IPs, DNS info of `zero.webappsecurity.com`.
* Create a flowchart: DNS resolution process.

### Assignment 4: Create Low-Privilege User
**Assigned to: [joshuazacharyjose](https://github.com/joshuazacharyjose)**

**🎯 What to do:** Create a new user account with limited permissions (no admin rights)
**📋 Scenario:** You're setting up a secure system where users can't make system changes
**🔧 How:** Use `adduser` to create user `student01`, then `usermod` to remove sudo privileges
**❓ Why:** Security principle - users should only have the minimum permissions they need (principle of least privilege)
**📊 Report:** Show screenshots of your commands, display the `/etc/passwd` file, explain why limited users are safer

* In Kali VM, create a user `student01` with no sudo access.
* Use `adduser`, `usermod`, and confirm permissions.
* **Evidence**: Screenshot of commands + `/etc/passwd` snippet.

### Assignment 5: File Creation and Permission
**Assigned to: [EVAN-KS](https://github.com/EVAN-KS)**

**🎯 What to do:** Create a file and set specific permissions using numbers (751)
**📋 Scenario:** You're learning how Linux controls who can read, write, or execute files
**🔧 How:** Use `touch` to create a file, then `chmod 751` to set permissions, use `ls -l` to verify
**❓ Why:** File permissions are crucial for security - wrong permissions can expose sensitive data or allow unauthorized access
**📊 Report:** Show your commands, explain what 751 means (owner: read/write/execute, group: read/execute, others: execute only), demonstrate with `ls -l`

* Create a file using `touch`. Change permission to `751`.
* Use `chmod`, `ls -l`, and explain octal notation.

### Assignment 6: What is Shodan?
**Assigned to: [Soumya-code-ai](https://github.com/Soumya-code-ai)**

**🎯 What to do:** Explore Shodan (the "Google for hackers") to see what information is publicly available about systems
**📋 Scenario:** You're learning about internet reconnaissance - what attackers can find without even touching your system
**🔧 How:** Go to [Shodan.io](https://shodan.io), search for `scanme.nmap.org`, explore the results
**❓ Why:** Shodan reveals exposed services, open ports, and system information that attackers use for initial reconnaissance
**📊 Report:** Document what you found about scanme.nmap.org, explain how this information could be used by both attackers and defenders, show screenshots

* Visit [Shodan.io](https://shodan.io), search for `scanme.nmap.org`.
* Document what data is visible and its use for attackers and defenders.

### Assignment 7: Explain Core Network Terms
**Assigned to: [Dineshbaburs](https://github.com/Dineshbaburs)**

**🎯 What to do:** Create a simple guide explaining 5 important networking concepts with pictures
**📋 Scenario:** You're teaching someone the basics of how networks work - like explaining how mail gets delivered
**🔧 How:** Research and create simple explanations with diagrams for NAT, ARP, MAC, IPv4, IPv6
**❓ Why:** Understanding these terms is fundamental to cybersecurity - you can't protect what you don't understand
**📊 Report:** One-page document with simple explanations, basic diagrams, real-world examples for each term

* Create a 1-page illustrated document:

  * NAT, ARP, MAC, IPv4, IPv6
  * One-line explanation and diagram each.

### Assignment 8: Directory Monitoring Bash Script
**Assigned to: [B3ttina](https://github.com/B3ttina)**

**🎯 What to do:** Create a small program that watches a folder and records when files are added, deleted, or changed
**📋 Scenario:** You're building a security monitoring system to detect unauthorized file changes
**🔧 How:** Write a 15-line bash script using `inotify` or similar to watch `/home/student/Downloads` folder
**❓ Why:** File monitoring helps detect malware, data theft, or unauthorized access - like having a security camera for your files
**📊 Report:** Show your script code, demonstrate it working, explain how it could be used for security monitoring

* Write a 15-line bash script to monitor changes in `/home/student/Downloads`.
* Log the change type (file created/deleted/modified).

### Assignment 9: Mini Port Scanner Script
**Assigned to: [AdithyaRaj672](https://github.com/AdithyaRaj672)**

**🎯 What to do:** Build your own simple port scanner that can check if doors (ports) are open on any computer
**📋 Scenario:** You're creating a security tool to quickly check what services are running on a target system
**🔧 How:** Write a bash script that asks for an IP address, scans the most common 1000 ports, saves results with date
**❓ Why:** Understanding how port scanners work helps you build better security tools and defend against them
**📊 Report:** Show your script code, demonstrate scanning a target, explain how it works and what the results mean

* Write a bash script that:

  * Takes IP as input
  * Scans top 1000 ports
  * Saves results in `scan_<date>.log`

### Assignment 10: Linux AI Help Chat using Groq API
**Assigned to: [Allanpremm](https://github.com/Allanpremm)**

**🎯 What to do:** Create a simple AI assistant that explains Linux commands in plain English
**📋 Scenario:** You're building a help system for new Linux users who don't understand technical commands
**🔧 How:** Use Groq's free API to create a Python chatbot (max 15 lines) that takes Linux commands and explains them
**❓ Why:** AI can make complex technical concepts accessible to everyone - bridging the gap between experts and beginners
**📊 Report:** Show your Python code, demonstrate the chatbot working, explain how AI can help with cybersecurity education

* Use Groq's free API to create a CLI chatbot.
* Input: Any Linux command.
* Output: Easy explanation.
* **Limit**: ≤ 15 lines Python code.

### Assignment 11: Ncat Chat Terminal
**Assigned to: [abelalexander18](https://github.com/abelalexander18)**

**🎯 What to do:** Create a simple chat system between two computers using network tools
**📋 Scenario:** You're learning how network communication works by building a basic chat application
**🔧 How:** Write a 10-line script using `ncat` - one terminal listens for connections, another connects and sends messages
**❓ Why:** Understanding network communication is crucial for cybersecurity - you need to know how data flows to protect it
**📊 Report:** Show your script, demonstrate the chat working between terminals, explain how this relates to network security

* Create a script with 10 lines to simulate chat using `ncat`.
* Terminal A: Listener
* Terminal B: Connects and sends message

### Assignment 12: Serve a Directory using Python
**Assigned to: [Darain-Brit-A](https://github.com/Darain-Brit-A)**

**🎯 What to do:** Turn your computer into a simple web server to share files over the internet
**📋 Scenario:** You're learning how web servers work by creating your own mini-website
**🔧 How:** Use `python3 -m http.server 8080` command in any folder to start a web server on port 8080
**❓ Why:** Understanding web servers helps you identify security vulnerabilities and protect against web-based attacks
**📊 Report:** Show screenshots of your server running, browser accessing it, terminal commands, explain what this teaches about web security

* Use `python3 -m http.server 8080` in a directory.
* Screenshot server + browser result + terminal command.

### Assignment 13: VirusTotal API Usage
**Assigned to: [SanMaria28](https://github.com/SanMaria28)**

**🎯 What to do:** Use VirusTotal's database to check if a file is malicious by analyzing its digital fingerprint
**📋 Scenario:** You're a security analyst who needs to quickly check if a suspicious file is safe or dangerous
**🔧 How:** Get free API key from VirusTotal, write 10-15 lines of Python/bash code using `curl` to check file hash
**❓ Why:** VirusTotal aggregates results from 70+ antivirus engines - much more reliable than single antivirus
**📊 Report:** Show your API code, demonstrate checking a file, explain how hash-based detection works, show API response

* Register for [VirusTotal](https://virustotal.com) API key.
* Use Python or bash with `curl` to check hash details of a test file.
* **Code limit**: 10-15 lines.

### Assignment 14: Sudo Usage Logging
**Assigned to: [shaundx5](https://github.com/shaundx5)**

**🎯 What to do:** Create a monitoring system that watches for admin privilege usage and records who uses it when
**📋 Scenario:** You're setting up security monitoring to track who gets admin access and when - like a security logbook
**🔧 How:** Write Python/Bash script that checks `/var/log/auth.log` every 30 seconds for sudo attempts
**❓ Why:** Monitoring admin access helps detect unauthorized privilege escalation and insider threats
**📊 Report:** Show your monitoring script, demonstrate it catching sudo usage, explain why logging admin actions is crucial for security

* Create a Python/Bash script that monitors `/var/log/auth.log` every 30s.
* If `sudo` success/fail found, log username + time.

### Assignment 15: System Hack Timeline
**Assigned to: [Patrick-Pio](https://github.com/Patrick-Pio)**

**🎯 What to do:** Research a famous cyber attack and create a step-by-step timeline of how it happened
**📋 Scenario:** You're a cybersecurity analyst investigating how a major breach occurred - like being a digital detective
**🔧 How:** Choose a real attack (like Equifax, SolarWinds, etc.), research the details, create 6-step timeline
**❓ Why:** Understanding attack patterns helps you build better defenses and recognize similar attacks in progress
**📊 Report:** Present your 6-step timeline, explain what went wrong at each stage, what could have prevented it, lessons learned

* Pick any past real-life attack (e.g., Equifax breach).
* Document a 6-step timeline (initial access → data exfiltration).

### Assignment 16: Detect Service Version with Nmap
**Assigned to: [Deanjb3](https://github.com/Deanjb3)**

**🎯 What to do:** Find out exactly what software versions are running on a website and check if they have known security holes
**📋 Scenario:** You're doing a vulnerability assessment - checking if the target is running outdated, vulnerable software
**🔧 How:** Use `nmap -sV` to detect service versions on `testphp.vulnweb.com`, then research known vulnerabilities
**❓ Why:** Outdated software versions often have known security flaws - attackers target these specific versions
**📊 Report:** List at least 3 services with versions found, research and document known CVEs for those versions, explain the risk

* Use `nmap -sV` on `testphp.vulnweb.com`.
* Summarize at least 3 detected services with versions and known CVEs.

### Assignment 17: Bash Script for Auto Ping and Log
**Assigned to: [ishaZaara](https://github.com/ishaZaara)**

**🎯 What to do:** Create an automated monitoring system that checks if a website is responding and records how fast it is
**📋 Scenario:** You're setting up network monitoring to track website performance and detect outages
**🔧 How:** Write a bash script that pings a domain every 5 minutes and saves response times with timestamps to CSV
**❓ Why:** Continuous monitoring helps detect network issues, DDoS attacks, or service disruptions early
**📊 Report:** Show your monitoring script, demonstrate it running, show sample CSV output, explain how this helps with security monitoring

* Create a script that:

  * Pings a domain every 5 mins
  * Logs response time in a CSV file with timestamp

### Assignment 18: Discover Hidden Directories
**Assigned to: [JoyAanchalRose](https://github.com/JoyAanchalRose)**

**🎯 What to do:** Find hidden folders on a website that aren't linked from the main page - like finding secret rooms
**📋 Scenario:** You're doing web reconnaissance to discover hidden content, admin panels, or backup files
**🔧 How:** Use `dirb` or `gobuster` tools to brute-force directory names on `testphp.vulnweb.com`
**❓ Why:** Hidden directories often contain sensitive files, admin panels, or backup data that shouldn't be public
**📊 Report:** Document at least 5 hidden directories you found, explain what each might contain, why they're security risks

* Use `dirb` or `gobuster` on `testphp.vulnweb.com`.
* Document at least 5 discovered directories.

### Assignment 19: Python Socket Port Scanner
**Assigned to: [Ramya-9739](https://github.com/Ramya-9739)**

**🎯 What to do:** Build your own port scanner from scratch using Python - understand how the tools actually work
**📋 Scenario:** You're learning network programming by creating the core functionality of tools like nmap
**🔧 How:** Write a 15-line Python script using sockets to scan ports 1-100, add delays between scans, format output nicely
**❓ Why:** Understanding how port scanners work at the code level helps you build better security tools and defend against them
**📊 Report:** Show your Python code, demonstrate it scanning a target, explain how sockets work, compare to professional tools

* Create a script that scans ports 1–100 on a given domain.
* Limit: 15 lines
* Add sleep between scans and proper output formatting.

### Assignment 20: Check Internet Exposure via Shodan
**Assigned to: [Rachel-joy07](https://github.com/Rachel-joy07)**

**🎯 What to do:** Check what information about your own internet connection is publicly visible to attackers
**📋 Scenario:** You're doing a personal security audit - seeing your network from an attacker's perspective
**🔧 How:** Find your public IP address, search it on Shodan, see what services and information are exposed
**❓ Why:** Understanding your own exposure helps you secure your systems - you can't protect what you don't know is vulnerable
**📊 Report:** Document what services are visible (hide your real IP), explain the security risks, provide recommendations to harden your system

* Search your public IP on Shodan.
* Document what services are visible (mask IP in report).
* Reflect on what to do to harden your system.

---

## Student Assignments - Round 2 (Students 21-40)

### Assignment 1: TCP and UDP Port Discovery
**Assigned to: [sasmitabtech](https://github.com/sasmitabtech)**

### Assignment 2: Full Port Scan
**Assigned to: [nithin811](https://github.com/nithin811)**

### Assignment 3: DNS and IP Discovery
**Assigned to: [NITHEE-11](https://github.com/NITHEE-11)**

### Assignment 4: Create Low-Privilege User
**Assigned to: [Kavin-cse](https://github.com/Kavin-cse)**

### Assignment 5: File Creation and Permission
**Assigned to: [SharonC-droid](https://github.com/SharonC-droid)**

### Assignment 6: What is Shodan?
**Assigned to: [dan-jose2006](https://github.com/dan-jose2006)**

### Assignment 7: Explain Core Network Terms
**Assigned to: [Joel-jarn](https://github.com/Joel-jarn)**

### Assignment 8: Directory Monitoring Bash Script
**Assigned to: [KARTHIK-RAJEEV](https://github.com/KARTHIK-RAJEEV)**

### Assignment 9: Mini Port Scanner Script
**Assigned to: [adisankar-oss](https://github.com/adisankar-oss)**

### Assignment 10: Linux AI Help Chat using Groq API
**Assigned to: [AnnmarieVinish](https://github.com/AnnmarieVinish)**

### Assignment 11: Ncat Chat Terminal
**Assigned to: [AnamiiiikaM](https://github.com/AnamiiiikaM)**

### Assignment 12: Serve a Directory using Python
**Assigned to: [SREEHARIS16](https://github.com/SREEHARIS16)**

### Assignment 13: VirusTotal API Usage
**Assigned to: [chrisbaptist07](https://github.com/chrisbaptist07)**

### Assignment 14: Sudo Usage Logging
**Assigned to: [annmary-aaa](https://github.com/annmary-aaa)**

### Assignment 15: System Hack Timeline
**Assigned to: [samvrith66](https://github.com/samvrith66)**

### Assignment 16: Detect Service Version with Nmap
**Assigned to: [Nikshitha2896](https://github.com/Nikshitha2896)**

### Assignment 17: Bash Script for Auto Ping and Log
**Assigned to: [SnehaT23](https://github.com/SnehaT23)**

### Assignment 18: Discover Hidden Directories
**Assigned to: [tanushree-2006](https://github.com/tanushree-2006)**

### Assignment 19: Python Socket Port Scanner
**Assigned to: [samuelbiju13](https://github.com/samuelbiju13)**

### Assignment 20: Check Internet Exposure via Shodan
**Assigned to: [RichardRajuChirayath](https://github.com/RichardRajuChirayath)**

---

## Student Assignments - Round 3 (Students 41-60)

### Assignment 1: TCP and UDP Port Discovery
**Assigned to: [vedantjoshi18](https://github.com/vedantjoshi18)**

### Assignment 2: Full Port Scan
**Assigned to: [Melwin-Thomas](https://github.com/Melwin-Thomas)**

### Assignment 3: DNS and IP Discovery
**Assigned to: [AlenSaijo](https://github.com/AlenSaijo)**

### Assignment 4: Create Low-Privilege User
**Assigned to: [JohnJoby2006](https://github.com/JohnJoby2006)**

### Assignment 5: File Creation and Permission
**Assigned to: [Sreesanth200677](https://github.com/Sreesanth200677)**

### Assignment 6: What is Shodan?
**Assigned to: [Ashweljohn](https://github.com/Ashweljohn)**

### Assignment 7: Explain Core Network Terms
**Assigned to: [BasudevDileep](https://github.com/BasudevDileep)**

### Assignment 8: Directory Monitoring Bash Script
**Assigned to: [MichelleDevasia](https://github.com/MichelleDevasia)**

### Assignment 9: Mini Port Scanner Script
**Assigned to: [Prisha-11-07](https://github.com/Prisha-11-07)**

### Assignment 10: Linux AI Help Chat using Groq API
**Assigned to: [Aksa-006](https://github.com/Aksa-006)**

### Assignment 11: Ncat Chat Terminal
**Assigned to: [SanjanaSudhir](https://github.com/SanjanaSudhir)**

### Assignment 12: Serve a Directory using Python
**Assigned to: [JoshinyMaria](https://github.com/JoshinyMaria)**

### Assignment 13: VirusTotal API Usage
**Assigned to: [SriRam-0511](https://github.com/SriRam-0511)**

### Assignment 14: Sudo Usage Logging
**Assigned to: [Monisha71](https://github.com/Monisha71)**

### Assignment 15: System Hack Timeline
**Assigned to: [JemimahAnna](https://github.com/JemimahAnna)**

### Assignment 16: Detect Service Version with Nmap
**Assigned to: [Reuben-Sunish](https://github.com/Reuben-Sunish)**

### Assignment 17: Bash Script for Auto Ping and Log
**Assigned to: [maxine-23](https://github.com/maxine-23)**

### Assignment 18: Discover Hidden Directories
**Assigned to: [Rhea-gracy](https://github.com/Rhea-gracy)**

### Assignment 19: Python Socket Port Scanner
**Assigned to: [Stacydsouza](https://github.com/Stacydsouza)**

### Assignment 20: Check Internet Exposure via Shodan
**Assigned to: [Tom-boby](https://github.com/Tom-boby)**

---

## Student Assignments - Round 4 (Students 61-80)

### Assignment 1: TCP and UDP Port Discovery
**Assigned to: [TenzinRigzin2460462](https://github.com/TenzinRigzin2460462)**

### Assignment 2: Full Port Scan
**Assigned to: [aadithyavimal-christ](https://github.com/aadithyavimal-christ)**

### Assignment 3: DNS and IP Discovery
**Assigned to: [jonac77](https://github.com/jonac77)**

### Assignment 4: Create Low-Privilege User
**Assigned to: [diyasusan-coder](https://github.com/diyasusan-coder)**

### Assignment 5: File Creation and Permission
**Assigned to: [Fariha006](https://github.com/Fariha006)**

### Assignment 6: What is Shodan?
**Assigned to: [SonalJoy10](https://github.com/SonalJoy10)**

### Assignment 7: Explain Core Network Terms
**Assigned to: [RAAPPO](https://github.com/RAAPPO)**

### Assignment 8: Directory Monitoring Bash Script
**Assigned to: [BarathCG](https://github.com/BarathCG)**

### Assignment 9: Mini Port Scanner Script
**Assigned to: [AmanVarunEkka](https://github.com/AmanVarunEkka)**

### Assignment 10: Linux AI Help Chat using Groq API
**Assigned to: [GOKUL06092006](https://github.com/GOKUL06092006)**

### Assignment 11: Ncat Chat Terminal
**Assigned to: [Abishek-gitit](https://github.com/Abishek-gitit)**

### Assignment 12: Serve a Directory using Python
**Assigned to: [Ridhi105](https://github.com/Ridhi105)**

### Assignment 13: VirusTotal API Usage
**Assigned to: [MINEAMICHEAL](https://github.com/MINEAMICHEAL)**

### Assignment 14: Sudo Usage Logging
**Assigned to: [Prajin-30](https://github.com/Prajin-30)**

### Assignment 15: System Hack Timeline
**Assigned to: [Ebinesh-03](https://github.com/Ebinesh-03)**

### Assignment 16: Detect Service Version with Nmap
**Assigned to: [JuliusDude](https://github.com/JuliusDude)**

### Assignment 17: Bash Script for Auto Ping and Log
**Assigned to: [JDANIELRAJ007](https://github.com/JDANIELRAJ007)**

### Assignment 18: Discover Hidden Directories
**Assigned to: [Abel0606](https://github.com/Abel0606)**

### Assignment 19: Python Socket Port Scanner
**Assigned to: [Sartaj-IT](https://github.com/Sartaj-IT)**

### Assignment 20: Check Internet Exposure via Shodan
**Assigned to: [Sankeeth-23](https://github.com/Sankeeth-23)**

---

## Student Assignments - Round 5 (Students 81-103)

### Assignment 1: TCP and UDP Port Discovery
**Assigned to: [alfindigo](https://github.com/alfindigo)**

### Assignment 2: Full Port Scan
**Assigned to: [Alanjeorge2005](https://github.com/Alanjeorge2005)**

### Assignment 3: DNS and IP Discovery
**Assigned to: [Nandana-19](https://github.com/Nandana-19)**

### Assignment 4: Create Low-Privilege User
**Assigned to: [sajidarryl](https://github.com/sajidarryl)**

### Assignment 5: File Creation and Permission
**Assigned to: [krupa2412](https://github.com/krupa2412)**

### Assignment 6: What is Shodan?
**Assigned to: [alvinjobi4](https://github.com/alvinjobi4)**

### Assignment 7: Explain Core Network Terms
**Assigned to: [joshuasenpai](https://github.com/joshuasenpai)**

### Assignment 8: Directory Monitoring Bash Script
**Assigned to: [A-M-K-x](https://github.com/A-M-K-x)**

### Assignment 9: Mini Port Scanner Script
**Assigned to: [joshuasantoshh](https://github.com/joshuasantoshh)**

### Assignment 10: Linux AI Help Chat using Groq API
**Assigned to: [johnevin965](https://github.com/johnevin965)**

### Assignment 11: Ncat Chat Terminal
**Assigned to: [AvrelPinto](https://github.com/AvrelPinto)**

### Assignment 12: Serve a Directory using Python
**Assigned to: [Tiswin-Saji](https://github.com/Tiswin-Saji)**

### Assignment 13: VirusTotal API Usage
**Assigned to: [AthreyRaj](https://github.com/AthreyRaj)**

### Assignment 14: Sudo Usage Logging
**Assigned to: [hackershay](https://github.com/hackershay)**

### Assignment 15: System Hack Timeline
**Assigned to: [Angela-Domingo](https://github.com/Angela-Domingo)**

### Assignment 16: Detect Service Version with Nmap
**Assigned to: [jessicanalinipaully](https://github.com/jessicanalinipaully)**

### Assignment 17: Bash Script for Auto Ping and Log
**Assigned to: [Prash-2402](https://github.com/Prash-2402)**

### Assignment 18: Discover Hidden Directories
**Assigned to: [LeoRineeth](https://github.com/LeoRineeth)**

### Assignment 19: Python Socket Port Scanner
**Assigned to: [ArthurFigrous](https://github.com/ArthurFigrous)**

### Assignment 20: Check Internet Exposure via Shodan
**Assigned to: [bigdaddy110](https://github.com/bigdaddy110)**

### Assignment 1: TCP and UDP Port Discovery (Repeat)
**Assigned to: [Tenzin-Choeying1](https://github.com/Tenzin-Choeying1)**

### Assignment 2: Full Port Scan (Repeat)
**Assigned to: [AntonyPraveenReddyK](https://github.com/AntonyPraveenReddyK)**

### Assignment 3: DNS and IP Discovery (Repeat)
**Assigned to: [jfs1336](https://github.com/jfs1336)**

---

## Assignment Distribution Summary

**Total Students:** 103
**Total Assignments:** 20 unique assignments
**Distribution Method:** 5 rounds with some assignments repeated in the final round
**Coverage:** Every student gets assigned to at least one assignment

**Round 1:** Students 1-20 (20 students)
**Round 2:** Students 21-40 (20 students)  
**Round 3:** Students 41-60 (20 students)
**Round 4:** Students 61-80 (20 students)
**Round 5:** Students 81-103 (23 students - includes 3 repeat assignments)

---

## Submission Guidelines

1. **Repository Setup**: Create `EH_sem3_2025_Notes` repository
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
