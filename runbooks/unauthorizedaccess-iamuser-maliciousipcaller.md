

UnauthorizedAccess:IAMUser/MaliciousIPCaller
--------------------------------------------

### An API was invoked from a known malicious IP address.

**Default severity: Medium**

* **Data source:** CloudTrail management events

This finding informs you that an API operation (for example, an attempt to launch an EC2 instance, create a new IAM user, or modify your AWS privileges) was invoked from a known malicious IP address. This can indicate unauthorized access to AWS resources within your environment.

**Remediation recommendations:**

If this activity is unexpected, your credentials may be compromised. For more information, see [Remediating potentially compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-creds.html).

