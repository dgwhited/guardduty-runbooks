DefenseEvasion:Kubernetes/MaliciousIPCaller
-------------------------------------------


### An API commonly used to evade defensive measures was invoked from a known malicious IP address.


**Default severity: High**


 * **Feature:** Kubernetes audit logs

This finding informs you that an API operation was invoked from an IP address that is associated with known malicious activity. The API observed is commonly associated with defense evasion tactics where an adversary is trying to hide their actions to avoid detection. 


**Remediation recommendations:**


If the user reported in the finding under the `KubernetesUserDetails` section is `system:anonymous`, investigate why the anonymous user was permitted to invoke the API and [revoke the permissions](https://aws.github.io/aws-eks-best-practices/security/docs/iam/#review-and-revoke-unnecessary-anonymous-access) if needed. If the user is an authenticated user, investigate to determine if the activity was legitimate or malicious. If the activity was malicious revoke access of the user and reverse any changes made by an adversary to your cluster. See [Remediating EKS Audit Log Monitoring findings Remediating EKS Runtime Monitoring findings](./guardduty-remediate-kubernetes.html) for guidance.

