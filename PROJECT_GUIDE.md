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
## ⚙️ Environment Setup

A virtualized SOC lab environment was created using Ubuntu Linux on Oracle VirtualBox to simulate real-world security monitoring conditions.

### 🔧 Setup Process

The following steps were performed to configure the environment:

* Installed Splunk Enterprise using the `.deb` package on Ubuntu
* Configured system permissions to allow Splunk to access log files
* Started and verified Splunk services
* Accessed the Splunk Web Interface via browser (`http://localhost:8000`)

### 🧠 Purpose

This setup provides a controlled environment for:

* Log ingestion and monitoring
* Detection engineering using SPL (Search Processing Language)
* Security event analysis and investigation

This environment simulates a basic SOC (Security Operations Center) workflow for hands-on cybersecurity practice.
