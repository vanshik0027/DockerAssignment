# DockerAssignment

## Elasticsearch-Filebeat-Kibana stack to monitor Nginx logs

## Contents

* **Nginx:** containing build image nginx web server

* **Elasticsearch:** containing build image and configuration for Elasticsearch
  
* **Filebeat:** containing build image and configuration for Filebeat to stream nginx logs Elasticsearch

* **Kibana:** containing build image and configure for Kibana to visualize data from an Elasticsearch index

## How it works

- Nginx access and error logs are written to a directory. The directory is mapped to a local volume.
  
- Filebeat reads the nginx logs from the local volume and sends it to an Elasticsearch index [filebeat-*].
  
- Kibana uses the index to visualize the access and the error logs.

## Pre-requisites

```bash
- docker
- docker-compose
```

## To run this stack

```bash
docker-compose up -d
```
## Access Components

Once the stack is up and running, you can access the following components:

**Nginx:** Visit http://localhost in your web browser.

**Kibana:** Visit http://localhost:5601 in your web browser.

## Log in to Kibana

To log in to Kibana and visualize the Nginx logs, use the following credentials:

**Username:** elastic
**Password:** changeme%
