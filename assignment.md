# Debugging Kubernetes Pods and Containers with kubectl

## What is kubectl?

The Kubernetes command line tool `kubectl` communicates with a Kubernetes cluster's control plane using the Kubernetes API. The Kubernetes [Command line tool (kubectl)](https://kubernetes.io/docs/reference/kubectl/) page provides an in-depth tool reference.

## Syntax for kubectl Commands
```shell
kubectl [command] [TYPE] [NAME] [flags]
```

## Useful kubectl Pod and Container Debugging Commands

### `kubectl get pods [--namespace]` 
Retrieves a list of all available pods and each pod's current status. You may have to specify the `namespace`

### `kubectl logs`
Retrieves the logs of a specific pod. Do use this when you have to review logs or need to debug a container.

### `kubectl exec`
Debugs a container from the inside or explores the enviroment of the container itself.

### `kubectl debug`
Another useful `kubectl` container debugging command. Creates a clone of a pod that does not terminate if an error is experienced inside the container.

## Debugging Kubernetes Pods and Containers with kubectl strategy

When using kubectl to debug Kubernetes pods and containers, we recommend executing the following `kubectl` commands in this order:
1. `kubectl get pods`
2. `kubectl logs`
3. `kubectl exec` to explore the inside of the container and review other log files or configurations. 

# References

- [Pods](https://kubernetes.io/docs/concepts/workloads/pods/)
- [Debug Pods](https://kubernetes.io/docs/tasks/debug/debug-application/debug-pods/)
- [Containers](https://kubernetes.io/docs/concepts/containers/)
- [Debug Init Containers](https://kubernetes.io/docs/tasks/debug/debug-application/debug-init-containers/)


```shell
kubectl get pods --namespace 
```
**Note:** The