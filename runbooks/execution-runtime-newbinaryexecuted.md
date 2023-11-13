Execution:Runtime/NewBinaryExecuted
-----------------------------------


### A newly created or recently modified binary file in a container has been executed.


**Default severity: Medium**


 * **Feature:** Runtime Monitoring

This finding informs you that a newly created or a recently modified binary file in a container was executed. It is the best practice to keep containers immutable at runtime, and binary files, scripts, or libraries should not be created or modified during the lifetime of the container. It is highly suspicious that the newly created binaries were executed in the container environment. This behavior is indicative of a malicious actor that has gained access to the workload, and has downloaded and executed malware or other software as part of the potential compromise.


The runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console.


**Remediation recommendations:**


If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating EKS Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-eks-runtime-monitoring.html).

