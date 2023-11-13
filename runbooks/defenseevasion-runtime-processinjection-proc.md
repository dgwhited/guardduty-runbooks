DefenseEvasion:Runtime/ProcessInjection.Proc
--------------------------------------------


### A process injection using proc filesystem was detected in a container or an Amazon EC2 instance.


**Default severity: High**


 * **Feature:** Runtime Monitoring

Process injection is a technique that threat actors use to inject code into processes to evade defenses and potentially elevate privileges. The proc filesystem (procfs) is a special filesystem in Linux that presents the virtual memory of process as a file. The path of that file is `/proc/PID/mem`, where `PID` is the unique ID of the process. A threat actor can write to this file to inject code into the process. This finding identifies potential attempts to write to this file. 


The runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console.


**Remediation recommendations:**


If this activity is unexpected, your resource type might have been compromised. For more information, see [Remediating EKS Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-eks-runtime-monitoring.html).

