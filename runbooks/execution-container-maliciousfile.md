Execution:Container/MaliciousFile
---------------------------------

### A malicious file has been detected on a standalone container.

**Default severity: Varies depending on the detected threat.**

* **Feature:** EBS Malware Protection

This finding indicates that the GuardDuty Malware Protection for EC2 scan has detected one or more malicious files on a container workload and no cluster information has been identified. For more information, see **Threats detected** section in the findings' details.

**Remediation recommendations:**

If this activity is unexpected, your container workload may be compromised. For more information, see [Remediating a potentially compromised standalone container](https://docs.aws.amazon.com/guardduty/latest/ug/remediate-compromised-standalone-container.html).