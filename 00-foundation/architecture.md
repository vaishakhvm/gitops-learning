# Target Architecture

This course separates application delivery from application deployment.

```text
Developer
   |
   v
Application repository
   |
   v
GitHub Actions: test, scan, build image
   |
   v
Container registry
   |
   v
GitOps repository: manifests, Helm values, overlays
   |
   v
Argo CD inside the cluster
   |
   v
Kubernetes resources
   |
   v
Running application
```

## Responsibilities

| Component | Responsibility |
| --- | --- |
| Application repository | Source code and application tests |
| GitHub Actions | Validate code, scan it, build and publish an image |
| Container registry | Store versioned container images |
| GitOps repository | Declare the desired deployment state |
| Argo CD | Watch Git, compare state and reconcile the cluster |
| Kubernetes | Run workloads and maintain resource-level desired state |

## Important boundary

A successful image build does not automatically mean a successful deployment. CI proves that an artifact can be built and tested. Argo CD and Kubernetes are responsible for applying and operating the declared version in the environment.

## Future evolution

The initial repository focuses on learning. Later sections can add separate application and GitOps repositories, environment overlays, promotion workflows, secrets management, progressive delivery, observability and policy checks.
