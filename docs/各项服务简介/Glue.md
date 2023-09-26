# Glue

- Managed extract, transform, and load (ETL) service
- Useful to prepare and transform data for analytics
- Fully serverless

![](https://hugo-mrcongliu.s3.ca-central-1.amazonaws.com/7ff503c3-bf58-de23-f985-e4f9aba1ba48.png)

![](https://hugo-mrcongliu.s3.ca-central-1.amazonaws.com/bd4d0554-b123-d75d-f139-607a16adf368.png)

![](https://hugo-mrcongliu.s3.ca-central-1.amazonaws.com/195ead23-ff11-226c-e23e-8cfc90f843a3.png)

### Key Features

- Glue Job Bookmarks: prevent re-processing old data
- Glue Elastic Views:
    - Combine and replicate data across mulitple data stores using SQL
    - No custom code, Glue monitors for changes in the source data, serverless
    - Leverages a virtual table
    - Glue DataBrew: clean and normalize data using pre-built transformation
    - Glue Studio: new GUI to create, run, and monitor ETL jobs in Glue
    - Glue Streaming ETL: built on Apache Spark Structured Streaming, compatible with Kinesis Data Streaming, Kafka, Managed Kafka(MSK)