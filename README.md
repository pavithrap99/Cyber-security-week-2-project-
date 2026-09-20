# 🔐 Offensive Security Reconnaissance: Footprinting & Network Discovery

## External Footprinting, Information Gathering & Internal Network Scanning

![NetworkWalks](https://img.shields.io/badge/NetworkWalks-Cybersecurity-blue)
![Footprinting](https://img.shields.io/badge/Footprinting-Reconnaissance-orange)
![TheHarvester](https://img.shields.io/badge/TheHarvester-OSINT-purple)
![Zenmap](https://img.shields.io/badge/Zenmap-Network_Scanning-green)
![Kali Linux](https://img.shields.io/badge/Kali_Linux-Security-blue)
![Ethical Hacking](https://img.shields.io/badge/Ethical_Hacking-Lab-red)
## project overview

 **Objective:**
Conduct a comprehensive external reconnaissance engagement against networkwalks.com and perform host discovery on an isolated lab network

**Engagement Type:** Passive Footprinting & Active Network Discovery

**Classification:** Educational / Authorized Testing

**Date of Execution:** 13-17 september 2026

**Intern:** Pavithra P | **Batch:** B083
## 🗺️ Engagement Scope

| **Target** | **Type** | **Activity** |
|------------|----------|--------------|
| `networkwalks.com` | External | Passive OSINT, DNS Enumeration, WAF Fingerprinting |
| `10.0.0.0/24` | Internal (Lab) | ICMP Host Discovery (Ping Scan) |

> 📌 **Authorization:** This engagement was performed under the NetworkWalks Letter of Authorization (LOA) for Batch B083. All activities were limited to passive reconnaissance and non-intrusive scanning.
## 🛡️ Security Arsenal
### 🕵️ Phase 1: External Footprinting

| **Tool** | **Function** | **Outcome** |
|----------|--------------|------------|
| `whois` | Domain Registry Intelligence | Registrar: GoDaddy |
| `whatweb` | Technology Stack Profiling | WordPress 7.1  / WP Download Manager 3.3.58 |
| `nslookup` | DNS Resolution | Server IP Identified |
| `curl -I` | HTTP Header Forensics | Apache / WP REST API Exposed |
| `wafw00f` | WAF Identification | ModSecurity (SpiderLabs) |
| `dnsrecon` | Full DNS Enumeration | BIND 50.87.144.87 / 31 Subdomains |
### Phase 2: OSINT & Open-Source Correlation

|**Tools**| **Function**|**Outcome**|
|---------|-------------|-----------|
|`theHarvester`|Aggregated source harvesting| 4 email / 31 subdomains / 3 ASNs|
### Phase 3: Local Network Discovery
|**Tool**|**Function**|**Outcome**|
|--------|------------|-----------|
|`Zenmap`|Ping Sweep (-sn)|	4 live hosts on|
## 🔍 Key Intelligence Highlights
|**Finding**|**Severity**|**Notes**|
|-----------|------------|---------|
|WordPress 7.1|	Informational|	Version disclosure|
|WP Download Manager 3.3.58|	Informational	|Version disclosure|
|ModSecurity (SpiderLabs) WAF	I|nformational|	Vendor fingerprintable|
|BIND version disclosure (50.87.144.87 )|	Informational	|Version disclosure|
|31 subdomains exposed|	Informational	|Expanded external attack surface|
|info@networkwalks.com|	Informational|	Generic contact point|
|10 open directories|	Informational|	Third-party public search discovery|
|DNSSEC not enabled	|Informational	|DNS spoofing risk (theoretical)|
|4 live hosts (Lab)|	N/A	|Tester's own network|
## 📊 Execution Summary
 |**PHASE**            |**TOOLS**   |**STATUS**     |
 |---------------------|------------|-------------- |
 |External Footprinting│ 6 Kali Tools│  ✅ COMPLETE | 
 │  OSINT Correlation  | Harvester   │  ✅ COMPLETE │
 │  Network Discovery  │  Zenmap     │  ✅ COMPLETE │
 │  Reporting          │Final Report │  ✅ COMPLETE │

OVERALL ENGAGEMENT STATUS: ✅ 100% COMPLETE 
## 🏁 Lessons Learned

1. **API dependency matters** – theHarvester's multi-source run was constrained by missing premium API keys (BuiltWith, Censys, DNSDumpster, etc.). A future run with full key provisioning would yield a more complete external footprint.

2. **Version ≠ Vulnerability** – WordPress 7.1 and WP Download Manager 3.3.58 were current releases at the time of assessment, correcting the template's initial assumption.

3. **WAF fingerprinting is trivial** – ModSecurity detection took only 2 requests. While the WAF is a positive security control, its vendor is identifiable, which may enable targeted bypass research.

4. **Subdomain enumeration reveals exposure** – 31 subdomains were discovered, including cpanel, webdisk, and webmail—high-value assets that should be reviewed for access controls and necessity of public exposure.

5. **Passive recon is powerful** – No active exploitation was performed, yet a complete infrastructure map was generated from public data alone.

---

## 🔒 Ethical Compliance

> ⚠️ **Disclaimer**
>
> This repository documents **educational research** conducted under explicit written authorization. All targets were either:
>
> 1. `networkwalks.com` – owned and authorized by Networkwalks Academy
> 2. `192.232.216.135.0/24` – the tester's own lab environment
>
> **No exploitation, data exfiltration, or service disruption occurred.**
>
> This work is intended solely for defensive cybersecurity education.

## 👤 About the Author

**Pavithra.P** is a cybersecurity enthusiast and intern at Networkwalks Academy (Batch B083). With a strong foundation in network security, penetration testing, and OSINT reconnaissance, Pavithra is passionate about understanding attacker methodologies to build better defenses.

**Areas of Interest:**
- 🔍 Offensive Security & Penetration Testing
- 🌐 OSINT & Passive Reconnaissance
- 🛡️ Network Security & Defense
- 📊 Security Reporting & Documentation

**Certifications Pursuing:**
- Networkwalks Cybersecurity Internship
- Ethical Hacking
**Connect:**
 - [![LinkedIn](https://img.shields.io/badge/LinkedIn-Pavithra-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pavithra-p-202131427/)
[![GitHub](https://img.shields.io/badge/GitHub-Pavithra-black?logo=github&logoColor=white)](https://github.com/pavithrap99)
 ## 🙏 Acknowledgments

- **Networkwalks Academy** – For curating this hands-on internship program
- **Waqas Karim (CCIE)** – For technical mentorship and industry perspective
- **Batch B083 Cohort** – For collaborative troubleshooting and shared insight
- 
**© 2026 Pavithra.p | Networkwalks Cybersecurity Internship | Batch B083**

