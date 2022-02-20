# kubernets

Learning kubernetes

- [x] Clusters
- [x] Nodes
- [x] Pods
- [x] Services
- [x] Deployment
- [x] Forward
- [ ] Autoscale HPA
- [ ] Ingress 
- [ ] Jobs 
- [ ] CronJob 

```bash
## KIND
kind create cluster --name=livek8s # 1 node
kind create cluster --config=cluster/multinodes.yaml # 3 nodes

## KUBE
kubectl config get-contexts # lista os contextos
kubectl config use-context {CONTTEXT_NAME} # Seta o contexto

## Comandos basicos
kubectl get nodes  # lista nodes
kubectl get pods   # lista pods
kubectl get services # lista service

## Comandos de Deploy
kubectl apply -f services/service-go/k8s/deployment.yaml # deploy
kubectl apply -f services/service-go/k8s/service.yaml # cria serviço
kubectl rollout undo deployment goserver # rollout

kubectl port-forward service/goserver-service 3000:3000 # publica/compartilha porta para acesso local

```

Subindo os serviços exemplo:

```bash
kubectl apply -f services/nginx/k8s 
kubectl apply -f services/go/k8s
```


### Links

Gerenciador cluster kubernets
https://k8slens.dev/

Facilitador para o uso do kubernets local:
https://kind.sigs.k8s.io/