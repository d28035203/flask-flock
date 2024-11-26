# Flask Flock

Flask + MongoDB API with Docker and Kubernetes manifests (Deployment, Service, StatefulSet, HPA).

## Features

- `GET /` welcome
- `GET|POST /data` JSON documents in MongoDB
- Docker image + K8s Flask + Mongo + HPA

## Tech

Python · Flask · PyMongo · Docker · Kubernetes

## Run (local idea)

```bash
git clone https://github.com/d28035203/flask-flock.git
cd flask-flock
# with env MONGO_INITDB_ROOT_USERNAME / PASSWORD and a Mongo service named mongodb
pip install -r requirements.txt
python app.py
```

## Kubernetes

```bash
kubectl apply -f mongodb-statefulset.yaml -f mongodb-service.yaml
kubectl apply -f flask-deployment.yaml -f flask-service.yaml -f flask-hpa.yaml
```

## License

MIT
