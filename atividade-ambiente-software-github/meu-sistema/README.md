# Atividade — Ambiente de Software

## Questão 1

O arquivo [`Dockerfile`](Dockerfile) contém as respostas dos itens:

- **a)** `FROM python:3.11-slim` 
- **b)** `WORKDIR /app` 
- **c)** `COPY requirements.txt .` e `RUN pip install --no-cache-dir -r requirements.txt` 
- **d)** `COPY . .` 
- **e)** `EXPOSE 5000` 
- **f)** `CMD ["python", "app.py"]` 

## Questão 2 

**a:**
```bash
docker build -t meu-sistema:1.0 .
```

**b:**
```bash
docker run -d --name sistema-web -p 8080:5000 meu-sistema:1.0
```

**c:**
```bash
docker ps
```

**d:**
```bash
docker logs sistema-web
```

**e:**
```bash
docker stop sistema-web
```

**f:**
```bash
docker rm sistema-web
```

## Questão 3

**a:**

A imagem é como a receita de um bolo, ela contém os ingredientes e as instruções de preparo.

Já o container é como o bolo sendo preparado a partir dessa receita, usando a imagem como base para sua criação.

**b:**

Isso aconteceu porque a imagem foi construída antes das alterações no arquivo `app.py`. Modificar o código local não atualiza automaticamente uma imagem Docker já construída. É necessário reconstruir a imagem e recriar o container:

