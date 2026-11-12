# PENETRATION TESTING REPORT 
### Footprinting & Network Scanning Phases

**W2-PM-FINAL  |  CYBERSECURITY  |  NETWORKWALKS**

| Field | Detail |
|---|---|
| **Pentester Name (Cybersecurity Professional)** | **Siddhartha Gautam** |
| **Program/Batch** | B084-Networkwalks |
| **Date** | 10 November 2026 |
| **Modules completed** | W2-PM1 (Multiple Kali Tools)<br>W2-PM5 (Zenmap Scanning) |
| **Client/Target** | 1. Networkwalks (secured written permission already)<br>2. My own local LAN Network |
| **Permission secured from client?** | Yes |
| **Phases covered** | **Phase 1:** Reconnaissance & Footprinting<br>**Phase 2:** Scanning & Network Discovery<br>**Phase 3-5:** In Progress |


# 1. Liability Disclaimer

I have only carried out these actions on systems and devices that I own or on which I have obtained formal authorization. All of these resources are solely for educational and research purposes. Nothing from here should be used to violate the law. You are accountable for every action you take. Misuse can result in a permanent record, severe penalties, job loss, and criminal charges. Unauthorized access is illegal in the majority of countries, even if no harm is done.
<br>PS: The instructor, the authors and Networkwalks are not responsible for what you do with this knowledge. Every action you take is your own responsibility.

# 2. Introduction
This report covers reconnaissance of networkwalks.com domain using multiple kali linux tools (1st module) and scanning my own local network using Zenmap (2nd module). The first module covers footprinting phase while the second module covers scanning phase; these phases are the initial steps to pen-testing.  Thus, together they show how an attacker moves from gathering public information to mapping live hosts on a network.
It is the Week 2 part of my ongoing internship program at Networkwalks.

# 3. Tools Used
The table below lists each tool used in this report and its purpose.
| Tool | Purpose |
|---|---|
| Kali Linux & Windows | Operating systems used for recon activities             |
| WHOIS                | Finds domain registration details (owner, dates, name servers).   |
| whatweb              | Fingerprints web technologies (server, CMS, plugins, IP).         |
| nslookup             | Resolves the domain name to its IP address using DNS.             |
| curl -I              | Reads the HTTP response headers of the website.                   |
| wafw00f              | Detects whether a Web Application Firewall protects the site.     |
| dnsrecon             | Enumerates all DNS records (NS, MX, SPF, TXT, SRV).               |
| Zenmap (Nmap GUI)    | Scans the local subnet to find live hosts, IPs and MAC addresses. |
| Windows CMD          | Local IP and MAC address identification                          |
