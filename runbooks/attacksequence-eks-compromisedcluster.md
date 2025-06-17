AttackSequence:EKS/CompromisedCluster
-------------------------------------

### A sequence of suspicious actions performed by potentially compromised Amazon EKS cluster.

* Default severity: Critical
* Data sources:

  + [EKS audit log events](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty/latest/ug/kubernetes-protection.html#guardduty_k8s-audit-logs)
  + [Runtime Monitoring for Amazon EKS](https://docs.aws.amazon.com/guardduty/latest/ug/how-runtime-monitoring-works-eks.html)
  + [Amazon EKS malware detection for Amazon EC2](https://docs.aws.amazon.com/guardduty/latest/ug/malware-protection.html)
  + [AWS CloudTrail data events for S3](./s3-protection.html#guardduty_s3dataplane)
  + [AWS CloudTrail management events](./guardduty_data-sources.html#guardduty_controlplane)
  + [VPC Flow Logs](./guardduty_data-sources.html#guardduty_vpc)
  + [Route53 Resolver DNS query logs](./guardduty_data-sources.html#guardduty_dns)

This finding informs you that GuardDuty detected a sequence of suspicious actions that indicates a potentially compromised Amazon EKS cluster in your environment. Multiple suspicious and anomalous attack behaviors, such as malicious processes or connection with malicious endpoints, were observed in the same Amazon EKS cluster.

GuardDuty uses its proprietary correlation algorithms to observe and identify the sequence of actions performed by using the IAM credential. GuardDuty evaluates findings across protection plans and other signal sources to identify common and emerging attack patterns. GuardDuty uses multiple factors to surface threats, such as IP reputation, API sequences, user configuration, and potentially impacted resources.

**Remediation actions**: If this behavior is unexpected in your environment, then your Amazon EKS cluster may be compromised. For comprehensive remediation guidance, see [Remediating EKS Protection findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-kubernetes.html) and [Remediating Runtime Monitoring findings](./guardduty-remediate-runtime-monitoring.html).

Additionally, since AWS credentials may have been compromised through the EKS cluster, see [Remediating potentially compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-creds.html). For steps to remediate other resources that may have been potentially impacted, see [Remediating detected GuardDuty security findings](./guardduty_remediate.html).