# Linux SSH Brute Force Detection – SOC Analyst Project

## 📌 Overview
This project demonstrates how a SOC Level 1 analyst detects and investigates SSH brute-force login attempts on a Linux server by analyzing authentication logs, correlating events, and making escalation decisions.

The project focuses on defensive security, log analysis, and SOC investigation methodology rather than offensive techniques.

---

## 🎯 Project Objectives
- Understand Linux SSH authentication logging
- Identify brute-force login attempts
- Apply event correlation and context analysis
- Differentiate false positives from real threats
- Practice SOC-style investigation and documentation
- Simulate escalation to higher SOC tiers

---

## 🖥️ Environment
- Operating System: Linux (Ubuntu-based)
- Service: SSH (Port 22)
- Log File: `/var/log/auth.log`
- Analyst Role: SOC Level 1

---

## 🚨 Threat Scenario
An external IP address attempts multiple SSH logins against a privileged Linux account (`root`) within a short time window.  
This behavior may indicate an automated brute-force attack.

---

## 🔍 Investigation Workflow
1. Alert triggered due to repeated SSH authentication failures
2. Authentication logs reviewed
3. Events correlated by IP address, user, and time window
4. Context applied (external IP, privileged account, timing)
5. Activity classified as suspicious
6. Alert escalated with proper documentation

---

## 🧠 Skills Demonstrated
- Linux authentication log analysis
- SSH brute-force detection
- Event correlation
- SOC alert investigation
- Incident documentation
- Escalation decision-making

---

## ⚠️ Disclaimer
This project is for educational and defensive security purposes only.
No real systems were attacked or compromised.
