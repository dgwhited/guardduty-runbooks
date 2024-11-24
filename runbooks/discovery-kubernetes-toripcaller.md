

Discovery:Kubernetes/TorIPCaller
--------------------------------

### An API commonly used to discover resources in a Kubernetes cluster was invoked from a Tor exit node IP address.

**Default severity: Medium**

* **Feature:** EKS audit logs

This finding informs you that an API was invoked from a Tor exit node IP address. The observed API is commonly used with the discovery stage of an attack wherein an attacker is gathering information to determine if your Kubernetes cluster is susceptible to a broader attack. Tor is software for enabling anonymous communication. It encrypts and randomly bounces communications through relays between a series of network nodes. The last Tor node is called the exit node. This can indicate unauthorized access to your Kubernetes cluster with the intent of hiding the adversary's true identity.

**Remediation recommendations:**

If the user reported in the finding under the `KubernetesUserDetails` section is `system:anonymous`, investigate why the anonymous user was permitted to invoke the APIand revoke the permissions, if needed, by following the instructions in [Security best practices for Amazon EKS](https://docs.aws.amazon.com/eks/latest/userguide/security-best-practices.html) in the *Amazon EKS User Guide*. If the user is an authenticated user, investigate to determine if the activity was legitimate or malicious. If the activity was malicious revoke access of the user and reverse any changes made by an adversary to your cluster. For more information, see [Remediating EKS Protection findings](./guardduty-remediate-kubernetes.html).

