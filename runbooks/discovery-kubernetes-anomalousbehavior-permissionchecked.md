Discovery:Kubernetes/AnomalousBehavior.PermissionChecked
--------------------------------------------------------


### A user checked their access permission in an anomalous way.


**Default severity: Low**


 * **Feature:** Kubernetes audit logs

This finding informs you that a user in your Kubernetes cluster successfully checked whether or not the known powerful permissions that can lead to privileged escalation and remote code execution, are allowed. For example, a common command used to check permissions for a user is `kubectl auth can-i`. If this behavior is not expected, it may indicate either a configuration mistake or that your credentials have been compromised.


The observed API was identified as anomalous by the GuardDuty anomaly detection machine learning (ML) model. The ML model evaluates all user API activity within your Amazon EKS cluster and identifies anomalous events that are associated with the techniques used by unauthorized users. The ML model also tracks multiple factors of the API operation, such as the user making the request, the location the request was made from, permission being checked, and the namespace that the user operated. You can find the details of the API request that are unusual, in the finding details panel in the GuardDuty console.


**Remediation recommendations:**


Examine the permissions granted to the Kubernetes user to ensure that all the permissions are needed. If the permissions were granted mistakenly or maliciously, revoke user access and reverse any changes made by an unauthorized user to your cluster. For more information, see [Remediating EKS Audit Log Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-kubernetes.html).


If your AWS credentials are compromised, see [Remediating compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_remediate.html#compromised-creds).



