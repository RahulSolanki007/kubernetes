# Kubernetes Examples

This repository contains basic Kubernetes manifests that create an nginx application using a Pod, ReplicaSet, or Deployment.

## Primitives

- `pods/pod-definition.yaml` creates a single `myapp` Pod.
- `replicaset/replicaset.yaml` creates a `myapp-replicaset` ReplicaSet with two nginx Pods.
- `deployment/deployment.yaml` creates a `myapp-deployment` Deployment with two nginx Pods.

All manifests use the `nginx` container image and assign the `app: frontend` label.

## Prerequisites

- A working Kubernetes cluster
- `kubectl` configured to access the cluster
- Internet access to pull the `nginx` container image

## Usage

Create individual resources:

```bash
kubectl apply -f pods/pod-definition.yaml
kubectl apply -f replicaset/replicaset.yaml
kubectl apply -f deployment/deployment.yaml
```

Create all resources from the repository root:

```bash
kubectl apply -f pods/
kubectl apply -f replicaset/
kubectl apply -f deployment/
```

View the resources:

```bash
kubectl get pods
kubectl get replicasets
kubectl get deployments
```

Delete individual resources:

```bash
kubectl delete -f pods/pod-definition.yaml
kubectl delete -f replicaset/replicaset.yaml
kubectl delete -f deployment/deployment.yaml
```

Delete all resources:

```bash
kubectl delete -f pods/
kubectl delete -f replicaset/
kubectl delete -f deployment/
```
