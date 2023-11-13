Policy:Kubernetes/AnonymousAccessGranted
----------------------------------------


### The `system:anonymous` user was granted API permission on a Kubernetes cluster.


**Default severity: High**


 * **Feature:** Kubernetes audit logs

This finding informs you that a user on your Kubernetes cluster successfully created a `ClusterRoleBinding` or `RoleBinding` to bind the user `system:anonymous` to a role. This enables unauthenticated access to the API operations permitted by the role. If this behavior is not expected, it may indicate a configuration mistake or that your credentials are compromised 


**Remediation recommendations:**


You should examine the permissions that have been granted to the `system:anonymous` user or `system:unauthenticated` group on your cluster and revoke unnecessary anonymous access. See  [Review and revoke unnecessary anonymous access](https://aws.github.io/aws-eks-best-practices/security/docs/iam/#review-and-revoke-unnecessary-anonymous-access) for guidance. If the permissions were granted maliciously, you should revoke access of the user that granted the permissions and reverse any changes made by an adversary to your cluster. See [Remediating Kubernetes findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-kubernetes.html) for guidance.

