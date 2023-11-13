UnauthorizedAccess:Lambda/TorClient
-----------------------------------


### A Lambda function is making connections to a Tor Guard or an Authority node.


**Default severity: High**


 * **Feature:** Lambda Network Activity Monitoring

This finding informs you that a Lambda function in your AWS environment is making connections to a Tor Guard or an Authority node. Tor is software for enabling anonymous communication. Tor Guards and Authority node act as initial gateways into a Tor network. This traffic can indicate that this Lambda function has been potentially compromised. It is now acting as a client on a Tor network.


**Remediation recommendations:**


If this activity is unexpected, your Lambda function may be compromised. For more information, see [Remediating a compromised Lambda function](https://docs.aws.amazon.com/guardduty/latest/ug/remediate-lambda-protection-finding-types.html).

