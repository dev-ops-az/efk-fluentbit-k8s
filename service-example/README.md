We will deploy 2 services example write data need to log to File in Kubernetes Node. In this case, We write data as type HostPath PV. File log will erase data when load over 10MB.

_ service A will write log to /var/log/containers/service_a.log
_ service B will write log to /var/log/containers/service_b.log


