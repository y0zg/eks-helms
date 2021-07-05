# Argocd-Rollout Installation Yaml 
![](https://miro.medium.com/max/1640/1*8MDBjrYv5W2ANPok4EO3Tg.png)


* This Yaml will install argocd-rolllouts.


**Usage:**
* Clone the repo
```
git clone -b main https://github.com/suyog1pathak/eks-helms.git
OR
git clone -b main git@github.com:suyog1pathak/eks-helms.git
```

* Change Directory
```
cd argocd-rollouts
```

* Create namespace
```
kubectl create namespace argo-rollouts
```

* Install 
```
kubectl apply -f main.yml -n argo-rollouts
```