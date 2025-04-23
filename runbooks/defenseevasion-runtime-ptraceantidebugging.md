DefenseEvasion:Runtime/PtraceAntiDebugging
------------------------------------------

### A process in a container or an Amazon EC2 instance has executed an anti-debugging measure using the ptrace system call.

**Default severity: Low**

* **Feature:** Runtime Monitoring

This finding shows that a process running on the listed Amazon EC2 instance or a container within your AWS environment has used the ptrace system call with the `PTRACE_TRACEME` option. This activity would cause an attached debugger to detach from the running process. If no debugger is attached, it has no effect. However, the activity in itself raises suspicion. This might indicate that malware is running on the system. Malware frequently uses anti-debugging techniques to evade analysis, and these techniques can be detected at runtime.

GuardDuty examines related runtime activity and context so that it generates this finding only when the associated activity and context are potentially suspicious.

The GuardDuty runtime agent monitors events from multiple resources. To identify the affected resource, view **Resource type** in the findings details in the GuardDuty console. Additional context, including process and process lineage information, is available in the finding for further investigation.

**Remediation recommendations:**

If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).