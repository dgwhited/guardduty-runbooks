PrivilegeEscalation:Runtime/RuncContainerEscape
-----------------------------------------------


### A container escape attempt through runC was detected.


**Default severity: High**


 * **Feature:** Runtime Monitoring

RunC is the low\-level container runtime that high\-level container runtimes, such as Docker and Containerd use to spawn and run containers. RunC is always executed with root privileges because it needs to perform the low\-level task of creating a container. A threat actor can gain host\-level access by either modifying or exploiting a vulnerability in runC binary. 


This finding detects modification of runC binary and potential attempts to exploit the following runC vulnerabilities:


 * [CVE\-2019\-5736](https://nvd.nist.gov/vuln/detail/CVE-2019-5736) – Exploitation of CVE\-2019\-5736 involves overwriting the runC binary from within a container. This finding gets invoked when runC binary is modified by a process inside a container.
* [CVE\-2024\-21626](https://nvd.nist.gov/vuln/detail/CVE-2024-21626) – Exploitation of CVE\-2024\-21626 involves setting the current working directory (CWD) or a container to an open file descriptor `/proc/self/fd/FileDescriptor`. This finding gets invoked when a container process with a current working directory under `/proc/self/fd/` is detected, for example, `/proc/self/fd/7`.

This finding may indicate that a malicious actor has attempted to perform exploitation in one of the following types of containers:


 * A new container with an attacker\-controlled image.
* An existing container that was accessible to the actor with write permissions on the host level runC binary.

The runtime agent monitors events from multiple resource types. To identify the potentially compromised resource, view **Resource type** in the findings panel in the GuardDuty console.


**Remediation recommendations:**


If this activity is unexpected, your resource might have been compromised. For more information, see [Remediating Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-runtime-monitoring.html).

