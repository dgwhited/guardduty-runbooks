UnauthorizedAccess:S3/MaliciousIPCaller.Custom
----------------------------------------------


### An S3 API was invoked from an IP address on a custom threat list.


**Default severity: High**


 * **Data source:** CloudTrail data events for S3

This finding informs you that an S3 API operation, for example, `PutObject` or `PutObjectAcl`, was invoked from an IP address that is included on a threat list that you uploaded. The threat list associated with this finding is listed in the **Additional information** section of a finding's details.


**Remediation recommendations:**


If this activity is unexpected for the associated principal, it may indicate that the credentials have been exposed or your S3 permissions are not restrictive enough. For more information, see [Remediating a compromised S3 bucket](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-s3).

