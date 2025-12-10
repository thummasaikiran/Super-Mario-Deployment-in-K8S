# Super-Mario-Deployment-in-K8S
 **How to run super mario**

# Apply deployment first
kubectl apply -f deployment.yaml

# Apply service second
kubectl apply -f service.yaml

# Port forward to localhost:8080
kubectl port-forward service/mario 8080:80

**The reason to forward to local port :**
LoadBalancer doesn't work on local computers (Minikube/Docker Desktop) without special setup. That's why we use port-forwarding to expose services to localhost.
 
