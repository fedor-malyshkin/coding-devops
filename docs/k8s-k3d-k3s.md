# K3D/K3S

The lightweight docker-based version of k8s (k3s in docker)

## Links
* Site
    * https://k3s.io/
    * https://k3d.io/
* Useful links
    * [Rancher Meetup - May 2020 - Simplifying Your Cloud-Native Development Workflow With K3s, K3c and K3d](https://www.youtube.com/watch?v=hMr3prm9gDM)
    * [November Meetup - GitOps with Rancher Continuous Delivery](https://www.youtube.com/watch?v=7o9_V-W60m8)

## Requirements
* docker
* root rights
* (and better the membership of the `docker` group)


## Installation

```shell
curl -s https://raw.githubusercontent.com/rancher/k3d/main/install.sh | bash
```

## Quick Start

Create a cluster named mycluster with just a single server node:

```shell
k3d cluster create mycluster
```
Use the new cluster with kubectl, e.g.:

```shell
kubectl get nodes
```

## Useful commands
```shell
# Current version of k3d and k3s
k3d version 
```
### Cluster management
```shell
# Get list of all clusters
k3d cluster getkube

# Create tailored cluster (6550 for kubectl, and published port on localhost:8080)
k3d cluster create  demo23 --agents 3 --api-port 6550 --port 8080:80@loadbalancer
kubectl config use-context k3d-demo23
kubectl cluster-info

# Stop this cluster
k3d cluster stop  demo23
# delete this cluster
k3d cluster delete  demo23
```

### Image management
```shell
(test!!!) k3d load image -c demo23 sample-image:label
```