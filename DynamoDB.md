# DyanmoDB

#### Performance

Amazon Dynamo DB Accelerator (DAX) is a fully managed, highly available, in-mrmory cahce that can reduce Amazon DynamoDB response times from millseconds to microseconds, even at millions of requests per second.

While you may use ElastiCache as your DB cahce, it will not reduce the DynamoDB resposne time from milliseconds to microseconds as compared with DynamoDB DAX.

#### DynamoDB Stream

DynamoDB Stream is an ordered flow of information about changes to items in an Amazon DynamoDB table. When you enable a stream on a table, DynamoDB captures information about every modification to data items in the table.

Whenever an application creates, updates or deletes itesm in the table, DynamoDB Streams writesa stream record with the primary key attribute(s) of the items that were modified. A stream record contains information about a data modification to a single item in a DynamoDB Table. You can configure a stream so that the stream records catpure additional information, such as the "before" and "after" images of modified items.
