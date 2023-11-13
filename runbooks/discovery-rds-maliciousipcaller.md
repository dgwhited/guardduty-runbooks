Discovery:RDS/MaliciousIPCaller
-------------------------------


### An IP address that is associated with a known malicious activity probed an RDS database in your account; no authentication attempt was made.


**Default severity: Medium**


 * **Feature:** RDS login activity monitoring

This finding informs you that an IP address associated with known a malicious activity probed an RDS database in your AWS environment, though no login attempt was made. This may indicate that a potentially malicious actor is attempting to scan for a publicly accessible infrastructure.


**Remediation recommendations:**


If this activity is unexpected for the associated database, it may indicate that there is an overly permissive access policy to the database or the database is publicly exposed. It is recommended to place the database in a private VPC, and limit the security group rules to allow traffic only from the necessary sources. For more information, see [Remediating potentially compromised database with failed login events](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-compromised-database-rds.html#gd-compromised-db-failed-attempt).

