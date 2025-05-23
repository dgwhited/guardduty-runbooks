Impact:S3/AnomalousBehavior.Permission
--------------------------------------

### An API commonly used to set the access control list (ACL) permissions was invoked in an anomalous way.

**Default severity: High**

* **Data source:** CloudTrail data events for S3

This finding informs you that an IAM entity in your AWS environment has changed a bucket policy or ACL on the listed S3 buckets. This change may publicly expose your S3 buckets to all the authenticated AWS users.

This API was identified as anomalous by GuardDuty's anomaly detection machine learning (ML) model. The ML model evaluates all the API requests in your account and identifies anomalous events that are associated with techniques used by adversaries. It tracks various factors of the API requests, such as the user who made the request, the location from which the request was made, the specific API that was requested, the bucket that was requested, and the number of API calls made. For more information on which factors of the API request are unusual for the user identity that invoked the request, see [Finding details](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_findings-summary.html#finding-anomalous).

**Remediation recommendations:**

If this activity is unexpected for the associated principal, it may indicate that the credentials have been exposed or your S3 permissions are not restrictive enough. For more information, see [Remediating a potentially compromised S3 bucket](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-s3.html).

We recommend an audit of your S3 bucket's contents to ensure that no objects were unexpectedly allowed to be accessed publicly.