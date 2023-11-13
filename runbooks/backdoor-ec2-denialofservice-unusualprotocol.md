Backdoor:EC2/DenialOfService.UnusualProtocol
--------------------------------------------


### An EC2 instance is behaving in a manner that may indicate it is being used to perform a Denial of Service (DoS) attack using an unusual protocol.


**Default severity: High**


 * **Data source:** VPC flow logs

This finding informs you that the listed EC2 instance in your AWS environment is generating a large volume of outbound traffic from an unusual protocol type that is not typically used by EC2 instances, such as Internet Group Management Protocol. This may indicate that the instance is compromised and is being used to perform denial-of-service (DoS) attacks using an unusual protocol. This finding detects DoS attacks only against publicly routable IP addresses, which are primary targets of DoS attacks.


**Remediation recommendations:**


If this activity is unexpected, your instance may be compromised. For more information, see [Remediating a compromised Amazon EC2 instance](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-ec2).

