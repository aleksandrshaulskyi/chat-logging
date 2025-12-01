# Chat-logging.

**Centralized structured logs for the distributed chat platform**

This microservice provides a full ELK-based logging pipeline for the entire chat system, including log shipping, storage, search, visualization, and pre-built dashboards for Kibana.

## 🚀 Overview

The logging service is built on top of the classic and battle-tested ELK stack:

- **Filebeat** → log shipping from microservices

- **Logstash** → parsing, enrichment, routing

- **Elasticsearch** → log indexing and storage

- **Kibana** → dashboards, visualizations, and search

The system comes with ready-to-import Kibana dashboards that visualize application logs in a clean, analytical manner — including both list-oriented views and aggregated charts.

Dashboards are located in:

```/kibana_dashboards/```

They include everything required to display logs produced by the chat services out of the box.

## Stage.
This service is in the stage of active development. Updates are released multiple times a week.

## Features.
Provides logging for the services of the system.

## Usage.

1) Clone the repository.
2) Create .env file in the backed directory using the env_example.txt as an example.  
In fact you can simply copy it as it does not contain anything project-specific at all.
3) ```docker-compose up --build``` in the directory where docker-compose.yaml file is located.
4) Kibana will be available at the address **http://localhost:5601**

## Recent updates.

None yet released.

## Back to Index repository of the whole chat system.

https://github.com/aleksandrshaulskyi/chat-index
