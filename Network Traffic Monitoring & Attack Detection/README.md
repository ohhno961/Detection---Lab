
# 🛰️ Detection Lab: Network Traffic Monitoring & Attack Detection
## Overview
This repository documents a progression of network security operations, moving from foundational packet capture to advanced forensic investigations. I engineered automated environments on Kali Linux to capture live traffic, developed custom IDS signatures using Suricata, and conducted deep-dive forensic analysis on malware-driven data exfiltration campaigns (Hawkeye Keylogger).

## 🛠️ Technical Stack
**Analysis Tools:** Wireshark, tcpdump, NetworkMiner

**IDS/IPS:** Suricata

**Automation:** Bash Scripting (Automated .pcap rotation)

**Forensics:** Base64 Decoding, SMTP stream reassembly, OSINT (VirusTotal, Whois)

**Protocols:** TCP/UDP, HTTP/HTTPS, DNS, SMTP, ICMP, DHCP

## 🔍 Core Projects & Investigations
### 1. Packet Capture Automation & CLI Mastery
**Objective:** Engineered a scalable environment for automated network monitoring using tcpdump and Bash.

**Automation:** Developed .sh scripts to automate capture sessions with timestamped logging and rotation.

**CLI Proficiency:** Utilized advanced tcpdump flags (-c, -G, -w, -nn, -XX) to isolate traffic flows from specific domains like coursera.org.

**Validation:** Transformed raw hexadecimal data into structured .pcap files, verifying protocol breakdowns and packet counts for reproducibility.

### 2. Signature Engineering (Suricata IDS)
**Objective:** Developed and validated custom Intrusion Detection System (IDS) signatures to detect malicious traffic patterns.

**Rule Development:** Examined and configured custom.rules to trigger alerts on specific network behaviors.

**Log Analysis:** Analyzed Suricata outputs including fast.log (legacy alerts) and eve.json (detailed telemetry) to verify rule effectiveness and reduce false positives.

**Alert Validation:** Ran Suricata against sample traffic to simulate real-time detection of reconnaissance and exploitation attempts.

### 3. Forensic Case Study: Hawkeye Malware Exfiltration
**Objective:** Conducted a full-chain forensic investigation into a Hawkeye Keylogger exfiltration campaign.

**Exfiltration Analysis:** Traced the malware’s behavior as it queried whatismyipaddress.com for host reconnaissance.

**SMTP Decoding:** Reassembled and decoded Base64 SMTP payloads to retrieve stolen credentials sent to an attacker-controlled email.

**Asset Mapping:** Performed Layer 2 MAC address analysis and DNS attribution to map the full extent of the compromised internal network.

**Timeline Correlation:** Reconstructed a 62-minute attack lifecycle, identifying the root cause and exfiltration paths.

## 🧠 Skills Demonstrated
**Protocol Analysis:** Deep understanding of the OSI Model, specifically inspecting traffic at the Frame, Ethernet, IP, and TCP/UDP layers.

**Traffic Filtering:** Expert-level use of Wireshark Display Filters (e.g., ip.addr, tcp contains, udp.port == 53) to isolate high-fidelity indicators.

**Malware Forensics:** Ability to identify Indicator of Compromise (IOCs) and map them to the MITRE ATT&CK matrix (e.g., T1041 - Exfiltration Over C2).

**Network Hygiene:** Verifying DNS resolution, TCP handshakes (SYN/ACK), and TTL values to identify anomalies or misconfigurations.
