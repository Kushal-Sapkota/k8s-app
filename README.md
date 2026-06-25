# k8s-app

Hands-on Kubernetes practice deploying a Node.js app on a local cluster using Minikube.

---

## Stack

- Kubernetes + Minikube
- kubectl
- Docker Hub image: `kushal81/cicd-app:v9`

---

## What's inside

- `pod.yaml` — single container pod
- `multi-pod.yaml` — app + sidecar logging container
- `replicaset.yaml` — maintains 3 pod replicas, self healing
- `deployment.yaml` — rolling update strategy, ropllback support
- `service.yaml` — NodePort Service, load balances across deployment pods, exposed on the port 30001
---

## Run it

```bash
minikube start --driver=docker
kubectl apply -f pod.yaml
kubectl port-forward pod/cicd-app 3000:3000
```

Open → `http://localhost:3000`

---

## Author

**Kushal Sapkota** · [GitHub](https://github.com/Kushal-Sapkota) · [Portfolio](https://kushalsapkota81.com.np)
