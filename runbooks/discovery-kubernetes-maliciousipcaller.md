Discovery:Kubernetes/MaliciousIPCaller
--------------------------------------

### An API commonly used to discover resources in a Kubernetes cluster was invoked from an IP address.

**Default severity: Medium**

* **Feature:** EKS audit logs

This finding informs you that an API operation was invoked from an IP address that is associated with known malicious activity. The observed API is commonly used with the discovery stage of an attack wherein an attacker is gathering information to determine if your Kubernetes cluster is susceptible to a broader attack.

###### For unauthenticated access

MaliciousIPCaller findings are not generated for unauthenticated access.

SuccessfulAnonymousAccess findings are generated for unauthenticated or anonymous access.

**Remediation recommendations:**

If the user reported in the finding under the `KubernetesUserDetails` section is `system:anonymous`, investigate why the anonymous user was permitted to invoke the API and revoke the permissions, if needed, by following the instructions in [Security best practices for Amazon EKS](https://docs.aws.amazon.com/eks/latest/userguide/security-best-practices.html) in the *Amazon EKS User Guide*. If the user is an authenticated user, investigate to determine if the activity was legitimate or malicious. If the activity was malicious revoke access of the user and reverse any changes made by an adversary to your cluster. For more information, see [Remediating EKS Protection findings](./guardduty-remediate-kubernetes.html).