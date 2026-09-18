# PENETRATION-TESTING


## Footprinting, Reconnaissance & Network Scanning

**Program:** Cybersecurity & Ethical Hacking
**Week:** 02
**Modules:** W2-PM1 & W2-PM5
**Author:** [Your Name]
**Date:** [Date]
**Platform:** Kali Linux & Windows

---

## 1. Introduction

This project covers the **footprinting, reconnaissance, and network scanning** phases of penetration testing.

During this practical, I used several Kali Linux tools to collect information from an authorized target. I also used Zenmap to discover active devices on my own local network.

The main goal was to understand how security professionals gather information, identify network assets, and document security-related observations before performing deeper testing.

> **Scope:** All activities were performed only on authorized systems, training environments, or my own network.

---

## 2. Objectives

* Understand the reconnaissance and footprinting process.
* Collect publicly available information about an authorized target.
* Identify web, DNS, and server-related information.
* Discover active devices on a local network.
* Identify IP and MAC addresses.
* Create a basic network topology.
* Document observations and potential security impact.

---

## 3. Tools Used

| Tool        | Purpose                             |
| ----------- | ----------------------------------- |
| WHOIS       | Domain and registration information |
| WhatWeb     | Web technology identification       |
| Nslookup    | DNS and IP information              |
| Curl        | HTTP header analysis                |
| Wafw00f     | WAF detection                       |
| DNSRecon    | DNS record enumeration              |
| Zenmap      | Network host discovery and topology |
| Windows CMD | IP and MAC address identification   |

---

# 4. Footprinting & Reconnaissance

I used multiple Kali Linux tools to gather different types of information about the authorized target.

### WHOIS

```bash
whois [target-domain]
```

**Observation:**
[Add your result and short observation]

📸 **Screenshot:** [Add screenshot]

### WhatWeb

```bash
whatweb [target-domain]
```

**Observation:**
[Add your result and short observation]

📸 **Screenshot:** [Add screenshot]

### Nslookup

```bash
nslookup [target-domain]
```

**Observation:**
[Add your IP/DNS result]

📸 **Screenshot:** [Add screenshot]

### Curl

```bash
curl -I https://[target-domain]
```

**Observation:**
[Add your HTTP header result]

📸 **Screenshot:** [Add screenshot]

### Wafw00f

```bash
wafw00f https://[target-domain]
```

**Observation:**
[Add your WAF result]

📸 **Screenshot:** [Add screenshot]

### DNSRecon

```bash
dnsrecon -d [target-domain]
```

**Observation:**
[Add your DNS records/result]

📸 **Screenshot:** [Add screenshot]

---

# 5. Network Scanning with Zenmap

I used Windows Command Prompt to identify my local network configuration before performing the scan.

```cmd
ipconfig
```

**IPv4:** [Your IP]
**Subnet:** [Your subnet]
**Gateway:** [Your gateway]

📸 **Screenshot:** [Add screenshot]

I then entered my local subnet into Zenmap and performed a **Ping Scan** to identify active hosts.

**Target Network:** `[Your subnet]`

### Discovered Hosts

| No. | IP Address | MAC Address | Status |
| --- | ---------- | ----------- | ------ |
| 1   | [IP]       | [MAC]       | Active |
| 2   | [IP]       | [MAC]       | Active |
| 3   | [IP]       | [MAC]       | Active |
| 4   | [IP]       | [MAC]       | Active |

📸 **Zenmap Screenshot:** [Add screenshot]

### Network Topology

I used Zenmap's **Topology** feature to visualize the discovered devices and exported the topology for documentation.

📸 **Topology Screenshot:** [Add screenshot]

---

# 6. Findings & Risk Analysis

| Finding                  | Observation    | Potential Impact                         | Risk         |
| ------------------------ | -------------- | ---------------------------------------- | ------------ |
| Web technology exposed   | [Your finding] | May assist further enumeration           | [Low/Medium] |
| IP address identified    | [Your finding] | Reveals network information              | [Low/Medium] |
| HTTP information exposed | [Your finding] | Provides technical details               | [Low/Medium] |
| DNS information exposed  | [Your finding] | Helps map infrastructure                 | [Low/Medium] |
| Active hosts discovered  | [Your finding] | Unknown devices may require verification | [Low/Medium] |

> These are reconnaissance observations, not confirmed vulnerabilities. Further authorized testing would be required to validate any vulnerability.

---

# 7. Recommendations

* Regularly review publicly exposed technical information.
* Keep software, CMS platforms, and plugins updated.
* Review HTTP headers and unnecessary information exposure.
* Monitor and maintain DNS records.
* Properly configure and monitor WAF protection.
* Perform regular internal network discovery.
* Investigate unknown devices on the network.
* Keep network documentation and topology updated.
* Always perform security testing within an authorized scope.

---

# 8. Learning Outcomes

This practical helped me gain hands-on experience with:

* Kali Linux reconnaissance tools
* DNS and domain enumeration
* Web technology fingerprinting
* HTTP header analysis
* WAF detection
* Network host discovery
* IP and MAC address identification
* Zenmap and network topology
* Security finding documentation

The main lesson I learned is that **good reconnaissance helps security professionals understand an environment before performing deeper security testing**.

---

# 9. Conclusion

In Week 2, I completed practical exercises covering **footprinting, reconnaissance, and network scanning**.

By using multiple Kali Linux tools and Zenmap, I learned how to collect information, identify active network devices, analyze observations, and document findings professionally.

This practical improved my understanding of the early stages of penetration testing and provided a strong foundation for the next phase of my cybersecurity learning.

---

## 10. Evidence

All practical evidence and screenshots are included in this section.

📸 WHOIS
📸 WhatWeb
📸 Nslookup
📸 Curl
📸 Wafw00f
📸 DNSRecon
📸 Windows IP Configuration
📸 Zenmap Scan
📸 Network Topology

---

## Author

**[Your Name]**
Cybersecurity & Ethical Hacking Student

**GitHub:** [Your GitHub]
**LinkedIn:** [Your LinkedIn]

**Project:** Week 02 – Footprinting, Reconnaissance & Network Scanning
