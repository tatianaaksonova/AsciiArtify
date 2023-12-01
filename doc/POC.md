# POC

The pilot version of AsciiArtify is currently in development, and the team has agreed to use a GitOps approach to manage the infrastructure. For deploying the GitOps system, the team has chosen ArgoCD.
Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes.

### Demo Environment
* minikube
    * `minikube start`
* `kubectl create namespace argocd`
