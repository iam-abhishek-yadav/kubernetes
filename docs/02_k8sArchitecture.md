# `Kubernetes Architecture`

## `Control Plane:`

The control plane is responsible for managing the overall state of the cluster and making global decisions, such as scheduling. It consists of several components:

1. **`API Server:`**
   - Exposes the Kubernetes API.
   - Accepts and processes RESTful requests, serving as the front-end for the Kubernetes control plane.

2. **`Scheduler:`**
   - Responsible for scheduling pods onto nodes in the cluster.
   - Takes into consideration factors like resource requirements, affinity/anti-affinity rules, and more.

3. **`etcd:`**
   - Key-value store used as the primary database for the cluster.
   - Stores the configuration data and provides a reliable and highly available data store for the entire cluster.

4. **`Controller Manager:`**
   - Manages controllers, which are responsible for regulating the state of the system.
   - Examples include the Replication Controller, which ensures the specified number of replicas of a pod are running.

5. **`Cloud Controller Manager:`**
   - Interfaces with the underlying cloud provider to manage resources.
   - Integrates cloud-specific features into the cluster.

## `Data Plane:`

The data plane is responsible for running application workloads (containers) and consists of the following components:

1. **`Container Runtime:`**
   - Responsible for running containers.
   - Options include:
     - **`dockershim:`** Intermediary layer that allows Kubernetes to use Docker as the container runtime.
     - **`containerD:`** Industry-standard core container runtime.
     - **`criO:`** Lightweight container runtime for Kubernetes.

2. **`kubelet:`**
   - Runs on each node in the cluster.
   - Ensures that containers are running in a Pod.
   - Communicates with the API server to receive instructions and report the status of the containers.

3. **`kube-proxy:`**
   - Maintains network rules on nodes.
   - Manages communication between different Pods and services.
   - Enables load balancing across the cluster.

## `Summary:`

- **`Control Plane:`** Manages the overall state and decisions of the cluster.
  - API Server, Scheduler, etcd, Controller Manager, Cloud Controller Manager.
- **`Data Plane:`** Responsible for running application workloads.
  - Container Runtime, kubelet, kube-proxy.

![Kubernetes Cluster Architecture](https://kubernetes.io/images/docs/kubernetes-cluster-architecture.svg)

This architecture ensures the scalability, reliability, and flexibility of Kubernetes clusters, enabling the orchestration of containerized applications in a distributed environment.
