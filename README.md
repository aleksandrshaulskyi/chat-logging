# Chat-logging.

The logging microservice for the distributed chat system.

## Brief.

The logging microservice built on top of probably the most
classic logging solution - ELK. And Filebeat service for log
transportation.

Comes with pre-built dashboards that are ready to be imported to Kibana
and contain both list representation of logs and visualizations. They can be found at
**/kibana_dashboards/** directory and contain everything that is needed to properly display
logs created by the application.

Might be worth noticing that in probably 90% of times I would utilize stack used
for metrics in this project - Open Telemetry | Prometheus | Grafana with Loki.
It is more light weight, more modern and easier-to-implement solution. And you would probably use
it for metrics anyway so.

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
