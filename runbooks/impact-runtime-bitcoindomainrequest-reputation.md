Impact:Runtime/BitcoinDomainRequest.Reputation
----------------------------------------------


### An Amazon EC2 instance or a container is querying a low reputation domain name that is associated with cryptocurrency-related activity.


**Default severity: High**


 * **Feature:** Runtime Monitoring

This finding informs you that the listed EC2 instance or the container within your AWS environment is querying a low reputation domain name associated with Bitcoin or other cryptocurrency-related activity. Threat actors may seek to take control over compute resources to maliciously repurpose them for unauthorized cryptocurrency mining.


Low reputation domains are based on a reputation score model. This model evaluates and ranks the characteristics of a domain to determine its likelihood of being malicious.


The runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console.


**Remediation recommendations:**


If you use this EC2 instance or the container to mine or manage cryptocurrency, or if these resources are otherwise involved in blockchain activity, this finding could represent expected activity for your environment. If this is the case in your AWS environment, we recommend that you set up a suppression rule for this finding. The suppression rule should consist of two filter criteria. The first filter criterion should use the **Finding type** attribute with a value of `Impact:Runtime/BitcoinDomainRequest.Reputation`. The second filter criterion should be the **Instance ID** of the instance or the **Container Image ID** of the container is involved in cryptocurrency or blockchain–related activity. For more information, see  [Suppression rules](https://docs.aws.amazon.com/guardduty/latest/ug/findings_suppression-rule.html).


If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating EKS Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-eks-runtime-monitoring.html).

