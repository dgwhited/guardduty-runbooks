DefenseEvasion:EC2/UnusualDoHActivity
-------------------------------------


### An Amazon EC2 instance is performing an unusual DNS over HTTPS (DoH) communication.


**Default severity: Medium**


 * **Data source:** VPC flow logs

This finding informs you that the listed Amazon EC2 instance within your AWS environment is behaving in a way that deviates from the established baseline. This EC2 instance doesn't have any recent history of DNS over HTTPS (DoH) communications with this public DoH server. The **Unusual** field in the finding details can provide information about the queried DoH server.


**Remediation recommendations:**


If this activity is unexpected, your instance may be compromised. For more information, see [Remediating a compromised Amazon EC2 instance](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-ec2).

