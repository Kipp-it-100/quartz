---
title: 
tags: 
icon: 
aliases:
---
## Overview

This note is home for all flashcards for the purpose of prep for the  [[SAA-C03 Exam|AWS Certified Solutions Architect-Associate (SAA-C03) Exam]]

Heading defining different decks are solely for the purpose of reducing clutter.  Grouping is without method or reason.

## SAA Deck 1
#flashcards/saa 

How many dimensions can you have per cloudwatch metric? :: There are **up to 30 dimensions per metric**
<!--SR:!2024-08-01,45,252-->

When being asked about improving performance for applications over TCP or UDP think... :: [[Global Accelerator]]
<!--SR:!2024-06-21,4,192-->

Which data sources are supported by GuardDuty? :: VPC Flow Logs, DNS Logs, CloudTrail events
<!--SR:!2024-06-22,5,170-->

Scenarios necessitating serverless architecture wont include what AWS product? :: EC2
<!--SR:!2024-06-26,22,250-->

How many messages per second are supported by SQS FIFO? :: 300
<!--SR:!2024-06-20,3,252-->

How many batch messages per operation are supported by SQS FIFO :: 10
<!--SR:!2024-06-24,7,212-->

EC2 Spot Blocks can be used for up to how long? :: 6 hours
<!--SR:!2024-07-18,31,252-->

RDS Multi-AZ follows what kind of replication? :: Synchronous
<!--SR:!2024-06-30,13,232-->

RDS Read replicas follow what kind of replication? :: Asynchronous
<!--SR:!2024-06-30,13,212-->

AWS Lamda Currently supports how many concurrent executions per AWS account per region? :: 1000
<!--SR:!2024-06-24,20,252-->

if exam is asking you for a caching solution that does not require a code change then what is definitely not a good choice :: [[ElastiCache]] needs application code to be modded to be implemented
<!--SR:!2024-07-25,38,250-->

True or false: You can use SQL on [[ElastiCache]].  :: False. ElastiCache is not compatible with SQL
<!--SR:!2024-07-20,33,252-->

Any time that you see that you need to rapidly evolve schemas/have a flexible type of database schema, a great choice would be... :: [[DynamoDB]]
<!--SR:!2024-07-13,26,272-->

If you encounter an exam question, it's asking about a dynamo DB implementation that is capable of microsecond read latency, you come to mind? :: A [[DynamoDB#Dynamo DB accelerator (DAX)|DynamoDB Accelerator (DAX)]]  cluster can be used as a read cache, providing miscrosecond latency
<!--SR:!2024-06-19,2,190-->

Which database option is ideal for serverless app development use cases that use small documents or for a distributed serverless cache? :: [[DynamoDB]]
<!--SR:!2024-06-18,1,132-->

What is the max object size that can be stored using [[Simple Storage Service|S3]]? :: 5 terabytes is the max object size for storage in [[Simple Storage Service|S3]]
<!--SR:!2024-07-30,43,250-->

when the exam presents a scenario with a need for NoSQL databases, you should be thinking? (2) :: [[DocumentDB]] and [[DynamoDB]]
<!--SR:!2024-07-12,25,252-->

When you see something related to graph databases, think... :: [[Neptune]]
<!--SR:!2024-07-03,16,292-->

Any time you see Apache Cassandra or the Cassandra Query Language (CQL), think [[Keyspaces]]

Any time you see financial transactions and "ledger" think... :: [[Quantum Ledger Database|QLDB]]
<!--SR:!2024-08-02,46,252-->

Which AWS databases support both in-transit and at-rest encryption? :: All of AWS database options are capable of encryption in-transit and at-rest.
<!--SR:!2024-06-20,19,250-->

Which database helps you store relational datasets, with SQL language compatibility and the capability of processing transactions such as insert, update, and delete? :: [[Relational Database Service]]
<!--SR:!2024-06-22,5,170-->

Which AWS service provides you with caching capability that is compatible with Redis API? :: [[ElastiCache]]
<!--SR:!2024-07-21,34,230-->

You want to migrate an on-premises MongoDB NoSQL database to AWS. You don't want to manage any database servers, so you want to use a managed NoSQL Serverless database, that provides you with high availability, durability, and reliability, and the capability to take your database global. Which database should you choose? :: [[DynamoDB]]
<!--SR:!2024-06-18,1,192-->

You are looking to perform Online Transaction Processing (OLTP). You would like to use a database that has built-in auto-scaling capabilities and provides you with the maximum number of replicas for its underlying storage. What AWS service do you recommend? :: [[Aurora]]
<!--SR:!2024-06-25,8,192-->

As a Solutions Architect, a startup company asked you for help as they are working on an architecture for a social media website where users can be friends with each other, and like each other's posts. The company plan on performing some complicated queries such as _"What are the number of likes on the posts that have been posted by the friends of Mike?"_. Which database do you recommend?  :: [[Neptune]]
<!--SR:!2024-06-18,17,252-->

You have a set of files, 100MB each, that you want to store in a reliable and durable key-value store. Which AWS service do you recommend? :: [[Simple Storage Service|S3]] is a key-value store (where the key is the full path of the object in the bucket)
<!--SR:!2024-07-03,29,272-->

A company has an on-premises website that uses ReactJS as its frontend, NodeJS as its backend, and MongoDB for the database. There are some issues with the self-hosted MongoDB database as there is a lot of maintenance required and they don’t have and can’t afford the resources or experience to handle those issues. So, a decision was made to migrate the website to AWS. They have decided to host the frontend ReactJS application in an S3 bucket and the NodeJS backend on a set of EC2 instances. Which AWS service can they use to migrate the MongoDB database that provides them with high scalability and availability without making any code changes? :: [[DocumentDB]]
<!--SR:!2024-06-18,1,210-->

A company using a self-hosted on-premises Apache Cassandra database which they want to migrate to AWS. Which AWS service can they use which provides them with a fully managed, highly available, and scalable Apache Cassandra database? :: [[Keyspaces]]
<!--SR:!2024-06-18,10,210-->

An online payment company is using AWS to host its infrastructure. Due to the application’s nature, they have a strict requirement to store an accurate record of financial transactions such as credit and debit transactions. Those transactions must be stored in secured, immutable, encrypted storage which can be cryptographically verified. Which AWS service is best suited for this use case? :: [[Quantum Ledger Database]]
<!--SR:!2024-08-05,49,250-->

A startup is working on developing a new project to reduce forest fires due to climate change. The startup is developing sensors that will be spread across the entire forest to make some readings such as temperature, humidity, and pressures which will help detect the forest fires before it happens. They are going to have thousands of sensors that are going to store a lot of readings each second. There is a requirement to store those readings and do fast analytics so they can predict if there is a fire. Which AWS service can they use to store those readings? :: [[Timestream]]
<!--SR:!2024-06-29,12,230-->

