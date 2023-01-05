# Kubernetes Dojo

1. Documentação de apoio
    - https://kubernetes.io/docs/home/

2. Curso Introduction to Kubernetes
    - https://kubernetes.io/training/

## Instalação Local Básica

1. Instalar Kubernetes
    - Docker Desktop -> Kubernetes e ativar (Enable Kubernetes)

1. Instalar Kubectl
    - https://kubernetes.io/docs/tasks/tools/

## Instalação Local Avançada
1. Instalar Krew
    - https://krew.sigs.k8s.io/docs/user-guide/setup/install

1. Instalar Kubectx e Kubens
    - kubectl krew install ctx
    - kubectl krew install ns

## Comandos Úteis

1. Aplica um yaml
```
kubectl apply -f {arquivo.yml}
```

2. Remover os recursos de um yaml
```
kubectl delete -f {arquivo.yml}
```

3. Listar recursos
```
kubectl get pods
kubectl get namespaces
kubectl get services
kubectl get cronjobs
```

4. Visualizar um recurso
```
kubectl describe pod {name}
kubectl describe namespace {name}
kubectl describe service {name}
kubectl describe namespace {name}
```

5. Ver os logs de um pod
```
kubectl logs {podname}[-c {containername}]
```

6. Ver o uso de recursos dos pods/containers (precisa ter o metrics server instalado)
```
kubectl top pods
kubectl top pods --containers
```

7. Port Forward
```
kubectl port-forward pods/{name} {LOCAL_PORT}:{CLUSTER_PORT}
kubectl port-forward deployment/{name} {LOCAL_PORT}:{CLUSTER_PORT}
kubectl port-forward service/{name} {LOCAL_PORT}:{CLUSTER_PORT}
```