CryptoCurrency:Runtime/BitcoinTool.B!DNS
----------------------------------------


### An Amazon EC2 instance or a container is querying a domain name that is associated with a cryptocurrency activity.


**Default severity: High**


 * **Feature:** Runtime Monitoring

This finding informs you that the listed EC2 instance or a container in your AWS environment is querying a domain name that is associated with Bitcoin or other cryptocurrency-related activity. Threat actors may seek to take control over the compute resources in order to maliciously repurpose them for unauthorized cryptocurrency mining.


The runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console.


**Remediation recommendations:**


If you use this EC2 instance or container to mine or manage cryptocurrency, or either of these is otherwise involved in blockchain activity, the CryptoCurrency:Runtime/BitcoinTool.B!DNS finding could be an expected activity for your environment. If this is the case in your AWS environment, we recommend that you set up a suppression rule for this finding. The suppression rule should consist of two filter criterion. The first criteria should use the **Finding type** attribute with a value of `CryptoCurrency:Runtime/BitcoinTool.B!DNS`. The second filter criteria should be the **Instance ID** of the instance or the **Container Image ID** of the container involved in cryptocurrency or blockchain activity. For more information, see [Suppression Rules](https://docs.aws.amazon.com/guardduty/latest/ug/findings_suppression-rule.html).


If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating EKS Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-eks-runtime-monitoring.html).

