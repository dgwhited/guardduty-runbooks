AttackSequence:EC2/CompromisedInstanceGroup
-------------------------------------------

### A sequence of suspicious actions indicating potentially compromised Amazon EC2 instances.

* Default severity: Critical
* Data sources:

  + [Runtime Monitoring for Amazon EC2](https://docs.aws.amazon.com/guardduty/latest/ug/how-runtime-monitoring-works-ec2.html)
  + [Malware detection for Amazon EC2](https://docs.aws.amazon.com/guardduty/latest/ug/malware-protection.html)
  + [VPC Flow Logs](./guardduty_data-sources.html#guardduty_vpc)
  + [Route53 Resolver DNS query logs](./guardduty_data-sources.html#guardduty_dns)

This finding indicates GuardDuty detected a sequence of suspicious actions suggesting potential compromise across a group of Amazon EC2 instances in your environment. Instance groups typically represent applications managed through infrastructure-as-code, sharing similar configurations such as Auto-scaling group, IAM instance profile role, AWS CloudFormation stack, Amazon EC2 launch template, AMI or VPC ID. GuardDuty observed multiple suspicious behaviors across one or more instances, including:

* Malicious processes
* Malicious files
* Suspicious network connections
* Cryptocurrency mining activities
* Suspicious usage of Amazon EC2 instance credentials

**Detection Method**: GuardDuty employs proprietary correlation algorithms to identify suspicious action sequences within Amazon EC2 instances. By evaluating findings across protection plans and various signal sources, GuardDuty identifies attack patterns using multiple factors such as IP and domain reputation and suspicious running processes.

**Remediation actions**: If this behavior is unexpected in your environment, your Amazon EC2 instances may be compromised. The compromise could involve:

* Multiple processes
* Instance credentials that may have been used to modify Amazon EC2 instances or other AWS resources

For threat containment recommendations, see [Remediating a potentially compromised Amazon EC2 instance](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-ec2.html). Note that the compromise may extend to one or more Amazon EC2 instances and involve compromised processes or instance credentials that could have been used to create or modify Amazon EC2 instances or other AWS resources. For comprehensive remediation guidance covering potentially impacted resources, see [Remediating detected GuardDuty security findings](./guardduty_remediate.html).