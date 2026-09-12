# 🛡️ Network Intrusion Detection System (NIDS)

A simple **Network-Based Intrusion Detection System (NIDS)** built using **Suricata** on Kali Linux.

This project monitors network traffic, detects predefined suspicious activity using custom rules, and generates alerts and logs when matching traffic is identified.

---

## 📌 Project Overview

Network Intrusion Detection Systems are security tools used to monitor network traffic and identify potentially suspicious or malicious activities.

In this project, **Suricata** is configured as a network-based IDS to:

- Monitor network traffic
- Inspect packets on a network interface
- Detect traffic matching custom security rules
- Generate security alerts
- Store detected events in log files
- Demonstrate intrusion detection using controlled test traffic

The project was developed as part of the **CodeAlpha Cyber Security Internship – Task 4**.

---

## 🎯 Objectives

The main objectives of this project are:

1. Set up a network-based intrusion detection system.
2. Configure custom detection rules.
3. Monitor network traffic continuously.
4. Detect suspicious network activity.
5. Generate alerts for detected events.
6. Record detection events in log files.
7. Demonstrate the working of an NIDS in a controlled environment.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Kali Linux | Security testing environment |
| Suricata 8.0.6 | Network Intrusion Detection System |
| Wi-Fi (`wlan0`) | Network interface monitored |
| Custom Suricata Rules | Traffic detection |
| ICMP | Test traffic |
| Terminal | Configuration and monitoring |

---

## 🏗️ Project Architecture

```text
                 Network Traffic
                        │
                        ▼
                 ┌──────────────┐
                 │    wlan0     │
                 │ Network      │
                 │ Interface    │
                 └──────┬───────┘
                        │
                        ▼
                 ┌──────────────┐
                 │  Suricata    │
                 │    NIDS      │
                 └──────┬───────┘
                        │
                 Packet Inspection
                        │
                        ▼
                 ┌──────────────┐
                 │ Detection    │
                 │    Rules     │
                 └──────┬───────┘
                        │
                        ▼
              ┌───────────────────┐
              │ Matching Traffic  │
              │ Detected          │
              └─────────┬─────────┘
                        │
                        ▼
                ┌──────────────┐
                │    Alert     │
                │  Generation  │
                └──────┬───────┘
                       │
                       ▼
                ┌──────────────┐
                │     Logs     │
                │  fast.log    │
                │  eve.json    │
                └──────────────┘
