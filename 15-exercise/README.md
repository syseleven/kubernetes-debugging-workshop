# Exercise 15: Java Web Application Debugging

## Objective

The Java web application fails to operate correctly due to multiple issues. Investigate and resolve the problems to ensure the application is fully functional.

## Tasks

1. **Fix the readiness and liveness probes:**
   - The probes are not working correctly. Health can be checked under path `/healthz`.

2. **Fix the Ingress misconfiguration:**
   - The Ingress rules are incomplete, resulting in `404 Not Found` errors when accessing the application.

3. **Fix the missing environment variable:**
   - The application relies on the `APP_MESSAGE` environment variable to display a message on the homepage, but this variable is missing.

## Instructions

1. **Set up the exercise:**
   - Create a namespace for this exercise, replacing `<yourname>` with your name or identifier:
     ```bash
     kubectl create namespace <yourname>-exercise15
     kubectl config set-context --current --namespace=<yourname>-exercise15
     ```
   - Edit the ingress resource under `manifests/ingress-java.yaml` to distinguish from others.
   - Deploy the manifests:
     ```bash
     kubectl apply -f manifests/
     ```

2. **Investigate the issues:**
   - Check the status of the pod, service, and Ingress.
   - Inspect logs, events, and resource configurations to identify the problems.

3. **Fix the issues:**
   - Resolve all identified problems to ensure the application operates correctly.

4. **Test the application:**
   - Access the application via the Ingress URL.

## Cleanup

After completing the exercise, clean up the namespace:
```bash
kubectl delete namespace <yourname>-exercise15
```

