What is a **Network**?
A network is a group of two or more devices (like computers, phones, printers) that are connected together to share:

1.Data and files

2.Internet connection

3.Resources (like printers or servers)

*Types of Networks*

| Type                                | Description                        | Example                        |
| ----------------------------------- | ---------------------------------- | ------------------------------ |
| **LAN** (Local Area Network)        | Small, local network               | Your home Wi-Fi or school lab  |
| **WAN** (Wide Area Network)         | Large-scale, long-distance network | The internet                   |
| **MAN** (Metropolitan Area Network) | City-wide network                  | Office buildings across a city |


*Why Networks Are Important*

1.Communication: Send emails, messages, or calls.

2.Sharing: Access files or printers across devices.

3.Remote access: Work from anywhere using internet-based networks.

4.Efficiency: Helps businesses connect systems and teams easily.

----

A **subnet** (short for subnetwork) is a smaller, logical part of a larger network. It helps organize and manage devices more efficiently.

Explanation:
Imagine your network is a big apartment building (main network), and each flat (subnet) holds a few residents (devices). All are part of the same building, but they are grouped to keep things organized.

A **subnet mask** defines how much of the IP address is the network part vs the host (device) part

-----

### What is a MAC ID (MAC Address)?

A **MAC ID**, or **MAC address** (**Media Access Control** address), is a **unique identifier** assigned to every device that connects to a network.

*Think of it like your device’s **permanent name tag** on the network
* It’s **built into your device’s network hardware** (like the Wi-Fi or Ethernet card).
* It **doesn’t change**, even if your IP address does.
* It’s used for **identifying devices** on a **local network**.

*Format:*
A MAC address looks like this:
00:1A:2B:3C:4D:5E
* It’s made up of **6 pairs of hexadecimal digits** (0–9, A–F).
* The first half shows the **manufacturer**, the second half is **unique to your device**.

*Example Use:*
* A router uses MAC addresses to **assign IP addresses** to devices.
* Schools/offices may **block or allow internet access** using MAC filters.
* MAC is used in **ARP (Address Resolution Protocol)** to map IP → MAC for communication inside local networks.
---

### What is an IP Address?

An **IP address (Internet Protocol address)** is a **unique number** assigned to every device connected to a network. It acts like your device’s **home address** on the internet or local network — allowing it to **send and receive data**.

*Two Main Types of IP Addresses:*

| Type     | Example                                   | Used For                    |
| -------- | ----------------------------------------- | --------------------------- |
| **IPv4** | `192.168.1.1`                             | Most common today           |
| **IPv6** | `2001:0db8:85a3:0000:0000:8a2e:0370:7334` | Newer version, future-proof |

*IP Address vs MAC Address:*

| Feature     | IP Address                     | MAC Address                           |
| ----------- | ------------------------------ | ------------------------------------- |
| Changes?    | Yes (can change with networks) | No (fixed to device)                  |
| Assigned by | Network (DHCP or manual)       | Hardware manufacturer                 |
| Used for    | Sending data across networks   | Identifying devices on local networks |

*Difference Between IPv4 and IPv6:*

| Feature              | **IPv4**                    | **IPv6**                                          |
| -------------------- | --------------------------- | ------------------------------------------------- |
| **Full Form**        | Internet Protocol version 4 | Internet Protocol version 6                       |
| **Size**             | 32-bit                      | 128-bit                                           |
| **Address Format**   | `192.168.0.1`               | `2001:db8::1`                                     |
| **Total Addresses**  | \~4.3 billion               | \~340 undecillion (huge!)                         |
| **Separator**        | Dot (`.`)                   | Colon (`:`)                                       |
| **Address Shortage** | Yes                         | No                                                |
| **Speed**            | Good                        | Slightly better for routing                       |
| **Usage**            | Still widely used           | Growing adoption (needed for IoT, future devices) |


### We’re running out of *IPv4 addresses*, which is why *IPv6* was created!

---

**NAT (Network Address Translation)** is a technique used in networking to allow multiple devices on a local (private) network to access the internet using a single public IP address.
NAT **translates private IP addresses** (used inside a local network) to a **public IP address** (used on the internet), and vice versa.

*Why NAT is Needed:*

1. **IPv4 address shortage** – Public IPs are limited, but NAT allows many devices to share one.
2. **Security** – Internal IP addresses are hidden from the internet.
3. **Network organization** – Easier to manage large private networks.


*How It Works:*

