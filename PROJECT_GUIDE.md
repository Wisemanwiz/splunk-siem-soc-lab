# 📘 SOC L1 SIEM Lab – Detailed Project Guide

---

## 📌 Project Summary

This project demonstrates the implementation of a Security Information and Event Management (SIEM) solution using Splunk in a simulated SOC (Security Operations Center) Level 1 environment.

The lab replicates real-world SOC workflows including log ingestion, detection engineering, threat investigation, and incident reporting.

---

## 🎯 Objectives

- Monitor and analyze system authentication logs
- Detect suspicious activity using Splunk SIEM
- Develop detection rules using SPL (Search Processing Language)
- Investigate potential security incidents
- Map detections to the MITRE ATT&CK framework
- Document findings in a structured, professional format

---

## 🧱 Lab Environment

### 🛠️ Technologies Used

- Splunk Enterprise (SIEM)
- Ubuntu Linux
- Oracle VirtualBox

---

## ⚙️ Implementation

### 1️⃣ Environment Setup

A virtualized lab environment was created using Ubuntu Linux on VirtualBox.

Key steps:

- Installed Splunk Enterprise (.deb package)
- Configured file permissions
- Started Splunk services
- Accessed the Splunk web interface

#### Commands Used

```bash
sudo dpkg -i splunk-<version>.deb
sudo chown -R $USER:$USER /opt/splunk
/opt/splunk/bin/splunk start --accept-license