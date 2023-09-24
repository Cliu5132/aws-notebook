# Athena

不仅能在S3中进行查询。还可以借助Data Source Connector（是一个Lambda Function），在几乎所有AWS数据库（甚至本地数据库）中进行查询。

- Serverless query service to analyze data stored in Amazon S3
- Uses standard SQL language to query the files (built on Presto)
- Supports CSV, JSON, ORC, Avro, and Parquet
- Pricing: $5.00 per TB of data scanned
- Commonly used with Amazon Quicksight for reporting/dashboards

## 提升性能
- 按列检索
- 压缩
- 分区
- 提升文件体积