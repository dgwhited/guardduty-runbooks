Backdoor:EC2/C&CActivity.B
--------------------------


### An EC2 instance is querying an IP that is associated with a known command and control server.


**Default severity: High**


 * **Data source:** VPC flow logs

This finding informs you that the listed instance within your AWS environment is querying an IP associated with a known command and control (C&C) server. The listed instance might be compromised. Command and control servers are computers that issue commands to members of a botnet. 


A botnet is a collection of internet-connected devices which might include PCs, servers, mobile devices, and Internet of Things devices, that are infected and controlled by a common type of malware. Botnets are often used to distribute malware and gather misappropriated information, such as credit card numbers. Depending on the purpose and structure of the botnet, the C&C server might also issue commands to begin a distributed denial of service (DDoS) attack.


###### Note

If the IP queried is log4j-related, then fields of the associated finding will include the following values:

 * service.additionalInfo.threatListName = Amazon
* service.additionalInfo.threatName = Log4j Related

**Remediation recommendations:**


If this activity is unexpected, your instance may be compromised. For more information, see [Remediating a compromised Amazon EC2 instance](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-ec2).

