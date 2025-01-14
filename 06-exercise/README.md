# Exercise

## Objective

An application is failing after a short time of running. Investigate and identify the issue.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise06
     kubectl config set-context --current --namespace=<yourname>-exercise06
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
   - Monitor resource usage and limits:
     ```bash
     kubectl top pod <pod-name>
     ```
   - Check for events related to resource constraints:
     ```bash
     kubectl describe pod <pod-name>
     ```

3. **Fix the issue:**
   - Identify the issue and modify the manifests as necessary.
   - Reapply the changes and monitor the performance to ensure the issue is resolved.

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise06
```
