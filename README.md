## Criar a imagem docker
Entar no diretório src e executar o comando abaixo
```sh
docker build -t ymritchie/conversao-temperatura-curso:v1 .
```

## Criar container a partir da imagem
```sh
docker run -d -p 8080:8080 ymritchie/conversao-temperatura-curso:v1
````