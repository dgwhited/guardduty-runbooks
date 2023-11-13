CredentialAccess:RDS/TorIPCaller.FailedLogin
--------------------------------------------


### A Tor IP address attempted to unsuccessfully log in to an RDS database in your account.


**Default severity: Medium**


 * **Feature:** RDS login activity monitoring

This finding informs you that a Tor exit node IP address attempted to log in to an RDS database in your AWS environment, but failed to provide the correct user name or password. Tor is a software for enabling anonymous communication. It encrypts and randomly bounces communications through relays between a series of network nodes. The last Tor node is called the exit node. This can indicate unauthorized access to the RDS resources in your account, with the intent of hiding the anonymous user's true identity.


**Remediation recommendations:**


If this activity is unexpected for the associated database, it may indicate that there is an overly permissive access policy to the database or the database is publicly exposed. It is recommended to place the database in a private VPC, and limit the security group rules to allow traffic only from the necessary sources. For more information, see [Remediating potentially compromised database with failed login events](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-compromised-database-rds.html#gd-compromised-db-failed-attempt).

