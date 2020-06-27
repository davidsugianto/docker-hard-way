FROM python:3.6.1-alpine AS builder

LABEL maintainer David Sugianto <idiots718@gmail.com>

WORKDIR /app/flask

COPY templates/ ./templates/
COPY app.py requirements.txt ./

RUN pip install --upgrade pip
RUN pip install -r requirements.txt

CMD [ "python", "app.py" ]
