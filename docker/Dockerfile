FROM python:3.9

COPY docker/requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt

# alias
RUN echo 'alias ll="ls -l --color"' >> ~/.bashrc
RUN echo 'alias py="python3"' >> ~/.bashrc
RUN echo 'alias kr="python3 /app/bot/bot/bot.py"' >> ~/.bashrc

# Copie tout pour le mettre dans /app/
COPY . /app/
ENTRYPOINT python3 /app/bot/bot/bot.py