## Criar a imgem docker
Entar diretório src e executar o comando abaixo
```sh
docker build -t ymritchie/conversao-temperatura-curso:v1 .
```

## Criar container a partir da imgem
```sh
docker run -d -p 8080:8080 ymritchie/conversao-temperatura-curso:v1
````