

Execution:Runtime/SuspiciousShellCreated
----------------------------------------

### A network service or network-accessible process on an Amazon EC2 instance, or in a container has started an interactive shell process.

**Default severity: Low**

* **Feature:** Runtime Monitoring

This finding informs you that a network-accessible service on an Amazon EC2 instance or in a container within your AWS environment has launched an interactive shell. Under certain circumstances, this scenario may indicate post-exploitation behavior. Interactive shells allow attackers to execute arbitrary commands on a compromised instance or container.

The GuardDuty runtime agent monitors events from multiple resources. To identify the affected resource, view **Resource type** in the findings details in the GuardDuty console. You can view the network-accessible process information in the parent process details.

**Remediation recommendations:**

If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).

