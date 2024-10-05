Policy:IAMUser/RootCredentialUsage
----------------------------------


### An API was invoked using root user sign\-in credentials.


**Default severity: Low**


 * **Data source:** CloudTrail management events or CloudTrail data events for S3

This finding informs you that the root user sign\-in credentials of the listed AWS account in your environment are being used to make requests to AWS services. It is recommended that users never use root user sign\-in credentials to access AWS services. Instead, AWS services should be accessed using least privilege temporary credentials from AWS Security Token Service (STS). For situations where AWS STS is not supported, IAM user credentials are recommended. For more information, see [IAM Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html).


###### Note

If S3 Protection is enabled for the account, then this finding may be generated in response to the attempts to run S3 data plane operations on Amazon S3 resources by using the root user sign\-in credentials of the AWS account. The API call used will be listed in the finding details. If S3 Protection is not enabled, then this finding can only be triggered by Event log APIs. For more information about S3 Protection, see [S3 Protection](https://docs.aws.amazon.com/guardduty/latest/ug/s3-protection.html).


**Remediation recommendations:**


If this activity is unexpected, your credentials may be compromised. For more information, see [Remediating potentially compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-creds.html).

