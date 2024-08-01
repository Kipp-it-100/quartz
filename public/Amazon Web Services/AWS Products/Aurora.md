---
icon: AiAurora
aliases:
- Amazon Aurora
---
# Overview
Amazon Aurora is a **MySQL and PostgreSQL**-compatible **relational database** built for the cloud, that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases.

- Compatible API for PostgreSQL/ MySQL
- Storage and compute are **seperated** 
	- Storage
		- data is stored in 6 replicas, across 3 AZ
			- Highly available
			- Self-healing
			- auto-scaling
	- Compute
		- Cluster of DB instance across multiple AZ optional
		- auto-scaling of Read Replicas
- Cluster: 
	- Custom endpoints for writer and reader DB instances
- Security
	- Same security/ monitoring/ maintenence features as [[Relational Database Service|RDS]]
- Backup and restore
	- **know these fore exam!!!**
- Aurora Serverless
	- For unpredicatable/ intermittent workloads
	- no capacity planning
- Aurora Global:
	- up to 16 DB Read instances in each region where database 
	- **sub-second** storage replication
- Aurora Machine Learning
	- perform ML using [[SageMaker]] and Comprehend on Aurora
- Aurora database cloning
	- new cluster from existing one
		- faster than restoring from snapshot
- Use case
	- Same as RDS but with: 
	- less maintenance
	- more flexibility
	- more performance
	- more features
	- 


## Aurora with multi-master cluster

Amazon Aurora (Aurora) is a fully managed relational database engine that's compatible with MySQL and PostgreSQL. With some workloads, Aurora can deliver up to five times the throughput of MySQL and up to three times the throughput of PostgreSQL without requiring changes to most of your existing applications. In a multi-master cluster, all DB instances have read/write capability. Currently, all DB instances in a multi-master cluster must be in the same AWS Region. You can't enable cross-Region replicas from multi-master clusters.

### Aurora Replica
- Aurora Replicas have two main purposes.
	- Issue queries to them to scale the read operations for your application
		- Typically do so by connecting to the reader endpoint of the cluster.
			- This allows for spreading the load for read-only connections across as many Aurora Replicas as you have in the cluster.
	- Increase availability
		- If a writer instance in cluster becomes unavailable, Aurora automatically promotes one of the reader instances to take its place as a new writer
Up to 15 Aurora replicas can be distributed across the AZs that a DB cluster spans within an AWS Region
#### Exam Alerts
#flashcards/saa 
- If you see a sentence pertaining to sub-second cross-region replication for your database, it is a hint to use... :: Global [[Aurora]]
<!--SR:!2024-06-18,1,150-->

#saa_exam_alerts 
#### Keywords
- sub-second latency as it regards storage replication can indicate Aurora Global
- 

