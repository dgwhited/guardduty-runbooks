Execution:EC2/MaliciousFile!AMI
-------------------------------

### A malicious file has been detected in an EC2 AMI.

**Default severity: Varies depending on the detected threat.**

* **Feature:** Malware Protection for Backup

This finding indicates that a GuardDuty Malware Protection for Backup scan has detected one or more malicious files in an AMI within your environment. For more information, view the Threats detected section in the finding details panel.

**Remediation recommendations:**

If this is unexpected, your AMI may be compromised. For more information, see [Remediating a potentially compromised EC2 AMI](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-ami.html).