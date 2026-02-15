
🛡️ Detection Lab: End-to-End Threat Investigation & SIEM Engineering

Overview
This repository contains a series of technical deep-dives into Network Traffic Analysis and SIEM (Splunk) Engineering. The projects transition from raw packet inspection with tcpdump and Wireshark to sophisticated threat hunting and detection engineering using the MITRE ATT&CK framework.

🛠️ Technical Stack
SIEM: Splunk Enterprise

IDS/NSM: Suricata, Zeek/Bro

Analysis Tools: Wireshark, TCPDump, NetworkMiner

Frameworks: MITRE ATT&CK, NIST Incident Response Lifecycle

Environment: Kali Linux, Windows Event Logs, Ubuntu

🛰️ Part 1: Network Traffic Monitoring & Attack Detection
Focus: Low-level packet analysis and signature-based detection.

Packet Capture Automation: Automated traffic collection using tcpdump on Kali Linux for continuous monitoring.

Protocol Analysis: Deep-dive investigation into SMTP data exfiltration and TCP stream reassembly.

Intrusion Detection (Suricata): Developed custom Suricata rules to identify and log malicious traffic patterns, transitioning from signature alerts to log analysis.

🔍 Part 2: SIEM Implementation & Log Analysis (Splunk)
Focus: Turning big data into actionable security intelligence.

Key Investigations:
Kerberoasting Detection: Analyzed Windows Event Logs (Event ID 4769) in Splunk to identify service ticket requests indicative of Kerberoasting attacks.

Log4j Investigation: Performed source-type pivoting and forensic analysis on Log4j payloads within Splunk Enterprise.

Tunneling & Exfiltration: Detected DNS/ICMP tunneling attempts by analyzing HTTPS traffic patterns and anomalies.

UltraVNC Threat Hunt: Investigated unauthorized remote access attempts using Windows Event Log analysis.

SOC Tier 2 Simulation: A full end-to-end simulation mapping alerts to the MITRE ATT&CK matrix, covering the full lifecycle from detection to response.

📈 Key Outcomes
Reduced Noise: Learned to tune Suricata rules to reduce false positives in a lab environment.

Mapping to MITRE: Every investigation was contextualized within the MITRE ATT&CK framework to understand the "The Big Picture" of the adversary's lifecycle.

Visualization: Built Splunk dashboards to visualize traffic spikes and suspicious login patterns.
