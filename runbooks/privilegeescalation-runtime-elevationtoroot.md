PrivilegeEscalation:Runtime/ElevationToRoot
-------------------------------------------

### A process running on the listed Amazon EC2 instance or container has assumed root privileges.

**Default severity: Medium**

* **Feature:** Runtime Monitoring

This finding informs you that a process running on the listed Amazon EC2 or in the listed container within your AWS environment has assumed root privileges through unusual or suspicious `setuid` binary execution. This indicates that a running process has been potentially compromised, for the EC2 instance through an exploit, or through `setuid` exploitation. By using the root privileges, the attacker can potentially execute commands on the instance or the container.

While GuardDuty is designed to not generate this finding type for activities involving regular use of the `sudo` command, it will generate this finding when it identifies the activity as unusual or suspicious.

GuardDuty examines related runtime activity and context, and generates this finding type only when the associated activity and context are unusual or suspicious.

The GuardDuty runtime agent monitors events from multiple resources. To identify the affected resource, view **Resource type** in the findings details in the GuardDuty console. Additional context, including process and process lineage information, is available in the finding for further investigation.

**Remediation recommendations:**

If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).