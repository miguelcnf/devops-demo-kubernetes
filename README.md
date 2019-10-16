# Kubernetes demo

#### Requirements

* Docker
* Curl

#### Demo

1. Install minikube: https://kubernetes.io/docs/tasks/tools/install-minikube/
2. Start minikube: `minikube start`
3. Reuse Docker daemon: `$(minikube docker-env)`
4. Build hello-world image: `docker build -t hello:latest .`
5. Apply hello-world deployment: `kubectl -f deployment.yml`
6. Expose hello-world service: `kubectl expose deployment hello-world --type=LoadBalancer --port=8080
`
7. Access it via minikube service: `curl $(minikube service --url hello-world)`

#### Extra

Explore kubernetes with:

* `kubectl get pods`
* `kubectl get deploy/hello-world`
* `kubectl get service/hello-world`
