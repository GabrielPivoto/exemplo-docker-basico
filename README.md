# Um exemplo básico de Docker - Alura 🐋 

## Como buildar:

```
docker build -t aplicacao/app-node:1.0 .
```
* -t para etiquetar a imagem
* :1.0 para explicitar a versão
* . para ser executado no contexto do diretório atual.

## Explicando o Dockerfile:

* Usa uma imagem base para construir. Pega a versão 14:
````
FROM node:14 
````
* Define o diretório de trabalho padrão do container:
````
WORKDIR /app-node
````

* Copia todo o conteúdo do diretório atual para o diretório do container:
```
COPY . .
```

* Comando que é executado enquanto a imagem está sendo criada:
```
RUN npm install
```

* Comando a ser executado quando o container for iniciado:
```
ENTRYPOINT npm start
```