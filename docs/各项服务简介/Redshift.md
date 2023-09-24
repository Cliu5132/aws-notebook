# Redshift

- Redshift is based on PostgreSQL, but it's not used for OLTP
- It's OLAP - online analytical processing (analytics and data warehousing)
- 10x better performance than other data warehouses, scale to PBs of data
- Columnar storage of data (instead of row based) & parallel query enginee
- Pay as you go based on the instances provisioned
- Has a SQL interface for performing the queries
- BI tools such as Amazon Quicksight or Tableau integrate with it
- Compared to Athena: faster queries / joins / aggregations thanks to indexes

## Redshift Cluster

![](https://hugo-mrcongliu.s3.ca-central-1.amazonaws.com/17188aa7-aec0-6beb-7b80-64434a2d2890.png)

- Leader node: for query planning, results aggregation
- Compute node: for performing the queries, send results to leader
- You provision the node size in advance
- You can use Reserved Instances for cost saving

### Snapshots & DR

- Redshift has "Multi-AZ" mode for some clusters
- Snapshots are point-in-time backups of a cluster, stored internally in S3
- Snapshots are incremental (only what has changed is saved)
- You can restore a snapshot into a new cluster
- Automated: every 8 hours, every 5 GB, or on a schedule. Set retention between 1 to 35 days
- Manual: snapshot is retained until you delete it
- You can configure Amazon Redshift to automatically copy snapshots (automated or manual) of a cluster to another AWS Region

![](https://hugo-mrcongliu.s3.ca-central-1.amazonaws.com/00363667-ea04-7e86-7291-5a0a96dd9125.png)

### Loading data into Redshift: Large inserts are MUCH better

![](https://hugo-mrcongliu.s3.ca-central-1.amazonaws.com/33a4c4c1-003f-b83d-3d2d-fafdad32e724.png)

## Redshift Spectrum

- Query data that is already in S3 without loading it
- Must have a Redshift cluster available to start the query
- The query is then submitted to thousands of Redshift Spectrum nodes

![](https://hugo-mrcongliu.s3.ca-central-1.amazonaws.com/f0e86205-a80c-6fd2-8769-c07ff4413efb.png)

