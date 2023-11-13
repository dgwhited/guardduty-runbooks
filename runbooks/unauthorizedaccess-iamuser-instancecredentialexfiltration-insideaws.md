UnauthorizedAccess:IAMUser/InstanceCredentialExfiltration.InsideAWS
-------------------------------------------------------------------


### Credentials that were created exclusively for an EC2 instance through an Instance launch role are being used from another account within AWS.


**Default severity: High\***


###### Note

This finding's default severity is High. However, if the API was invoked by an account affiliated with your AWS environment, the severity is Medium.


 * **Data source:** CloudTrail management events or S3 data events

This finding informs you when your EC2 instance credentials are used to invoke APIs from an IP address that is owned by a different AWS account than the one that the associated EC2 instance is running in.


AWS does not recommend redistributing temporary credentials outside of the entity that created them (for example, AWS applications, EC2, or Lambda). However, authorized users can export credentials from their EC2 instances to make legitimate API calls. If the `remoteAccountDetails.Affiliated` field is `True` the API was invoked from an account associated with your AWS environment. To rule out a potential attack and verify the legitimacy of the activity, contact the IAM user to whom these credentials are assigned.


###### Note

If GuardDuty observes continued activity from a remote account, its machine learning (ML) model will identify this as an expected behavior. Therefore, GuardDuty will stop generating this finding for activity from that remote account. GuardDuty will continue to generate findings for new behavior from other remote accounts and will re-evaluate learned remote accounts as the behavior changes over time.


**Remediation recommendations:**


In response to this finding you can use the following workflow to determine a course of action:


 1. Identify the remote account involved from the `service.action.awsApiCallAction.remoteAccountDetails.accountId` field.
2. Next determine if that account is affiliated with your GuardDuty environment from the `service.action.awsApiCallAction.remoteAccountDetails.affiliated` field.
3. If the account is affiliated, contact the remote account owner, and the owner of the EC2 instance credentials to investigate.
4. If the account is not affiliated, first evaluate is that account is associated with your organization but is not a part of your GuardDuty multi-account set up, or if GuardDuty has not yet been enabled in the account. Otherwise contact the owner of the EC2 credentials to determine if there is a use case for a remote account to use these credentials.
5. If the owner of the credentials does not recognize the remote account the credentials may have been compromised by a threat actor operating within AWS. You should take the steps recommended in [Remediating a compromised Amazon EC2 instance](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-ec2) to secure your environment. Additionally you can [submit an abuse report](https://support.aws.amazon.com/#/contacts/report-abuse) to the AWS Trust and Safety team to begin an investigation into the remote account. When submitting your report to AWS Trust and Safety please include the full JSON details of the finding.
