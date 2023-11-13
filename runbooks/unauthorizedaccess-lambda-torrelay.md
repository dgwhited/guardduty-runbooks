UnauthorizedAccess:Lambda/TorRelay
----------------------------------


### A Lambda function is making connections to a Tor network as a Tor relay.


**Default severity: High**


 * **Feature:** Lambda Network Activity Monitoring

This finding informs you that a Lambda function in your AWS environment is making connections to a Tor network in a manner that suggests that it's acting as a Tor relay. Tor is software for enabling anonymous communication. Tor enables anonymous communication by forwarding the client's potentially illicit traffic from one Tor relay to another. 


**Remediation recommendations:**


If this activity is unexpected, your Lambda function may be compromised. For more information, see [Remediating a compromised Lambda function](https://docs.aws.amazon.com/guardduty/latest/ug/remediate-lambda-protection-finding-types.html).



