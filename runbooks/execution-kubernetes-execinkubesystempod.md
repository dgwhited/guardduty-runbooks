Execution:Kubernetes/ExecInKubeSystemPod
----------------------------------------


### A command was executed inside a pod within the `kube-system` namespace


**Default severity: Medium**


 * **Feature:** Kubernetes audit logs

This finding informs you that a command was executed in a pod within the `kube-system` namespace using **Kubernetes exec API**. `kube-system` namespace is a default namespaces, which is primarily used for system level components such as `kube-dns` and `kube-proxy`. It is very uncommon to execute commands inside pods or containers under `kube-system` namespace and may indicate suspicious activity. 


**Remediation recommendations:**


If the execution of this command is unexpected, the credentials of the user identity used to execute the command may be compromised. Revoke access of the user and reverse any changes made by an adversary to your cluster. See [Remediating EKS Audit Log Monitoring findings Remediating EKS Runtime Monitoring findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-kubernetes.html) for guidance.

