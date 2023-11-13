UnauthorizedAccess:EC2/RDPBruteForce
------------------------------------


### An EC2 instance has been involved in RDP brute force attacks.


**Default severity: Low\***


###### Note

This finding's severity is low if your EC2 instance was the target of a brute force attack. This finding's severity is high if your EC2 instance is the actor being used to perform the brute force attack.


 * **Data source:** VPC flow logs

This finding informs you that an EC2 instance in your AWS environment was involved in a brute force attack aimed at obtaining passwords to RDP services on Windows-based systems. This can indicate unauthorized access to your AWS resources.


**Remediation recommendations:**


If your instance's **Resource Role** is `ACTOR`, this indicates your instance has been used to perform RDP brute force attacks. Unless this instance has a legitimate reason to be contacting the IP address listed as the `Target`, it is recommended that you assume your instance has been compromised and take the actions listed in [Remediating a compromised Amazon EC2 instance](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-ec2). 


If your instance's **Resource Role** is `TARGET`, this finding can be remediated by securing your RDP port to only trusted IPs through Security Groups, ACLs, or firewalls. For more information see [Tips for securing your EC2 instances (Linux)](http://aws.amazon.com/articles/tips-for-securing-your-ec2-instance/).

