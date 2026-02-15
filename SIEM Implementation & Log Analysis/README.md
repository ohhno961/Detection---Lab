
# 🛡️ Detection Lab: SIEM Implementation & Log Analysis
## Overview
This repository documents a comprehensive series of SOC Analyst operations focused on Detection Engineering and Advanced Threat Hunting. Using Splunk Enterprise as the primary SIEM platform, I conducted end-to-end investigations into sophisticated attack vectors, ranging from DNS Tunneling and Kerberoasting to Log4j exploitation. This lab bridges the gap between raw telemetry (Zeek, Sysmon, Windows Event Logs) and actionable security intelligence.

## 🛠️ Technical Stack
**SIEM Platform:** Splunk Enterprise

**Query Language:** SPL (Search Processing Language)

**Data Sources:** Zeek/Bro (Network), Sysmon (Endpoint), Windows Event Logs (.evtx), Access Combined (Web)

**Frameworks:** MITRE ATT&CK, NIST Incident Response Lifecycle

**Environment:** Kali Linux (Local Instance), Windows Server (Active Directory)

## 🔍 Core Investigations & Project Reports
### 1. Network Traffic & Covert Communication
**DNS/Zeek Tunneling Detection:**

**Objective:** Validated the ingestion of Zeek tunnel logs to detect covert communication channels.

**Analysis:** Mapped protocol activity (TEREDO, AYIYA) and identified top source IPs to pinpoint potential exfiltration or C2 behavior.

**HTTPS Traffic Analysis:**

**Objective:** Conducted deep-dives into HTTPSLOGS to identify beaconing patterns and internal compromises via port/IP correlation.

### 2. Adversary Simulation & MITRE Mapping
**End-to-End SOC Simulation:**

**Objective:** A "Red vs. Blue" exercise executing MITRE ATT&CK techniques against an Active Directory environment.

**Outcome:** Developed and tuned correlation rules to detect credential theft, persistence, and lateral movement.

**Kerberoasting Investigation (Event ID 4769):**

**Objective:** Analyzed TGS ticket requests to identify RC4 encryption downgrades indicative of Kerberoasting.

**Findings:** Confirmed use of AES encryption and absence of suspicious service account targeting, validating the environment's current hardening status.

### 3. Endpoint Forensics & Vulnerability Research
**Sysmon Backdoor Investigation (Unit 42):**

**Objective:** Traced the behavior of an UltraVNC backdoor using Sysmon operational logs.

**Analysis:** Pivoted through process creation events to isolate malicious file activity and suspicious network connections.

**Log4j & Web Access Investigation:**

**Objective:** Conducted a deep-dive into Log4j sourcetypes and access_combined logs to identify automated scanners.

**Outcome:** Identified distributed mass-scanning behavior and spoofed user agents (e.g., legacy browsers) targeting sensitive paths like /phpMyAdmin and /admin.

## 📈 SOC Tier 2 Operations & Methodology
**Exploratory Data Analysis:** I apply a "Hypothesis-Driven" approach, starting with Data Validation (checking index and sourcetype) before moving to Threat Hunting.

**Detection Engineering:** Expertise in creating KQL/SPL queries that reduce false positives by filtering for "Normal vs. Extreme" behavior.

**Geofencing & Anomaly Detection:** Implemented queries to isolate login attempts and web requests from unauthorized geographies (e.g., country NOT LIKE '%MEX%').

**Relational Logic:** Utilizing Inner/Left Joins in Splunk to map employees to machines, ensuring 100% asset accountability during triage.

## 🧠 Skills Demonstrated
**Advanced SPL:** Expert in stats, dc (distinct count), eval, and transaction commands for complex correlation.

**Log Forensics:** Proficiency in converting .evtx to JSON and parsing raw text into structured SIEM fields.

Attacker Mindset: Understanding the Full Intrusion Chain, from initial reconnaissance to web shell execution and cleanup.

Professional Reporting: Ability to translate technical log data into Executive Summaries with clear "Key Business Value."
