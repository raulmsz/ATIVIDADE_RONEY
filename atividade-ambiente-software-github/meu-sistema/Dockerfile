# Questão 1 - Item a
FROM python:3.11-slim
# Questão 1 - Item b
WORKDIR /app
# Questão 1 - Item c
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
# Questão 1 - Item d
COPY . .
# Questão 1 - Item e
EXPOSE 5000
# Questão 1 - Item f
CMD ["python", "app.py"]
