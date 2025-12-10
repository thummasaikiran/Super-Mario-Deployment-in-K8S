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




 ![super-mario-bros-](https://github.com/user-attachments/assets/f1dc3a5f-33d1-4190-80e7-690b7dd677a6)

