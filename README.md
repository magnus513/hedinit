# Hedin IT
This project contains the cloud journey proposal (Azure) roadmap for Hedin IT.

## Intro
When I write this document I assume this as the [target architecture](https://github.com/magnus513/ewfhometest). This could of cause change depending of Hedin IT´s target architecure.

## Create HLD
HLD (High Level Design). This is an image of the Azure environment with technical data e.g. VNet, subnets, services etc. **5 days**

## Create AKS (Azure Kubernetes Service) cluster
### Step 1
Create two basic AKS cluster (TEST, PROD) using IaC (InfrastructureAsCode) terraform gitrepo. **7 days** 
### Step 2
Hot deploy an application into the cluster and make it run with success. k8s config for AKS in gitrepo. **5 days**
### Step 3
Documentation how to perform operations in AKS.
* Add more resources
* Update AKS (kubelet,kubeadm,kubelet) versions
* Troubleshooting
### HA
Needs definition
### Scaling
Needs definition

## Code version handling
Usage of github (git) and the magic with github actions.

## Create CI/CD pipeline
### CI
Build/Test and save artifact using Azure DevOps and artifactory repo.
#### Quality Gates in Azure DevOps
* SonarQube (Bugs,Code smells,Coverage,Duplications,Maintainability,Reliability,Security,Technical Debt,Vulnerabilities)
* [Snyk](https://snyk.io/
* Save and version for artifact (artifactory, nexus).
### CD
Deploy artifact as docker container with tag (semantic version).

Usage of tool is very important. We could start with a light version: Azure DevOps and later on implement something like [flux](https://www.cncf.io/projects/flux/).

## O11Y - observability
Investigate and instal best choice of monitoring service 
* [Prometheus](https://www.cncf.io/projects/prometheus/)
* Thanos
### Create alarms
### Create runbook for incidents

## On-boarding documentation
Create On-boarding documentation for new DevOps member into the Hedin IT organization.