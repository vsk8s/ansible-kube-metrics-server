# kube-metrics-server
Ansible role to deploy metrics server on a Kubernetes cluster.

## Deployment
This role assumes that:
1. You have kubectl installed on your local machine
2. You have a valid kubeconfig with full privileges for your target cluster
3. You have [configured](https://kubernetes.io/docs/tasks/access-kubernetes-api/configure-aggregation-layer/) aggregator routing and requestheader settings in your kube-apiserver
4. The required certificate files are present in your local machine under the directories that you have specified (see below)

## Variables

|Name|Default value|Description|
|----|-------------|-----------|
|`kube_metrics_server_version`|`v0.3.6`|The version of the metrics-server.|
|`kube_metrics_server_kubeconfig`|`~/.kube/config`|Path to the kubeconfig to use.|
|`kube_metrics_server_resource_state`|`present`|The state of the metrics-server (present, absent, etc.)|
|`kube_metrics_server_certfile`|`/tmp/metrics-server.cert`|Certificate signed by Requestheader CA for metrics-server.|
|`kube_metrics_server_keyfile`|`/tmp/metrics-server.key`|Private key for metrics-server certificate.|
|`kube_metrics_server_requestheader_client_ca`|`/tmp/kube-requestheader-ca.cert`|Requestheader CA file used by kube-apiserver and metrics-server.|
|`kube_metrics_server_kubelet_cafile`|`/tmp/kubelet-ca.cert`|Kubelet CA file, used to connect to nodes to get metrics.|
|`kube_metrics_server_metric_resolution`|`10s`|The polling resolution of the metrics-server.|
|`kube_metrics_server_verbosity`|`2`|Verbosity level of metrics-server for logging.|

## Resources
[metrics-server GitHub repository](https://github.com/kubernetes-incubator/metrics-server)

[Kubernetes documentation on aggegation layer](https://kubernetes.io/docs/tasks/access-kubernetes-api/configure-aggregation-layer/)

