## Creating your own Project

Create a new project called __mlflow-sandbox__

``oc new-project mlflow-sandbox``{{execute}}

## Install Helm

Add Larribas helm repository

``helm repo add larribas https://larribas.me/helm-charts``{{execute}}

```bash
"larribas" has been added to your repositories
```

Add MLflow operator

``helm install mlflow-sandbox larribas/mlflow --version 1.0.1``{{execute}}


To grant or bind an Security Context Constraints to any user with the oc command

``oc adm policy add-scc-to-user anyuid -z mlflow-sandbox``{{execute}}

<span style="color:red">*CAUTION*</span>, anyuid provides all features of the restricted SCC this will be the equivalent as allowing UID 0, or root user, both inside and outside the container.


## Install MLflow

``pip install mlflow``{{execute}}



