Policy:Kubernetes/ExposedDashboard
----------------------------------


### The dashboard for a Kubernetes cluster was exposed to the internet


**Default severity: Medium**


 * **Feature:** Kubernetes audit logs

This finding informs you that Kubernetes dashboard for your cluster was exposed to the internet by a Load Balancer service. An exposed dashboard makes the management interface of your cluster accessible from the internet and allows adversaries to exploit any authentication and access control gaps that may be present. 


**Remediation recommendations:**


You should ensure that strong authentication and authorization is enforced on Kubernetes Dashboard. You should also implement network access control to restrict access to the dashboard from specific IP addresses. 

