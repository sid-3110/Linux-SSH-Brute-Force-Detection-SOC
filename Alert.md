# SIEM Alert: Linux SSH Authentication Anomaly

---

## Alert ID
SOC-LNX-SSH-0007

---

## Alert Name
Multiple Failed SSH Authentication Attempts

---

## Alert Type
Authentication Anomaly

---

## Alert Severity
Medium

---

## Alert Status
New

---

## Alert Description
This alert was generated after detecting multiple failed SSH authentication attempts on a Linux server from a single source IP address within a short time window.

The behavior exceeds the normal threshold for authentication failures and requires analyst review.

---

## Detection Logic (High-Level)
The alert is triggered when:
- SSH authentication failure events are detected
- Multiple failures originate from the same source IP
- The same user account is targeted
- Events occur repeatedly within a defined time window

---

## Affected Asset
- Hostname: PROD-LINUX-01
- Asset Type: Linux Server
- Operating System: Ubuntu Linux
- Service: SSH
- Port: 22

---

## Affected Account
- Username: root
- Account Privilege Level: Privileged

---

## Event Details
- Log Source: `/var/log/auth.log`
- Event Type: Failed SSH Authentication
- Event Message: `Failed password`
- Number of Failed Attempts: 20
- Time Window: 4 minutes

---

## Source Information
- Source IP Address: 103.71.88.19
- Source Network: External
- Geo Location: Unknown
- Known Reputation: Not Available

---

## Event Timeline
| Timestamp (UTC) | Event Description |
|-----------------|------------------|
| 03:12:01 | SSH authentication failure |
| 03:12:05 | SSH authentication failure |
| 03:12:10 | SSH authentication failure |
| 03:12:15 | SSH authentication failure |
| 03:12:20 | SSH authentication failure |

---

## Analyst Notes (Initial)
This alert indicates repeated SSH authentication failures targeting a privileged account from an external source.  
Further investigation is required to determine whether the activity represents a false positive or a malicious brute-force attempt.

---

## Recommended Analyst Actions
- Review authentication logs for related events
- Correlate failures by source IP, user, and time
- Check for any successful login events following failures
- Apply user, system, and timing context
- Determine appropriate classification (false positive or suspicious)

---

## MITRE ATT&CK (Potential Mapping)
- Tactic: Credential Access
- Technique: T1110 – Brute Force
- Sub-Technique: T1110.001 – Password Guessing
