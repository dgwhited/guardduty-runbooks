PrivilegeEscalation:Runtime/RuncContainerEscape
-----------------------------------------------


### An attempt to gain host access of a container was detected.


**Default severity: High**


 * **Feature:** Runtime Monitoring

This finding informs you that the host runC binary file has been potentially overwritten. runC is the low-level container runtime that high-level container runtimes, such as Docker and Containerd, use to spawn and run containers. runC is always executed with root privileges because it needs to perform a low-level task of creating a container. A well-known vulnerability ([CVE-2019-5736 Detail](https://nvd.nist.gov/vuln/detail/CVE-2019-5736)) in the past allowed malicious containers to override the host's runC binary file and gained root-level access to the host when the modified runC binary was executed.


This finding may also indicate that a malicious actor has potentially executed a command in one of the following two types of containers:


 * A new container with an attacker-controlled image.
* An existing container that was previously accessible to the attacker with write permissions.

The runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console.


**Remediation recommendations:**


If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating EKS Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-eks-runtime-monitoring.html).

