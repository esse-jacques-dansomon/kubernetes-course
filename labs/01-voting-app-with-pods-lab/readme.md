# Voting app with pods

```shell
alias k="kubectl"
k create -f db.yaml
k create -f redis.yaml
k create -f worker.yaml
k create -f vote-app.yaml
k create -f result-app.yaml

k delete -f db.yaml
k delete -f redis.yaml
k delete -f worker.yaml
k delete -f vote-app.yaml
k delete -f result-app.yaml

minikube service vote-service --url
minikube service result-service --url
```