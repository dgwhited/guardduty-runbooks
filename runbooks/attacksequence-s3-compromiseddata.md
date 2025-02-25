AttackSequence:S3/CompromisedData
---------------------------------

### A sequence of API requests was invoked in a potential attempt to exfiltrate or destroy data in Amazon S3.

* Default severity: Critical
* Data sources: [AWS CloudTrail data events for S3](https://docs.aws.amazon.com/guardduty/latest/ug/s3-protection.html#guardduty_s3dataplane) and [AWS CloudTrail management events](./guardduty_data-sources.html#guardduty_controlplane)

This finding informs you that GuardDuty detected a sequence of suspicious actions indicative of data compromise in one or more Amazon Simple Storage Service (Amazon S3) buckets, by using potentially compromised AWS credentials. Multiple suspicious and anomalous attack behaviors (API requests) were observed, resulting in higher confidence of the credentials are being misused.

GuardDuty uses its correlation algorithms to observe and identify the sequence of actions performed by using the IAM credential. GuardDuty then evaluates findings across protection plans and other signal sources to identify common and emerging attack patterns. GuardDuty uses multiple factors to surface threats, such as IP reputation, API sequences, user configuration, and potentially impacted resources.

**Remediation actions**: If this activity is unexpected in your environment, your AWS credentials, or Amazon S3 data may have potentially exfiltrated or destroyed. For steps to remediate, see [Remediating potentially compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-creds.html) and [Remediating a potentially compromised S3 bucket](./compromised-s3.html).