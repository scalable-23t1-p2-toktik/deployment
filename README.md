# deployment
The submodules here doesn't serve functional purpose other than a placeholder to redirect to the
repo that is part of this assignment

# Prerequisite
- minikube
  - ``` curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 ```
  - ``` sudo install minikube-linux-amd64 /usr/local/bin/minikube ```

Before kubectl, do:
```
minikube start
```

When kubectl apply is done, run:
```
minikube tunnel
```
