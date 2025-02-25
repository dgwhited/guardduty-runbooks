PrivilegeEscalation:Kubernetes/PrivilegedContainer
--------------------------------------------------

### A privileged container with root level access was launched on your Kubernetes cluster.

**Default severity: Medium**

* **Feature:** EKS audit logs

This finding informs you that a privileged container was launched on your Kubernetes cluster using an image has never before been used to launch privileged containers in your cluster. A privileged container has root level access to the host. Adversaries can launch privileged containers as a privilege escalation tactic to gain access to and then compromise the host.

**Remediation recommendations:**

If this container launch is unexpected, the credentials of the user identity used to launch the container may be compromised. Revoke access of the user and reverse any changes made by an adversary to your cluster. For more information, see [Remediating EKS Protection findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-kubernetes.html).