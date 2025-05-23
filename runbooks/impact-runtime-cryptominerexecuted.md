Impact:Runtime/CryptoMinerExecuted
----------------------------------

### A container or an Amazon EC2 instance is executing a binary file that is associated with a cryptocurrency mining activity.

**Default severity: High**

* **Feature:** Runtime Monitoring

This finding informs you that a process running on the listed EC2 instance or container in your AWS environment is executing a binary file that is associated with a cryptocurrency mining activity. Threat actors may seek to take control over compute resources to maliciously repurpose them for unauthorized cryptocurrency mining.

The GuardDuty runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console. Additional context, including process and process lineage information, is available in the finding for further investigation.

**Remediation recommendations:**

The GuardDuty runtime agent monitors events from multiple resources. To identify the affected resource, view **Resource type** in the findings details in the GuardDuty console and see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).