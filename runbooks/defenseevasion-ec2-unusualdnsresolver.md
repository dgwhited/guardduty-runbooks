DefenseEvasion:EC2/UnusualDNSResolver
-------------------------------------


### An Amazon EC2 instance is communicating with an unusual public DNS resolver.


**Default severity: Medium**


 * **Data source:** VPC flow logs

This finding informs you that the listed Amazon EC2 instance in your AWS environment is behaving in a way that deviates from the baseline behavior. This EC2 instance has no recent history of communicating with this public DNS resolver. The **Unusual** field in the finding details panel in the GuardDuty console can provide information about the queried DNS resolver.


**Remediation recommendations:**


If this activity is unexpected, your instance may be compromised. For more information, see [Remediating a compromised Amazon EC2 instance](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-ec2).

