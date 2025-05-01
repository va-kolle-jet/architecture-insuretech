minikube start --addons=metrics-server

kubectl apply -f ./deployment.yaml
kubectl apply -f ./service.yaml
kubectl apply -f ./hpa.yaml

kubectl get services

kubectl port-forward svc/scaletestapp 8080:8080

minikube dashboard
