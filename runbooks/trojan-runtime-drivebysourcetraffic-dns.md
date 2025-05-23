Trojan:Runtime/DriveBySourceTraffic!DNS
---------------------------------------

### An Amazon EC2 instance or a container is querying a domain name of a remote host that is a known source of Drive-By download attacks.

**Default severity: High**

* **Feature:** Runtime Monitoring

This finding informs you that a process running on the listed EC2 instance or the container in your AWS environment might be compromised because it is querying a domain name of a remote host that is a known source of drive-by download attacks. These are unintended downloads of computer software from the internet that can initiate an automatic installation of a virus, spyware, or malware.

The GuardDuty runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console. Additional context, including process and process lineage information, is available in the finding for further investigation.

**Remediation recommendations:**

If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).