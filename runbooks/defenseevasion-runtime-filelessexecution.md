DefenseEvasion:Runtime/FilelessExecution
----------------------------------------


### A process in a container or an Amazon EC2 instance is executing code from memory.


**Default severity: Medium**


 * **Feature:** Runtime Monitoring

This finding informs you when a process is executed using an in-memory executable file on disk. This is a common defense evasion technique that avoids writing the malicious executable to the disk to evade file system scanning-based detection. Although this technique is used by malware, it also has some legitimate use cases. One of the examples is a just-in-time (JIT) compiler that writes compiled code to memory and executes it from memory.


The runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console.


**Remediation recommendations:**


If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating EKS Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-eks-runtime-monitoring.html).

