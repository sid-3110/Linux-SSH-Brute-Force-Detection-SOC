# SOC Investigation Notes – Linux SSH Alert

## Alert Summary
Multiple failed SSH login attempts detected on a production Linux server.

---

## Investigation Details
- Log Source: /var/log/auth.log
- Event Type: Failed SSH authentication
- Target Account: root
- Source IP: 103.71.88.19
- Attempts: Multiple failures within minutes

---

## Analysis
- Activity originated from an external IP
- Privileged account was targeted
- No successful login events observed
- Pattern consistent with automated brute-force behavior

---

## Assessment
The activity is classified as a suspicious SSH brute-force attempt.

---

## Action Taken
- Alert escalated to SOC Level 2
- No evidence of successful compromise at this stage
