Backdoor:Runtime/C&CActivity.B
------------------------------

### An Amazon EC2 instance or a container is querying an IP that is associated with a known command and control server.

**Default severity: High**

* **Feature:** Runtime Monitoring

This finding informs you that a process running on the listed EC2 instance or a container within your AWS environment is querying an IP address associated with a known command and control (C&C) server. The listed instance or container might be potentially compromised. Command and control servers are computers that issue commands to members of a botnet.

A botnet is a collection of internet-connected devices that might include PCs, servers, mobile devices, and Internet of Things devices, that are infected and controlled by a common type of malware. Botnets are often used to distribute malware and gather misappropriated information, such as credit card numbers. Depending on the purpose and structure of the botnet, the C&C server might also issue commands to begin a distributed denial of service (DDoS) attack.

###### Note

If the IP queried is log4j-related, then the fields of the associated finding will include the following values:

* `service.additionalInfo.threatListName = Amazon`
* `service.additionalInfo.threatName = Log4j Related`

The GuardDuty runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console. Additional context, including process and process lineage information, is available in the finding for further investigation.

**Remediation recommendations:**

If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).