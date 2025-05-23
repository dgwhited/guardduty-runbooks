Impact:Runtime/SuspiciousDomainRequest.Reputation
-------------------------------------------------

### An Amazon EC2 instance or a container is querying a low reputation domain name that is suspicious in nature due to its age, or low popularity.

**Default severity: Low**

* **Feature:** Runtime Monitoring

This finding informs you that a process running on the listed EC2 instance or the container within your AWS environment is querying a low reputation domain name that is suspected of being malicious. The observed characteristics of this domain were consistent with previously observed malicious domains. However, our reputation model was unable to definitively relate it to a known threat. These domains are typically newly observed or receive a low amount of traffic.

Low reputation domains are based on a reputation score model. This model evaluates and ranks the characteristics of a domain to determine its likelihood of being malicious.

The GuardDuty runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console. Additional context, including process and process lineage information, is available in the finding for further investigation.

**Remediation recommendations:**

If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).