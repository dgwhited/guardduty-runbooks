UnauthorizedAccess:Runtime/TorRelay
-----------------------------------

### Your Amazon EC2 instance or a container is making connections to a Tor network as a Tor relay.

**Default severity: High**

* **Feature:** Runtime Monitoring

This finding informs you that a process running on the listed EC2 instance or a container in your AWS environment is making connections to a Tor network in a manner that suggests that it's acting as a Tor relay. Tor is software for enabling anonymous communication. Tor increases anonymity of communication by forwarding the client's possibly illicit traffic from one Tor relay to another.

The GuardDuty runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console.

The GuardDuty runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console. Additional context, including process and process lineage information, is available in the finding for further investigation.

**Remediation recommendations:**

If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).