Execution:EC2/MaliciousFile!RecoveryPoint
-----------------------------------------

### A malicious file has been detected in an AWS Backup EC2 Recovery Point.

**Default severity: Varies depending on the detected threat.**

* **Feature:** Malware Protection for Backup

This finding indicates that a GuardDuty Malware Protection for Backup scan has detected one or more malicious files in an EC2 recovery point within your environment. The impacted Recovery Point could be an EBS snapshot or an EC2 AMI. For more information, view the Threats detected section in the finding details panel.

**Remediation recommendations:**

If this is unexpected, your EC2 recovery point may be compromised. For more information, see [Remediating a potentially compromised EC2 Recovery Point](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-ec2-recoverypoint.html).