DefenseEvasion:IAMUser/BedrockLoggingDisabled
---------------------------------------------

### Logging for Amazon Bedrock was disabled.

**Default severity: Medium**

* **Data source:** CloudTrail management events

This finding informs you that logging was disabled for Bedrock model invocations in your account. This can be an attacker's attempt to hide malicious activity like data exfiltration or abuse of AI models. Disabling logging removes visibility into the data sent to models and how the models are used.

**Remediation recommendations:**

If this activity is unexpected, your credentials may be compromised. For more information, see [Remediating potentially compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-creds.html).