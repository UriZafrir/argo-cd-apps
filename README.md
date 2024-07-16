kubectl port-forward service/argo-cd-argocd-server -n argocd 8080:443
http://localhost:8080
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d