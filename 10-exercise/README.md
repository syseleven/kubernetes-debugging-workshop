# Exercise 10

## Objective

A web application is not accessible through its Ingress resource. Investigate and fix the issue to make the application accessible.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise10
     kubectl config set-context --current --namespace=<yourname>-exercise10
     ```
   - Edit the ingress ressource in `manifests/ingress.yaml` and replace `YOURNAME` to distinguish from others
   - Deploy the manifests:
     ```bash
     kubectl apply -f manifests/
     ```

2. **Investigate the issue:**
   - Check the status of the deployment, service, and ingress:
     ```bash
     kubectl get deployment
     kubectl get svc
     kubectl get ingress
     ```
   - Try reaching the ingress:
     ```bash
     # first get ip of ingress LB, 
     # e.g. `kubectl get svc -n ingress-nginx ingress-nginx-controller`
     curl <ingress-controller-ip> -H "Host: web-app.local"
     ```
   - Describe the ingress and check for any misconfigurations:
     ```bash
     kubectl describe ingress <ingress-name>
     ```
   - Check logs of the ingress controller (e.g., Traefik, NGINX) for additional clues:
     ```bash
     kubectl logs -n <ingress-controller-namespace> <ingress-controller-pod>
     ```

3. **Fix the issue:**
   - Identify and resolve the root cause of the misconfiguration.
   - Verify the application is accessible through the ingress resource.

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise10
```
