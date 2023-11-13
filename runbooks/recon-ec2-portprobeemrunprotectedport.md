Recon:EC2/PortProbeEMRUnprotectedPort
-------------------------------------


### An EC2 instance has an unprotected EMR related port which is being probed by a known malicious host.


**Default severity: High**


 * **Data source:** VPC flow logs

This finding informs you that an EMR related sensitive port on the listed EC2 instance that is part of an cluster in your AWS environment is not blocked by a security group, an access control list (ACL), or an on-host firewall such as Linux IPTables, and that known scanners on the internet are actively probing it. Ports that can trigger this finding, such as port 8088 (YARN Web UI port), could potentially be used for remote code execution. 


**Remediation recommendations:**


You should block open access to ports on clusters from the internet and restrict access only to specific IP addresses that require access to these ports. For more information see, [Security Groups for EMR Clusters](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-security-groups.html).

