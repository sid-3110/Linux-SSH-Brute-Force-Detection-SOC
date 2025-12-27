# SIEM Alert Explanation – Linux SSH Brute Force Detection

## Alert Name
Multiple Failed SSH Login Attempts

---

## Alert Description
This alert is generated when multiple failed SSH authentication attempts are detected from the same source IP address within a short time window.

The goal of this alert is to identify potential brute-force attacks targeting SSH services on Linux servers.

---

## Alert Severity
Medium

Severity is classified as Medium because the activity indicates malicious intent but does not confirm a successful compromise.

---

## Alert Trigger Conditions
The alert is triggered when:
- Multiple SSH login failures are detected
- The same source IP address is involved
- The same user account is targeted
- Attempts occur within a short time period
- Logs indicate SSH authentication failures

---

## Log Source
- OS: Linux (Ubuntu)
- Log File: `/var/log/auth.log`
- Service: SSH (Port 22)

---

## Example Log Event
