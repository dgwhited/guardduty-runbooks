Impact:EC2/MaliciousDomainRequest.Custom
----------------------------------------

### An EC2 instance is querying a domain on a custom threat entity list.

**Default severity: Medium**

* **Data source:** DNS logs

This finding informs you that the listed Amazon EC2 instance within your AWS environment is querying a domain name that is included in threat entity list that you uploaded and activated. In GuardDuty, a threat entity list consists of known malicious domain names and IP addresses. GuardDuty generates findings based on the activity associated with the uploaded threat entity list. You can view name of the threat entity list in the finding details.

**Remediation recommendations:**

If this activity is unexpected, your instance may be compromised. For more information, see [Remediating a potentially compromised Amazon EC2 instance](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-ec2.html).