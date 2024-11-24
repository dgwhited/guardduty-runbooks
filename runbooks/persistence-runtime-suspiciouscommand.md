

Persistence:Runtime/SuspiciousCommand
-------------------------------------

### A suspicious command has been executed on an Amazon EC2 instance or in a container, which allows an attacker to persist access and control in your AWS environment.

**Default severity: Medium**

* **Feature:** Runtime Monitoring

This finding informs you that a suspicious command has been executed on an Amazon EC2 instance or in a container within your AWS environment. The command installs a persistence method which allows malware to run uninterruptedly, or allows an attacker to continuously access the potentially compromised instance or container resource type. This could potentially mean that a system service has been installed or modified, the `crontab` has been modified, or a new user has been added to the system configuration.

GuardDuty examines related runtime activity and context, and generates this finding type only when the associated activity and context are unusual or suspicious.

The Amazon EC2 instance or the container that is listed in the finding detail might have been compromised.

The GuardDuty runtime agent monitors events from multiple resources. To identify the potentially compromised resource, view **Resource type** in the findings details in the GuardDuty console. You can find the details about the suspicious command in the `service.runtimeDetails.context` field of the finding JSON.

**Remediation recommendations:**

If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).

