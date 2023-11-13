Policy:S3/AccountBlockPublicAccessDisabled
------------------------------------------


### An IAM entity invoked an API used to disable S3 Block Public Access on an account.


**Default severity: Low**


 * **Data source:** CloudTrail management events

This finding informs you that Amazon S3 Block Public Access was disabled at the account level. When S3 Block Public Access settings are enabled, they are used to filter the policies or access control lists (ACLs) on buckets as a security measure to prevent inadvertent public exposure of data. 


Typically, S3 Block Public Access is turned off in an account to allow public access to a bucket or to the objects in the bucket. When S3 Block Public Access is disabled for an account, access to your buckets is controlled by the policies, ACLs, or bucket-level Block Public Access settings applied to your individual buckets. This does not necessarily mean that the buckets are shared publicly, but that you should audit the permissions applied to the buckets to confirm that they provide the appropriate level of access.


**Remediation recommendations:**


If this activity is unexpected for the associated principal, it may indicate that the credentials have been exposed or your S3 permissions are not restrictive enough. For more information, see [Remediating a compromised S3 bucket](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-s3).

