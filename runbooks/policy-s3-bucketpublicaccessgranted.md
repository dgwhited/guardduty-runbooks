

Policy:S3/BucketPublicAccessGranted
-----------------------------------

### An IAM principal has granted public access to an S3 bucket to all AWS users by changing bucket policies or ACLs.

**Default severity: High**

* **Data source:** CloudTrail management events

This finding informs you that the listed S3 bucket has been publicly exposed to all authenticated AWS users because an IAM entity has changed a bucket policy or ACL on that S3 bucket.

After a policy or ACL change is detected, GuardDuty uses automated reasoning powered by [Zelkova](https://aws.amazon.com/blogs/security/protect-sensitive-data-in-the-cloud-with-automated-reasoning-zelkova/), to determine if the bucket is publicly accessible.

###### Note

If a bucket's ACLs or bucket policies are configured to explicitly deny or to deny all, this finding may not reflect the current state of the bucket. This finding will not reflect any [S3 Block Public Access](https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-control-block-public-access.html) settings that may have been enabled for your S3 bucket. In such cases, the `effectivePermission` value in the finding will be marked as `UNKNOWN`.

**Remediation recommendations:**

If this activity is unexpected for the associated principal, it may indicate that the credentials have been exposed or your S3 permissions are not restrictive enough. For more information, see [Remediating a potentially compromised S3 bucket](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-s3.html).

