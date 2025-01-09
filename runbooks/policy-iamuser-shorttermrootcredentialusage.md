

Policy:IAMUser/ShortTermRootCredentialUsage
-------------------------------------------

### An API was invoked by using restricted root user credentials.

**Default severity: Low**

* **Data source:** AWS CloudTrail management events or AWS CloudTrail data events for S3

This finding informs you that restricted user credentials created for the listed AWS account in your environment, are being used to make requests to AWS services. It is recommended to use root user credentials only for those [tasks that require root user credentials](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html#root-user-tasks).

When possible, access the AWS services by using least privilege IAM roles with temporary credentials from AWS Security Token Service (AWS STS). For scenarios where AWS STS is not supported, the best practice is to use IAM user credentials. For more information, see [Security best practices in IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html) and [Root user best practices for your AWS account](https://docs.aws.amazon.com/IAM/latest/UserGuide/root-user-best-practices.html) in the *IAM User Guide*.

**Remediation recommendations:**

If this activity is unexpected, your credentials may be compromised. For more information, see [Remediating potentially compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-creds.html).

