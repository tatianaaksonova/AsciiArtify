# POC

The pilot version of AsciiArtify is currently in development, and the team has agreed to use a GitOps approach to manage the infrastructure. For deploying the GitOps system, the team has chosen Argo CD.
Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes.

### Demo Environment
* minikube
    * `minikube start`
* `kubectl create namespace argocd`

### Deploy Argo CD

* `kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml`

Get IP of Argo CD service
* `kubectl -n argocd get svc/argocd-server`

Get password for login to ArgoCD
* `kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d`

Open ArgoCD in browser and login. Username `admin` and password from previous step.
