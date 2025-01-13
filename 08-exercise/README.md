# Exercise 8

## Objective

An application is failing. Investigate and fix the issue.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise08
     kubectl config set-context --current --namespace=<yourname>-exercise08
     ```
   - Deploy the manifests:
     ```bash
     kubectl apply -f manifests/
     ```

2. **Investigate the issue:**
   - Check the status of the pods and persistent volume claim:
     ```bash
     kubectl get pods
     kubectl get pvc
     kubectl get pv
     ```
   - Describe the pods, PVC, and PV to gather more information:
     ```bash
     kubectl describe pod <pod-name>
     kubectl describe pvc <pvc-name>
     kubectl describe pv <pv-name>
     ```
   - Inspect events and logs to identify the problem.

3. **Fix the issue:**
   - Identify and resolve the root cause of the problem.
   - Make the necessary updates to the resources to resolve the issue.

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise08
```
