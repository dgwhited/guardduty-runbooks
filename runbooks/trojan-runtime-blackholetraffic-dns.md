Trojan:Runtime/BlackholeTraffic!DNS
-----------------------------------


### An Amazon EC2 instance or a container is querying a domain name that is being redirected to a black hole IP address.


**Default severity: Medium**


 * **Feature:** Runtime Monitoring

This finding informs you the listed EC2 instance or the container in your AWS environment might be compromised because it is querying a domain name that is being redirected to a black hole IP address. Black holes are places in the network where incoming or outgoing traffic is silently discarded without informing the source that the data didn't reach its intended recipient.


The runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console.


If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating EKS Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-eks-runtime-monitoring.html).

