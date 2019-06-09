# Core concepts (Weights 19% of Exam)
===============================================================================

## Understanding Kubernetes Architecture:
* Kubernetes Cluster Architecture
* Kubernetes API Primitives.
* Kubernetes Services and Network Primitives

###### For details and diagram refer to below:

1. Important [Link to pod of Minireva](https://interactive.linuxacademy.com/diagrams/ThePodofMinerva.html).
2. Important Links to Official Kubernetes Documentations:
    * [Kubernetes Components Overview](https://kubernetes.io/docs/concepts/overview/components)
    * [API Server](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-apiserver/)
    * [Scheduler](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-scheduler/)
    * [Controller Manager](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-controller-manager/)
    * [ectd Datastore](https://kubernetes.io/docs/concepts/overview/components/#etcd)
    * [kubelet](https://kubernetes.io/docs/reference/command-line-tools-reference/kubelet/)
    * [kube-proxy](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-proxy/)
    * [Container Runtime](https://kubernetes.io/docs/concepts/overview/components/#container-runtime)

###### Kubernetes Cluster Architecture:
Kubernetes architecture has two main roles: the master role and the worker role. This section we learned about the at what each roles is and the individual components that it make it run .

## We deployed a pod:
Below is an example how to deploy a pod in kubernetes cluster. We only have to deploy a pod in master and master will orchestrate it through out the Cluster.

```yml
cat << EOF | kubectl create -f -
apiversion: v1
kind: pod
metadata:
  name: ngnix
spec:
  container:
    -name: ngnix
    image: nginx
EOF    
```
