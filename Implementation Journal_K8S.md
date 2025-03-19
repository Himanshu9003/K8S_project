#                **IMPLEMENTATION JOURNAL \-**  **Kubernetes Two-Tier Application Deployment & Monitoring** 

| Submitted By | Himanshu Singh |
| :---- | :---- |
| Submitted To | Vipin Sir |
| Test Case Version | Version 1.0 |
| Reviewer  Name | Vipin Sir |

**Goal \-**

Install and set up a Minikube single-node Kubernetes cluster. Understand the architecture of Kubernetes. Deploy a **two-tier Flask application with MySQL** on the cluster by Kubectl using YAML manifests. Install and set up **Prometheus and Grafana** for monitoring running applications on cluster, setting up **alerts**, and exposing the application to the **internet using the NGINX Ingress Controller**.

**Table of Contents**

## 

## **Pre-requisites**

## Hardware Requirements

* **CPU:** Minimum 4-core processor.  
* **RAM:** At least 8GB RAM (Recommended: 16GB).  
* **Storage:** Minimum 50GB free disk space.

## Software Requirements

* **OS:** Ubuntu 20.04 or above.  
* **Tools:**  
  * Minikube (Latest Version)  
  * kubectl  
  * Podman or Docker  
  * Helm (for Prometheus/Grafana installation)  
  * NGINX Ingress Controller

## Networking Requirements

* **Minikube Networking:** Cluster network with NodePort access.  
* **Public Internet Access:** Required for exposing the app via Nginx or cloud-based LoadBalancer.


## **STEPS**:

## STEP 1:  Install Docker 

## Command executed \-  

| \# Add Docker's official GPG key:sudo apt-get updatesudo apt-get install ca-certificates curlsudo install \-m 0755 \-d /etc/apt/keyringssudo curl \-fsSL https://download.docker.com/linux/ubuntu/gpg \-o /etc/apt/keyrings/docker.ascsudo chmod a+r /etc/apt/keyrings/docker.asc\# Add the repository to Apt sources:echo \\  "deb \[arch=$(dpkg \--print-architecture) signed-by=/etc/apt/keyrings/docker.asc\] https://download.docker.com/linux/ubuntu \\  $(. /etc/os-release && echo "${UBUNTU\_CODENAME:-$VERSION\_CODENAME}") stable" | \\  sudo tee /etc/apt/sources.list.d/docker.list \> /dev/nullsudo apt-get updatesudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin |
| :---- |

