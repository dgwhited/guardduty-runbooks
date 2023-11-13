Discovery:Kubernetes/MaliciousIPCaller
--------------------------------------


### An API commonly used to discover resources in a Kubernetes cluster was invoked from an IP address.


**Default severity: Medium**


 * **Feature:** Kubernetes audit logs

This finding informs you that an API operation was invoked from an IP address that is associated with known malicious activity. The observed API is commonly used with the discovery stage of an attack wherein an attacker is gathering information to determine if your Kubernetes cluster is susceptible to a broader attack. 


**Remediation recommendations:**


If the user reported in the finding under the `KubernetesUserDetails` section is `system:anonymous`, investigate why the anonymous user was permitted to invoke the API and [revoke the permissions](https://aws.github.io/aws-eks-best-practices/security/docs/iam/#review-and-revoke-unnecessary-anonymous-access) if needed. If the user is an authenticated user, investigate to determine if the activity was legitimate or malicious. If the activity was malicious revoke access of the user and reverse any changes made by an adversary to your cluster. See [Remediating EKS Audit Log Monitoring findings Remediating EKS Runtime Monitoring findings](./guardduty-remediate-kubernetes.html) for guidance.

