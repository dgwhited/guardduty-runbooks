Execution:Runtime/ReverseShell
------------------------------

### A process in a container or an Amazon EC2 instance has created a reverse shell.

**Default severity: High**

* **Feature:** Runtime Monitoring

A reverse shell is a shell session created on a connection that is initiated from the target host to the actor's host. This is opposite to a normal shell that is initiated from the actor's host to the target's host. Threat actors create a reverse shell to execute commands on the target after gaining initial access to the target. This finding identifies potentially suspicious reverse shell connections.

GuardDuty examines related runtime activity and context, and generates this finding type only when the associated activity and context are found to be unusual or suspicious.

**Remediation recommendations:**

The GuardDuty security agent monitors events from multiple sources. To identify the impacted resource, view **Resource type** in the finding details in the GuardDuty console. If this activity is unexpected, your resource type might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).