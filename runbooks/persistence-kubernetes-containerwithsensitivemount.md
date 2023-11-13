Persistence:Kubernetes/ContainerWithSensitiveMount
--------------------------------------------------


### A container was launched with a sensitive external host path mounted inside.


**Default severity: Medium**


 * **Feature:** Kubernetes audit logs

This finding informs you that a container was launched with a configuration that included a sensitive host path with write access in the `volumeMounts` section. This makes the sensitive host path accessible and writable from inside the container. This technique is commonly used by adversaries to gain access to the host's filesystem. 


**Remediation recommendations:**


If this container launch is unexpected, the credentials of the user identity used to launch the container may be compromised. Revoke access of the user and reverse any changes made by an adversary to your cluster. See [Remediating Kubernetes findings](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty-remediate-kubernetes) for guidance. If this container launch is expected, it's recommended that you use a suppression rule consisting of a filter criteria based on the `resource.KubernetesDetails.KubernetesWorkloadDetails.containers.imagePrefix` field. In the filter criteria the `imagePrefix` field should be same as the `imagePrefix` specified in the finding. To learn more about creating suppression rules see [Suppression rules](https://docs.aws.amazon.com/guardduty/latest/ug/findings_suppression-rule).

