Policy:Kubernetes/KubeflowDashboardExposed
------------------------------------------


### The **Kubeflow** dashboard for a Kubernetes cluster was exposed to the Internet


**Default severity: Medium**


 * **Feature:** Kubernetes audit logs

This finding informs you that **Kubeflow** dashboard for your cluster was exposed to the Internet by a Load Balancer service. An exposed **Kubeflow** dashboard makes the management interface of your **Kubeflow** environment accessible from the Internet and allows adversaries to exploit any authentication and access control gaps that may be present. 


**Remediation recommendations:**


You should ensure that strong authentication and authorization is enforced on **Kubeflow** Dashboard. You should also implement network access control to restrict access to the dashboard from specific IP addresses.

