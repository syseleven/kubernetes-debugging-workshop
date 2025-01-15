# Exercise 11

## Objective

A new version of an application is being rolled out, but several issues prevent the application from functioning properly. Investigate and fix the problems to ensure a successful rollout.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise11
     kubectl config set-context --current --namespace=<yourname>-exercise11
     ```
   - Deploy the manifests:
     ```bash
     kubectl apply -f manifests/
     ```

2. **Investigate the issues:**
   - Check the status of the deployment, pods, service, and ingress.
   - Investigate events, logs, and resource configurations to identify the problems.
   - Try reaching the ingress:
     ```bash
     # first get ip of ingress LB, 
     # e.g. `kubectl get svc -n ingress-nginx ingress-nginx-controller`
     curl <ingress-controller-ip> -H "Host: customer-app.local"
     ```

3. **Fix the issues:**
   - Resolve all the problems to ensure the application is functional and accessible.

4. **Test the application:**
   - All pods should be running and in a healthy state.
   - Verify that the application is reachable via the specified ingress.

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise11
```
