## Criar a imagem docker enviar a imagem para o docker hub
Entar no diretório src e executar o comando abaixo
```sh
docker build -t ymritchie/conversao-temperatura-curso:v1 .
docker tag ymritchie/conversao-temperatura-curso:v1 ymritchie/conversao-temperatura-curso:latest
docker login
docker push ymritchie/conversao-temperatura-curso:v1
docker push ymritchie/conversao-temperatura-curso:latest
```

## Criar container a partir da imagem
```sh
docker run -d -p 8080:8080 ymritchie/conversao-temperatura-curso:v1
```

## Iniciar o k3d e executar o Deployment
```sh
k3d cluster create meucluster -p "8080:30000@loadbalancer"
cd k8s
kubectl apply -f deployment.yaml
```