# Exercise 12

## Objective

A multi-service application consists of a frontend, backend, and database. Users are reporting failures when accessing the application, and some services are unable to communicate with each other. Investigate and fix the issues to restore proper functionality.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise12
     kubectl config set-context --current --namespace=<yourname>-exercise12
     ```
   - Deploy the manifests:
     ```bash
     kubectl apply -f manifests/
     ```

2. **Investigate the issues:**
   - Check the status of the deployments, pods, and services:
     ```bash
     kubectl get deployments
     kubectl get pods
     kubectl get svc
     ```
   - Inspect logs for errors in each service:
     ```bash
     kubectl logs <frontend-pod>
     kubectl logs <backend-pod>
     kubectl logs <database-pod>
     ```

3. **Fix the issues:**
   - Investigate and resolve the configuration, networking, and resource problems across the frontend, backend, and database.
   - Ensure all services are functional and communicate correctly.

4. **Test the application:**
   - All pods should be running and in a healthy state.
   - Verify that users can access the application via the frontend and that all service dependencies are working.

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise12
```
