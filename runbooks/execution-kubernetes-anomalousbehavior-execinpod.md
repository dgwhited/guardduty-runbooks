

Execution:Kubernetes/AnomalousBehavior.ExecInPod
------------------------------------------------

### A command was executed inside a pod in an anomalous way.

**Default severity: Medium**

* **Feature:** EKS audit logs

This finding informs you that a command was executed in a pod using the Kubernetes exec API. The Kubernetes exec API allows running arbitrary commands in a pod. If this behavior is not expected for the user, namespace, or pod, it may indicate either a configuration mistake or that your AWS credentials are compromised.

The observed API was identified as anomalous by the GuardDuty anomaly detection machine learning (ML) model. The ML model evaluates all user API activity within your EKS cluster. This ML model also identifies anomalous events that are associated with the techniques used by an unauthorized user. The ML model also tracks multiple factors of the API operation, such as the user making the request, the location the request was made from, the user agent used, and the namespace that the user operated. You can find the details of the API request that are unusual, in the finding details panel in the GuardDuty console.

**Remediation recommendations:**

If the execution of this command is unexpected, the credentials of the user identity used to execute the command may have been compromised. Revoke user access and reverse any changes made by an unauthorized user to your cluster. For more information, see [Remediating EKS Protection findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-kubernetes.html).

If your AWS credentials are compromised, see [Remediating potentially compromised AWS credentials](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-creds.html).

