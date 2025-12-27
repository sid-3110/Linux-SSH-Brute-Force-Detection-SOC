DOCUMENTATION

Summary:
Multiple failed SSH authentication attempts were detected on a production Linux server targeting a privileged account from an external IP address during non-business hours.

Assessment:
Event correlation revealed repeated authentication failures from the same external source within a short time window, consistent with an automated SSH brute-force attempt. No successful authentication events were observed.

Action Taken:
The alert was escalated to SOC Level 2 with supporting evidence for deeper investigation and appropriate containment actions.
