# spike_argocd

Testing out Argo CD

Based off of [argocd-app-config](https://gitlab.com/nanuchi/argocd-app-config)

See also: [ArgoCD Tutorial for Beginners | GitOps CD for Kubernetes](https://www.youtube.com/watch?v=MeU5_k9ssrs)

## Testing it out

* install minikube TODO reference
* Install Argo CD [](https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd)
* access ArgoCD UI
  * kubectl get svc -n argocd
  * kubectl port-forward svc/argocd-server 8080:443 -n argocd
* login with admin user and below token (as in documentation):
  * kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 --decode && echo
* kubectl apply -f application.yaml