* Device in private network (e.g., 192.168.0.5) wants to visit a website.
* NAT router replaces the source IP with its public IP (e.g., 203.0.113.12).
* The website replies to the public IP, and NAT router sends the response back to the correct internal device.

*Types of NAT:*

| Type                                                  | Description                                                                                   |
| ----------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| **Static NAT**                                        | One-to-one mapping between private and public IP.                                             |
| **Dynamic NAT**                                       | Private IP is mapped to any available public IP from a pool.                                  |
| **PAT (Port Address Translation)** / **NAT Overload** | Many private IPs share one public IP using different ports. Most common type in home routers. |

*Example:*

| Device | Private IP   | Public IP (NAT) |
| ------ | ------------ | --------------- |
| Laptop | 192.168.1.10 | 203.0.113.12    |
| Phone  | 192.168.1.11 | 203.0.113.12    |

Both appear as `203.0.113.12` to websites.

---
**TCP vs UDP**

| Feature                    | **TCP (Transmission Control Protocol)**                         | **UDP (User Datagram Protocol)**                        |
| -------------------------- | --------------------------------------------------------------- | ------------------------------------------------------- |
| **Connection Type**        | Connection-oriented (requires a handshake before data transfer) | Connectionless (no handshake; data is sent immediately) |
| **Reliability**            | Reliable — guarantees delivery of data                          | Unreliable — no delivery guarantee                      |
| **Ordering**               | Ensures data packets arrive **in order**                        | No guarantee of packet order                            |
| **Error Checking**         | Yes (checksums + acknowledgment + retransmission)               | Yes (checksums only, no retransmission)                 |
| **Acknowledgment (ACKs)**  | Yes — sender waits for acknowledgment from receiver             | No — sender does not wait for any response              |
| **Flow Control**           | Yes — uses sliding window to manage how much data is sent       | No flow control mechanism                               |
| **Congestion Control**     | Yes — reduces speed when network is congested                   | No — keeps sending regardless of network load           |
| **Speed**                  | Slower (due to all the checks and confirmations)                | Faster (minimal overhead)                               |
| **Packet Size**            | Typically larger (header is 20 bytes)                           | Smaller (header is 8 bytes)                             |
| **Data Transmission**      | Stream-based (continuous flow)                                  | Message-based (sends discrete packets called datagrams) |
| **Use Case Suitability**   | Best for **data integrity** and **accuracy**                    | Best for **low-latency** or **real-time** apps          |
| **Typical Applications**   | Web (HTTP/HTTPS), Email (SMTP, IMAP), File Transfer (FTP)       | Gaming, Streaming (YouTube, Netflix), VoIP, DNS         |
| **Overhead**               | High (due to tracking, acknowledgments, etc.)                   | Low (faster transmission, but riskier)                  |
| **Transmission Guarantee** | Guaranteed delivery, order, and integrity                       | Best-effort delivery — no guarantees                    |
| **Protocol Header Size**   | 20–60 bytes                                                     | 8 bytes                                                 |
| Analogy                    |                                                                 |                                                         |
| **Like mailing a package** | With tracking, signature, and delivery confirmation             | Just dropping it in the mailbox with no tracking        |

-----
**Reconnaissance** is the first phase of ethical hacking or penetration testing (also used by attackers) — where the goal is to gather information about a target system/network before launching an attack.

Two types: Active and Passive

| Type           | **Active Reconnaissance**                                             | **Passive Reconnaissance**                                                      |
| -------------- | --------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **Definition** | Directly interacting with the target system to gather info            | Gathering info without interacting with the target system                       |
| **Visibility** | **Detectable** by firewalls, IDS/IPS (Intrusion Detection Systems)    | **Undetectable**, as no direct contact is made                                  |
| **Risk**       | High — increases chances of getting caught                            | Low — stealthier and safer                                                      |
| **Techniques** | - Port scanning<br>- Ping sweeps<br>- Banner grabbing<br>- Traceroute | - WHOIS lookup<br>- DNS records<br>- Social media<br>- Google hacking (dorking) |
| **Tools Used** | - Nmap<br>- Netcat<br>- Nikto<br>- Hping                              | - Maltego<br>- Recon-ng<br>- Google<br>- Shodan                                 |
| **Purpose**    | Map open ports, services, OS info                                     | Collect public info (names, IPs, domains, emails)                               |
| **Example**    | Scanning a web server to see which ports are open                     | Searching LinkedIn to find employees at a company                               |

