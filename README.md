# estudo-kubernetes
Repositório criado para armazenar códigos criados durante o aprendizado do K8S.

## Comandos utilizados

### Docker

Após a criação do Dockerfile com as alterações necessárias na imagem

Constuir uma nova imagem com o nome e tag:
```
docker build -t luisthiagop/noticia-alura:v# .
```
Upload para o DockerHub:
```
docker push luisthiagop/noticia-alura:v# 
```
Executar a imagem para testar, definindo a utilização do bash:
```
docker run -it luisthiagop/noticia-alura:v# bash 
```

### kubectl

Dentro da pasta kubernetes

Listagem:
```
kubectl get pods
kubectl get deployments
kubectl get services
```

Dentro da pasta kubernetes

Criar o deployment apartir de um arquivo:
```
kubectl create -f deployment-aplicacao.yml
```

Deletar o deployment apartir de um arquivo:
```
kubectl delete -f deployment-aplicacao.yml
```

Criar o service apartir de um arquivo:
```
kubectl create -f servico-aplicacao-noticia.yml
```

Deletar o service apartir de um arquivo:
```
kubectl delete -f servico-aplicacao-noticia.yml
```

Também é possível deletar apartir do nome encontrado nas listagens.

### Minikube

Abrir o dashboard:
```
minikube dashboard
```

Obter url para acesso ao serviço:
```
minikube service servico-aplicacao-noticia.yml --url
```


