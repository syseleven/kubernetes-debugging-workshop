# Exercise 9

## Objective

A frontend application is unable to communicate with its backend. Investigate and fix the issue to restore communication between the frontend and backend.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise09
     kubectl config set-context --current --namespace=<yourname>-exercise09
     ```
   - Deploy the manifests:
     ```bash
     kubectl apply -f manifests/
     ```

2. **Investigate the issue:**
   - Check the status of the pods and services:
     ```bash
     kubectl get pods
     kubectl get svc
     ```
   - Verify if the frontend can communicate with the backend using logs:
     ```bash
     kubectl logs <frontend-pod-name>
     ```
   - Inspect the network policy in place and how it affects traffic:
     ```bash
     kubectl describe networkpolicy <network-policy-name>
     ```

3. **Fix the issue:**
   - Ensure the applications can communicate successfully.
   - Make the necessary updates to the resources to resolve the issue.

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise09
```
