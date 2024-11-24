

Persistence:Kubernetes/SuccessfulAnonymousAccess
------------------------------------------------

### An API commonly used to obtain high-level permissions to a Kubernetes cluster was invoked by an unauthenticated user.

**Default severity: High**

* **Feature:** EKS audit logs

This finding informs you that an API operation was successfully invoked by the `system:anonymous` user. API calls made by `system:anonymous` are unauthenticated. The observed API is commonly associated with the persistence tactics where an adversary has gained access to your cluster and is attempting to maintain that access. This activity indicates that anonymous or unauthenticated access is permitted on the API action reported in the finding and may be permitted on other actions. If this behavior is not expected, it may indicate a configuration mistake or that your credentials are compromised.

**Remediation recommendations:**

You should examine the permissions that have been granted to the `system:anonymous` user on your cluster and ensure that all the permissions are needed. If the permissions were granted mistakenly or maliciously, you should revoke access of the user and reverse any changes made by an adversary to your cluster. For more information, see [Security best practices for Amazon EKS](https://docs.aws.amazon.com/eks/latest/userguide/security-best-practices.html) in the *Amazon EKS User Guide*.

For more information, see [Remediating EKS Protection findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-kubernetes.html).

