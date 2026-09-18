# 🛡️ PENETRATION TESTING 


## FOOTPRINTING & NETWORK SCANNING



 **Pentester Name:** Indra Bahadur Kc  

**Program / Batch:** B083 – Networkwalks

**Week:** 02

**Date:** 18-09-2026

### 📚 Modules Completed

* W2-PM1 – Multiple Kali Linux Tools
* W2-PM2- Google Hacking Database / Google Dorking
* W2-PM3 — Maltego Domain & Email Reconnaissance
* W2-PM4 — theHarvester OSINT 
* W2-PM5 – Zenmap Scanning

### 🎯 Target

* Networkwalks — authorized educational target
* My own local LAN network
* available resources 

### 🔐 Authorization

All activities were performed within the authorized scope of the practical exercise or on my own network.

---

#  ⚠️ Liability Disclaimer

This report is created for educational and cybersecurity training purposes. All testing was performed only on authorized systems and my own local network.

The commands and techniques shown should only be used in environments where proper permission has been obtained. Unauthorized scanning or access may violate laws and organizational policies.

---

#  📝 Introduction

During Week 02 of my Cybersecurity & Ethical Hacking internship, I worked on two important penetration-testing phases: **footprinting/reconnaissance** and **network scanning**.

For the first activity, I used several Kali Linux tools to collect publicly available information about the assigned domain. For the second activity, I used **Zenmap** to discover active devices on my own local network.

The main goal was to understand how cybersecurity professionals gather information about a target and document their findings before performing deeper security testing. 🔍

---

#  🧰 Tools Used

| Tool           | Purpose                             |
| -------------- | ----------------------------------- |
| 🐧 Kali Linux  | Reconnaissance and security testing |
| 🔎 WHOIS       | Domain and registration information |
| 🌐 WhatWeb     | Website technology identification   |
| 📡 Nslookup    | Domain-to-IP resolution             |
| 📋 Curl        | HTTP header inspection              |
| 🛡️ Wafw00f    | WAF detection                       |
| 🗂️ DNSRecon   | DNS record enumeration              |
| 🌐 Google-exploit DB | Exploit Database — (GHDB)    | 
| 🔍 Maltego       |  network important information      |
| 📧 theHarvester  | website emails ID's sub-domain info  |
| 🗺️ Zenmap     | Network host discovery              |
| 💻 Windows CMD | Local IP and network information    |

---

#  🔍 Activities Performed

## PM1. Footprinting & Reconnaissance

I performed reconnaissance using **WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, and DNSRecon**. Each tool provided different information about the target.

### 🔎 WHOIS

I used WHOIS to collect publicly available domain-registration information and identify the domain's name servers.

```bash
whois networkwalks.com
```

**Observation:** Domain registration and name-server information was returned.

<img width="2856" height="1596" alt="Screenshot 2026-09-16 075534" src="https://github.com/user-attachments/assets/22438a66-6378-4304-acaf-517e5bf1b303" />


---

### 🌐 WhatWeb

WhatWeb was used to identify technologies used by the website.

```bash
whatweb networkwalks.com
```

**Observation:** The practical identified **WordPress 7.0.4** and **WP Download Manager 3.3.58**.

This information can help a security professional identify technologies that may require further security review.

<img width="2856" height="826" alt="Screenshot 2026-09-16 075828" src="https://github.com/user-attachments/assets/325de99b-64c7-434b-ba16-fe757b8fd668" />


---

### 📡 Nslookup

Nslookup was used to resolve the domain name to its IP address.

```bash
nslookup networkwalks.com
```

**Observation:** The sample result identified **192.232.216.135**.

*Replace this with my actual result if different.*

<img width="2736" height="746" alt="Screenshot 2026-09-16 080038" src="https://github.com/user-attachments/assets/10cbeb5c-b09b-4920-8adb-4fea3fc9b1d2" />


---

### 📋 Curl

Curl was used to inspect the website's HTTP response headers.

```bash
curl -I https://networkwalks.com
```

**Observation:** The response provided technical information and showed the WordPress REST API endpoint `/wp-json/`.

