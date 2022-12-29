helm repo add gitlab https://charts.gitlab.io/

helm repo update
helm upgrade --install gitlab gitlab/gitlab \
  --timeout 600s \
  --set global.hosts.domain=sxxpqp.top \
  --set global.hosts.externalIP=172.16.0.201 \
  --set certmanager-issuer.email=me@example.com \
  --set postgresql.image.tag=13.6.0


  kubectl get secret gitlab-gitlab-initial-root-password -ojsonpath='{.data.password}' | base64 --decode ; echo"# gitlab--k8s-deloy" 
# gitlab--k8s-deloy
