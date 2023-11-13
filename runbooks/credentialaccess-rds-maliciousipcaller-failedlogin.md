CredentialAccess:RDS/MaliciousIPCaller.FailedLogin
--------------------------------------------------


### An IP address that is associated with a known malicious activity unsuccessfully attempted to log in to an RDS database in your account.


**Default severity: Medium**


 * **Feature:** RDS login activity monitoring

This finding informs you that an IP address associated with known malicious activity attempted to log in to an RDS database in your AWS environment, but failed to provide the correct user name or password. This indicates that a potentially malicious actor may be attempting to compromise the RDS database in your account.


**Remediation recommendations:**


If this activity is unexpected for the associated database, it may indicate that there is an overly permissive access policy to the database or the database is publicly exposed. It is recommended to place the database in a private VPC, and limit the security group rules to allow traffic only from the necessary sources. For more information, see [Remediating potentially compromised database with failed login events](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-compromised-database-rds.html#gd-compromised-db-failed-attempt).

