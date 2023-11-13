Stealth:S3/ServerAccessLoggingDisabled
--------------------------------------


### S3 server access logging was disabled for a bucket.


**Default severity: Low**


 * **Data source:** CloudTrail management events

This finding informs you that S3 server access logging is disabled for a bucket within your AWS environment. If disabled, no web request logs are created for any attempts to access the identified S3 bucket, however, S3 management API calls to the bucket, such as [DeleteBucket](https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucket.html), are still tracked. If S3 data event logging is enabled through CloudTrail for this bucket, web requests for objects within the bucket will still be tracked. Disabling logging is a technique used by unauthorized users in order to evade detection. To learn more about S3 logs, see  [S3 Server Access Logging](https://docs.aws.amazon.com/AmazonS3/latest/dev/ServerLogs.html) and [S3 Logging Options](https://docs.aws.amazon.com/AmazonS3/latest/userguide/logging-with-S3.html) .


**Remediation recommendations:**


If this activity is unexpected for the associated principal, it may indicate that the credentials have been exposed or your S3 permissions are not restrictive enough. For more information, see [Remediating a compromised S3 bucket](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-s3).

