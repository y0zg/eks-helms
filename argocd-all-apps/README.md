# Argocd custom apps Installation Chart <img src="https://cncf-branding.netlify.app/img/projects/helm/icon/color/helm-icon-color.svg" width="30px">
![](https://argoproj.github.io/argo-cd/assets/argocd-ui.gif)


* This chart will deploy Argocd-applications from defined GitHub/helm repositories in cluster provided that Argocd is already installed.

* Please modify the applications in values.yml as per the requirement and commit this chart in your deployment repo for Gitops.

* It is recommended that this helm chart should go to the cluster via Gitops only so please do necessary changes in values.yml

**Usage:**
* Clone the repo
```
git clone -b main https://github.com/suyog1pathak/eks-helms.git
OR
git clone -b main git@github.com:suyog1pathak/eks-helms.git
```

* Change Directory
```
cd argocd-all-apps
```

* Install helm chart with vars
```
helm install argocd-apps .
```