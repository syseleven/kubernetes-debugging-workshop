# Exercise 5

## Objective

An application is stuck in a `CrashLoopBackOff` state. Your task is to investigate and fix the issue so that the application starts successfully.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise05
     kubectl config set-context --current --namespace=<yourname>-exercise05
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
   - Describe the pods to examine the issue:
     ```bash
     kubectl describe pod <pod-name>
     ```
   - Inspect the logs of the crashing pod:
     ```bash
     kubectl logs <pod-name>
     ```

3. **Fix the issue:**
   - Identify and resolve the root cause of the `CrashLoopBackOff` state.
   - Update the deployment as necessary and verify the application starts successfully.

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise05
```
