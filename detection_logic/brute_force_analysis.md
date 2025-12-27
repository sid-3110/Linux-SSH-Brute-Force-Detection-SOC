# SSH Brute Force Detection Logic

## Indicators Observed
- Repeated SSH authentication failures
- Same external IP address
- Same target account (`root`)
- Short time window
- Automated behavior pattern

---

## Why This Is Suspicious
- Privileged accounts are high-value targets
- Repeated failures indicate automation
- External IP suggests internet-based attack
- Timing aligns with common brute-force behavior

---

## What This Is Not
- Not a single user typo
- Not internal system activity
- Not a service account failure
- Not scheduled maintenance

---

## Detection Conclusion
The observed pattern matches a classic SSH brute-force attack attempt.
