# deployment
The submodules here doesn't serve functional purpose other than a placeholder to redirect to the
repo that is part of this assignment

# Prerequisite (In Linux, cuz I don't know other OS)

## Docker Desktop Route:
- Go to setting, enable kubernetes

- Go to /k8s directory with your favorite terminal, then:
  - ``` kubectl apply -f . ```

## Minikube Route:

- Install minikube:
  - ``` curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 ```
  - ``` sudo install minikube-linux-amd64 /usr/local/bin/minikube ```


- Install kubectl:
  - ``` curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" ```
  - ``` sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl ```

- Install helm:
  - ``` curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 ```
  - ``` chmod 700 get_helm.sh ```
  - ``` ./get_helm.sh ```

- Install traefik:
  - ``` helm repo add traefik https://traefik.github.io/charts ```
  - ``` helm repo update ```
  - ``` helm install traefik traefik/traefik ```

- Run minikube
  - ``` minikube start ```

- Go to /k8s directory with your favorite terminal, then:
  - ``` kubectl apply -f . ```

- (Maybe) You'll have to check the traefik service to get the address to access the web app:
  - ``` kubectl describe service traefik ```
  - Then access the webapp through the that IPv4 address
