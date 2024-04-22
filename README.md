# gitops-demo

Before demo:

kubectl create namespace argocd
helm install argocd argo/argo-cd --namespace argocd

kubectl port-forward -n argocd  svc/argocd-server 8080:443 &

kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d ; echo

https://argocd.localhost.lund.ai:8080/


Add Repo:
https://github.com/ErikLundJensen/gitops-demo.git

Create namespace App

Show created objects

Delete App

Create ApplicationSet
kubectl apply -f ~/demo/2024april/kind-demo/gitops/bootstrap/applicationset.yaml -n argocd