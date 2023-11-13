Trojan:EC2/DropPoint
--------------------


### An EC2 instance is attempting to communicate with an IP address of a remote host that is known to hold credentials and other stolen data captured by malware.


**Default severity: Medium**


 * **Data source:** VPC flow logs

This finding informs you that an EC2 instance in your AWS environment is trying to communicate with an IP address of a remote host that is known to hold credentials and other stolen data captured by malware.


**Remediation recommendations:**


If this activity is unexpected, your instance may be compromised. For more information, see [Remediating a compromised Amazon EC2 instance](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-ec2).

