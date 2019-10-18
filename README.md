# metrics-server
Ansible role to deploy metrics server on a Kubernetes cluster.

## Variables

|Name|Default value|Description|
|----|-------------|-----------|
|`metrics_server_version`|v0.3.6|The version of the metrics-server.|
|`metrics_server_kubeconfig`|~/.kube/config|Path to the kubeconfig to use.|
|`metrics_server_resource_state`|present|The state of the metrics-server (present, absent, etc.)|
