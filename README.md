# Um exemplo básico de Docker 🐋 

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