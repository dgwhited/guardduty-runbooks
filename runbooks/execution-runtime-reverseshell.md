Execution:Runtime/ReverseShell
------------------------------


### A process in a container or an Amazon EC2 instance has created a reverse shell.


**Default severity: High**


 * **Feature:** Runtime Monitoring

A reverse shell is a shell session created on a connection that is initiated from the target host to the actor's host. This is opposite to a normal shell that is initiated from the actor's host to the target's host. Threat actors create a reverse shell to execute commands on the target after gaining initial access to the target. This finding identifies a potential attempt to create a reverse shell. 


**Remediation recommendations:**


If this activity is unexpected, your resource type might have been compromised.

