







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

> 💡 Note on Logging Stack Choice
>
> While ELK is a classic and powerful logging solution, in ~90% of real production work I would choose a more modern, lightweight stack:
>
> - OpenTelemetry
> - Prometheus
> - Grafana
> - Loki (instead of Elasticsearch)
>
> This combination integrates better with observability setups, has lower operational burden, and is usually already deployed for metrics.
>
> ELK is used here primarily to demonstrate experience with both ecosystems.

## 🧩 Features

- Centralized structured logging for all microservices
- Automatic log shipping via Filebeat
- Parsing and enrichment pipelines via Logstash
- Kibana dashboards for log exploration and analytics
- Docker-based, fully runnable locally

⚙️ Usage

1) Clone the repository

2) Inside the backend directory, create a .env file using env_example.txt

3) You can simply copy it — nothing project-specific inside

4) Run the stack: ```docker-compose up --build```

After startup, open Kibana:

👉 **http://localhost:5601**

Depending on your hardware, Elasticsearch may take a moment to initialize.

## 🔗 Back to the Main Index Repository

To explore the full distributed chat system:

https://github.com/aleksandrshaulskyi/chat-index
