# GitOps Learning Journey

A hands-on learning journey to understand and implement GitOps using Kubernetes, Argo CD, Helm, Kustomize and GitHub Actions.

The goal of this repository is to learn GitOps by building, deploying, troubleshooting and improving a real working environment step by step.

---

## 🎯 Learning Goals

* Understand GitOps principles
* Understand declarative infrastructure and applications
* Learn Kubernetes fundamentals required for GitOps
* Learn Argo CD
* Build GitOps-based deployments
* Learn Kustomize
* Learn Helm
* Implement CI + GitOps
* Manage multiple environments
* Understand GitOps security
* Implement deployment strategies
* Troubleshoot GitOps environments
* Build a production-style GitOps architecture

---

## 🏗️ Target Architecture

```text
Developer
    |
    v
Application Repository
    |
    v
GitHub Actions
    |
    +---- Test
    +---- Security Scan
    +---- Docker Build
    +---- Push Image
    |
    v
Container Registry
    |
    v
GitOps Repository
    |
    v
Argo CD
    |
    v
Kubernetes
    |
    v
Application
```

---

## 📚 Course Structure

| Section              | Topic                           |
| -------------------- | ------------------------------- |
| `00-foundation`      | GitOps concepts and environment |
| `01-kubernetes`      | Kubernetes fundamentals         |
| `02-argocd`          | Argo CD                         |
| `03-gitops`          | GitOps implementation           |
| `04-kustomize`       | Kustomize                       |
| `05-helm`            | Helm                            |
| `06-secrets`         | Secrets management              |
| `07-ci-cd`           | CI/CD integration               |
| `08-environments`    | Dev/UAT/Prod                    |
| `09-advanced-argocd` | Advanced Argo CD                |
| `10-production`      | Production GitOps               |

---

## 🧪 Lab Environment

The initial lab will use:

* Ubuntu/Linux
* Git
* Docker
* Kubernetes
* Minikube
* kubectl
* Helm
* Argo CD
* GitHub Actions

---

## 📈 Learning Approach

This repository follows a hands-on approach.

For each topic:

```text
Learn
  ↓
Build
  ↓
Deploy
  ↓
Break
  ↓
Troubleshoot
  ↓
Fix
  ↓
Document
```

The objective is to understand not only **how** GitOps works, but also **why** each component is used.

---

## 🗓️ Progress

* [x] Repository created
* [ ] Day 1 — GitOps foundation
* [ ] Day 2 — Kubernetes fundamentals
* [ ] Day 3 — Kubernetes application deployment
* [ ] Day 4 — Argo CD setup
* [ ] Day 5 — First GitOps application
* [ ] Day 6 — Sync and reconciliation
* [ ] Day 7 — Drift and self-healing
* [ ] Day 8 — Pruning
* [ ] Day 9 — Rollback
* [ ] Day 10 — GitOps repository structure

More topics will be added as the course progresses.

---

## 🚀 Long-Term Goal

Build a complete GitOps platform demonstrating:

```text
Git
 +
GitHub Actions
 +
Docker
 +
Container Registry
 +
Kubernetes
 +
Argo CD
 +
Kustomize
 +
Helm
 +
Security
 +
Monitoring
```

and understand how these components work together in a production-oriented DevOps environment.
