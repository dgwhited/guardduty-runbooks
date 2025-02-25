Execution:EC2/MaliciousFile
---------------------------

### A malicious file has been detected on an EC2 instance.

**Default severity: Varies depending on the detected threat.**

* **Feature:** EBS Malware Protection

This finding indicates that the GuardDuty Malware Protection for EC2 scan has detected one or more malicious files on the listed EC2 instance within your AWS environment. This listed instance might be compromised. For more information, see **Threats detected** section in the findings' details.

**Remediation recommendations:**

If this activity is unexpected, your instance may be compromised. For more information, see [Remediating a potentially compromised Amazon EC2 instance](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-ec2.html).