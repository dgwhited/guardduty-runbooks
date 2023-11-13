Persistence:Kubernetes/MaliciousIPCaller.Custom
-----------------------------------------------


### An API commonly used to obtain persistent access to a Kubernetes cluster was invoked from an IP address on a custom threat list.


**Default severity: Medium**


 * **Feature:** Kubernetes audit logs

This finding informs you that an API operation was invoked from an IP address that is included on a threat list that you uploaded. The threat list associated with this finding is listed in the **Additional Information** section of a finding's details. The API observed is commonly associated with persistence tactics where an adversary has gained access to your Kubernetes cluster and is attempting to maintain that access. 


**Remediation recommendations:**


If the user reported in the finding under the `KubernetesUserDetails` section is `system:anonymous`, investigate why the anonymous user was permitted to invoke the API and [revoke the permissions](https://aws.github.io/aws-eks-best-practices/security/docs/iam/#review-and-revoke-unnecessary-anonymous-access) if needed. If the user is an authenticated user, investigate to determine if the activity was legitimate or malicious. If the activity was malicious revoke access of the user and reverse any changes made by an adversary to your cluster. See [Remediating EKS Audit Log Monitoring findings Remediating EKS Runtime Monitoring findings](./guardduty-remediate-kubernetes.html) for guidance.

