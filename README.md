# Big Data Streaming Ingest Pipeline with Google Cloud Pub/Sub and DataFlow with Apache Beam

| | |
|-|-|
|__Title__| Big Data Streaming Ingest Pipeline with Google Cloud Pub/Sub and DataFlow with Apache Beam
|__Presenter__ | __George Oboh__ <br>Cloud Data Engineer<br>
|__Website__ | <a href="https://goboh.io">https://goboh.io</a>


This project creates a big data pipeline streaming ingest pipeline to move streaming data from a source system to Google BigQuery. In this project, we simulate a streaming source by publishing messages from Python code to a Google Pub/Sub message queue. The project steps are as follows:

1. Create a Compute VM (see `Notebook-instance.ipynb`). This VM will execute code that published data to a Pub/Sub message queue (see `Data-to-pubsub.ipynb`). This data will be CSV lines. We may stop the iterator after 5 billion. 
2. Create a Pub/Sub instance to connect publishers to subscribers (see `Data-Ingest-Build.ipynb`).
3. Create a DataFlow job to read (or subscribe) from a Pub/Sub message and write to a BigQuery table (see `Dataflow-build.ipynb`). It should update or append to the table on each write.
4. Verify that the BigQuery data is correct.

The project workflow is illustrated below.

<img src="s3_gcp_nifi.png" alt="streaming-pubsub-dataflow-bigquery">