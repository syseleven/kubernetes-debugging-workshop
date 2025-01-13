# Exercise 4

## Objective

An application is failing to start. Investigate and fix the issue to get the application running.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise04
     kubectl config set-context --current --namespace=<yourname>-exercise04
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
   - Describe the pods and inspect logs for errors:
     ```bash
     kubectl describe pod <pod-name>
     kubectl logs <pod-name>
     ```
   - Inspect the deployment and secret to identify misconfigurations:
     ```bash
     kubectl get secret
     kubectl describe secret <secret-name>
     ```

3. **Fix the issue:**
   - Identify and resolve the misconfiguration in the deployment or secret.
   - Apply the necessary changes and verify the pod starts successfully.

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise04
```
