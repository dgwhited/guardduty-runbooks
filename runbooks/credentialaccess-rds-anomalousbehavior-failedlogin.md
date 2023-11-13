CredentialAccess:RDS/AnomalousBehavior.FailedLogin
--------------------------------------------------


### One or more unusual failed login attempts were observed on an RDS database in your account.


**Default severity: Low**


 * **Feature:** RDS login activity monitoring

This finding informs you that one or more anomalous failed logins were observed on an RDS database in your AWS environment. A failed login attempts from public IP addresses may indicate that the RDS database in your account has been subject to an attempted brute force attack by a potentially malicious actor.


These failed logins were identified as anomalous by the GuardDuty anomaly detection machine learning (ML) model. The ML model evaluates all database login events in your [Supported Amazon Aurora databases](https://docs.aws.amazon.com/guardduty/latest/ug/rds-protection.html#rds-pro-supported-db) and identifies anomalous events that are associated with techniques used by adversaries. The ML model tracks various factors of the RDS login activity such as the user that made the request, the location the request was made from, and the specific database connection details that were used. For information about the RDS login activity that are potentially unusual, see [RDS login activity-based anomalies](./guardduty_findings-summary.html#rds-pro-login-anomaly).


**Remediation recommendations:**


If this activity is unexpected for the associated database, it may indicate that the database is publicly exposed or there is an overly permissive access policy to the database. It is recommended to place the database in a private VPC, and limit the security group rules to allow traffic only from the necessary sources. For more information, see [Remediating potentially compromised database with failed login events](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-compromised-database-rds.html#gd-compromised-db-failed-attempt).

