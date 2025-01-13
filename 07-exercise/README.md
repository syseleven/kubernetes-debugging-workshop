# Exercise 7

## Objective

An application is failing. Investigate and resolve the issue so the application runs and becomes ready.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise07
     kubectl config set-context --current --namespace=<yourname>-exercise07
     ```
   - Deploy the manifests:
     ```bash
     kubectl apply -f manifests/
     ```

2. **Investigate the issue:**
   - Check the status of the deployment and pods:
     ```bash
     kubectl get deployment
     kubectl get pods
     ```
   - Describe the pods to gather more information:
     ```bash
     kubectl describe pod <pod-name>
     ```
   - Inspect the events and logs to identify the problem:
     ```bash
     kubectl logs <pod-name>
     ```

3. **Fix the issue:**
   - Identify the root cause of the failure.
   - Make the necessary updates to the resources to resolve the issue.

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise07
```
