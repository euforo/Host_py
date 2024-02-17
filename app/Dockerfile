# Use uma imagem base
FROM python:3.9-slim

# Instale o supervisor para gerenciar os processos
RUN apt-get update && apt-get install -y supervisor

# Crie um novo usuário
RUN useradd -ms /bin/bash myuser

# Crie a estrutura de diretórios para a aplicação e os logs
RUN mkdir -p /app /logs && \
    chown -R myuser:myuser /app /logs

# Defina o diretório de trabalho para a aplicação
WORKDIR /app

# Copie o arquivo de aplicação para dentro do contêiner
COPY . /app


# Configure o ambiente virtual Python (venv)
RUN python -m venv /venv 


# Crie a pasta env manualmente
RUN mkdir -p /app/env

# Copie o conteúdo do ambiente virtual Python para a pasta env
RUN cp -r /venv/* /app/env && \
    chown -R myuser:myuser /app/env

# Configure o supervisor para iniciar o nginx e o aplicativo Python
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

# Configure o supervisor para iniciar o nginx e o aplicativo Python
CMD ["supervisord", "-c", "/etc/supervisor/conf.d/supervisord.conf"]

