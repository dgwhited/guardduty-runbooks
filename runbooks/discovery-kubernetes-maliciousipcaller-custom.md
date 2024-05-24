Discovery:Kubernetes/MaliciousIPCaller.Custom
---------------------------------------------


### An API commonly used to discover resources in a Kubernetes cluster was invoked from an IP address on a custom threat list.


**Default severity: Medium**


 * **Feature:** EKS audit logs

This finding informs you that an API was invoked from an IP address that is included on a threat list that you uploaded. The threat list associated with this finding is listed in the **Additional Information** section of a finding's details. The observed API is commonly used with the discovery stage of an attack wherein an attacker is gathering information to determine if your Kubernetes cluster is susceptible to a broader attack. 


**Remediation recommendations:**


If the user reported in the finding under the `KubernetesUserDetails` section is `system:anonymous`, investigate why the anonymous user was permitted to invoke the API and revoke the permissions, if needed, by following the instructions in [Security best practices for Amazon EKS](https://docs.aws.amazon.com/eks/latest/userguide/security-best-practices.html) in the *Amazon EKS User Guide*. If the user is an authenticated user, investigate to determine if the activity was legitimate or malicious. If the activity was malicious revoke access of the user and reverse any changes made by an adversary to your cluster. For more information, see [Remediating EKS Audit Log Monitoring findings](./guardduty-remediate-kubernetes.html).

