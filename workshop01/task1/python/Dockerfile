FROM python:3.12.7-slim-bullseye

LABEL name=python-bear-app

ARG APP_DIR=/app

WORKDIR ${APP_DIR}

COPY main.py utils.py run.sh requirements.txt ./
ADD public public 
ADD templates templates
COPY .gitignore ./

RUN pip install -r requirements.txt

ENTRYPOINT ["sh", "run.sh"]