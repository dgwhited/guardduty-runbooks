AttackSequence:ECS/CompromisedCluster
-------------------------------------

### A sequence of suspicious actions performed by potentially compromised Amazon ECS cluster.

* Default severity: Critical
* Data sources:

  + [Runtime Monitoring for Amazon ECS Fargate](https://docs.aws.amazon.com/guardduty/latest/ug/how-runtime-monitoring-works-ecs-fargate.html)
  + [Runtime Monitoring for EC2 Instances in Amazon ECS](https://docs.aws.amazon.com/guardduty/latest/ug/how-runtime-monitoring-works-ec2.html)
  + [GuardDuty Malware Protection for Amazon EC2](https://docs.aws.amazon.com/guardduty/latest/ug/malware-protection.html)

This finding informs you that GuardDuty detected a sequence of suspicious signals indicating a potentially compromised Amazon ECS cluster in your environment. These signals may include malicious processes, communications with malicious endpoints, or cryptocurrency mining behaviors.

GuardDuty uses proprietary correlation algorithms and multiple detection factors to identify sequences of suspicious actions within Amazon ECS clusters. Through analysis across protection plans and various signal sources, GuardDuty identifies common and emerging attack patterns, providing high-confidence detection of potential compromises.

**Remediation actions**: If this behavior is unexpected in your environment, your Amazon ECS cluster may be compromised. For threat containment recommendations, see [Remediating a potentially compromised ECS cluster](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-ecs.html). Note that the compromise may extend to one or more ECS tasks or container workloads, which could have been used to create or modify AWS resources. For comprehensive remediation guidance covering potentially impacted resources, see [Remediating detected GuardDuty security findings](./guardduty_remediate.html).