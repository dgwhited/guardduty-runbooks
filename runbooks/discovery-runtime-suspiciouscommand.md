Discovery:Runtime/SuspiciousCommand
-----------------------------------

### A suspicious command has been executed on an Amazon EC2 instance or in a container, which allows an attacker to gain information about the local system, surrounding AWS infrastructure, or container infrastructure.

**Default severity: Low**

**Feature:** Runtime Monitoring

This finding informs you that the listed Amazon EC2 instance or container in your AWS environment has executed a command that might provide an attacker with crucial information to potentially advance the attack. The following information may have been retrieved:

* Local system such as user or network configuration,
* Other available AWS resources and permissions, or
* Kubernetes infrastructure such as services and pods.

The Amazon EC2 instance or the container that is listed in the finding detail might have been compromised.

The GuardDuty runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings details in the GuardDuty console. You can find the details about the suspicious command in the `service.runtimeDetails.context` field of the finding JSON.

**Remediation recommendations:**

If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).