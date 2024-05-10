
## Instructions for Running Project ##

1. run `docker-compose up --build` to start docker containers

2. cd to root directory hadoop to run commands
- you can run `make-target` commands (`make event-counter` and `make location-mapreducer` to aggregate jobs by location and events 
- hadoop should not be launched locally but through docker compose file and makefile commands

3. run `make hadoop_solved` should produce solution


# Project Layout Documentation


## Kafka Server
1. Kafka.py: Consumer script that consumes messages from Kafka and exports to PostgreSQL
2. test_kafka.py: pytest script that tests our functions for consumption & Postgres instantiation/connection.
3. kafka_sqlite.py: Consumer script that consumes messages from Kafka and exports to SQLITE
4. health_data.db: SQLite DB with persisted health event data

# NOTE: We were successfully able to persist data in both PostgreSQL and Sqlite, but we had trouble connecting it to our Spark Dataframe in our notebook.

## Spark Explore

1. EDA.ipynb: Contains EDA visualizations
2. Webpage visualizations (Directory) Contains an HTML web page that hosts our graphs. You must go live to see these graphs. If not, you can simply see the graphs themselves in the directory. **Visualizations** **included**: **Past Outbreaks** (Geographical World Map, Anomaly Histogram), **Next predicted outbreak**, **Event Streaming Visualization**, ** LSTM Model Performance**

## Kubernetes

1. To use Kubernetes and Google Console to deploy the containers, first navigate to `kafka-server` and execute the command `kubectl apply -f .`
2. Run `kubectl get services` to show services that are running. 

   

