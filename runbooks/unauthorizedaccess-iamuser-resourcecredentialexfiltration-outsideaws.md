UnauthorizedAccess:IAMUser/ResourceCredentialExfiltration.OutsideAWS
--------------------------------------------------------------------

### Credentials that were created exclusively for an AWS Lambda resource are being used from an IP address outside of AWS.

**Default severity: High**

* **Data source:** CloudTrail management events or CloudTrail data events for S3

This finding informs you that a host outside of AWS attempted to run AWS API operations using temporary AWS credentials that were created on a AWS Lambda resource in your AWS environment. The listed Lambda resource might be compromised, and the temporary credentials from this Lambda might have been exfiltrated to a remote host outside of AWS.

AWS does not recommend redistributing temporary credentials outside of the entity that created them (for example AWS applications like Amazon Elastic Compute Cloud (Amazon EC2), or AWS Lambda). However, authorized users can export credentials from their Lambda resources to make legitimate API calls. To rule out a potential attack and verify the legitimacy of the activity, validate if the use of instance credentials from the remote IP in the finding is expected.

###### Note

If GuardDuty observes continued activity from a remote host, its machine learning (ML) model will identify this as an expected behavior. Therefore, GuardDuty will stop generating this finding for activity from that remote host. GuardDuty will continue to generate findings for new behavior from other remote hosts and will re-evaluate learned remote hosts as the behavior changes over time.

**Remediation recommendations:**

This finding gets generated when networking is configured to route the internet traffic such that it egresses from an on-premises gateway rather than from a VPC Internet Gateway (IGW). Common configurations, such as using [AWS Outposts](https://docs.aws.amazon.com/outposts/latest/userguide/) or VPC VPN connections, can result in traffic routed this way. If this is expected behavior, then GuardDuty recommends using [Suppression rules](./findings_suppression-rule.html) to create a rule with a two-filter criteria. The first criteria is **finding type**, which should be `UnauthorizedAccess:IAMUser/ResourceCredentialExfiltration.OutsideAWS`. The second filter criteria is **API caller IPv4 Address** with the IP address or CIDR range for your on-premises internet gateway.

If this activity is unexpected, your credentials may have been compromised. For information about steps to remediate this finding type, see [Remediating potentially compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-creds.html).