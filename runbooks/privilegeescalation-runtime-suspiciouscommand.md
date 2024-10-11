PrivilegeEscalation:Runtime/SuspiciousCommand
---------------------------------------------


### A suspicious command has been executed on an Amazon EC2 instance or in a container, which allows an attacker to escalate privileges.


**Default severity: Medium**


 * **Feature:** Runtime Monitoring

This finding informs you that a suspicious command has been executed on an Amazon EC2 instance or in a container within your AWS environment. The command attempts to perform privilege escalation, which allows an adversary to perform high privilege tasks.


GuardDuty examines related runtime activity and context, and generates this finding type only when the associated activity and context are unusual or suspicious.


The Amazon EC2 instance or the container that is listed in the finding detail might have been compromised.


The GuardDuty runtime agent monitors events from multiple resources. To identify the affected resource, view **Resource type** in the findings details in the GuardDuty console.


**Remediation recommendations:**


If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).



