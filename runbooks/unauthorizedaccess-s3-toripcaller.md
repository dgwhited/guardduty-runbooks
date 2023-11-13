UnauthorizedAccess:S3/TorIPCaller
---------------------------------


### An S3 API was invoked from a Tor exit node IP address.


**Default severity: High**


 * **Data source:** CloudTrail data events for S3

This finding informs you that an S3 API operation, such as `PutObject` or `PutObjectAcl`, was invoked from a Tor exit node IP address. Tor is software for enabling anonymous communication. It encrypts and randomly bounces communications through relays between a series of network nodes. The last Tor node is called the exit node. This finding can indicate unauthorized access to your AWS resources with the intent of hiding the attacker's true identity.


**Remediation recommendations:**


If this activity is unexpected for the associated principal, it may indicate that the credentials have been exposed or your S3 permissions are not restrictive enough. For more information, see [Remediating a compromised S3 bucket](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-s3).



