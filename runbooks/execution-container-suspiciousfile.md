Execution:Container/SuspiciousFile
----------------------------------


### A suspicious file has been detected on a standalone container.


**Default severity: Varies depending on the detected threat.**


This finding indicates that the GuardDuty Malware Protection scan has detected one or more suspicious files on a container with no cluster information. For more information, see **Threats detected** section in the findings' details.


`SuspiciousFile` type detections indicate that potentially unwanted programs such as adware, spyware, or dual use tools are present on an impacted resource. These programs could have a negative impact on your resource, or be used by attackers for malicious purposes. For example, networking tools can be used legitimately or maliciously by adversaries as hack tools to try and compromise resources.


When a suspicious file has been detected, evaluate whether you expect to see the detected file in your AWS environment. If the file is unexpected, follow the remediation recommendations provided in the next section.


**Remediation recommendations:**


If this activity is unexpected, your container workload may be compromised. For more information, see [Remediating a compromised standalone container](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#remediate-compromised-standalone-container).



