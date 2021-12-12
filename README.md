# FIAPFASE4_Kubernetes

## Pre-reqs:
1. Docker: https://docs.docker.com/desktop/windows/install/
2. Minikube: https://minikube.sigs.k8s.io/docs/start/
3. Kompose: https://github.com/kubernetes/kompose/releases/download/v1.26.0/kompose-windows-amd64.exe - copie local e adicione ao path
4. Kubectl: https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/

## Para iniciar o minikube:
1. Minikube start

## Para aplicar os arquivos no Kubernetes cluster:
via terminal digitar: kubectl apply -f rabbitmqeightshop-claim0-persistentvolumeclaim.yaml,rabbitmqeightshop-deployment.yaml,rabbitmqeightshop-service.yaml,notificationservice-pod.yaml,notificationservice-service.yaml,purchaseservice-pod.yaml,purchaseservice-service.yaml

## Para subir os servicos individuais, exemplo:
1. Abra um novo terminal e digite: minikube service rabbitmqeightshop
2. Abra um novo terminal e digite: minikube service purchaseservice
3. Abra um novo terminal e digite: minikube service notificationservice

## Para acessar detalhes do servico:
1. Abra um novo terminal e digite: kubectl describe svc purchaseservice

## Para acessar a dashboard do minikube:
1. Abra um novo terminal e digite: minikube dashboard

## Opcional - Caso queira gerar novos arquivos a serem aplicados no Kubernetes a partir de um docker compose apos mudancas no mesmo: 
1. Acesse o diretorio do docker compose.yaml:
2. via terminal digite: kompose 