Policy:Kubernetes/AdminAccessToDefaultServiceAccount
----------------------------------------------------


### The default service account was granted admin privileges on a Kubernetes cluster.


**Default severity: High**


 * **Feature:** Kubernetes audit logs

This finding informs you that the default service account for a namespace in your Kubernetes cluster was granted admin privileges. Kubernetes creates a default service account for all the namespaces in the cluster. It automatically assigns the default service account as an identity to pods that have not been explicitly associated to another service account. If the default service account has admin privileges, it may result in pods being unintentionally launched with admin privileges. If this behavior is not expected, it may indicate a configuration mistake or that your credentials are compromised. 


**Remediation recommendations:**


You should not use the default service account to grant permissions to pods. Instead you should create a dedicated service account for each workload and grant permission to that account on a needs basis. To fix this issue, you should create dedicated service accounts for all your pods and workloads and update the pods and workloads to migrate from the default service account to their dedicated accounts. Then you should remove the admin permission from the default service account. See [Remediating EKS Audit Log Monitoring findings Remediating EKS Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-kubernetes.html#compromised-kubernetes-user) for additional guidance and resources.

