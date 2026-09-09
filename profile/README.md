# SINTRATEL · Docket

Task management platform for a legal firm, built and operated with a complete
continuous engineering cycle: infrastructure as code, GitOps delivery, testing,
observability and change management.

## Where to start

| Repository | What it holds |
|---|---|
| [docket-architecture](https://github.com/sintratel-docket-platform/docket-architecture) | The architecture, the decision records, and the engineering standards |
| [docket-terraform-modules](https://github.com/sintratel-docket-platform/docket-terraform-modules) | Reusable Terraform modules, versioned by tag |
| [docket-gitops](https://github.com/sintratel-docket-platform/docket-gitops) | Kubernetes manifests and Argo CD configuration |

The application is five services and a queue: a Vue.js frontend, authentication
in Go, user profiles in Java, task management in Node.js, and a Python worker
consuming Redis.

## How the platform is built

Terraform provisions AWS and an EKS cluster split across stacks by lifecycle, so
the expensive parts are destroyed and recreated routinely. GitHub Actions builds
and publishes images to ECR with no long-lived credentials, using OIDC. Argo CD
reconciles the cluster against the manifest repository, and promotion between
development, staging and production is a version reference changed through a
pull request.

The reasoning behind each of those choices is recorded as a numbered ADR in
[decisions.md](https://github.com/sintratel-docket-platform/docket-architecture/blob/main/decisions.md).
