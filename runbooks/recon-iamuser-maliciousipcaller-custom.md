Recon:IAMUser/MaliciousIPCaller.Custom
--------------------------------------


### An API was invoked from a known malicious IP address.


**Default severity: Medium**


 * **Data source:** CloudTrail management events

This finding informs you that an API operation that can list or describe AWS resources in an account within your environment was invoked from an IP address that is included on a custom threat list. The threat list used will be listed in the finding's details. An attacker might use stolen credentials to perform this type of reconnaissance of your AWS resources in order to find more valuable credentials or determine the capabilities of the credentials they already have.


**Remediation recommendations:**


If this activity is unexpected, your credentials may be compromised. For more information, see [Remediating compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-creds).

