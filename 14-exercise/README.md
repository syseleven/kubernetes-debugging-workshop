# Exercise 14

## Objective

An application is deployed across two namespaces: frontend and backend. The frontend cannot communicate with the backend, and external traffic to the frontend is not routed correctly. Investigate and resolve these issues to restore communication and external access.

## Instructions

1. **Set up the exercise:**
   - Create two namespaces for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise14-frontend
     kubectl create namespace <yourname>-exercise14-backend
     ```
   - Deploy the manifests:
     ```bash
     kubectl apply -n <yourname>-exercise14-backend -f manifests/backend/
     kubectl apply -n <yourname>-exercise14-frontend -f manifests/frontend/
     ```

2. **Investigate the issues:**
   - Check the status of deployments, services, and the ingress:
     ```bash
     kubectl get deployments -n <yourname>-exercise14-frontend
     kubectl get deployments -n <yourname>-exercise14-backend
     kubectl get ingress -n <yourname>-exercise14-frontend
     ```
   - Inspect logs, network policies, and routing configurations for issues.
   - Try reaching the ingress:
     ```bash
     # first get ip of ingress LB, 
     # e.g. `kubectl get svc -n ingress-nginx ingress-nginx-controller`
     curl <ingress-controller-ip> -H "Host: frontend-app.local"
     ```

3. **Fix the issues:**
   - Resolve the network isolation issue between namespaces.
   - Fix the ingress routing problem to allow external access to the frontend.

4. **Test the application:**
   - Verify that the frontend communicates with the backend and that the application is accessible externally.

## Cleanup

After completing the exercise, clean up the namespaces:
```bash
kubectl delete namespace <yourname>-exercise14-frontend
kubectl delete namespace <yourname>-exercise14-backend
```