<img width="2854" height="1590" alt="Screenshot 2026-09-16 080602" src="https://github.com/user-attachments/assets/335c4639-2469-4407-93ee-9658ef7ee2b1" />


---

### 🛡️ Wafw00f

Wafw00f was used to determine whether a Web Application Firewall was protecting the website.

```bash
wafw00f https://networkwalks.com
```

**Observation:** The practical identified **ModSecurity (SpiderLabs)**.

<img width="2850" height="950" alt="Screenshot 2026-09-16 080533" src="https://github.com/user-attachments/assets/549610a3-10f2-4317-9bf4-799bc664263b" />


---

### 🗂️ DNSRecon

DNSRecon was used to collect DNS information.

```bash
dnsrecon -d networkwalks.com
```

**Observation:** The results included information about name servers, mail servers, SPF/TXT records, and service records.

<img width="2860" height="1120" alt="Screenshot 2026-09-16 080729" src="https://github.com/user-attachments/assets/d71df886-5b94-4d17-8f16-c870b613689a" />


---

## 🧪 PM2 — Google Hacking Database / Google Dorking
🎯 Objective
The second task focused on understanding Google Dorking, also known as Google Hacking.

The purpose was to explore how specially constructed search queries can identify publicly indexed web resources.

🌐 Platform Used
Exploit Database — Google Hacking Database (GHDB)

The Google Hacking Database contains examples of search operators and queries that can be used to locate specific types of publicly indexed information.
🔎 Search Performed
A search for:cam

performed within the Google Hacking Database.

The database returned multiple examples involving:

📷 IP cameras

🌐 Webcams

📡 Camera monitoring systems
<img width="2862" height="1690" alt="Screenshot 2026-09-16 082204" src="https://github.com/user-attachments/assets/842c6fd6-e217-48ed-a457-dde64711ab69" />
<img width="2876" height="1738" alt="Screenshot 2026-09-16 082154" src="https://github.com/user-attachments/assets/1a056115-a8b3-4f67-8eac-1cf4f21d620a" />

## 🔎 PM3 — Maltego Domain & Email Reconnaissance
📌 Objective

The objective of this task was to use Maltego to perform passive reconnaissance and identify publicly available information associated with a target domain.
🛠️ Tool Used

    🔍 Maltego Graph Desktop 4.13.0

🔍 Methodology

Maltego was used to create a graph containing the target domain and related entities. The investigation focused on identifying publicly available relationships between the domain and other information.

During the investigation, Maltego identified an email address associated with the domain.

<img width="2878" height="1822" alt="Screenshot 2026-09-18 060828" src="https://github.com/user-attachments/assets/dde7bcaa-d74c-47ee-8cf6-6fe87f207259" />

Evidence Description:
The screenshot shows the Maltego graph containing the discovered domain and its relationship to an associated email address. The graph demonstrates how publicly available information can be correlated to build a picture of the target's external footprint.


## 🕵️ PM4 — theHarvester OSINT 
📌 Objective

The objective of this task was to use theHarvester to collect publicly available information related to a target domain, including hostnames and other OSINT data.
🛠️ Tools Used

    🕵️ theHarvester 4.11.1

    🐧 Kali Linux

🔍 Methodology

theHarvester was executed against the target domain using multiple available search and OSINT sources.

The tool attempted to collect information such as:

    🌐 Hostnames

    📧 Email addresses

    🔎 Publicly indexed information

    🖥️ Infrastructure-related information

<img width="2628" height="1560" alt="Screenshot 2026-09-18 063127" src="https://github.com/user-attachments/assets/4010c56f-464d-40c4-94a8-bdf693e7f37e" />
<img width="2880" height="1766" alt="Screenshot 2026-09-18 062158" src="https://github.com/user-attachments/assets/4ca3c36e-705c-4d2a-a489-86ecc4e94230" />

## PM5. 🗺️ Network Scanning with Zenmap

For the second activity, I used **Zenmap** to discover active devices on my own local network.

First, I checked my network configuration using:

```cmd
ipconfig
```

