# Login once

argocd login localhost:9090 --insecure
 
# Then create the app without needing --server flag

argocd app create simple-new-app \

  --repo https://github.com/neerajk555/argocd-demo.git \

  --path my-argocd-app \

  --dest-server https://kubernetes.default.svc \

  --dest-namespace default
 
argocd app create simple-new-app \

  --repo https://github.com/neerajk555/argocd-demo.git \

  --path my-argocd-app \

  --dest-server https://kubernetes.default.svc \

  --dest-namespace default \

  --server localhost:9090 \

  --server-crt /path/to/argocd-server.crt
 
