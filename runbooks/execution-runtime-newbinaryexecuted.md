

Execution:Runtime/NewBinaryExecuted
-----------------------------------

### A newly created or recently modified binary file in a container has been executed.

**Default severity: Medium**

* **Feature:** Runtime Monitoring

This finding informs you that a newly created or a recently modified binary file, in a container was executed. It is the best practice to keep containers immutable at runtime, and binary files, scripts, or libraries should not be created or modified during the lifetime of the container. This behavior indicates that a malicious actor that has gained access to the container, has downloaded, and executed malware or other software as part of the potential compromise. Although this type of activity could be an indication of a compromise, it is also a common usage pattern. Therefore, GuardDuty uses mechanisms to identify suspicious instances of this activity and generates this finding type only for suspicious instances.

The GuardDuty runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console. To identify the modifying process and new binary, view the **Modifying process** details and the **Process** details

The details of the modifying process are included in the `service.runtimeDetails.context.modifyingProcess` field of the finding JSON, or under **Modifying Process** in the finding details panel. For this finding type, the modifying process is `/usr/bin/dpkg`, as identified by the `service.runtimeDetails.context.modifyingProcess.executablePath` field of the finding JSON, or as a part of **Modifying Process** in the finding details panel.

The details of the executed new or modified binary are included in the `service.runtimeDetails.process` of the finding JSON, or the **Process** section under **Runtime details**. For this finding type, the new or modified binary is `/usr/bin/python3.8`, as indicated by `service.runtimeDetails.process.executablePath` (**Executable path**) field.

**Remediation recommendations:**

If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).

