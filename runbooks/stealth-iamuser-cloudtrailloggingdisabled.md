Stealth:IAMUser/CloudTrailLoggingDisabled
-----------------------------------------


### AWS CloudTrail logging was disabled.


**Default severity: Low**


 * **Data source:** CloudTrail management events

This finding informs you that a CloudTrail trail within your AWS environment was disabled. This can be an attacker's attempt to disable logging to cover their tracks by eliminating any trace of their activity while gaining access to your AWS resources for malicious purposes. This finding can be triggered by a successful deletion or update of a trail. This finding can also be triggered by a successful deletion of an S3 bucket that stores the logs from a trail that is associated with GuardDuty.


**Remediation recommendations:**


If this activity is unexpected, your credentials may be compromised. For more information, see [Remediating compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-creds).

