# Voting app with pods

```shell
alias k="kubectl"
k create -f db-deploy.yaml
k create -f redis-deploy.yaml
k create -f worker-deploy.yaml
k create -f vote-app-deploy.yaml
k create -f result-app-deploy.yaml

k delete -f vote-app.yaml
k delete -f result-app.yaml
k delete -f worker.yaml

minikube service vote-service --url
minikube service result-service --url
```