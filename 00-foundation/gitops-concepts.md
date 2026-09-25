# GitOps Concepts

## What is GitOps?

GitOps is an operating model in which Git stores the declarative desired state of an application or infrastructure. An automated controller continuously compares that desired state with the actual state of the target environment and takes action to reconcile differences.

Git is therefore more than a source-code repository: it provides versioning, review, audit history and a repeatable change process for operations.

## Core ideas

### Desired state

The desired state describes what should exist: for example, the application image, replica count, service and configuration that Kubernetes should run. It is usually expressed as Kubernetes YAML, Helm values or Kustomize overlays.

### Actual state

The actual state is what is currently running in the cluster. It can differ from Git because of a new deployment, an outage, a manual change or an incomplete reconciliation.

### Declarative configuration

Declarative configuration describes the end result rather than a sequence of imperative commands. Kubernetes and GitOps controllers determine how to move from the current state to the requested state.

### Reconciliation

A controller repeatedly observes both states and works to make actual state match desired state. This loop is what makes GitOps continuous rather than a one-time deployment.

### Drift and self-healing

Drift occurs when the cluster differs from Git. A GitOps controller can report the drift and, when configured to do so, restore the declared state automatically. This is self-healing.

## Pull versus push

In a push-based model, a CI system or deployment script needs credentials and actively sends changes to the cluster. In a pull-based model, an in-cluster controller such as Argo CD reads the Git repository and applies the desired state. Pull-based deployment reduces the exposure of cluster credentials in external systems and gives the cluster responsibility for convergence.

CI remains useful for testing, scanning and publishing an image. GitOps generally separates that work from deployment: CI updates the image reference in the GitOps repository, and Argo CD reconciles the cluster.

## Why Argo CD exists

Kubernetes provides reconciliation for individual resources, but it does not natively provide a complete Git repository workflow, application health view, Git revision history and multi-application synchronization experience. Argo CD fills that role by continuously monitoring Git and Kubernetes, reporting sync and health status, and applying the declared manifests.

## Questions to revisit

- What is the source of truth for this project?
- Which system owns each change?
- How would a manual cluster change be detected?
- What should happen when a deployment fails halfway through?