Any time you need to analyze data in S3 using a serverless SQL engine, think... :: [[Athena]]
<!--SR:!2024-06-21,13,230-->

You have five [[CloudFormation]] templates; each template is for a different application architecture. This architecture varies between your blog apps and your gaming apps. What determines the cost of using the CloudFormation templates? ::  [[CloudFormation]] does not have any additional cost but you are charged for the underlying resources it builds.
<!--SR:!2024-06-20,3,230-->

If you want to use an [[Secure Sockets Layer|SSL]] protocol but do not want to terminate the connection on your load balancer, you can use a __________ protocol for connection from the client to your load balancer. :: [[Transmission Control Protocol|TCP]]
<!--SR:!2024-07-22,35,250-->

You are building an automated transcription service in which "Amazon EC2 worker" instances process an uploaded audio file and generate a text file. You must storer retrieved, but you do not know what the storage capacity requirements  both of these files in the same durable storage until the text file is are. Which storage option is both cost-efficient and scalable? :: A single Amazon [[Simple Storage Service|S3]] bucket
<!--SR:!2024-07-18,31,232-->

In the event of a planned or an unplanned outage of your primary DB instance, Amazon RDS automatically switches to a standby replica in another Availability Zone if you have enabled_________. :: Multiple Availability Zones
<!--SR:!2024-06-29,12,230-->

Which of the following approaches provides the lowest cost for Amazon elastic block store snapshots while giving you the ability to fully restore data? :: Maintain two snapshots: the original snapshot and the latest incremental snapshot.
<!--SR:!2024-07-18,31,250-->

A user has created multiple data points for the CloudWatch metrics with the dimensions, Box=UAT, App = Document and Box = UAT, App = Notes. If the user queries CloudWatch with the dimensions parameter as, Server=prod, what data will he get? :: It will not return any data as the dimension for Box=UAT does not exist
<!--SR:!2024-06-20,3,230-->

You try to enable lifecycle policies on one of the S3 buckets created by you, but you are not able to do so on that particular bucket. What could be the reason? :: Versioning is not enabled on that bucket.
<!--SR:!2024-06-20,19,252-->

Which IAM policy condition key should be used if you want to check whether the request was sent using SSL? :: AWS: secure transport
<!--SR:!2024-06-27,10,232-->

