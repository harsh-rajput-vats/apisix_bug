# APISIX Gateway deployment steps for Kubernetes

  

### Notes:

Proceed to further step only if all workloads/pods are in running state from previous step. You may have to wait few minutes for that.


### Step 0: Environment Setup

0.1. Install minikube

0.2. `minikube start`, also you can use `minikube dashboard` for visualization of pods

0.3. Create required namespace `kubectl create namespace seda-redesign`


### Step 1: Start etcd

`kubectl apply -f etcd.yaml`

  

### Step 2: Start apisix

`kubectl apply -f apisix.yaml`

  

### Step 3: Start apisix-dashboard

`kubectl apply -f apisix-dashboard.yaml`

  

### Forward port to dashboard

`kubectl port-forward service/apisix-dashboard 8080:80 -n seda-redesign`