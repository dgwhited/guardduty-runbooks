Trojan:Lambda/BlackholeTraffic
------------------------------


### A Lambda function is attempting to communicate with an IP address of a remote host that is a known black hole.


**Default severity: Medium**


 * **Feature:** Lambda Network Activity Monitoring

This finding informs you that a listed Lambda function within your AWS environment is trying to communicate with an IP address of a black hole (or a sink hole). Black holes are places in the network where incoming or outgoing traffic is silently discarded without informing the source that the data didn't reach its intended recipient. A black hole IP address specifies a host machine that is not running or an address to which no host has been assigned. The listed Lambda function is potentially compromised.


**Remediation recommendations:**


If this activity is unexpected, your Lambda function may be compromised. For more information, see [Remediating a compromised Lambda function](https://docs.aws.amazon.com/guardduty/latest/ug/remediate-lambda-protection-finding-types.html).

