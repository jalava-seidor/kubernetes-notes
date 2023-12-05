# Kubernetes

Orchestration platform for automating containerized applications

## Basics

Components: **Control plane** and **Data Plane**

### Control Plane

#### `kube-apiserver`

The API server is the main entry point for interacting with Kubernetes. It exposes an API that can be used to create, read, update, and delete Kubernetes resources.

#### `etcd`

Etcd is a distributed key-value store that Kubernetes uses to store its state. Etcd is responsible for storing the configuration of the cluster, as well as the current state of all the resources in the cluster.

#### `kube-scheduler`

The scheduler is responsible for assigning pods to nodes. It considers the available resources on each node, as well as the constraints of the pods, to make sure that the pods are scheduled to run on the nodes where they can run the most efficiently.

#### `kube-controller-manager`

The controller manager is a collection of controllers that perform various tasks, such as managing the lifecycle of pods, replicating pods to ensure that the desired number of pods are running, and managing the lifecycle of services

#### `cloud-controller-manager`

The cloud-controller-manager is responsible for mana
ging the interaction between Kubernetes and cloud providers. It can perform tasks such as creating and managing cloud resources, such as load balancers and volumes

### Data Plane

The nodes in the cluster, workers with the application and dependencies.

#### Container Runtime

`Docker` or `containerd`

#### `kubelet`

Responsible for communications between the control plane and the nodes.

#### Addons

Extra functionalities:

- DNS
- Web UI
