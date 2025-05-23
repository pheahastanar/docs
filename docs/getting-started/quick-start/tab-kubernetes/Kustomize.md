
# Kustomize Setup for Kubernetes

Kustomize allows you to customize Kubernetes YAML configurations.

## Prerequisites

- Kubernetes cluster is set up.
- Kustomize is installed.

## Steps

1. **Clone the Open WebUI Manifests:**

   ```bash
   git clone https://github.com/open-webui/k8s-manifests.git
   cd k8s-manifests
   ```

2. **Apply the Manifests:**

   ```bash
   kubectl apply -k .
   ```

3. **Verify Installation:**

   ```bash
   kubectl get pods
   ```

:::warning

If you intend to scale Open WebUI using multiple nodes/pods/workers in a clustered environment, you need to setup a NoSQL key-value database.
There are some [environment variables](https://docs.openwebui.com/getting-started/env-configuration/) that need to be set to the same value for all service-instances, otherwise consistency problems, faulty sessions and other issues will occur!

:::

## Access the WebUI

Set up port forwarding or load balancing to access Open WebUI from outside the cluster.
