UnauthorizedAccess:IAMUser/ConsoleLoginSuccess.B
------------------------------------------------


### Multiple worldwide successful console logins were observed.


**Default severity: Medium**


 * **Data source:** CloudTrail management events

This finding informs you that multiple successful console logins for the same IAM user were observed around the same time in various geographical locations. Such anomalous and risky access location patterns indicate potential unauthorized access to your AWS resources. 


**Remediation recommendations:**


If this activity is unexpected, your credentials may be compromised. For more information, see [Remediating compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-creds).

