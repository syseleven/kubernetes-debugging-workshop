# Exercise 3

## Objective

An application is failing to start. Investigate and fix the issue so the application can run successfully.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise03
     kubectl config set-context --current --namespace=<yourname>-exercise03
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
   - Inspect the logs of the pod's container:
     ```bash
     kubectl logs <pod-name>
     ```
   - Check the ConfigMap to ensure it is created and properly referenced.

3. **Fix the issue:**
   - Identify and resolve the misconfiguration in the deployment or the ConfigMap.
   - Apply the necessary changes and verify the pod starts successfully.

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise03
```
