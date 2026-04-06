# 🔐 Network Traffic Analysis & Anomaly Detection using Wireshark

## 📌 Overview

This project focuses on analyzing real-time network traffic using Wireshark to understand protocol behavior and detect anomalies. It includes both normal traffic inspection and simulated malicious activities such as port scanning, DNS anomalies, and ICMP flooding.

---

## 🎯 Objectives

* Perform packet-level network traffic analysis
* Analyze DNS, HTTP, and TCP protocols
* Detect anomalies and suspicious patterns
* Simulate real-world attack scenarios
* Document findings with evidence

---

## 🛠️ Tools Used

* Wireshark
* Nmap
* Windows OS (Packet capture environment)

---

## ⚙️ Methodology

### 1. Packet Capture

* Captured live network traffic using Wireshark
* Selected active network interface (Wi-Fi/Ethernet)
* Saved capture file in `.pcap` format

---

### 2. Traffic Generation

Normal Traffic:

* Web browsing (HTTP/HTTPS)
* DNS queries (`nslookup`)
* ICMP requests (`ping`)

Simulated Malicious Traffic:

* Port scanning using Nmap
* DNS query flooding with random domains
* ICMP flood using continuous ping

---

## 🔍 Protocol Analysis

### 📡 DNS Analysis

* Filter: `dns`
* Observed domain queries and responses
* Identified high-frequency and randomized domain requests

---

### 🌐 HTTP Analysis

* Filter: `http`
* Inspected GET/POST requests and server responses
* Analyzed communication patterns

---

### 🔗 TCP Analysis

* Filter: `tcp`
* Analyzed 3-way handshake (SYN, SYN-ACK, ACK)
* Observed retransmissions and reset packets

---

## 🚨 Simulated Attack Scenarios

### 🔴 1. Port Scanning (Reconnaissance Attack)

* Tool: Nmap
* Command:

```bash
nmap -sS localhost
```

* Detection:

  * High volume of SYN packets
  * Multiple destination ports
  * Incomplete TCP handshakes

---

### 🔴 2. DNS Anomaly (Beaconing Simulation)

* Generated repeated queries to random domains
* Detection:

  * High-frequency DNS traffic
  * Randomized domain names

---

### 🔴 3. ICMP Flood (Traffic Spike Simulation)

* Command:

```bash
ping -t 8.8.8.8
```

* Detection:

  * Continuous ICMP packets
  * Increased traffic volume

---

## 📊 Statistical Analysis

Used Wireshark statistics to analyze traffic patterns:

* Protocol Hierarchy → Protocol distribution
* Conversations → Communication between endpoints
* Endpoints → Most active devices

---

## 📸 Key Screenshots

### 🔹 TCP SYN Scan Detection

Screenshots/04_SYN-Scan.png

### 🔹 DNS Anomaly Detection

![DNS Anomaly](screenshots/06_dns_anomaly.png)

### 🔹 ICMP Flood Traffic

![ICMP Flood](screenshots/07_icmp_flood.png)

### 🔹 Protocol Hierarchy

![Protocol Stats](screenshots/09_protocol_hierarchy.png)

---

## 📁 Project Structure

```
network-traffic-analysis-wireshark/
│
├── README.md
├── report/
├── screenshots/
├── captures/
└── scripts/
```

---

## 📌 Key Findings

* Detected SYN-based port scanning behavior
* Observed high-frequency DNS queries resembling beaconing
* Identified continuous ICMP traffic indicating possible flooding
* Analyzed TCP reset and retransmission patterns

---

## ✅ Conclusion

This project demonstrates practical skills in network traffic analysis, protocol inspection, and anomaly detection using Wireshark. Simulated attack scenarios provided insight into real-world network threats and their detection techniques.

---

## 🚀 Future Improvements

* Integration with IDS tools like Snort
* Automated traffic analysis using Python
* Machine learning-based anomaly detection

---

## 📬 Author

Aryan
[GitHub: your-profile-link](https://github.com/Aryantyagitv)

