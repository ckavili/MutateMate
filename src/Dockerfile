FROM ubi8/python-39


WORKDIR /app

COPY . /app


RUN pip3 install -r requirements.txt


EXPOSE 8080


ENTRYPOINT gunicorn -w 4 app:app -b 0.0.0.0:8080 --certfile=/tmp/k8s-webhook-server/serving-certs/tls.crt --keyfile=/tmp/k8s-webhook-server/serving-certs/tls.key