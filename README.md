# kube-metrics-server
Ansible role to deploy metrics server on a Kubernetes cluster.

## Variables

|Name|Default value|Description|
|----|-------------|-----------|
|`kube_metrics_server_version`|v0.3.6|The version of the metrics-server.|
|`kube_metrics_server_kubeconfig`|~/.kube/config|Path to the kubeconfig to use.|
|`kube_metrics_server_resource_state`|present|The state of the metrics-server (present, absent, etc.)|
|`kube_metrics_server_certfile`|`/path`| - |
|`kube_metrics_server_keyfile`|`/path`| - |
|`kube_metrics_server_requestheader_client_ca`|`/path`| - |
|`kube_metrics_server_kubelet_cafile`|`/path`| - |
