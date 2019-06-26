## Understanding Kubernetes Architecture
======================================================================
# This topic has a total weight of 19% in exam

#### Note: Below is an interactive diagream which help understand K8 in details
https://interactive.linuxacademy.com/diagrams/ThePodofMinerva.html


  ## Kubernetes Architecture has two main roles:

  #### Master Node:
  There are 4 components in master node
  * API server: The communication hib for all cluster components. It exposes the Kubernetes API.[See Documentation for more details](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-apiserver/)
  * Scheduler: Assigns your app to worker node. AUto-detcets which pod to assign to which node based on resource requirements.
  * Control Manager: Maintains the cluster. Handles node failures, replicating components, maintaining the correct amount of pods,etc.
  * etcd: Data store that stores the cluster configuration


#### Worker Node:
There are 3 components in worker node:
  * kubelet: Runs and manages the containers on the node and talks to the API server
  * kube-proxy: Load balances traffic between applications components.
  * container runtime: The Program that runs your container (Docker,rkt,containerd).
