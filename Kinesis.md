# Kinesis

Amazon Kinesis Data Firehose can capture, transform and load streaming data into:

* S3
* Redshift
* Elaticsearch Service
* Splunk

#### Kinesis Data Streams

Kinesis Data Steams is a massively scalable, highly durable data ingestion and processing service optimized for streaming data. You can configure hudreds of thousands of data producers to continously put data into a Kinesis Data Stream.

**Key concepts:**
* **Data Producer** - an application that emits data records as they are generated to a Kinesis Data Stream.
* **Data Consumer** - a distributed Kinesis application or AWS service retrieving data from all shards in a stream as generated.
* **Data Stream** - A logical grouping of shards
* **Shard** - The base throughput unit of a Kinesis Data Stream. A shard is an append-only log. A shard contains a ordered sequence of records ordered by arrival time. One shard can ingest up to 1,000 data records per second, or 1MB/sec.
A new shard iterator is returned by every **GetRecords** request (as `NextShardIterator`), which you then use in the next **GetRecords** request (as `ShardIterator`).Typically, this shard iterator does not expire before you use it. However, you may find that shard iterators expire because you have not called **GetRecords** for more than 5 minutes, or because you've performed a restart of your consumer application.

If the shard iterator expires immediately before you can use it, this might indicate that the DynamoDB table used by Kinesis does not hae enough capacity to store the lease data. This situation is more likely to happen if you have a large number of shards. To solve this problem, increate the write capacity assigned to the shard table.
