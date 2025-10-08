# Debugging Kubernetes with kubectl

## What is kubectl?

kubectl is the CLI that is used to interact with k8s. The kubectl cli commmunicates with the kubernettes API server.

## Syntax for kubectl Commands
```shell
kubectl [command] [TYPE] [NAME] [flags]
```

## Useful kubectl Debugging Commands

| kubectl Command | Description |
| ----------- | ----------- |
| kubectl get pods [--namespace]  | Retrieves a list of all available pods and each pod's current status. You may have to specify the `namespace`. |
| kubectl logs | Retrieves the logs of a specific pod. Do use this when you have to review logs or need to debug a container. |
| kubectl exec | Debugs a container from the inside or explores the enviroment of the container itself. |
| kubectl debug | Another option to considering when debugging a container. Creates a clone of a pod that does not terminate if an error is experienced inside the container. |

## Debugging Kubernetes with kubectl strategy

When using kubectl to debug Kubernetes, we recommend executing the following kubectl commands in this order:
1. `kubectl get pods`
2. `kubectl logs`
3. `kubectl exec` to explore the inside of the container and review other log files or configurations. 

# References

- https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#-strong-getting-started-strong-
- [What is Kubernetes](https://kubernetes.io/docs/concepts/overview/)


```shell
kubectl get pods --namespace 
```
**Note:** The