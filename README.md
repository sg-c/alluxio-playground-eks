# alluxio-playground-eks

## Prerequisites
### Install kubectl and eksctl
```
# mac os
brew install weaveworks/tap/eksctl
brew upgrade eksctl && brew link --overwrite eksctl
```
Check the kubectl version and make sure its version is >= 1.24.
```
# check kubectl version
kubectl version | grep Client | cut -d : -f 5
# check eksctl version
eksctl version
```
## Create EKS cluster
```
eksctl create cluster -f cluster.yaml
```

## Clean up
After using the EKS resources, make sure you clean them up to stop generating costs.
```
eksctl delete cluster -f cluster.yaml
```
