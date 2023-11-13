UnauthorizedAccess:Lambda/MaliciousIPCaller.Custom
--------------------------------------------------


### A Lambda function is making connections to an IP address on a custom threat list.


**Default severity: Medium**


 * **Feature:** Lambda Network Activity Monitoring

This finding informs you that a Lambda function in your AWS environment is communicating with an IP address included on a threat list that you uploaded. In GuardDuty, a [threat list](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_upload-lists.html) consists of known malicious IP addresses. GuardDuty generates findings based on the uploaded threat lists. You can view the details of the threat list in the finding details on the GuardDuty console.


**Remediation recommendations:**


If this activity is unexpected, your Lambda function may be compromised. For more information, see [Remediating a compromised Lambda function](https://docs.aws.amazon.com/guardduty/latest/ug/remediate-lambda-protection-finding-types.html).

