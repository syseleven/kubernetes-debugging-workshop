# Exercise 13

## Objective

An application is failing to start and behaving inconsistently across replicas due to issues with ConfigMap and Secret usage. Investigate and fix the problems to ensure the application runs correctly.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise13
     kubectl config set-context --current --namespace=<yourname>-exercise13
     ```
   - Deploy the manifests:
     ```bash
     kubectl apply -f manifests/
     ```

2. **Investigate the issues:**
   - Check the status of the deployment and pods:
     ```bash
     kubectl get deployments
     kubectl get pods
     ```
   - Inspect the logs and describe the pods to gather more information:
     ```bash
     kubectl logs <pod-name>
     kubectl describe pod <pod-name>
     ```
   - Examine the ConfigMap and Secret usage in the deployment manifest.

3. **Fix the issues:**
   - Resolve the misconfigurations in the ConfigMap and Secret usage.
   - Ensure that all pods start and behave consistently.

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise13
```
