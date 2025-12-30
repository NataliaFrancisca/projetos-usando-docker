# 🖥️ Servidor Web com Nginx


### 📁 Arquivo Dockerfile:

Nesse arquivo vamos adicionar as configurações necessárias para criar a imagem do nosso servidor web.

```docker
# imagem oficial do nginx
FROM nginx:latest

# copiamos o arquivo index.html para o diretório padrão do Nginx
COPY index.html /usr/share/nginx/html/index.html

# expõe a porta 80
EXPOSE 80
```

### 📷 Criando imagem:
_para criar a imagem devemos estar na mesma pasta do arquivo Dockerfile_

Para criar a imagem, usamos o comando:

```bash
  docker build -t meu-nginx .
```

### 🚢 Subindo container:
_não precisa estar na mesma pasta do Dockerfile_

E para subir o container, vamos usar o comando:

```bash
  docker run -d -p 8080:80 --name nginx-simples meu-nginx
```

### Acessando a página web
Vamos acessar a página web usando o endereço: http://localhost:8080/
