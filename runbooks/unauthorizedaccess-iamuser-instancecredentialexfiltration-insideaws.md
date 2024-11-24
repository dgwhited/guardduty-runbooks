

UnauthorizedAccess:IAMUser/InstanceCredentialExfiltration.InsideAWS
-------------------------------------------------------------------

### Credentials that were created exclusively for an EC2 instance through an Instance launch role are being used from another account within AWS.

**Default severity: High\***

###### Note

This finding's default severity is High. However, if the API was invoked by an account affiliated with your AWS environment, the severity is Medium.


* **Data source:** CloudTrail management events or CloudTrail data events for S3

This finding informs you when your Amazon EC2 instance credentials are used to invoke APIs from an IP address or an Amazon VPC endpoint, that is owned by a different AWS account than the one that the associated Amazon EC2 instance is running in. VPC endpoint detection is only available for services that support network activity events for VPC endpoints. For information about services that support network activity events for VPC endpoints, see [Logging network activity events](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-network-events-with-cloudtrail.html) in the *AWS CloudTrail User Guide*.

AWS does not recommend redistributing temporary credentials outside of the entity that created them (for example, AWS applications, Amazon EC2, or AWS Lambda). However, authorized users can export credentials from their Amazon EC2 instances to make legitimate API calls. If the `remoteAccountDetails.Affiliated` field is `True` the API was invoked from an account associated with the same administrator account. To rule out a potential attack and verify the legitimacy of the activity, contact the AWS account owner or IAM principal to whom these credentials are assigned.

###### Note

If GuardDuty observes continued activity from a remote account, its machine learning (ML) model will identify this as an expected behavior. Therefore, GuardDuty will stop generating this finding for activity from that remote account. GuardDuty will continue to generate findings for new behavior from other remote accounts and will re-evaluate learned remote accounts as the behavior changes over time.

**Remediation recommendations:**

This finding gets generated when AWS API requests are made inside AWS through an Amazon EC2 instance outside of your AWS account, by using your Amazon EC2 instance's session credentials. It may be customary, such as for Transit Gateway architecture in a [hub and spoke](https://docs.aws.amazon.com/whitepapers/latest/building-scalable-secure-multi-vpc-network-infrastructure/transit-vpc-solution.html) configuration, to route traffic through a single hub egress VPC with AWS service endpoints. If this behavior is expected, then GuardDuty recommends you to use [Suppression rules](./findings_suppression-rule.html) and create a rule with a two-filter criteria. The first criteria is the finding type, which, in this case, is UnauthorizedAccess:IAMUser/InstanceCredentialExfiltration.InsideAWS. The second filter criteria is the remote account ID of the remote account details.

In response to this finding you can use the following workflow to determine a course of action:

1. Identify the remote account involved from the `service.action.awsApiCallAction.remoteAccountDetails.accountId` field.
2. Determine if that account is affiliated with your GuardDuty environment from the `service.action.awsApiCallAction.remoteAccountDetails.affiliated` field.
3. If the account **is** affiliated, contact the remote account owner and the owner of the Amazon EC2 instance credentials to investigate.
   
   If the account **is not** affiliated, then the first step is to evaluate if that account is associated with your organization but is not a part of your GuardDuty multiple-account environment set up, or if GuardDuty has not yet been enabled in this account. Next, contact the owner of the Amazon EC2 instance credentials to determine if there is a use case for a remote account to use these credentials.
4. If the owner of the credentials does not recognize the remote account the credentials may have been compromised by a threat actor operating within AWS. You should take the steps recommended in [Remediating a potentially compromised Amazon EC2 instance](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-ec2.html), to secure your environment.
   
   Additionally, you can [submit an abuse report](https://support.aws.amazon.com/#/contacts/report-abuse) to the AWS Trust and Safety team to begin an investigation into the remote account. When submitting your report to AWS Trust and Safety, include the full JSON details of the finding.