I then entered my local subnet into Zenmap and performed a **Ping Scan**.

### Observation

The sample identified three live hosts:

* 10.0.0.1
* 10.0.0.2
* 10.0.0.4


These are sample values and should be replaced with my actual scan results.

Zenmap also provided available IP and MAC address information. Finally, I used the **Topology** section to create a visual representation of the discovered network.
<img width="2878" height="1562" alt="Screenshot 2026-09-18 070134" src="https://github.com/user-attachments/assets/0c105542-180b-4838-963f-ccfc2a80ecad" />
<img width="2880" height="1606" alt="Screenshot 2026-09-18 070153" src="https://github.com/user-attachments/assets/efd5dbce-7d03-48da-849c-cce40e0edb26" />



---

# ⚠️ Risk Analysis

| Finding                            | Potential Impact                                     | Risk   |
| ---------------------------------- | ---------------------------------------------------- | ------ |
| Web technology information exposed | May help identify software requiring security review | Medium |
| Server IP identifiable             | Provides information about the web service           | Low    |
| HTTP information exposed           | May assist further enumeration                       | Low    |
| WAF technology identifiable        | Reveals part of the security architecture            | Low    |
| DNS information exposed            | Helps build an infrastructure profile                | Medium |
| Multiple local hosts discovered    | Unknown devices may require investigation            | Medium |
| Public domain info was identified |	Could assist with attack-surface mapping	            |  Low   |
| email associated with domain was identified |	Could potentially be used for phishing,spam attempts | Low |

These are **security observations, not confirmed vulnerabilities**. No exploitation or vulnerability validation was performed during these exercises. 

---

# 🛡️ Recommendations

Based on the observations, I recommend:

1. **Review publicly exposed technology information.**
2. **Keep CMS platforms, plugins, and other software updated.**
3. **Review HTTP headers** for unnecessary technical information.
4. **Regularly review DNS records** and remove unnecessary entries.
5. **Properly configure and monitor the WAF.**
6. **Perform regular internal network discovery.**
7. **Investigate unknown or unauthorized devices.**
8. **Keep network topology documentation updated.**
9. **Always perform security testing with proper authorization.**
10. **Regularly review information publicly associated with organizational domains**
11. **Minimize unnecessary exposure of organizational email addresses.**
12. **Enable MFA on accounts associated with publicly exposed email addresses.**
13. **Monitor for phishing and impersonation attempts.**
14. **Remove unnecessary publicly accessible information where appropriate

---

# 7. 📸 Evidence

The following evidence should be included in the GitHub repository:

* WHOIS result
* WhatWeb result
* Nslookup result
* Curl headers
* Wafw00f result
* DNSRecon result
* Windows `ipconfig`
* Exploit -db
* Maltego Domain & Email Reconnaissance
* theHarvester OSINT
* Zenmap scan
* IP/MAC information
* Zenmap network topology

---

# 8. 🎯 Conclusion

During Week 02, I gained practical experience in **footprinting, reconnaissance, and network scanning**.

I learned how different Kali Linux tools can provide useful information about a website and its infrastructure. I also learned how Zenmap can be used to discover active devices and visualize a local network.

The biggest lesson for me was that **information gathering is an important part of cybersecurity**. Before performing deeper security testing, a professional needs to understand the environment and carefully document what has been discovered.

I also learned that a technical observation is not automatically a vulnerability. Proper validation and authorized testing are required before confirming a security issue.

Overall, this practical improved my understanding of reconnaissance tools, network discovery, risk identification, and professional cybersecurity reporting. 🔐💻

---

# 👤 Author & Project Information

**Author:** Indra bahadur Kc
**Program:** Cybersecurity & Ethical Hacking
**Batch:** B083 – Networkwalks
**Week:** 02

### 🚀 Project Summary

**Focus:** Footprinting, Reconnaissance & Network Scanning
**Tools:** Kali Linux, WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, DNSRecon, exploit-DB, Maltego, theHarvester, Zenmap

**🔐 Learn responsibly. Test ethically. Document professionally.**
