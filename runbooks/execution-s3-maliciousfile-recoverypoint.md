Execution:S3/MaliciousFile!RecoveryPoint
----------------------------------------

### A malicious file has been detected in an AWS Backup S3 Recovery Point.

**Default severity: Varies depending on the detected threat.**

* **Feature:** Malware Protection for Backup

This finding indicates that a GuardDuty Malware Protection for Backup scan has detected one or more malicious objects in an S3 Recovery Point within your environment. For more information, view the Threats detected section in the finding details panel.

**Remediation recommendations:**

If this is unexpected, your S3 recovery point may be compromised. For more information, see [Remediating a potentially compromised S3 Recovery Point](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-s3-recoverypoint.html).