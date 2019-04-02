
Kafka
Apache™ Kafka is a fast, scalable, durable, and fault-tolerant publish-subscribe messaging system. Kafka is well known for its high throughput, reliability and replication. Kafka works well in combination with Apache Flink and Apache Spark for real-time analysis and rendering of streaming data.

In this setup Kafka is used to collect and buffer the events, that are then ingested by Druid. We need Kafka to persist the data and act as a buffer when there are bursts of events, that happen when there is, for example, an airing of a TV commercial.

Druid
Druid is an open-source analytics data store designed for business intelligence (OLAP) queries on event data. Druid provides low latency real-time data ingestion from Kafka, flexible data exploration, and fast data aggregation.

Druid will do the processing of the data and shape it in the form that we request. Existing Druid deployments have scaled to trillions of events and petabytes of data, so we won't have to worry about scale.

Superset
Apache™ Superset is a data exploration and visualization web application and provides an intuitive interface to explore and visualize datasets, and create interactive dashboards. Initially developed by Airbnb, but now in the running to become an Apache™ project.
# Setup
git clone solution
cd into folder
git submodule update --init --recursive

docker-compose rm -f && docker-compose build && docker-compose up
