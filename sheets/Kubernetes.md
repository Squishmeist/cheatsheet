# Kubernetes

# Installation

1. **Install Kubectl**: Follow the instructions on the [official Kubernetes website](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/) to install Kubectl.

   ```sh
   snap install kubectl --classic
   ```

2. Connect with azure kubernetes services

   ```sh
   az login
   ```

   ```sh
   az account set --subscription <key>
   ```

   ```sh
   az aks get-credentials --resource-group <resource-name> --name <cluster-name> --overwrite-existing
   ```

# Commands

To go into a cluster

```sh
kubectl config use-context <cluter-name>
```

To show pods

```sh
kubectl get pod
```

To show logs

```sh
kubectl get logs <pod-name>
```

To show live logs

```sh
kubectl get logs -f <pod-name>
```

To get into pod

```sh
kubectl exec -it <pod-name> -- /bin/sh
```

Restart pod

```sh
kubectl rollout restart <deployment-name>
```
