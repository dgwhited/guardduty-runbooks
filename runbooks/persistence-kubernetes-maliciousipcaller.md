Persistence:Kubernetes/MaliciousIPCaller
----------------------------------------


### An API commonly used to obtain persistent access to a Kubernetes cluster was invoked from a known malicious IP address.


**Default severity: Medium**


 * **Feature:** EKS audit logs

This finding informs you that an API operation was invoked from an IP address that is associated with known malicious activity. The API observed is commonly associated with persistence tactics where an adversary has gained access to your Kubernetes cluster and is attempting to maintain that access. 


**Remediation recommendations:**


If the user reported in the finding under the `KubernetesUserDetails` section is `system:anonymous`, investigate why the anonymous user was permitted to invoke the API and revoke the permissions, if needed, by following the instructions in [Security best practices for Amazon EKS](https://docs.aws.amazon.com/eks/latest/userguide/security-best-practices.html) in the *Amazon EKS User Guide*. If the user is an authenticated user, investigate to determine if the activity was legitimate or malicious. If the activity was malicious revoke access of the user and reverse any changes made by an adversary to your cluster. For more information, see [Remediating EKS Audit Log Monitoring findings](./guardduty-remediate-kubernetes.html).

