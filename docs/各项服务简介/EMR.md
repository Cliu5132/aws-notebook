# EMR

- Amazon EMR = Elastic MapReduce
- can create Hadoop Clusters to analyze & process Big Data
- one cluster can contain hundreds of EC2 instances
- bundled with Apache Spark, HBase, Presto, Flink ...
- no need to worry about provisioning and configuartion, EMR takes care of that
- Auto-scaling and integrated with Spot instances

### Use case: data processing, machine learning, web indexing, big data

## Node Types & Purchasing

- Master Node: Manage the cluster, coordinate, manage health - long running
- Core Node: Run tasks and store data - long running
- Task Node: Optional, just to run tasks, usually Spot
- Purchasing options:
    - On-demand: reliable, predictable, won't be terminated
    - Reserved (min 1 year): cost savings (default use for EMR)
    - Spot Instances: cheaper, can be determinated, less reliable
- you can choose long-running cluster, or transient (temporary) cluster