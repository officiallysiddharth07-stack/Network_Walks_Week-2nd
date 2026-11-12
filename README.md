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
| whois                | Finds domain registration details (owner, dates, name servers).   |
| whatweb              | Fingerprints web technologies (server, CMS, plugins, IP).         |
| nslookup             | Resolves the domain name to its IP address using DNS.             |
| curl -I              | Reads the HTTP response headers of the website.                   |
| wafw00f              | Detects whether a Web Application Firewall protects the site.     |
| dnsrecon             | Enumerates all DNS records (NS, MX, SPF, TXT, SRV).               |
| Zenmap (Nmap GUI)    | Scans the local subnet to find live hosts, IPs and MAC addresses. |
| Windows CMD          | Local IP and MAC address identification                          |

# 4. Activities Performed
## 4.1 Footprinting & Reconnaissance

Using six Kali Linux tools—WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, and DNSRecon—I conducted reconnaissance against the networkwalks.com domain. Different kinds of information on the target were gathered using each instrument.

I started by using **whois** to find the domain's name servers and collect publicly accessible domain registration information. Information regarding domain registration and hosting infrastructure was obtained from the results.

I then used **whatweb** to determine which technologies the website was using. WordPress 7.0.4 and WP Download Manager 3.3.58 were found in the results, along with further data that the website disclosed.

I was able to resolve the domain name to its IP address using **Nslookup**. 192.232.216.135 was found in the given result.

I examined the HTTP response headers using Curl and the -I option. This revealed the WordPress REST API endpoint /wp-json/ and offered more details about the web application.

I then used **wafw00f** to check if the website was protected by a Web Application Firewall. ModSecurity (SpiderLabs) was found in the outcome.

Lastly, I enumerated DNS records using **dnsrecon**. Name servers, mail servers, SPF/TXT records, service records, and DNS software information were all included in the results.

## 4.2 Network Scanning with Zenmap

For the second activity, I used Zenmap to perform network discovery on my local network. The practical required me to identify my local IP address and subnet, discover live hosts, identify their IP and MAC addresses, and generate a network topology.<br>
I first used the Windows ipconfig command to identify my local IP address and LAN subnet. I then entered the subnet into Zenmap and selected Ping Scan to identify active hosts.<br>
The example results provided in the practical identified one live host:<br>
•	192.168.56.1<br>
The example result didn’t include any MAC addresses. But, I scanned the mac address using ipconfig/all in my Windows cmd.
Also, I opened the Topology section in Zenmap, enabled the legend and saved the network topology in PDF format as required by the practical task.


