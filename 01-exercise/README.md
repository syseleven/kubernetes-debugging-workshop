# Exercise 1

## Objective

A deployment has been created in your namespace, but the pod is stuck in a non-healthy state. Your task is to investigate and fix the issue so that the pod starts successfully.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise01
     kubectl config set-context --current --namespace=<yourname>-exercise01
     ```
   - Deploy the provided manifests:
     ```bash
     kubectl apply -f manifests/
     ```

2. **Investigate the issue:**
   - Check the status of the deployment:
     ```bash
     kubectl get deployment
     ```
   - Examine the pods:
     ```bash
     kubectl get pods
     kubectl describe pod <pod-name>
     ```
   - Investigate events, logs, and other resources to identify the problem.

3. **Fix the issue:**
   - Once you've identified the root cause, modify the manifest or Kubernetes resource(s) to resolve the problem.
   - Apply your changes and verify:
     - the pod is running successfully

## Cleanup

After completing the exercise, delete the namespace to clean up:
```bash
kubectl delete namespace <yourname>-exercise01
```
