InitialAccess:IAMUser/AnomalousBehavior
---------------------------------------

### An API commonly used to gain unauthorized access to an AWS environment was invoked in an anomalous way.

**Default severity: Medium**

* **Data source:** CloudTrail management event

This finding informs you that an anomalous API request was observed in your account. This finding may include a single API or a series of related API requests made in proximity by a single [user identity](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-event-reference-user-identity.html). The API observed is commonly associated with the initial access stage of an attack when an adversary is attempting to establish access to your environment. APIs in this category are typically get token, or session operations, such as, `StartSession`, or `GetAuthorizationToken`.

This API request was identified as anomalous by GuardDuty's anomaly detection machine learning (ML) model. The ML model evaluates all API requests in your account and identifies anomalous events that are associated with techniques used by adversaries. The ML model tracks various factors of the API request, such as, the user that made the request, the location the request was made from, and the specific API that was requested. Details on which factors of the API request are unusual for the user identity that invoked the request can be found in the [finding details](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_findings-summary.html#finding-anomalous).

**Remediation recommendations:**

If this activity is unexpected, your credentials may be compromised. For more information, see [Remediating potentially compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-creds.html).