# Helm

The package manager for Kubernetes

## Links
* Site
    * https://helm.sh
* Useful links
    * [An Introduction to Helm](https://youtu.be/Zzwq9FmZdsU)

## Requirements
* k8s cluster


## Installation

```shell
curl https://baltocdn.com/helm/signing.asc | sudo apt-key add -
sudo apt-get install apt-transport-https --yes
echo "deb https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
sudo apt-get update
sudo apt-get install helm
```

## Quick Start
Once you have Helm ready, you can add a chart repository. Check Artifact Hub for available Helm chart repositories.

```shell
helm repo add bitnami https://charts.bitnami.com/bitnami
```
