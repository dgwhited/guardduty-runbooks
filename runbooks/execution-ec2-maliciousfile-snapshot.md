Execution:EC2/MaliciousFile!Snapshot
------------------------------------

### A malicious file has been detected in an EBS snapshot.

**Default severity: Varies depending on the detected threat.**

* **Feature:** Malware Protection for Backup

This finding indicates that a GuardDuty Malware Protection for Backup scan has detected one or more malicious files in an EBS snapshot within your environment. For more information, view the Threats detected section in the finding details panel.

**Remediation recommendations:**

If this is unexpected, your snapshot may be compromised. For more information, see [Remediating a potentially compromised EBS Snapshot](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-snapshot.html).