Allow users to use actions that start with 'Describe' across all the EC2 resources. ::: What does the following policy for Amazon EC2 do? { "Statement": [{ "Effect":"Allow", "Action":"ec2: Describe*", "Resource":"*" }
<!--SR:!2024-06-21,4,270!2024-06-20,12,252-->

To create an Amazon [[Elastic Block Store|EBS-backed]] from an Amazon EBS-backed instance that is either running or has stopped ::: For what purpose is the string "create image" API action used?
<!--SR:!2024-06-20,3,250!2024-07-14,27,230-->

dedicated instance ::: If you launch an instance into a [[Virtual Private Cloud|VPC]] that has an <mark style="background: #FFB8EBA6;">instance tenancy</mark> of a ______________, your instance is automatically a Dedicated Instance, regardless of the tenancy of the instance
<!--SR:!2024-07-11,24,250!2024-06-20,3,210-->

This is a serverless query service used to analyze data stored on [[Simple Storage Service|S3]]. :: [[Athena]]
<!--SR:!2024-06-20,16,250-->

What language is used by [[Athena]] to query files? :: [[Athena]] uses standard SQL language to query files.
<!--SR:!2024-07-21,34,250-->

What other AWS service is Athena commonly used with for the purpose of reporting/dashboards?  :: [[QuickSight]].
<!--SR:!2024-07-27,40,250-->

[[Redshift]] (mostly) supports what kind of deployments? :: [[Redshift]] only supports **single-AZ** deployments
<!--SR:!2024-07-28,41,250-->

What kind of pricing model does [[Redshift]] follow? :: Pay-as-you-go based on **instances provisioned**
<!--SR:!2024-06-18,1,190-->

Any time you see anything related to big data  clusters with [[Apache Hadoop|Hadoop]] clusters, you would think... :: [[Elastic MapReduce]]
<!--SR:!2024-07-03,16,212-->

reserved instances require a a minimum reservation time of how long? :: 1 year
<!--SR:!2024-07-09,22,252-->

Logs from this AWS product are stored in an [[Simple Storage Service|Amazon S3]] bucket, so if you see mentions of "S3 storage for logs" or "log file storage," it could indicate... :: [[CloudTrail]]
<!--SR:!2024-07-12,25,270-->

- Think infrastructure as code, think... :: [[CloudFormation]]
<!--SR:!2024-07-06,19,252-->


## SAA Deck 2
#flashcards/saa 

What does ETL stand for? :: Extract, Transform, and Load
<!--SR:!2024-07-04,30,272-->

[[DynamoDB]]: SQL or NoSQL? :: [[DynamoDB]] is **NoSQL**
<!--SR:!2024-08-07,51,252-->

[[Aurora]]: SQL or NoSQL? :: [[Aurora]] is a **MySQL** and **PostgreSQL**- compatible **relational database**
<!--SR:!2024-07-21,34,232-->

Aurora Global can have up to how many read instances in each region where database is...unfinished :: Up to 16 DB read instances.
<!--SR:!2024-08-03,47,252-->

How fast can [[Aurora|Aurora Global]] perform storage replication? :: [[Aurora|Aurora Global]] is capable of **sub-second** storage replication
<!--SR:!2024-06-18,1,172-->

What is the main purpose of [[Relational Database Service|RDS]]Multi-AZ deployments?
?
The primary purpose of Multi-AZ is **high availability**
<!--SR:!2024-06-20,3,229--> 

[[Relational Database Service|RDS]]Read replicas can be within which infrastructural locations?
?
Read replicas can be within:
- an Availability Zone
- Cross-AZ
- Cross-Region
<!--SR:!2024-06-18,10,210-->

what is the main purpose of [[Relational Database Service|RDS]] Multi-Region deployments?
?
the main purposes of Multi-Region
- **disaster recovery**
- **local performance**
<!--SR:!2024-06-23,6,169-->

RDS Multi-region deployments follow which kind of replication?
?
Multi-region deploys follow **Asynchronous** replication
<!--SR:!2024-06-20,3,229-->

how rapidly can [[Relational Database Service|RDS]] Multi-AZ with **two readable standbys** can be expected to achieve auto-failover?
?
[[Relational Database Service]] deployments with Multi-AZ with two readable standbys typically auto-failover in **under 35 seconds**.  This occurs with zero data loss and obvi, no manual intervention.
<!--SR:!2024-06-18,1,190-->

how rapidly can [[Relational Database Service|RDS]] Multi-AZ with **one standby** can be expected to achieve auto-failover?
?
60 seconds
<!--SR:!2024-06-22,14,230-->

There are 7 [[Relational Database Service]] engines that are compatible with both Single-AZ and Multi-AZ/**single standby** deployments. What are they?
?
RDS engines available with both of these deployment types are:
- Amazon RDS for [[PostgreSQL]]
- Amazon RDS for [[MySQL]]
- Amazon RDS for [[MariaDB]]
- Amazon RDS for [[SQL Server]]
- Amazon RDS for [[Oracle Corporation|Oracle]]
- Amazon RDS for [[IBM Db2|Db2]]
<!--SR:!2024-06-18,1,130-->

Which two [[Relational Database Service|RDS]] engines are compatible with Multi-AZ with two readable standbys?
?
- [[Relational Database Service|Amazon RDS]] for [[PostgreSQL]]
- [[Relational Database Service|Amazon RDS]] for [[MySQL]]
<!--SR:!2024-06-18,1,130-->

which replication method is well-suited for use-cases in which data integrity and zero data loss are priorities?
?
**synchronous replication**
- it provides strong data consistency, ensuring the data on the primary and replica are identical at all time.
- This makes it ideal for applications where data integrity is crucial, such as financial transactions, inventory systems, and critical databases.
<!--SR:!2024-06-20,3,229-->

which replication method is heavier on performance overhead of the two?
?
**syncronous replication**
- it needs to wait for ack from the replica, introducing latency and reducing overall system performance
- it also requires more bandwidth and processing power to maintain real-time sync
	- this is costly and resource hungry
<!--SR:!2024-06-25,17,249-->

[[CloudTrail]] can stream data to only two locations.  What are they?
?
[[cloudtrail]] can only stream to:
1. [[Simple Storage Service|S3]] buckets
2. [[CloudWatch]] logs
<!--SR:!2024-06-27,10,209-->

[[Aurora]] DB instances auto-scale vertically up to what size?
?
**128 TB** per [[Aurora]] database instance
<!--SR:!2024-06-18,1,209-->

What are the four most common use cases for [[Kinesis Data Analytics]]?
?
1. **Streaming** ETL
2. **Continuous** metric generation
3. responsive **real-time** analytics
4. **interactive** querying of data
<!--SR:!2024-06-18,1,130-->

[[Kinesis Data Analytics]] for [[Apache Flink]] provides how much running application storage per Kinesis Processing Unit (KPU)?
?
**50 GB**
<!--SR:!2024-06-27,10,209-->

[[API Gateway]] offers two options to create RESTful APIs.  What are they?
?
1. [[HTTP APIs]]
2. **[[REST API|REST APIs]]**
<!--SR:!2024-06-18,1,189-->

Question referring to a key-value store is usually an indication of what kind of database?
?
"Key-value" store is likely a keyword for a **nonrelational** or **noSQL** database
<!--SR:!2024-06-18,1,209-->

Which [[cognito]] pool type boasts built-in user management?
?
[[Cognito]] **User pools**
<!--SR:!2024-06-27,10,189-->

How many virtual CPUs (vCPUs) does an [[Snowball|AWS Snowball]] Edge Storage Optimized device contain:
?
**40 vCPUs**
<!--SR:!2024-06-24,7,205-->

Each [[Aurora]] database cluster is/can have how many primary instances?
?
**One:** clusters can have one and only one primary instance.  Emphasis on the singular form of the word "instance"
<!--SR:!2024-06-24,7,205-->


## SAA Deck 3
#flashcards/saa 

keywords related to auditing and monitoring, such as "audit," "monitor," "logging," or "tracking" may be an indication of....
?
[[CloudTrail]]
<!--SR:!2024-07-15,28,245-->

You have tranfered approx 70 GB this billing period (consisting of 1 month) out of [[Simple Storage Service|S3]] to the net.  How will this effect your bill?
?
**Not at all,** As data egress from s3 is completely free of charge for the first 100 GB transferred out to the net over month
<!--SR:!2024-06-18,1,145-->

you monthly bill for [[Simple Storage Service|S3]] egress out to the net is ***exactly*** 9 cents.  This means exactly how many gigabytes have gone out.
?
**1,100 GB** which can also be expressed as **10.1 TB**
<!--SR:!2024-06-19,2,185-->

This month you have transfered a lot of data out of [[Simple Storage Service|S3]] the internet: about **200 TB**.  How much will this cost you **per GB** over 150 TB
?
per the pricing policies of [[Simple Storage Service|S3]], you can expect to pay $0.05 per GB for data exceeding the 150 TB pricing tier
<!--SR:!2024-06-20,3,205-->

Explain the pricing for [[Athena]]
?
[[Athena]] is charged at a **fixed amount** of $5.00 per TB data scanned
<!--SR:!2024-06-18,1,199-->

(Blank) is a good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP, as well as for HTTP use cases that specifically require static IP addresses or deterministic, fast regional failover.
?
[[Global Accelerator]]
<!--SR:!2024-06-18,1,199-->

Which AWS destinations can [[Kinesis Firehose]] write to?
?
[[Simple Storage Service|S3]]
[[Redshift]] (**through s3**)
[[OpenSearch Service]]

a question asking about what to use if you wanted to encrypt all unencrypted objects in a given s3 bucket, the answer may be...
?
[[Simple Storage Service#S3 Batch Operations|S3 Batch Operations]]

Which s3 encryption method is enabled by default for new buckets and new objects?
?






## Maybe Pile


```
#### other 1




Amazon AWS DevPay and Amazon AWS FPS ::: If you want to build your own payments application, then you should take advantage of the richness and flexibility of _____________.



Reference the logical IDs of both the block stores and the instance ::: If you want to map Amazon Elastic Block Store to an Amazon EC2 instance for AWS CloudFormation resources?





Subnet ::: In a VPC network, access control lists (ACLs) act as a firewall for associated subnets, controlling both inbound and outbound traffic at the __________ level.














1, 1 MB ::: In DynamoDB you can issue a scan request. By default, the scan operation processes data sequentially. DynamoDB returns data to the application in _________ increments, and an application performs additional scan operations to retrieve the next ___________ of data



Amazon Resource Names ::: AWS requires ____________ when you need to specify a resource uniquely across all of AWS, such as in IAM policies, Amazon Relational Database Service (Amazon RDS) tags, and API calls.

Amazon SWF ::: ___________ is a task coordinator and state management service for cloud applications.

IPv4 vs IPv6 ::: IP address mechanisms are supported by ELB

Customer Gateway ::: A ___________ is a physical device or software application on your side of the VPN connection

Modify the Network ACLs (NACLs) associated with all public subnets in the VPC to deny access from the IP address block. ::: You are currently hosting multiple applications in a VPC and have logged numerous port scans coming in from a specific IP address block. Your security team has requested that all access to the offending IP address block be denied for the next 24 hours. Which of the following is the best method to quickly and temporarily deny access to the specified IP address block?

Controller service ::: Which ELB component is responsible for monitoring the Load Balancers?

Multi-site solution ::: Which disaster recovery method involves running your site in AWS and on your existing on-site infrastructure in an active-active configuration?

IP address of client ::: An application hosted at the EC2 instances receives HTTP requests through the ELB. Each request has an X-Forwarded-For request header, having three IP addresses. Which of the following IP address will be a part of this header?

Changes are automatically applied to all instances that are associated with the security group. ::: You have launched an instance in EC2-Classic and you want to make some change to the security group rule. How will these changes be effective?

Move two instances to another Availability Zone. ::: You have an application running on Amazon Web Services. The application has 4 EC2 instances in Availability Zone us-east-1c. You're using Elastic Load Balancer to load balance traffic across your four instances. What changes would you make to create a fault tolerant architecture?

Regions ::: The load balancer does not distribute traffic across ________.

A list of any of the stacks you have created or have deleted up to 90 days ago. ::: In context of CloudFormation, which of the following information do you get from the AWS Cloud Formation list-stacks Command?

updates the route tables ::: When you use the wizard in the console to create a VPC with a gateway, the wizard automatically __________ to use the gateway.

Amazon CloudFormation ::: You've created production architecture on AWS. It consists of one load balancer, one route53 domain, two Amazon S3 buckets, Auto Scaling policy, and Amazon CloudFront for content delivery. Your manager asks you to duplicate this architecture by using a JSON based template. Which of the following AWS service would you use to achieve this?

Configure the security group of EC2, which allows access to the ELB source security group. ::: You have configured a website www.abc.com and hosted it on WebLogic Server and you are using ELB with the EC2 instances for load balance. Which of the following would you configure to ensure that the EC2 instances accept requests only from ELB?

Outputs ::: You have written a CloudFormation template that creates one Elastic Load Balancer fronting two EC2 instances. Which section of the template should you edit so that the DNS of the load balancer is returned upon creation of the stack?

A collection of related Workflows ::: What does a 'Domain" refer to in Amazon SWF?

SSL certificate will be installed at ELB and the listener port should be changed from 80 to 443 to allow the traffic to reach EC2 ::: Once you've successfully created a Microsoft windows stack on AWS CloudFormation, you can log in to your instance with _______ to configure it manually.

Remote Desktop ::: You have created a custom configured Amazon instance using Linux, containing all your software and applications. If you want to use the same setup again, what is the best way to do it

Create an EBS Image (AMI) ::: With regards to VPC, what is the default maximum number of virtual private gateways allowed per region?

The power to scale computing resources up and down easily with minimal friction ::: Elasticity is a fundamental property of the cloud. Which of the following best describes elasticity?

Region ::: With regards to RDS, the standby should be in the same ______________ as the primary instance

AWS Management Console
Command line interface (CLI)
IAM QUERY API ::: AWS Identity and Access Management is available through which of the following interfaces?

Increasing resources result in a proportional increase in performance. ::: Scalability is a fundamental property of a good AWS system. Which of the following best describes scalability on AWS?

Use SAML (Security Assertion Markup Language) to enable single sign-on between AWS and LDAP. ::: Which technique can be used to integrate AWS IAM (Identity and Access Management) with an on-premises LDAP (Light Weight Directory Access Protocol) directory service?

Stop all DML and DDL operations on non-transactional tables and wait for them to complete
Flush and lock those tables
Create the Read Replica using the Create DB instance Read Replica API
Check the progress of the Replica creation using the describe DB instances API ::: If you are using a non-transactional engine such as My ISAM, which of the following steps need to be performed to successfully set up your Read Replica so it has a consistent copy of your data?

www.abc.com to d111111abcdef8.cloudfront.net ::: In CloudFront, if you add a CNAME for www.abc.com to your distribution, you also need to create (or update) a CNAME record with your DNS service to route queries for ___________.

Build the replica set using EC2 instances and manage the Mongo DB instances yourself. ::: Your manager has asked you to build a MongoDB replica set in the Cloud. Amazon Web Services does not provide a MongoDB service. How would you go about setting up the MongoDB replica set?

DynamoDB ::: Your company has an application that requires access to a NoSQL database. Your IT departments have no desire to manage the NoSQL servers. Which Amazon service provides a fully managed and highly available NoSQL service

10,000 ::: How many requests per second can Amazon CloudFront handle?

You can specify your origin Amazon S3 bucket or HTTP server. ::: When you need to use CloudFront to distribute your content you need to create a distribution. You also need to specify the configuration settings. Which of the following configuration settings would you specify?

Create a new Cloud Trail with one new S3 bucket to store the logs and with the global services option selected. Use IAM roles S3 bucket policies and Multi Factor Authentication (MFA) delete on the S3 bucket that stores your logs. ::: You currently operate a web application in the AWS US-East region. The application runs on an auto-scaled layer of EC2 instances and an RDS Multi-AZ database. Your IT security compliance officer has tasked you to develop a reliable and durable logging solution to track changes made to your EC2, IAM, and RDS resources. The solution must ensure the integrity and confidentiality of your log data. Which of these solutions would you recommend?

EC2 instance status Check Failed
EC2 CPU utilization
Auto Scaling group CPU utilization ::: Which of the following metrics can have a CloudWatch Alarm?

Partial Upfront
No Upfront
ALL Upfront ::: Which of the following payment options are associated with Reserved Instances?

There is a limit of 20 EC2 instances in each region; you can request to increase the limit. ::: You have a website www.abc.com which is used quite frequently. Therefore, you decide to use 50 EC2 instances, with two availability zones in two regions, each with 25 instances. However, while starting the servers, you are able to start only 20 servers and then the requests start failing. Why?

Reduced Redundancy Storage ::: www.picsee.com website has millions of photos and also thumbnails for each photo. Thumbnails can easily be reproduced from the actual photo. However, a thumbnail takes less space than actual photo. Which of the following is the best solution to store thumbnails?

S3
SQS
SNS ::: You want your Hadoop job to be triggered based on the event notification of a file upload action. Which of the following components can help you implement this in AWS?

Versioning in S3 ::: www.dropbag.com is a website where you have file sharing and storing services like Google Drive and Google Dropbox. During the sync up from desktop you accidently deleted an important file. Which of the simple storage service will help you retrieve the deleted file

AWS S3 ::: www.picnic.com is a photo and video hosting website and they have millions of users. Which of the following is a good solution for storing big data object, by reducing costs, scaling to meet demand, and increasing the speed of innovation?

Verify that the private key file corresponds to the Amazon EC2 key pair assigned at launch, Verify that you are connecting with the appropriate user name for your AMI. ::: You try to connect via SSH to a newly created Amazon EC2 instance and get one of the following error messages: 'Network error: connection timed out" or "Error connecting to [instance], reason :-> Connection timed out: connect,' you have confirmed that the network and security group rules are configured correctly and the instance is passing status checks. What steps should you take to identify the source of the behavior? (Select all that apply)

5 ::: With regards to VPC, what is the default maximum number of virtual private gateways allowed per region?
#### other 2

VPC :: *Virtual Private Cloud*

(A __________ is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS cloud.)

(A __________ is a component of the Networking Service.)

(A __________ must set DNS Hostnames to "Yes" for instances launched in the subnet to get DNS Names.)

(By default you can only have 5 __________ per AWS region.)

Elastic Beanstalk :: __________ is an Orchestration service for deploying infrastructure including EC, S3, SNS, CloudWatch, Autoscaling, and Elastic Load Balancers.

__________ is specifically designed to run a developer's code on an infrastructure that is automatically provisioned to host that code.

__________ can be used to create Web Server and Worker environments.

LAMBDA :: AWS __________ is a Server-less compute service that runs your code in response to events and automatically manages the underlying compute resources for you.

Route 53 :: __________ is a scalable and highly available (DNS).

The name __________ is a reference to TCP or UDP port, where DNS server requests are addressed.

With __________ You can register domains, Route Internet traffic to domain resources and conduct health checks of resources.

__________ supports a Maximum of 50 domain names, however this limit can be increased by contacting AWS support

EMR :: *Elastic Map Reduce*
__________ processes big data across a Hadoop cluster of virtual servers on EC2 and S3.
__________ is a compute service specifically designed to assist you in processing large data sets.

CloudFormation :: An easy way to create and manage a collection of related AWS resources, provisioning and updating them in an orderly and predictable fashion.

CloudFront :: A web service that speeds up distribution of your static and dynamic web content, such as .html, .css, .php, and image files, to your users.
A service that uses a CDN to distribute content around the world.

CDN :: *Content Delivery Network*
Delivers content based on geographic locations of the user, origin of the webpage and the content delivery server.
A system of distributed servers that deliver pages and other Web content to a user

Glacier :: A secure, durable, and extremely low-cost cloud storage service for data archiving and long-term backup.
The best choice for long term data archival

S3 :: *Simple Storage Service*
__________ offers durable, available storage for flat files.
Makes it simple and practical to collect, store, and analyze data - regardless of format - all at massive scale.
Durability of 99.999999999% (11x9's) 
Availability of 99.99%
Applies to Standard, Infrequent Access (IA) and Glacier
Has a minimum file size of 0 Bytes
This is a Global service, and its reliability and durability are not bound to any Region or Availability Zone.

RDS :: *Relational Database Services*
__________ offers the following database engines: SQL, MySQL, MariaDB, PostgreSQL, Aurora, and Oracle.
__________ is a web service that makes it easier to set up, operate, and scale a relational database in the cloud.
If you are using Provisioned IOPS storage with MySQL and Oracle, the maximum size Volume is 6 TB by default.
I/O operations are suspended for the duration of a snapshot.
You cannot use the secondary database as an independent read node.
The maximum provisioned IOPS capacity on and Oracle and MySQL instance (Using Provisioned IOPS) is 30,000 IOPS

Redshift :: __________ is a fast, fully managed data warehouse that makes it simple and cost-effective to analyze all your data using standard SQL and your existing BI tools
This Service is used primarily for data warehousing.
__________ Supports Cross-Region Snapshots.
Amazon __________ uses a hierarchy of encryption keys to encrypt the database. You can use a KMS or HMS to manage top level encryption keys in this hierarchy.

Kinesis :: __________ enables you to process and analyze data as it arrives and respond in real-time.
__________ is used for collating large amounts of data streamed from multiple sources.

CloudTrail :: __________ is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account.
__________ allows AWS customers to record API calls, sending log files to Amazon S3 buckets for storage.
You can turn on a trail across ALL regions for your AWS account.

OpsWorks :: A configuration management service that uses Chef, an automation platform that treats server configurations as code.

Elastic Transcoder :: Media transcoding in the cloud.
This service is designed to be highly scalable, easy to use and a cost effective way for developers and businesses to convert media for multiple uses.

AWS Storage Gateway :: This is a hybrid storage service that enables your on-premises applications to seamlessly use AWS cloud storage.
Your applications connect to the service through a gateway appliance using standard storage protocols, such as NFS and iSCSI.
This device connects to AWS storage services, such as S3, Glacier, and EBS, providing storage for files, volumes, and virtual tapes in AWS.
The service includes a highly-optimized data transfer mechanism, with bandwidth management, automated network resilience, and efficient data transfer.
This service provides a local cache for low-latency on-premises access to your most active data.

S3 - RRS :: *Reduced Redundancy Storage*
<!--SR:!2024-04-15,3,250-->
__________ is an S3 option that enables customers to store noncritical, reproducible data at lower levels of redundancy than S3's standard storage.
__________ has a Durability of 99.99% and Availability of 99.99%
There is no charge for replicating data from your Primary Instance to your Secondary instance.

EBS :: *Elastic Block Storage*
__________ provides persistent block storage volumes for use with Amazon EC2 instances in the AWS Cloud.

S3 - IA :: *Standard Infrequent Access*
S3 storage class for data that is accessed less frequently, but requires rapid access when needed.

DynamoDB :: __________ is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability.
__________ synchronously replicates data across three facilities in an AWS Region, giving you high availability and data durability.
__________ is best suited for non relational databases

Massive Paralell Computations :: Spot Instances

IAM :: *Identity and Access Management*
__________ enables you to securely control access to AWS services and resources for your users.
You can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources.

DynamoDB Eventually Consistent Reads (Default) :: DynamoDB Consistency model that Maximizes your read throughput. However, might not reflect the results of a recently completed write.
DynamoDB Consistency Model where Consistency across all copies of data is usually reached within a second.

DynamoDB Strongly Consistent Reads :: DynamoDB Consistency Model that Returns a result that reflects all writes that received a successful response prior to the read.

DynamoDB Cross-Region replication :: DynamoDB Service that provides Efficient disaster recovery.
DynamoDB Service that provides Faster reads.
DynamoDB Service that provides Easier traffic management
DynamoDB Service that facilitates Easy regional migration
DynamoDB Service that facilitates Live data migration

Cloudformation - Format Version :: (Optional) Specifies the AWS CloudFormation template version that the template conforms to.
(Optional) Cloudformation Section that can change independently of the API and WSDL versions.

Cloudformation - Description :: (Optional) Cloudformation Section that describes the template. This section must always follow the template format version section.

Cloudformation - Metadata. :: (Optional) Cloudformation Section that provides additional information about the template.

Cloudformation - Parameters :: (Optional) Cloudformation Section that specifies values that you can pass in to your template at runtime (when you create or update a stack).
(Optional) Cloudformation Section you can refer to in the Resources and Outputs sections of the template.

Cloudformation - Mappings :: (Optional) Cloudformation Section that is similar to a lookup table. With keys and values that you can use to specify conditional parameter values.

Cloudformation - Conditions :: (Optional) Cloudformation Section that controls whether certain resources or properties are created or assigned a value during stack creation or update.

Cloudformation - Transform :: (Optional) Cloudformation Section for serverless (Lambda-based) applications, specifies the version of the Serverless Application Model (AWS SAM) to use.

Cloudformation - Resources :: (Required) Cloudformation Section that specifies the stack resources and their properties, such as an EC2 instance or an S3 bucket.

Cloudformation - Outputs :: (Optional) Cloudformation Section that describes the values that are returned whenever you view your stack's properties.

IAM - User :: IAM Entity that represents the person or service who uses the IAM user to interact with AWS.

IAM - Group :: IAM Entity that you can use to specify permissions for a collection of users, which can make those permissions easier to manage for those users.

IAM - Role :: IAM Entity that is very similar to a user, with permission policies that determine what the identity can and cannot do in AWS.
IAM Entity that does not have any credentials (password or access keys) associated with it.
IAM Entity that Instead of being uniquely associated with one person, is intended to be assumable by anyone who needs it.

IAM - Temporary Credentials :: IAM Entity that is primarily used with IAM Roles. Can be requested to have more restricted set of permissions than a standard user.
IAM Entity that can be set to expire automatically after a set period of time. You control the expiration of the Entity.
You can use the AWS Security Token Service (STS) to create and provide trusted users with credentials that can control access to your AWS resources.

IAM - AWS Account Root User :: IAM Entity that has complete unrestricted access to all resources in your AWS account, including billing and password changes.
IAM Entity that should NOT be used for everyday access.

EC2 - Instance Type: General purpose :: T2, M4 & M5
__________ instances provide a balance of compute, memory, and networking resources, and can be used for a variety of workloads.

EC2 - Instance Type: Compute optimized :: C4 & C5
__________ instances are ideal for compute-bound applications that benefit from high-performance processors.

EC2 - Instance Type: Memory optimized :: R4, X1 & X1e
__________ instances are designed to deliver fast performance for workloads that process large data sets in memory.

EC2 - Instance Type: Storage optimized :: D2, H1 & I3
__________ instances are designed for workloads that require high, sequential read and write access to very large data sets on local storage.

EC2 - Instance Type: Accelerated computing :: F1, P3, P2 & G3
If you require high processing capability, you'll benefit from using __________ instances, which provide access to hardware-based compute accelerators such as Graphics Processing Units (GPUs) or Field Programmable Gate Arrays (FPGAs).

Default VPC :: A logically isolated VNET in the AWS cloud that is automatically created for your AWS account the first time you provision EC2 resources
A __________ exists in each AWS region

RDS - Read Replica :: __________ is Supported by these Databases MySQL, MariaDB & PostgreSQL

VM - Import/Export :: __________ enables customers to import VM images in order to create EC2 instances. Customers can also export previously imported EC2 instances to create VMs.

AWS - Supported SDKs :: Android, Browser, iOS, Java, .NET, Node.js, PHP, Python, Ruby, GO, C++ AWS Mobile

SQS :: *Simple Queue Service*
__________ is a web service that gives you access to message queues that store messages waiting to be processed. 
__________ offers a reliable, highly-scalable, hosted queue for storing messages in transit between computers.
You can move data between diverse, distributed app components without losing messages and without requiring each component to be always available.

SQS - Message Retention :: You can configure a retention period from 1 minute to 14 days the default retention period is 4 days

RDS - Website Endpoints :: The two general forms of RDS __________ are as follows: 
bucket-name.s3-website-region.amazonaws.com 
and 
bucket-name.s3-website.region.amazonaws.com

Kinesis - Shards :: A __________ is a uniquely identified group of data records in a stream.
A stream is composed of one or more __________ each of which provides a fixed unit of capacity.

Virtual Private Cloud (VPC) - Flow Logs :: __________ enables you to capture information about the IP traffic going to and from network interfaces in your VPC.

ELB :: *Elastic Load Balancing*
An __________ automatically distributes incoming application traffic across Amazon EC2 instances,containers, or resources identified by IP addresses.
You can setup __________ to handle incoming app traffic across Amazon EC2 instances in a single Availability Zone or multiple Availability Zones.
__________ is one of the most Ideal solutions for adding elasticity to your application.

IGW :: *Internet Gateway*
An __________ is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the Internet.

CloudWatch Logs :: You can use __________ to monitor, store, and access your log files from Amazon EC2 instances, AWS CloudTrail, and other sources.

Provisioned IOPS SSD (io1) Volumes - 50:1 :: The maximum ratio of IOPS to volume size

Instance Metadata :: __________ is data about your instance that you can use to configure or manage the running instance.
__________ can be accessed using this URI: http://169.254.169.254/latest/meta-data/
__________ can only be accessed from within the Instance

API Gateway :: An __________ is a fully managed service that makes it easy for developers to publish, maintain, monitor, and secure APIs at any scale.
<!--SR:!2024-04-15,3,250-->
All of the APIs created with the __________ expose HTTPS endpoints only.

EC2 - Container Service :: __________ is a highly scalable, high performance container management service.
__________ supports Docker and allows you to easily run apps on a managed cluster of EC2 instances.

AMI :: *Amazon Machine Image*
Provides the information required to launch an instance.
You specify an __________ when you launch an instance, and you can launch as many instances from this __________ as needed.
You can also create __________s and sell them to other Amazon EC2 users.
You can customize the instance that you launch from a public __________ and then save that configuration as a custom __________ for your own use.

Route Tables :: Contains a set of rules, called routes, that are used to determine where network traffic is directed.

EC2Rescue :: This is an easy-to-use tool that you can run on an Amazon EC2 Linux instance to diagnose and troubleshoot possible problems.

EBS Snapshot :: A point-in-time snapshot of an EBS volume, can be used as a baseline for new volumes or for data backup.
Can be created using a AWS CLI or Windows Powershell

S3 - Cross-Region Replication :: __________ is a bucket-level feature that enables automatic, asynchronous copying of objects across buckets in different AWS regions.
You might configure __________ on a bucket for various reasons, including these: Compliance Requirements, Minimize Latency, Operational reasons.

S3 - Cross-Region Replication - Requirements :: The source and destination buckets must be versioning-enabled.
The source and destination buckets must be in different AWS regions.
You can replicate objects from a source bucket to only one destination bucket.
S3 must have permission to replicate objects from that source bucket to the destination bucket on your behalf.
If the source bucket owner also owns the object, the bucket owner has full permissions to replicate the object.
if you are setting this up in a cross-account scenario, the source bucket owner must have permission to replicate objects in the destination bucket.
Amazon S3 must have permission to replicate objects from that source bucket to the destination bucket on your behalf.
If the source bucket owner also owns the object, the bucket owner has full permissions to replicate the object.
if you are setting this up in a cross-account scenario, the source bucket owner must have permission to replicate objects in the destination bucket.

First and Last One :: This is the number of IP addresses that are reserved for AWS in a Subnet CIDR block.

Reserved Instance Marketplace :: This is a platform that supports the sale of third-party and AWS customers' unused Standard Reserved Instances, and vary in term lengths and pricing.

VPC - Security Groups :: __________ act as a virtual firewall for your instance to control inbound and outbound traffic.
When you launch an instance in a VPC, you can assign up to five (5) __________ to the instance.

Redshift - Columnar Storage :: This is an important factor in optimizing analytic query performance.
It drastically reduces the overall disk I/O requirements and reduces the amount of data you need to load from disk.
Uses a block size of 1 MB, which is more efficient

CloudWatch :: __________ is a monitoring service for AWS cloud resources and the applications you run on AWS
Use __________ to collect and track metrics, collect and monitor log files, set alarms, and automatically react to changes in your AWS resources.
The default dashboard does not show a metric for memory usage

Kinesis - Streams :: Supports changes to the data record retention period of your stream.
This is an ordered sequence of data records meant to be written to and read from in real-time. 
Stores records from hours by default, up to hours.

S3 - Versioning :: __________ is a means of keeping multiple variants of an object in the same bucket.
You can use __________ to preserve, retrieve, and restore every version of every object stored in your Amazon S3 bucket. 
With __________ you can easily recover from both unintended user actions and application failures.

ElastiCache :: __________ is a web service that makes it easy to deploy, operate, and scale an in-memory data store or cache in the cloud.
__________ improves the performance of web applications by allowing you to retrieve information from fast, managed, in-memory data stores.
__________ uses Redis and Memcached engines

Step Functions :: __________ makes it easy to coordinate the components of distributed applications and microservices using visual workflows.
__________ are a reliable way to coordinate components and step through the functions of your application.

EBS Volume :: __________ only persist if instructed to do so when they are created
Cannot delete __________ if it is used as the root device of a registered AMI.
an __________ can only be attached to a single EC2 Instance at the same time

Placement Group :: __________ is a logical grouping of instances within a single Availability Zone.
A __________ is recommended for applications that benefit from low network latency, high network throughput, or both.

SWF :: *Simple Workflow*
__________ helps developers build, run, and scale background jobs that have parallel or sequential steps.
A _______ is a fully-managed state tracker and task coordinator in the Cloud.

SES :: *Simple Email Service*
__________ is a powerful, affordable, and highly-scalable email sending and receiving platform for businesses and developers.
__________ integrates seamlessly with your applications and with other AWS products.

SNS :: *Simple Notification Service*
__________ is a flexible, fully managed pub/sub messaging and mobile notifications service for coordinating delivery of messages to subscribed endpoints and clients.

CDN - Edge :: __________ is the location where content will be cached. This is separate to an AWS Region/AZ
You can write to the __________ (i.e. put an object on the __________).
Objects are cached for the life of the TTL (Time To Live)

CDN - Origin :: The origin of the files the CDN will distribute.

CDN - Distribution :: This is the name given to the CDN which consists of a collection of edge locations

CloudFront - Origin :: Can be S3 Bucket, EC2 Instance, Elastic Load Balancer, Route or a non-AWS origin server

CloudFront - Web Distribution :: Used to serve content over HTTP and HTTPS
The content can be Static or Dynamic, Multi-Media or a Live Event

CloudFront - RTMP Distribution :: Stream media files using Adobe Media Server and the Adobe *Real-Time Messaging Protocol* 
 RTMP. Must use an Amazon S3 bucket as the origin.

CloudFront - Edge :: You can clear the cache on these, but you are subject to charges.

S3 - Bucket - Security :: By Default , When newly created, S3 Bucket __________ is PRIVATE
You can control access to these with; Bucket __________ Policies and ACLs
S3 Bucket __________ can be configured to create access logs for all requests, and the logs can be sent to a different S3 Bucket.

S3 - Encryption - In Transit :: Uses SSL/TLS

SSE-S :: *Server Side Encryption at rest with S3 Managed Keys*

SSE-KMS :: *Server Side Encryption at rest with AWS Key Management Service*
__________ provides an audit trail, so you can see who used your key to access which object and when, as well as view failed attempts to access data from users without permission to decrypt the data.

SSE-C :: *Server Side Encryption at rest with Customer Provided Keys*

S3 - Client Side Encryption :: __________ at rest where data is encrypted on the client side and uploaded to S3.

Storage Gateway - File Gateway :: Uses NFS for storing flat files in S3

Storage Gateway - Volumes Gateway :: Uses iSCSI Uses block storage and is comprised of Stored Volumes and Cached Volumes

Storage Gateway - Tape Gateway :: Uses VTL A backup solution that creates virtual tapes to send to S3
<!--SR:!2024-04-15,3,250-->

Storage Gateway - Volumes Gateway - Stored Volumes :: The Volumes are stored on premise and incremental backups are sent to S3

Storage Gateway - Volumes Gateway - Cached Volumes :: The Volumes are stored primarily on S3, while retaining your most frequently access data on premise.

Snowball :: This is a Petabyte-scale data transport solution that uses secure appliances to transfer larege amounts of data into and out of AWS

Snowball Edge :: Is a TB data tranfer device with on-board storage and compute capabilities. AWS Datacenter in a box

Snowmobile :: For Exabyte-scale data transfers to AWS, you can tranfer upt to 100 PB per Snowmobile

AWS Import/Export :: __________ (deprecated) service would allow customers to ship disks to AWS for import into their account.

S3 - Transfer Acceleration :: Utilizes the CloudFront Edge Network to accelerate your uploads to S3.

EC2 - Instance Type - D :: Specialty - Dense Storage
Use Case - Fileservers
Data Warehousing
Hadoop 

EC2 - Instance Type - R :: Specialty - Memory Optimized
Use Case - Memory Intensive Apps
DBs

EC2 - Instance Type - M :: Specialty - General Purpose
Use Case - Application Servers

EC2 - Instance Type - C :: Specialty - Compute Optimized
Use Case - CPU Intensive Apps
DBs

EC2 - Instance Type - G :: Specialty - Graphics Intensive
Use Case - Video Emcoding
D Application Streaming

EC2 - Instance Type - I :: Specialty - High Speed Storage
Use Case - NoSQL DBs, Data Warehousing etc.

EC2 - Instance Type - F :: Specialty - Field Programmable Gate Array
Use Case - Hardware acceleration for your code.

EC2 - Instance Type - T :: Specialty - Lowest Cost, General Purpose
Use Case - Web Servers
Small DBs

EC2 - Instance Type - P :: Specialty - Graphics, General Purpose
Use Case - Machine Learning, Bit Coin Mining etc.

EC2 - Instance Type - X :: Specialty - Memory Optimized
Use Case - SAP HANA
Apache Spark etc.

Elastic IP :: Limited to 5 per region

EC2 - Selection :: Is based on:
Memory Requirements
Required number of I/O operations

AWS Config :: A service that enables you to assess, audit, and evaluate the configurations of your AWS resources.
Continuously monitors and records your AWS resource configurations and allows you to automate the evaluation of recorded configurations against desired configurations.

RDS - Multi-AZ :: Amazon RDS will automatically provision and manage a "standby" replica in a different Availability Zone (independent infrastructure in a physically separate location).
These deployments utilize synchronous replication, making database writes concurrently on both the primary and standby so that the standby will be up-to-date in the event a fail-over occurs.
With These instances and automated backups, I/O activity is no longer suspended on your primary during your preferred backup window, since backups are taken from the standby.

Uptime SLA for EC2 and EBS :: 99.99%

URL To determine your instance's IPv4 addresses :: http://169.254.169.254/latest/meta-data

S3 - Webpage Redirect :: If your Amazon S3 bucket is configured for website hosting, you can redirect requests for an object to another object in the same bucket or to an external URL.

S3 - Minimum Object Size :: 0 Bytes

True or False: A Placement Group can be stretched across multiple availability zones or peered VPCs :: False

ECS :: *Elastic Container Service*
This is a highly scalable, high-performance container orchestration service that supports Docker containers and allows you to easily run and scale containerized applications on AWS.
Eliminates the need for you to install and operate your own container orchestration software, manage and scale a cluster of virtual machines, or schedule containers on those virtual machines.

True or False: It's possible to have a Multi-AZ copy of your read replica :: False

EFS :: *Elastic File System*
Provides simple, scalable, elastic file storage for use with AWS Cloud services and on-premises resources.
Provides multiple EC2 instances with low-latency, shared access to a fully-managed file system, and is designed to perform well for a wide variety of workloads, with the ability to scale to thousands of concurrent connections.

True or False: Classic ELBs support both IPv4 and IPv6. :: True

True or False: Availability Zones in a given Region are connected by low-latency links, facilitating the development of fault-tolerant, high-availability applications. :: True

True or False: you can write objects directly to an edge location. :: True

RDS - Upgrading :: When upgrading an instance class your database will be temporarily unavailable while the DB Instance Class is modified. This period of unavailability typically lasts only a few minutes, and will occur during the maintenance window for your DB Instance, unless you specify that the modification should be applied immediately.

VPG :: *Virtual Private Gateway*
__________ is the VPN concentrator on the Amazon side of the VPN connection. 
You create a __________ and attach it to the VPC from which you want to create the VPN connection.

Redshift - Enhanced VPC Routing :: Forces all COPY and UNLOAD traffic between your cluster and your data repositories through your Amazon VPC. 
If Enhanced this service is not enabled, Amazon Redshift routes traffic through the Internet, including traffic to other services within the AWS network.

ECS - Tasks :: With IAM roles for this service, you can specify an IAM role that can be used by the containers in a task.
Instead of creating and distributing your AWS credentials to the containers or using the EC2 instance's role, you can associate an IAM role with an this service's definition or RunTask API operation.

Aurora :: This is a fully managed, MySQL- and PostgreSQL-compatible, relational database engine.
It combines the speed and reliability of high-end commercial databases with the simplicity and cost-effectiveness of open-source databases.
It delivers up to five times the throughput of MySQL and up to three times the throughput of PostgreSQL without requiring changes to most of your existing applications.
Amazon __________ does NOT support schema changes.

Aurora - Cluster Endpoint :: A __________ endpoint is an endpoint for an Aurora DB cluster that connects to the current primary instance for that DB cluster. 
Each Aurora DB cluster has a __________ endpoint and one primary instance.

Aurora - Reader Endpoint :: A __________ endpoint is an endpoint for an Aurora DB cluster that connects to one of the available Aurora Replicas for that DB cluster. 
Each Aurora DB cluster has a __________ endpoint. 
If there is more than one Aurora Replica, the __________ endpoint directs each connection request to one of the Aurora Replicas.

Aurora - Instance Endpoint :: An __________ endpoint is an endpoint for a DB instance in an Aurora DB cluster that connects to that specific DB instance. 
Each DB instance in a DB cluster, regardless of instance type, has its own unique __________ endpoint. So, there is one __________ endpoint for the current primary instance of the DB cluster, and there is one __________ endpoint for each of the Aurora Replicas in the DB cluster.

EBS - Provisioned IOPS SSD :: Highest performance SSD volume designed for latency-sensitive transactional workloads.
Used for I/O-intensive NoSQL and relational databases.

EBS - General Purpose SSD :: General Purpose SSD volume that balances price performance for a wide variety of transactional workloads.
Used for Boot volumes, low-latency interactive apps, dev & test

EBS - Throughput Optimized HDD :: Low cost HDD volume designed for frequently accessed, throughput intensive workloads.
Used for Big data, data warehouses, log processing.

EBS - Cold HDD :: Lowest cost HDD volume designed for less frequently accessed workloads.
Used for Colder data requiring fewer scans per day.

S3 - Pre-Signed URLs :: A __________ URL provides access to an object without requiring AWS security credentials or permissions.
When you create a __________ URL, you must provide your security credentials, specify a bucket name, an object key, an HTTP method, and an expiration date and time. 
The pre-signed URL is valid only for the specified duration.

```



```



