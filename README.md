# Dockerfiles

## Usage

### OpenKM

```
docker run --name openkm -p 8080:8080 --detach openkm
```

### ElasticSearch + PDF support + ElasticHQ UI

```
docker build -t elasticsearch-pdf-hq .
```

Elastic HQ: <http://localhost:9200/_plugin/hq/>

```
docker run --name elasticsearch -p 9200:9200 --detach elasticsearch-pdf-hq
```

### Kali Linux

```
docker run -v /data:/root -w /root -i -t --net=host lisogallo/kali-linux bash
```
