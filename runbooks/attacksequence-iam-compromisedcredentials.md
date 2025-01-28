

AttackSequence:IAM/CompromisedCredentials
-----------------------------------------

### A sequence of API requests that were invoked by using potentially compromised AWS credentials.

* Default severity: Critical
* Data source: [AWS CloudTrail management events](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_data-sources.html#guardduty_controlplane)

This finding informs you that GuardDuty detected a sequence of suspicious actions made by using AWS credentials that impacts one or more resources in your environment. Multiple suspicious and anomalous attack behaviors were observed by the same credentials, resulting in higher confidence that the credentials are being misused.

GuardDuty uses its proprietary correlation algorithms to observe and identify the sequence of actions performed by using the IAM credential. GuardDuty evaluates findings across protection plans and other signal sources to identify common and emerging attack patterns. GuardDuty uses multiple factors to surface threats, such as IP reputation, API sequences, user configuration, and potentially impacted resources.

**Remediation actions**: If this behavior is unexpected in your environment, then your AWS credentials may have been compromised. For steps to remediate, see [Remediating potentially compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-creds.html). The compromised credentials may have been used to create or modify additional resources, such as Amazon S3 buckets, AWS Lambda functions, or Amazon EC2 instances, in your environment. For steps to remediate other resources that may have been potentially impacted, see [Remediating detected GuardDuty security findings](./guardduty_remediate.html).

