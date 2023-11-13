CredentialAccess:RDS/AnomalousBehavior.SuccessfulLogin
------------------------------------------------------


### A user successfully logged into an RDS database in your account in an anomalous way.


**Default severity: Variable**


###### Note

Depending on the anomalous behavior associated with this finding, the default severity can Low, Medium, and High. 

 * **Low** – If the user name associated with this finding logged in from an IP address that is associated with a private network.
* **Medium** – If the user name associated with this finding logged in from a public IP address.
* **High** – If there is a consistent pattern of failed login attempts from public IP addresses indicative of overly permissive access policies.

 * **Feature:** RDS login activity monitoring

This finding informs you that an anomalous successful login was observed on an RDS database in your AWS environment. This may indicate that a previous unseen user logged into an RDS database for the first time. A common scenario is an internal user logging into a database that is accessed programmatically by applications and not by individual users. 


This successful login was identified as anomalous by the GuardDuty anomaly detection machine learning (ML) model. The ML model evaluates all database login events in your [Supported Amazon Aurora databases](https://docs.aws.amazon.com/guardduty/latest/ug/rds-protection.html#rds-pro-supported-db) and identifies anomalous events that are associated with techniques used by adversaries. The ML model tracks various factors of the RDS login activity such as the user that made the request, the location the request was made from, and the specific database connection details that were used. For information about the login events that are potentially unusual, see [RDS login activity-based anomalies](./guardduty_findings-summary.html#rds-pro-login-anomaly).


**Remediation recommendations:**


If this activity is unexpected for the associated database, it is recommended to change the password of the associated database user, and review available audit logs for activity performed by the anomalous user. Medium and high severity findings may indicate that there is an overly permissive access policy to the database, and user credentials may have been exposed or compromised. It is recommended to place the database in a private VPC, and limit the security group rules to allow traffic only from the necessary sources. For more information, see [Remediating potentially compromised database with successful login events](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-compromised-database-rds.html#gd-compromised-db-successful-attempt).

