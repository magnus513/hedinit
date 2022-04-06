# Hedin IT
This project contains the cloud journey proposal (Azure) roadmap for Hedin IT.

## Intro
When I write this document I assume this as the [target architecture](https://github.com/magnus513/ewfhometest). This could of cause change depending of Hedin IT´s target architecure.

## Create HLD
HLD (High Level Design). This is an image of the Azure environment with technical data e.g. VNet, subnets, services etc. **2 days**

## Create AKS (Azure Kubernetes Service) cluster
### Step 1
Create two basic AKS cluster (TEST, PROD) using IaC (InfrastructureAsCode) terraform gitrepo. **3 days** 
### Step 2
Hot deploy an application into the cluster and make it run with success. k8s config for AKS in gitrepo. **2 days**
### Step 3
Documentation how to perform operations in AKS.
* Add more resources
* Update AKS (kubeadm,kubelet) versions
* Troubleshooting
### HA
### Scaling

## Create CI/CD pipeline
### CI
Build/Test and save artifact using Azure DevOps and artifactory repo.
### CD
Deploy artifact as docker container with tag (semantic version).

## O11Y - observability
Investigate and install best choice of monitoring service (Prometheus?).
### Create alarms
### Create runbook for incidents