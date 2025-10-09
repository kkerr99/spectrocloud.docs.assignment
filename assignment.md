# Debug Kubernetes Pods and Containers with Kubectl

## Kubectl Overview

The Kubernetes command line tool kubectl communicates with a Kubernetes cluster's control plane using the Kubernetes Application Programming Interface. The Kubernetes [Command line tool (kubectl)](https://kubernetes.io/docs/reference/kubectl/) page provides an in-depth tool reference.

##  Kubectl Command Syntax
```shell
kubectl [command] [TYPE] [NAME] [flags]
```

## Useful Kubectl Pod and Container Debugging Commands

| Kubectl Command | Description | Command Reference Page |
| ----------- | ----------- | ----------- |
| `kubectl get pods [--namespace <value>]`  | Retrieves a list of all available pods and each pod's current status. **Note:** You may need to specify the namespace value. | [get](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#get) |
| `kubectl logs`  | Retrieves the logs of a specific pod. Execute this command to review pod logs or debug a container. | [logs](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#logs) |
| `kubectl exec`  | Debugs a container from the inside or explores the enviroment of the container itself. | [exec](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#exec) |
| `kubectl debug`  | Creates a clone of a pod that does not terminate if an error is experienced inside the container. | [debug](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#debug) |

## Debug Kubernetes Pods and Containers with Kubectl Strategy

When using kubectl to debug Kubernetes pods and containers, we recommend executing the following commands in this order:
1. `kubectl get pods`
2. `kubectl logs`
3. `kubectl exec` (to explore the inside of the container and review other log files or configurations). 

## References

- [kubectl Quick Reference](https://kubernetes.io/docs/reference/kubectl/quick-reference/)
- [Pods](https://kubernetes.io/docs/concepts/workloads/pods/)
- [Debug Pods](https://kubernetes.io/docs/tasks/debug/debug-application/debug-pods/)
- [Containers](https://kubernetes.io/docs/concepts/containers/)
- [Debug Init Containers](https://kubernetes.io/docs/tasks/debug/debug-application/debug-init-containers/)