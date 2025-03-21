Execution:ECS/MaliciousFile
---------------------------

### A malicious file has been detected on an ECS cluster.

**Default severity: Varies depending on the detected threat.**

* **Feature:** EBS Malware Protection

This finding indicates that the GuardDuty Malware Protection for EC2 scan has detected one or more malicious files on a container workload that belongs to an ECS cluster. For more information, see **Threats detected** section in the findings' details.

**Remediation recommendations:**

If this activity is unexpected, your container belonging to the ECS cluster may be compromised. For more information, see [Remediating a potentially compromised ECS cluster](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-ecs.html).