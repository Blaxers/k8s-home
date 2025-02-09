1. To deploy app use argocd
kubectl port-forward svc/argocd-server -n argocd 8080:80
2. Credentials for argocd
kubectl -n argocd get secret argocd-initial-admin-secret \cret \
-o jsonpath="{.data.password}" | base64 -d; echo