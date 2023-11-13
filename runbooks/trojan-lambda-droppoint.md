Trojan:Lambda/DropPoint
-----------------------


### A Lambda function is attempting to communicate with an IP address of a remote host that is known to hold credentials and other stolen data captured by malware.


**Default severity: Medium**


 * **Feature:** Lambda Network Activity Monitoring

This finding informs you that a listed Lambda function within your AWS environment is trying to communicate with an IP address of a remote host that is known to hold credentials and other stolen data captured by malware.


**Remediation recommendations:**


If this activity is unexpected, your Lambda function may be compromised. For more information, see [Remediating a compromised Lambda function](https://docs.aws.amazon.com/guardduty/latest/ug/remediate-lambda-protection-finding-types.html).

