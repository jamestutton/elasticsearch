# ElasticSearch cluster deployment on kubernetes

This project is based on a rework of https://github.com/cesargomezvela/elasticsearch which is based on the work of **Paulo Pires**,https://github.com/pires/kubernetes-elasticsearch-cluster

### Deploy


###### kubernetes

```SHELL
cd kubernetes
kubectl create -f 001_elasticsearch-discovery-svc.yaml
kubectl create -f 002_elasticsearch-svc.yaml
kubectl create -f 003_elasticsearch-master.yaml
kubectl rollout status -f 003_elasticsearch-master.yaml
kubectl create -f 004_elasticsearch-ingest-svc.yaml
kubectl rollout status -f 005_elasticsearch-ingest.yaml
kubectl create -f 100_elasticsearch-nodeport.yaml
kubectl create -f 900_es-data-non-persistant.yaml
kubectl rollout status -f 900_es-data-non-persistant.yaml
```
