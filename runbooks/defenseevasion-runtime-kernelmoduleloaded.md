DefenseEvasion:Runtime/KernelModuleLoaded
-----------------------------------------

### A kernel module was loaded on an Amazon EC2 instance, indicating an attempt to gain kernel-level access.

**Default severity: High**

* **Feature:** Runtime Monitoring

This finding indicates that a kernel module was loaded on the listed EC2 instance. Since kernel modules have the highest system-level privileges (ring 0), this could indicate that a threat actor has gained kernel-level access. This level of access allows complete control over the system.

The GuardDuty runtime agent monitors events from multiple resources. To identify the affected resource, view **Resource type** in the findings details in the GuardDuty console. When applicable, additional context, including process and process lineage information, is available in the finding for further investigation.

**Remediation recommendations:**

If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).