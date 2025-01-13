# Kubernetes Debugging Workshop

This workshop provides hands-on exercises focused on common debugging tasks in Kubernetes. Each exercise is designed to simulate real-world issues developers and operators might encounter while working with Kubernetes-managed applications, such as:

- Pods failing to start due to incorrect configurations or missing resources.
- Connectivity issues between services and their pods.
- Applications failing due to misconfigured ConfigMaps or missing Secrets.
- Pods getting stuck in `CrashLoopBackOff` states.
- Problems with resource limits causing throttling or crashes.
- Persistent volume claims not being bound or accessible.
- Network policies blocking traffic unexpectedly.
- Misconfigured readiness or liveness probes.
- Issues with Ingress routing making applications inaccessible.

## Workshop Overview

- **Audience**: Developers and operators using managed Kubernetes clusters.
- **Focus**: Debugging common application issues in Kubernetes.
- **Cluster Setup**: A shared workshop cluster where each participant works in their own namespace.

### Directory Structure
Each exercise is in a separate directory. Each directory contains:

- A `README.md` file with the exercise description, setup instructions, and cleanup steps.
- A `manifests/` directory with YAML files needed to create the exercise scenario.

### Solutions
The solutions for these exercises will be kept separate to prevent students from cheating.
