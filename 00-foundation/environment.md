# Lab Environment

## Required tools

- Git
- Docker
- kubectl
- Minikube
- Helm
- Kubernetes cluster
- Argo CD
- GitHub account and GitHub Actions

Argo CD and the Kubernetes cluster are intentionally deferred until the relevant course days. Day 1 only establishes the repository and documents the target environment.

## Verification checklist

Run the commands that apply to the tools already installed:

```bash
git --version
docker --version
kubectl version --client
minikube version
helm version
```

For a running cluster, later verify:

```bash
kubectl cluster-info
kubectl get nodes
```

## Safety notes

- Never commit tokens, kubeconfig files, private keys or real credentials.
- Use `.env.example` for documented variable names and keep real `.env` files local.
- Use disposable local clusters while learning.
- Record commands and outcomes in the progress tracker.
