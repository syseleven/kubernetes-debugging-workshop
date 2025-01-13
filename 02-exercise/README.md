# Exercise 2

## Objective

A service has been deployed in your namespace, but it doesn't seem to forward traffic to the pods. Your task is to investigate and resolve the issue to make the service functional.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise02
     kubectl config set-context --current --namespace=<yourname>-exercise02
     ```
   - Deploy the manifests:
     ```bash
     kubectl apply -f manifests/
     ```

2. **Investigate the issue:**
   - Check the status of the service:
     ```bash
     kubectl get service
     ```
   - Inspect the endpoints:
     ```bash
     kubectl get endpoints
     ```
   - Describe the service and the pods to gather more information:
     ```bash
     kubectl describe service <service-name>
     kubectl describe pod <pod-name>
     ```

3. **Fix the issue:**
   - Identify the root cause of the connectivity problem.
   - Update the necessary resource(s) to fix the issue.
   - Test the service to confirm it forwards traffic correctly.

4. **Test the service:**
   - Use a `kubectl port-forward` command to test the service locally:
     ```bash
     kubectl port-forward service/broken-service 8080:80
     curl http://localhost:8080
     ```

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise02
```
