Execution:Kubernetes/MaliciousFile
----------------------------------

### A malicious file has been detected on an Kubernetes cluster.

**Default severity: Varies depending on the detected threat.**

* **Feature:** EBS Malware Protection

This finding indicates that the GuardDuty Malware Protection for EC2 scan has detected one or more malicious files on a container workload that belongs to a Kubernetes cluster. If this is an EKS managed cluster, the findings details will provide additional information about the impacted EKS resource. For more information, see **Threats detected** section in the findings' details.

**Remediation recommendations:**

If this activity is unexpected, your container workload may be compromised. For more information, see [Remediating EKS Protection findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-kubernetes.html).