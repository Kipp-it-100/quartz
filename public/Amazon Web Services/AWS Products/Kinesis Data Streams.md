---
icon: AiKinesisDataStreams
---
# ChatGPT Overview

AWS Kinesis Data Streams is a scalable and durable real-time data streaming service provided by Amazon Web Services. It enables developers to continuously capture gigabytes of data per second from hundreds of thousands of sources such as website clickstreams, database event streams, financial transactions, social media feeds, IT logs, and location-tracking events. This service is designed to facilitate real-time analytics and enable quick responses to information as it is received.

### Key Features of AWS Kinesis Data Streams

1. **Real-Time Data Streaming**: Kinesis Data Streams allows for the collection, processing, and analysis of streaming data in real time. This enables businesses to make timely decisions based on the most current data available.
    
2. **High Throughput and Scalability**: It can handle thousands of data producers and scale from megabytes to terabytes per hour and from thousands to millions of PUT operations per second. The scaling process is straightforward, allowing you to increase or decrease the throughput as needed.
    
3. **Durability and Reliability**: Data records are stored on Kinesis Data Streams for up to 365 days, allowing applications to process and reprocess the data as needed. The service replicates the data across multiple AWS Availability Zones (AZs) to enhance data integrity and reliability.
    
4. **Easy Integration with AWS Ecosystem**: Kinesis Data Streams integrates seamlessly with other AWS services such as AWS Lambda, AWS Kinesis Data Firehose, AWS Kinesis Data Analytics, Amazon S3, Amazon Redshift, Amazon EMR, and Amazon DynamoDB. This integration supports diverse applications, from real-time analytics to complex event processing.
    
5. **Flexible Consumption Choices**: You can build custom, real-time applications using popular programming languages such as Java, Python, and Ruby with Kinesis Client Library (KCL), or you can process streams with SQL using AWS Kinesis Data Analytics.
    

### How It Works

- **Stream Creation**: You start by creating a data stream in the AWS Management Console or via the AWS SDK. A stream is composed of one or more shards, which are the base throughput units of Kinesis Data Streams.
    
- **Data Production**: Data producers continually push data records into Kinesis Data Streams. Each record consists of a sequence number, partition key, and data blob. The partition key determines which shard a given data record belongs to.
    
- **Data Consumption**: Data consumers (applications built using the Kinesis Client Library, AWS Lambda, or AWS Kinesis Data Analytics) then process data from the stream. Consumers can access the data in real time or replay data from a specific point within the retention period.
    
- **Monitoring and Scaling**: You can monitor your streams via Amazon CloudWatch to track metrics such as Get and Put requests, iterator age, and more. If necessary, you can adjust the number of shards in a stream to scale the throughput up or down.
    

### Benefits

- **Real-Time Processing**: Enables immediate data processing needs, which is crucial for time-sensitive decisions that depend on the freshest data.
    
- **Customizable Data Retention**: The ability to configure the retention period from 24 hours up to 365 days allows flexibility in how data is reprocessed and analyzed over time.
    
- **Decoupling and Independency**: The service allows producers and consumers to operate independently at different rates and scales. Producers and consumers can be scaled and managed without impacting each other.
    

### Use Cases

- **Real-Time Analytics**: For applications like dashboarding, real-time analytics, and anomaly detection across various sectors such as finance, retail, and online services.
    
- **Log and Event Data Collection**: Collecting and processing large streams of log data or event records from software applications and services.
    
- **IoT Data Processing**: Handling large streams of data from IoT devices, such as sensors and telemetry, for real-time monitoring and processing.
    

AWS Kinesis Data Streams is a powerful tool for handling large-scale, real-time data ingestion and processing, allowing businesses to react quickly to new information and maintain a competitive advantage in data-driven decision-making.

# Notes
- Shards
	- Provisioned
	- Can scale # of shards
- Retention
	- 1-365 days
## Capacity Modes

### Provisioned Mode
- You choose # of shards provisioned
	- Scale manually or using API
- Each shard gets 1 MB/s in (or 1000 records per sec)
- Each shard gets 2 MB/s out (classic or enhanced fan-out consumer)
- You pay per shard provisioned per hour

### On-Demand Mode
- No need to provision or manage capacity 
- Default capacity provisioned (4MB/s in or 4000 records per sec)
- Scales automatically based on observed throughput peak during the last 30 days
- Pay per stream per hour & data in/out per GB
