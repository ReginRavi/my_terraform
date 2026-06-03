---
layout: default
title: AWS Certified AI Practitioner (AIF-C01) Guide
date: 2026-05-24 02:00:00 +0000
permalink: /2026-05-24-introduction-to-AWS/
categories: AWS
tags: [AWS, AI, Machine-Learning, Certification]
---

# AWS Certified AI Practitioner (AIF-C01)

The **AWS Certified AI Practitioner (AIF-C01)** is a foundational-level certification designed for professionals who want to demonstrate a broad understanding of AI, machine learning (ML), and generative AI (GenAI) on AWS.

It is particularly well-suited for:
* **Non-technical roles** like sales, marketing, and project management.
* **IT professionals** looking to pivot into AI.

---

## Exam Quick Facts

| Feature           | Details                                                                   |
| :---------------- | :------------------------------------------------------------------------ |
| **Exam Code**     | AIF-C01                                                                   |
| **Format**        | 65 questions (Multiple choice, multiple response, matching, and ordering) |
| **Duration**      | 90 minutes                                                                |
| **Cost**          | $100 USD                                                                  |
| **Passing Score** | 700 / 1,000 (Scaled score)                                                |
| **Delivery**      | Online proctored or at a Pearson VUE testing center                       |

---

## Exam Domains & Weighting

The exam is divided into five key domains that cover everything from basic terminology to responsible AI practices:

### 🧠 Domain 1: Fundamentals of AI and ML (20%)
* **Basic terminology** (AI vs. ML vs. Deep Learning).
* **ML pipeline stages** (data prep, training, evaluation, deployment).
* **Identifying business use cases** for AI.

#### AI vs. Machine Learning vs. Deep Learning

The terms Artificial Intelligence, Machine Learning, and Deep Learning are often used interchangeably, but they represent nested subsets of the same field. Think of them like nesting dolls: Deep Learning is a specific type of Machine Learning, which is a specific type of Artificial Intelligence.

* **Artificial Intelligence (AI)**: The broadest category. It refers to any technique that enables computers to mimic human intelligence. This includes everything from simple "if-then" logic to the most complex neural networks.
  * **Key Concept**: The goal is to create systems that can perform tasks normally requiring human intelligence, such as visual perception, speech recognition, and decision-making.
  * **AWS Context**: When you use Amazon Lex to build a chatbot, you are using AI.
* **Machine Learning (ML)**: A subset of AI. Instead of being explicitly programmed with rules (e.g., "If $x$ happens, do $y$"), the system uses algorithms to find patterns in data and make predictions.
  * **Key Concept**: The system "learns" and improves its performance over time as it is exposed to more data.
  * **Example**: A system that looks at thousands of emails to learn the difference between "Spam" and "Not Spam."
  * **AWS Context**: Amazon SageMaker is the primary platform used to build, train, and deploy these ML models.
* **Deep Learning (DL)**: A specialized subset of Machine Learning. It is inspired by the structure of the human brain and uses Artificial Neural Networks with many layers (hence the "deep" in the name).
  * **Key Concept**: DL is exceptionally good at handling unstructured data like images, video, and natural language. While standard ML might need a human to identify "features" (like telling the computer to look for ears/tails to identify a dog), DL can figure those features out on its own.
  * **Example**: Facial recognition software or self-driving car systems.
  * **AWS Context**: Services like Amazon Rekognition (image analysis) use Deep Learning under the hood.

| Feature          | Artificial Intelligence   | Machine Learning                         | Deep Learning                           |
| :--------------- | :------------------------ | :--------------------------------------- | :-------------------------------------- |
| **Scope**        | The overarching field.    | A subset of AI.                          | A subset of ML.                         |
| **Method**       | Mimicking human behavior. | Learning from data patterns.             | Using multi-layered neural networks.    |
| **Data Type**    | Any logic/rules.          | Mostly structured (tables/spreadsheets). | Unstructured (images, voice, text).     |
| **Human Effort** | High (for rule-based AI). | Medium (feature engineering).            | Low (the model finds its own features). |

> **Exam Tip**: If a question asks about "simulating human intelligence," the answer is AI. If it asks about "improving from experience/data," it's ML. If it mentions "neural networks" or "large-scale unstructured data," think Deep Learning.

#### Types of Machine Learning

Machine Learning models learn from data in different ways, primarily categorized into three types:

* **Supervised Learning ("The Teacher")**: In supervised learning, the model is trained on a labeled dataset. This means every input comes with the "correct answer" (the target variable or label).
  * **How it works**: The model learns the relationship between the input features and the labels.
  * **The Goal**: Predict an outcome for new, unseen data.
  * **Two Main Types**:
    * **Classification**: Predicting a category or class (e.g., Is this email "Spam" or "Not Spam"?).
    * **Regression**: Predicting a continuous numerical value (e.g., What will the price of this house be?).
  * **Exam Keyword**: If the question mentions "labels," "historical data with known outcomes," or "predicting a specific value/class," it is almost certainly Supervised Learning.
* **Unsupervised Learning ("The Explorer")**: In unsupervised learning, the model is given unlabeled data. There is no "answer key." The model's job is to look at the data and find internal structures, patterns, or anomalies on its own.
  * **How it works**: It groups similar data points or identifies things that don't belong.
  * **The Goal**: Discover hidden patterns or structures.
  * **Common Techniques**:
    * **Clustering**: Grouping similar items (e.g., Customer segmentation for marketing).
    * **Anomaly Detection**: Identifying outliers (e.g., Detecting fraudulent credit card transactions).
    * **Dimensionality Reduction**: Simplifying data while keeping key information.
  * **Exam Keyword**: If the question mentions "unlabeled data," "grouping," "clustering," or "finding patterns" without specifying an outcome, think Unsupervised Learning.
* **Reinforcement Learning (RL) ("The Agent")**: Reinforcement learning is distinct because it involves an agent interacting with an environment. It learns through a process of trial and error to maximize a cumulative reward.
  * **How it works**: The agent performs an action, receives feedback (reward for good, penalty for bad), and updates its strategy to perform better next time.
  * **The Goal**: Make a sequence of decisions to achieve a long-term objective.
  * **Examples**: Teaching an AI to play a video game, optimizing traffic light timings, or training autonomous vehicles.
  * **Exam Keyword**: Look for terms like "agent," "environment," "reward/penalty," "trial and error," or "sequence of decisions."

| Feature             | Supervised                | Unsupervised                    | Reinforcement         |
| :------------------ | :------------------------ | :------------------------------ | :-------------------- |
| **Data**            | Labeled                   | Unlabeled                       | None (Interaction)    |
| **Key Mechanism**   | Map inputs to labels      | Find hidden structure           | Reward/Penalty loop   |
| **Common Use Case** | Prediction (Churn, Price) | Segmentation, Anomaly Detection | Optimization, Control |

> **Pro-Tip for the Exam**: When you see a scenario-based question, use this simple 3-Step Decision Tree:
> * **Do I have labeled data (correct answers)?** If yes → **Supervised Learning**.
> * **Do I have unlabeled data but need to find groupings/anomalies?** If yes → **Unsupervised Learning**.
> * **Is this about an agent learning by interacting and getting rewards?** If yes → **Reinforcement Learning**.


### 🎨 Domain 2: Fundamentals of Generative AI (24%)
* **Concepts** like tokens, chunking, and embeddings.
* **The lifecycle** of Foundation Models (FMs).
* **Capabilities and limitations** of GenAI (e.g., hallucinations).

### 🚀 Domain 3: Applications of Foundation Models (28%)
* **Model Selection**: Choosing the right pre-trained model based on cost and latency.
* **Prompt Engineering**: Techniques like Zero-shot, Few-shot, etc.
* **Customization**: Methods like RAG (Retrieval-Augmented Generation) and Fine-tuning.

### ⚖️ Domain 4: Guidelines for Responsible AI (14%)
* **Fairness & Transparency**: Addressing bias and ensuring visibility.
* **Human-Centered Design**: Explainability in AI models.

### 🛡️ Domain 5: Security, Compliance, and Governance (14%)
* **AWS Shared Responsibility Model** for AI.
* **Governance protocols** and data privacy in AI solutions.

---

## Target Knowledge & Services

You don’t need to be a coder, but you should be familiar with the **"What"** and **"Why"** of these AWS services:

* 🪨 **Amazon Bedrock**: Building GenAI apps with FMs.
* 🧪 **Amazon SageMaker**: The core platform for building and deploying ML models.
* 🤖 **AWS AI Services**: Pre-built tools including:
  * **Amazon Q**: AI assistant.
  * **Amazon Polly**: Text-to-speech.
  * **Amazon Rekognition**: Image analysis.
  * **Amazon Lex**: Chatbots.

---

## Common AWS Architectural & Migration Patterns

In addition to foundational AI/ML services, a well-rounded AWS practitioner should understand standard cloud architectures, event processing, caching strategies, and database migration workflows.

### 🏛️ Enterprise Application Architecture
A high-level multi-tier enterprise architecture on AWS organizes resources into distinct zones: User Access, Data Ingestion, Application Processing, and Data Persistence.

![Enterprise Application Architecture]({{ "/assets/images/AWS/aws_enterprise_architecture.png" | relative_url }})

* **Zone 1: User Access & Clients**: Employs user devices and web browsers routed securely through Route 53, CloudFront, and Web Application Firewall (WAF).
* **Zone 2: Data Ingestion & Interface**: Utilizes EventBridge, Load Balancers, and EC2 Application Servers.
* **Zone 3: Application Logic & Processing**: Implements API Gateways, microservices, and SQS queues.
* **Zone 4: Data Persistence & Analytics**: Stores data across relational databases (RDS), NoSQL (DynamoDB), session caches (ElastiCache), data lakes (S3), analytics engines (EMR), and data warehouses (Redshift).

---

### ⚡ Serverless Event Processing Workflow
Serverless architectures leverage event-driven components to ingest, route, process, and store streaming data without managing servers.

![Serverless Event Processing Workflow]({{ "/assets/images/AWS/aws_serverless_event_processing.png" | relative_url }})

* **Event Ingestion & Routing**: Uses Amazon EventBridge for event routing and Amazon S3 or Kinesis Data Streams for high-throughput ingestion.
* **Event Processing & Enrichment**: Employs AWS Lambda functions for real-time computation and data processing.
* **Event Consumers & Storage**: Delivers data to SQS/SNS for alerts/consumers, and stores persistent data in Redshift, DynamoDB, or S3.

---

### 💾 AWS Caching Strategies
Caching improves response latency and reduces load on database tiers. Different use cases warrant different caching strategies:

![AWS Caching Strategies]({{ "/assets/images/AWS/aws_caching_strategies.png" | relative_url }})

* **Cache-Aside (Side-Cache)**: The application checks the cache first. On a miss, it queries the database and updates the cache.
* **Read-Through**: The application queries the cache, and the cache automatically fetches from the database on a miss (e.g., DynamoDB Accelerator - DAX).
* **Write-Through**: The application writes to the cache, which synchronously updates the database.
* **Write-Back (Write-Behind)**: The application writes to the cache, which asynchronously batches writes to the database.

---

### 🔄 AWS Database Migration Service (DMS)
AWS DMS helps migrate databases to AWS quickly and securely. It supports both homogeneous (same engine) and heterogeneous (different engine) migrations.

#### DMS Migration Workflow
![AWS DMS Migration Workflow]({{ "/assets/images/AWS/aws_dms_migration_workflow.png" | relative_url }})

1. **Source Data Environments**: Supports homogeneous (RDS PostgreSQL) or heterogeneous (Oracle, SQL Server) source databases.
2. **AWS Replication Engine**: A replication instance processes schema conversion (via SCT) and data migration, using Change Data Capture (CDC) for ongoing replication.
3. **Target Data Environments**: Targets include relational engines (Aurora, Redshift) or NoSQL/Analytics targets (DynamoDB, Kinesis).
4. **Monitoring & Governance**: Integrates with CloudWatch, IAM, and CloudTrail.

#### DMS Monitoring & Alerts Variant
A variation of the DMS workflow tailored for enhanced monitoring and logging:
![AWS DMS Monitoring & Alerts]({{ "/assets/images/AWS/aws_dms_monitoring_alerts.png" | relative_url }})

#### Common DMS Migration Flows
A summary of common end-to-end migration scenarios supported by AWS DMS:
![AWS DMS Migration Flows]({{ "/assets/images/AWS/aws_dms_migration_flows.png" | relative_url }})

---

### 🛡️ AWS Backup Centralized Workflow
AWS Backup provides a fully managed, policy-based service that simplifies backup management at scale, enabling centralized control over backup and restore workflows.

![AWS Backup: Centralized Backup and Restore Workflow]({{ "/assets/images/AWS/aws_backup.png" | relative_url }})

* **Backup Sources**: Supports computing (EC2, EBS), databases (RDS, Aurora, DynamoDB), storage (S3, EFS), on-premises servers (via Storage Gateway), and hybrid environments (SSM, CloudFormation).
* **Central Control**: The AWS Backup Service coordinates definitions, policy execution, scheduling, retention, and auditing.
* **Storage & Recovery**: Backups are secured in encrypted, immutable Backup Vaults, with options for cross-region replication and point-in-time restore (PITR).

---

* Transfer data in single s3 bucket from global – s3 transfer acceleration
* Analyze/query data in s3- amazon athena
* Ec2 private access from vpc to s3- vpc gateway endpoint
* Ebs instance in multi az need storage- EFS
* Transfer large amount data within 2 weeks – months etc- snowball devices
* Decouple application- SQS
* Storage class s3
* Serverless compute- lambda (15 min)
* Serverless microservice architecture- ECS with Fargate
* Need to store key along with automatic rotation- secret manager
* Store static/dynamic global application- cloudfront with s3
* Relational db option for serverless- aurora
* More read needed in RDS- RDS read replica
* Data visualization- amazon quicksight
* Temporary secure access- IAM role
* Virtual firewall appliances- gateway LB
* Connection drain in rds too much load in DB- RDS proxy
* Configuration changes- aws config
* Voice over Internet protocol, UDP- Network Load Balancer, Global accelerator
* Real time, near real time- KDS, KDF
* Amazon Appflow- SaaS to s3
* Amazon AppFlow is an integration service that enables you to securely transfer data between SaaS applications and AWS services without code.
* Security assesment of ec2 instance- AWS Inspector
* Application – image should not have inappropriate content- Amazon Recognition
* ML? UDEMY? Textract, Comprehend, transcribe, translate
* ACM- certificate manager-import the cert SSL/TLS cert
* Hybrid- DC can use VPN backup
* API- SQS- Lambda-Dynamodb
* Retain data 7 years – aws backup
* Amazon FSx read little HPC- Lustre windows ,appl- window
* DDOS- Aws shield
* Sql injection, cross site- WAF
* AWS glue- data integration
* AWS Org- SCP
* Guardials across multiple account- AWS control tower
* S3 object lock- governance (some can access with permission), compliance (no users can access manipulate data)
* SFTP to upload files- aws transfer family
* url swapping, rolling deploy, blue green etc-elastic beanstalk
* aws cognito- user, identity pool
* session data management/cache- elasticache

---

A company runs an environment where data is stored in an Amazon S3 bucket. The objects are accessed frequently throughout the day. The company has strict da ta encryption requirements for data that is stored in the S3 bucket. The company currently uses AWS Key Management Service (AWS KMS) for encryption. The company wants to optimize costs associated with encrypting S3 objects without making additional calls to AWS KMS. Which solution will meet these requirements?

* A. Use server-side encryption with Amazon S3 managed keys (SSE-S3).
* B. Use an S3 Bucket Key for server-side encryption with AWS KMS keys (SSE-KMS) on the new objects.
* C. Use client-side encryption with AWS KMS customer managed keys.
* D. Use server-side encryption with customer-provided keys (SSE-C) stored in AWS KMS.

The correct solution is **B. Use an S3 Bucket Key for server-side encryption with AWS KMS keys (SSE-KMS) on the new objects.**

### Detailed Breakdown of the Answer

To solve this problem, you need to satisfy three conditions:

1. Keep using **AWS KMS** to satisfy strict data encryption requirements.
2. **Optimize costs** associated with data encryption.
3. Reduce/minimize making **additional calls** to AWS KMS.

### Why B is the Correct Choice:

When you use server-side encryption with AWS KMS (SSE-KMS), Amazon S3 normally calls AWS KMS every single time an object is uploaded or downloaded to generate or read a unique data key. For frequently accessed data, these cryptographic api call volumes generate very high AWS KMS request bills.

An **Amazon S3 Bucket Key** acts as a baseline cache directly at the S3 tier. Instead of calling AWS KMS for every object request, S3 creates a temporary bucket-level data key from KMS and caches it locally within the storage architecture. S3 then derives unique object keys from this bucket key.

- **Result:** This configuration cuts down traffic to AWS KMS by up to **99%**, drastically dropping your encryption api request costs without changing your root KMS master keys.

### Why the Other Options are Incorrect:

- **A. Use server-side encryption with Amazon S3 managed keys (SSE-S3):**
    - *Reason:* While this solution is highly cost-effective (it has no API call charges), it completely removes AWS KMS from the loop and uses S3-managed keys instead. This violates the constraint to optimize costs *while continuing to use AWS KMS*.
- **C. Use client-side encryption with AWS KMS customer managed keys:**
    - *Reason:* Moving encryption tasks onto client computing frameworks does not reduce or avoid hitting the AWS KMS endpoint grid. Your client applications would still have to issue active API requests to AWS KMS for every local execution script.
- **D. Use server-side encryption with customer-provided keys (SSE-C) stored in AWS KMS:**
    - *Reason:* This option is conceptually flawed. SSE-C requires *you* to manually send the cryptographic key to Amazon S3 in every single HTTP header request. S3 does not look inside or communicate with AWS KMS on your behalf during an SSE-C operation.

---

An online gaming company is transitioning user data storage to Amazon DynamoDB to support the company's growing user base. The current architecture includes DynamoDB tables that contain user profiles, achievements, and in-game transactions. The company needs to design a robust, continuously available, and resilient DynamoDB architecture to maintain a seamless gaming experience for users. Which solution will meet these requirements MOST cost-effectively?

* A. Create DynamoDB tables in a single AWS Region. Use on-demand capacity mode. Use global tables to replicate data across multiple Regions.
* B. Use DynamoDB Accelerator (DAX) to cache frequently accessed data. Deploy tables in a single AWS Region and enable auto scaling. Configure Cross-Region Replication manually to additional Regions.
* C. Create DynamoDB tables in multiple AWS Regions. Use on-demand capacity mode. Use DynamoDB Streams for Cross-Region Replication between Regions.
* D. Use DynamoDB global tables for automatic multi-Region replication. Deploy tables in multiple AWS Regions. Use provisioned capacity mode. Enable auto scaling.

The correct solution is **D. Use DynamoDB global tables for automatic multi-Region replication. Deploy tables in multiple AWS Regions. Use provisioned capacity mode. Enable auto scaling.**

### Detailed Breakdown of the Solution

To find the best choice, we must address three key requirements: **high availability/resiliency**, **scalability**, and **cost-effectiveness**.

### 1. Resiliency and Availability (Multi-Region)

A "continuously available and resilient" architecture for a growing global user base requires a multi-Region deployment. If one AWS Region goes down, users must be seamlessly rerouted to an active database in another Region with minimal latency.

- **DynamoDB Global Tables** are the AWS-native, best-practice solution for this. They provide fully managed, active-active replication across multiple AWS Regions, ensuring that writes in any Region are automatically replicated to the others.

### 2. Scaling and Cost-Effectiveness (Capacity Mode)

Online gaming workloads typically exhibit highly predictable, cyclical patterns (e.g., traffic surges during evenings and weekends, and drops during late-night hours).

- **Provisioned Capacity Mode with Auto Scaling** dynamically adjusts Read Capacity Units (RCUs) and Write Capacity Units (WCUs) up and down based on the actual traffic curve.
- Compared to *On-Demand Capacity Mode* (which charges a fixed premium flat fee per million requests), provisioned capacity with auto scaling is **significantly more cost-effective** for high-volume, predictable scaling patterns.

### Why the Other Options are Incorrect

- **A. Create DynamoDB tables in a single AWS Region. Use on-demand capacity mode...**
    - *Reason 1:* You cannot build a Global Table out of a single Region; Global Tables must span multiple Regions to provide high availability.
    - *Reason 2:* On-demand capacity mode is much more expensive than provisioned capacity with auto scaling for predictable, high-throughput gaming workloads.
- **B. Use DynamoDB Accelerator (DAX) to cache frequently accessed data... Configure Cross-Region Replication manually...**
    - *Reason 1:* Configuring Cross-Region Replication manually (typically via custom Lambda code and DynamoDB Streams) introduces massive operational overhead, engineering maintenance costs, and potential lag. It defeats the purpose of using fully managed Global Tables.
    - *Reason 2:* DAX adds architectural complexity and cost, and while it helps with read performance, it does not solve write availability across multiple Regions.
- **C. Create DynamoDB tables in multiple AWS Regions. Use on-demand capacity mode. Use DynamoDB Streams...**
    - *Reason 1:* Like Option B, writing custom code via DynamoDB Streams to manage multi-Region replication is error-prone and operationally expensive compared to using native Global Tables.
    - *Reason 2:* It uses the more expensive On-Demand capacity mode.

---

A company is building an application on AWS. The application uses multiple AWS Lambda functions to retrieve sensitive data from a single Amazon S3 bucket for processing. The company must ensure that only authorized Lambda functions can access the data. The solution must comply with the **principle of least privilege**. Which solution will meet these requirements?

* A. Grant full S3 bucket access to all Lambda functions through a shared IAM role.
* B. Configure the Lambda functions to run within a VPC. Configure a bucket policy to grant access based on the Lambda functions' VPC endpoint IP addresses.
* C. Create individual IAM roles for each Lambda function. Grant the **IAM** roles access to the S3 bucket. Assign each IAM role as the Lambda execution role for its corresponding Lambda function.
* D. Configure a bucket policy granting access to the Lambda functions based on their function ARNs.

---

A company needs to design a resilient web application to process customer orders. The web application must automatically handle increases in web traffic and application usage without affecting the customer experience or losing customer orders. Which solution will meet these requirements?

* A. Use a NAT gateway to manage web traffic. Use Amazon EC2 Auto Scaling groups to receive, process, and store processed customer orders. Use an AWS Lambda function to capture and store unprocessed orders.
* B. Use a Network Load Balancer (NLB) to manage web traffic. Use an Application Load Balancer to receive customer orders from the NLUse Amazon Redshift with a Multi-AZ deployment to store unprocessed and processed customer orders.
* C. Use a Gateway Load Balancer (GWLB) to manage web traffic. Use Amazon Elastic Container Service (Amazon ECS) to receive and process customer orders. Use the GWLB to capture and store unprocessed orders. Use Amazon DynamoDB to store processed customer orders.
* D. Use an Application Load Balancer to manage web traffic. Use Amazon EC2 Auto Scaling groups to receive and process customer orders. Use Amazon Simple Queue Service (Amazon SQS) to store unprocessed orders. Use Amazon RDS with a Multi-AZ deployment to store processed customer orders.

The correct solution is **D. Use an Application Load Balancer to manage web traffic. Use Amazon EC2 Auto Scaling groups to receive and process customer orders. Use Amazon Simple Queue Service (Amazon SQS) to store unprocessed orders. Use Amazon RDS with a Multi-AZ deployment to store processed customer orders.**

### Detailed Explanation

To design a system that handles highly fluctuating traffic without dropping data or degrading performance, you must build **horizontal scalability** into your compute tier and introduce an **asynchronous buffer** to protect the ingestion path.

### Why D is the Correct Choice:

This option utilizes a highly available, standard multi-tier design pattern:

1. **Application Load Balancer (ALB):** Acts as a managed proxy tier to absorb and cleanly distribute unpredictable client-side web traffic spikes.
2. **Amazon EC2 Auto Scaling Groups (ASG):** Scales the processing compute capacity up or down dynamically based on custom metrics (like CPU usage or queue depth), optimizing cost and ensuring seamless performance.
3. **Amazon SQS (Decoupling & Protection):** SQS acts as a durable, highly scalable buffer. If your application tier encounters a massive sudden rush of orders that outpaces your compute auto-scaling rate, the orders are held safely inside the message queue. They are never lost and are steadily drained as compute capacity scales up.
4. **Amazon RDS with a Multi-AZ Deployment:** Provides a highly available, robust transactional database layer. Synchronous replication to a standby replica across a separate availability zone guarantees business continuity and data persistence without affecting customer transactions in a failure event.

### Why the Other Options are Incorrect

- **A. Use a NAT gateway to manage web traffic...**
    - *Reason:* A NAT Gateway is strictly used to allow instances in private subnets to establish outbound connectivity to the internet. It cannot receive, intercept, or distribute inbound client web traffic.
- **B. Use a Network Load Balancer... Use Amazon Redshift with a Multi-AZ deployment...**
    - *Reason:* Amazon Redshift is a column-oriented Data Warehouse optimized for deep analytical workloads (OLAP). It is not designed to handle highly frequent, low-latency transactional queries (OLTP) like writing real-time customer retail orders.
- **C. Use a Gateway Load Balancer... Use the GWLB to capture and store unprocessed orders.**
    - *Reason:* A Gateway Load Balancer (GWLB) is specialized for deploying, scaling, and managing third-party virtual network appliances (like firewalls, intrusion detection systems, and deep packet inspection utilities). Furthermore, a load balancer cannot capture, stage, or *store* unprocessed data packets. Caching or storing unprocessed messages requires a messaging queue engine like Amazon SQS or Amazon MQ.

---

A company is migrating from a monolithic architecture for a web application that is hosted on Amazon EC2 to a serverless microservices architecture. The company wants to use AWS services that support an event-driven, loosely coupled architecture. The company wants to use the publish/subscribe (pub/sub) pattern. Which solution will meet these requirements MOST cost-effectively?

* A. Configure an Amazon API Gateway REST API to invoke an AWS Lambda function that publishes events to an Amazon Simple Queue Service (Amazon SQS) queue. Configure one or more subscribers to read events from the SQS queue.
* B. Configure an Amazon API Gateway REST API to invoke an AWS Lambda function that publishes events to an Amazon Simple Notification Service (Amazon SNS) topic. Configure one or more subscribers to receive events from the SNS topic.
* C. Configure an Amazon API Gateway WebSocket API to write to a data stream in Amazon Kinesis Data Streams with enhanced fan-out. Configure one or more subscribers to receive events from the data stream.
* D. Configure an Amazon API Gateway HTTP API to invoke an AWS Lambda function that publishes events to an Amazon Simple Notification Service (Amazon SNS) topic. Configure one or more subscribers to receive events from the topic.

The correct solution is **D. Configure an Amazon API Gateway HTTP API to invoke an AWS Lambda function that publishes events to an Amazon Simple Notification Service (Amazon SNS) topic. Configure one or more subscribers to receive events from the topic.**

### Detailed Breakdown of the Solution

To choose the best answer, the solution must meet three requirements: implement a **serverless microservices architecture**, use a **publish/subscribe (pub/sub) pattern**, and do so **MOST cost-effectively**.

### 1. Meeting the Publish/Subscribe (Pub/Sub) Requirement

In a pub/sub pattern, a publisher broadcasts an event once, and multiple independent subscribers automatically intercept it.

- **Amazon SNS (Simple Notification Service)** is the core AWS serverless service built explicitly for the pub/sub model. Publishers push events to an SNS *Topic*, which then instantly duplicates and fan-outs the payload out to multiple downstream subscribers (such as AWS Lambda functions, SQS queues, or HTTP endpoints).
- **Why Option A is incorrect:** Amazon SQS is a *message queue* built for **point-to-point decoupling**, not broad pub/sub fan-out. A message in an SQS queue can only be pulled and successfully processed by **one subscriber**. Once a subscriber processes and deletes it, it vanishes from the queue.

### 2. Evaluating Cost-Effectiveness (HTTP APIs vs. REST APIs)

Amazon API Gateway offers both **REST APIs** and **HTTP APIs**.

- **HTTP APIs** are designed explicitly to offer minimal features at lower costs. They are up to **70% cheaper** and offer lower latency compared to standard API Gateway REST APIs, making them the most cost-effective solution for simple proxy forwarding to AWS Lambda.
- This optimization instantly makes **Option D superior to Option B**.

### Why the Other Options are Incorrect

- **A. Configure an Amazon API Gateway REST API... publishes events to an Amazon SQS queue...**
    - *Reason:* As noted above, SQS follows a point-to-point model where messages are consumed by a single subscriber. It does not natively support broadcasting or a pub/sub pattern. Additionally, REST APIs are more expensive than HTTP APIs.
- **B. Configure an Amazon API Gateway REST API... publishes events to an Amazon SNS topic...**
    - *Reason:* While this successfully builds a pub/sub architecture using SNS, it relies on API Gateway **REST APIs**. Since the requirement specifies the *most cost-effective* solution, Option D wins because HTTP APIs are significantly cheaper.
- **C. Configure an Amazon API Gateway WebSocket API to write to a data stream in Amazon Kinesis Data Streams...**
    - *Reason 1:* A Kinesis Data Stream with enhanced fan-out is optimized for high-throughput, sequential real-time data ingestion and analytics streaming. It is significantly more expensive and architecturally heavy compared to a basic serverless SNS pub/sub setup.
    - *Reason 2:* WebSocket APIs maintain persistent, two-way state connections, which are cost-inefficient and unnecessary for generic microservice event publishing.

---

A company needs to grant a team of developers access to the company's AWS resources. The company must maintain a high level of security for the resources. The company requires an access control solution that will prevent unauthorized access to the sensitive data. Which solution will meet these requirements?

* A. Share the IAM user credentials for each development team member with the rest of the team to simplify access management and to streamline development workflows.
* B. Define IAM roles that have fine-grained permissions based on the principle of least privilege. Assign an IAM role to each developer.
* C. Create IAM access keys to grant programmatic access to AWS resources. Allow only developers to interact with AWS resources through API calls by using the access keys.
* D. Create an AWS Cognito user pool. Grant developers access to AWS resources by using the user pool.

The correct answer is **B. Define IAM roles that have fine-grained permissions based on the principle of least privilege. Assign an IAM role to each developer.**

### Detailed Breakdown of the Answer

To choose the correct solution, you must satisfy two primary constraints: **maintain a high level of security** and **prevent unauthorized access to sensitive data** by developers accessing corporate AWS resources.

### Why B is the Correct Choice:

- **The Principle of Least Privilege:** This foundational cybersecurity standard ensures identities are only given the baseline, minimum permissions required to perform their discrete technical jobs. By creating specific AWS Identity and Access Management (IAM) policies with fine-grained restrictions (e.g., granting read access only to specific S3 data paths or blocking write permissions on production databases), the threat vector of accidental or malicious data modification is contained.
- **IAM Roles:** Assigning developers specific permissions via IAM Roles allows the team to securely authenticate. If a team member changes positions or leaves the company, fine-grained access parameters can be cleanly modified or revoked centrally without changing global configuration items.

### Why the Other Options are Incorrect

- **A. Share the IAM user credentials for each development team member with the rest of the team...**
    - *Reason:* Sharing credentials completely eliminates individual **accountability** and audit tracking. If sensitive database layers are altered or corrupted, CloudTrail logs will only display the shared user identifier, making it impossible to establish which employee initiated the changes. This is a severe threat to basic operational compliance.
- **C. Create IAM access keys to grant programmatic access... Allow only developers to interact... through API calls...**
    - *Reason:* Long-lived programmatic IAM Access Keys (`AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`) represent a major security vulnerability if they are hardcoded into application repositories, leaked, or exposed on developer machines. Relying exclusively on access keys for direct engineer interactions violates best practices, which favor using short-lived temporary security credentials.
- **D. Create an AWS Cognito user pool. Grant developers access to AWS resources...**
    - *Reason:* **Amazon Cognito User Pools** are designed to provide Authentication and Authorization frameworks for *external end-users* of consumer-facing web or mobile applications (e.g., customer logins for a retail site). It is not intended for managing infrastructure access control permissions for a corporate engineering team, which is exclusively the domain of IAM and AWS IAM Identity Center.

---

A company is building a web application that serves a content management system. The content management system runs on Amazon EC2 instances behind an Application Load Balancer (ALB). The EC2 instances run in an Auto Scaling group across multiple Availability Zones. Users are constantly adding and updating files, blogs, and other website assets in the content management system. A solutions architect must implement a solution in which all the EC2 instances share up-to-date website content with the least possible lag time. Which solution meets these requirements?

* A. Update the EC2 user data in the Auto Scaling group lifecycle policy to copy the website assets from the EC2 instance that was launched most recently. Configure the ALB to make changes to the website assets only in the newest EC2 instance.
* B. Copy the website assets to an Amazon Elastic File System (Amazon EFS) file system. Configure each EC2 instance to mount the EFS file system locally. Configure the website hosting application to reference the website assets that are stored in the EFS file system.
* C. Copy the website assets to an Amazon S3 bucket. Ensure that each EC2 instance downloads the website assets from the S3 bucket to the attached Amazon Elastic Block Store (Amazon EBS) volume. Run the S3 sync command once each hour to keep files up to date.
* D. Restore an Amazon Elastic Block Store (Amazon EBS) snapshot with the website assets. Attach the EBS snapshot as a secondary EBS volume when a new EC2 instance is launched. Configure the website hosting application to reference the website assets that are stored in the secondary EBS volume.

The correct answer is **B. Copy the website assets to an Amazon Elastic File System (Amazon EFS) file system. Configure each EC2 instance to mount the EFS file system locally. Configure the website hosting application to reference the website assets that are stored in the EFS file system.**

### Detailed Explanation

To support a distributed environment where users are **constantly updating assets** (files, blogs, images) on a traditional CMS app like WordPress or Drupal running across an Auto Scaling group, the underlying storage tier must natively support **shared concurrent file access** with the **least possible lag time**.

### Why B is the Correct Choice:

- **Simultaneous Read/Write Filesystem:** **Amazon EFS** is a managed, POSIX-compliant file system that allows hundreds of Amazon EC2 instances to mount the exact same storage target concurrently across multiple Availability Zones.
- **Zero Caching Lag:** When a user uploads a blog asset onto EC2 Instance A, Instance A writes that asset directly into the mounted EFS volume. Because the filesystem is shared globally in real time, EC2 Instance B can instantly read, populate, and display that new file to another user without any file synchronization scripts or delay. This fulfills the requirement for the *least possible lag time*.

### Why the Other Options are Incorrect

- **A. Update the EC2 user data... to copy website assets from the EC2 instance that was launched most recently...**
    - *Reason:* EC2 User Data scripts **only execute once** during an instance's initial boot cycle. They cannot handle continuous, real-time file additions or modifications generated by users throughout the day. Pinning modifications strictly to a single instance breaks load balancing logic.
- **C. Copy the website assets to an Amazon S3 bucket... Run the S3 sync command once each hour...**
    - *Reason:* While using an Amazon S3 bucket for central asset storage is an architecture pattern, setting an `aws s3 sync` cron job to run **once each hour** introduces up to **60 minutes of latency (lag)** before other instances fetch updates. This explicitly violates the requirement to share up-to-date content with the *least possible lag time*.
- **D. Restore an Amazon Elastic Block Store (Amazon EBS) snapshot... Attach it as a secondary volume...**
    - *Reason:* Amazon EBS volumes are strictly block-level devices designed to be attached to a **single EC2 instance** at a time (outside of specialized cluster filesystems using multi-attach). Furthermore, snapshots are static point-in-time backups; they cannot dynamically capture or stream subsequent file mutations written by web applications in real time.

---

A company's near-real-time streaming application is running on AWS. As the data is ingested, a job runs on the data and takes 30 minutes to complete. The workload frequently experiences high latency due to large amounts of incoming data. A solutions architect needs to design a scalable and serverless solution to enhance performance. Which combination of steps should the solutions architect take? (Choose two.)

* A. Use Amazon Kinesis Data Firehose to ingest the data.
* B. Use AWS Lambda with AWS Step Functions to process the data.
* C. Use AWS Database Migration Service (AWS DMS) to ingest the data.
* D. Use Amazon EC2 instances in an Auto Scaling group to process the data.
* E. Use AWS Fargate with Amazon Elastic Container Service (Amazon ECS) to process the data.

The correct solutions are **A. Use Amazon Kinesis Data Firehose to ingest the data** and **E. Use AWS Fargate with Amazon Elastic Container Service (Amazon ECS) to process the data.**

### Detailed Explanation

To solve this problem, you must construct a pipeline that satisfies three rigid constraints:

1. Natively supports a **near-real-time streaming ingestion** pattern.
2. Accommodates a long-running data processing task that takes **30 minutes to complete**.
3. Delivers a **scalable and serverless** operational architecture to eliminate ingestion latency bottlenecks.

### Step 1: Ingesting Stream Data Serverlessly (Option A)

- **Amazon Kinesis Data Firehose** is a fully managed, serverless streaming ingestion service. It scales automatically to handle massive spikes in incoming data volume without requiring manual provisioning. It can capture, transform, and continuously load streaming data directly into downstream analytics engines or storage targets (such as Amazon S3 or Amazon OpenSearch Service).
- **Why Option C is incorrect:** AWS Database Migration Service (AWS DMS) is designed to migrate relational databases, data warehouses, and NoSQL stores to the AWS Cloud. It is not an ingestion service meant for near-real-time application event streaming.

### Step 2: Processing the Long-Running Job Serverlessly (Option E)

- The prompt states that the processing job **takes 30 minutes to complete**. This constraint is critical because standard AWS Lambda functions have a **hard timeout limit of 15 minutes**. Because of this, Lambda cannot be used directly to run this job, eliminating *Option B*.
- **AWS Fargate** paired with **Amazon ECS** is the ideal serverless alternative. Fargate abstracts away the underlying EC2 instance management entirely (making it serverless), while allowing containerized processing tasks to run **indefinitely without a 15-minute execution limit**. It can dynamically scale out the number of container tasks to process high-volume streams, successfully reducing latency.
- **Why Option D is incorrect:** While an EC2 Auto Scaling group can easily run a 30-minute processing script, it requires you to choose, patch, maintain, and manage the underlying virtual servers. This directly violates the constraint to choose a **serverless** solution.

### Why the Other Options are Incorrect

- **B. Use AWS Lambda with AWS Step Functions to process the data.**
    - *Reason:* As noted above, an individual AWS Lambda invocation will abruptly time out after 15 minutes. While Step Functions can orchestrate complex workflows, breaking a continuous 30-minute streaming data compute block into multiple 15-minute chunks adds unnecessary architectural complexity compared to a standard containerized job on Fargate.
- **C. Use AWS Database Migration Service (AWS DMS) to ingest the data.**
    - *Reason:* This tool is meant for data warehouse and relational database migrations (like moving an on-premises Oracle database to Amazon RDS). It cannot capture real-time streaming application payloads.
- **D. Use Amazon EC2 instances in an Auto Scaling group to process the data.**
    - *Reason:* EC2 instances are non-serverless infrastructure components. You are fully responsible for OS updates, security patches, and monitoring server scale.

---

A company wants to enhance its ecommerce order-processing application that is deployed on AWS. The application must process each order exactly once without affecting the customer experience during unpredictable traffic surges. Which solution will meet these requirements?

* A. Create an Amazon Simple Queue Service (Amazon SQS) FIFO queue. Put all the orders in the SQS queue. Configure an AWS Lambda function as the target to process the orders.
* B. Create an Amazon Simple Notification Service (Amazon SNS) standard topic. Publish all the orders to the SNS standard topic. Configure the application as a notification target.
* C. Create a flow by using Amazon AppFlow. Send the orders to the flow. Configure an AWS Lambda function as the target to process the orders.
* D. Configure AWS X-Ray in the application to track the order requests. Configure the application to process the orders by pulling the orders from Amazon CloudWatch.

The correct solution is **A. Create an Amazon Simple Queue Service (Amazon SQS) FIFO queue. Put all the orders in the SQS queue. Configure an AWS Lambda function as the target to process the orders.**

### Detailed Breakdown of the Solution

To choose the optimal solution, the architecture must fulfill two critical business constraints: **process each order exactly once** and protect the system during **unpredictable traffic surges without affecting user experience**.

### 1. Processing Exactly Once (Idempotency and De-duplication)

- **Amazon SQS FIFO (First-In-First-Out) queues** are specifically engineered to provide **exactly-once processing**. They natively prevent duplicate entries using a transaction *Message Deduplication ID*. If a transient network glitch causes the frontend application to submit the same order twice within a 5-minute window, the SQS FIFO engine automatically filters out the duplicate.

### 2. Managing Traffic Surges (Decoupling and Buffering)

- Placing an asynchronous queue between your frontend order ingestion and your backend database functions introduces a **durable buffer**.
- During a sudden surge in order volumes, incoming customer transactions are staged safely in the SQS FIFO queue. This decouples the workload, meaning traffic surges do not overwhelm backend dependencies.
- SQS then invokes your serverless **AWS Lambda** processing targets up to defined concurrency thresholds. This ensures the app processes every single order smoothly without crashing or dropping user requests.

### Why the Other Options are Incorrect

- **B. Create an Amazon Simple Notification Service (Amazon SNS) standard topic...**
    - *Reason:* An SNS **Standard** topic follows an *at-least-once* delivery model, which explicitly means messages can occasionally be duplicated. Furthermore, standard topics do not support deduplication logic, which fails the requirement to process each order *exactly once*.
- **C. Create a flow by using Amazon AppFlow...**
    - *Reason:* **Amazon AppFlow** is a fully managed integration service designed to securely transfer data between Software-as-a-Service (SaaS) cloud applications (like Salesforce, Zendesk, or Slack) and AWS storage targets (like Amazon S3 or Redshift). It is not designed to act as a real-time transactional message broker or buffer for an internal e-commerce order-processing application.
- **D. Configure AWS X-Ray... Configure the application to process the orders by pulling the orders from Amazon CloudWatch.**
    - *Reason 1:* **AWS X-Ray** is a distributed debugging and tracing tool used to visualize application latency maps and log microservice call paths. It has no data-buffering capabilities and cannot store order payloads.
    - *Reason 2:* **Amazon CloudWatch** is an infrastructure monitoring and logging service. It gathers operational metrics, system events, and log files. It cannot act as a message queue backend to store, transition, or execute customer retail transactions.

---

A development team uses multiple AWS accounts for its development, staging, and production environments. Team members have been launching large Amazon EC2 instances that are underutilized. A solutions architect must prevent large instances from being launched in all accounts. How can the solutions architect meet this requirement with the LEAST operational overhead?

* A. Update the IAM policies to deny the launch of large EC2 instances. Apply the policies to all users.
* B. Define a resource in AWS Resource Access Manager that prevents the launch of large EC2 instances.
* C. Create an IAM role in each account that denies the launch of large EC2 instances. Grant the developers IAM group access to the role.
* D. Create an organization in AWS Organizations in the management account with the default policy. Create a service control policy (SCP) that denies the launch of large EC2 instances, and apply it to the AWS accounts.

The correct answer is **D. Create an organization in AWS Organizations in the management account with the default policy. Create a service control policy (SCP) that denies the launch of large EC2 instances, and apply it to the AWS accounts.**

### Detailed Explanation

The objective is to restrict specific actions (preventing the launch of oversized, underutilized Amazon EC2 instances) across **multiple AWS accounts** simultaneously while ensuring the solution requires the **LEAST operational overhead**.

### Why D is the Correct Choice:

- **Centralized Governance:** **AWS Organizations** allows you to consolidate and manage multiple AWS accounts from a single management console.
- **Service Control Policies (SCPs):** SCPs are a type of organization policy that you can use to manage permissions in your organization. An SCP acts as a global guardrail or maximum permission boundary. By writing a single policy that denies `ec2:RunInstances` for specific instance types (e.g., `m5.24xlarge`, `r5.metal`) and attaching it to the root of the Organization or an Organizational Unit (OU), you instantly enforce this rule across **all** linked development, staging, and production accounts.
- **Overriding Root Permissions:** SCPs override even full root/admin (`"*"`) permissions inside the member accounts. This single policy solves the multi-account constraint centrally, minimizing overhead.

### Why the Other Options are Incorrect

- **A. Update the IAM policies to deny the launch of large EC2 instances. Apply the policies to all users.**
    - *Reason:* Because the development team uses *multiple standalone AWS accounts*, a solutions architect would have to log into each account individually, locate every developer user/group/role, and manually attach the policy. Furthermore, standard IAM policies do not restrict the account's local **Root user**. This introduces high operational overhead and leaves a security gap.
- **B. Define a resource in AWS Resource Access Manager that prevents the launch of large EC2 instances.**
    - *Reason:* **AWS Resource Access Manager (AWS RAM)** is explicitly used to safely share specific AWS resources (such as VPC Subnets, Transit Gateways, or Route 53 Resolver rules) across accounts within an organization. It does not possess any authorization guardrails or policy engines capable of enforcing EC2 instance size limitations.
- **C. Create an IAM role in each account that denies the launch of large EC2 instances...**
    - *Reason:* IAM roles are built to *allow* permissions when assumed, so structuring a role strictly to *deny* an action is architecturally incorrect. Even if implemented via custom permission boundaries, configuring this on a role-by-role basis across every separate corporate environment creates massive operational overhead and does not restrict users who bypass that specific role.

---

A company hosts its application in the AWS Cloud. The application runs on Amazon EC2 instances in an Auto Scaling group behind an Elastic Load Balancing (ELB) load balancer. The application connects to an Amazon DynamoDB table.

For disaster recovery (DR) purposes, the company wants to ensure that the application is available from another AWS Region with minimal downtime. Which solution will meet these requirements with the LEAST downtime?

* A. Create an Auto Scaling group and an ELB in the DR Region. Configure the DynamoDB table as a global table. Configure DNS failover to point to the new DR Region's ELB.
* B. Create an AWS CloudFormation template to create EC2 instances, ELBs, and DynamoDB tables to be launched when necessary. Configure DNS failover to point to the new DR Region's ELB.
* C. Create an AWS CloudFormation template to create EC2 instances and an ELB to be launched when necessary. Configure the DynamoDB table as a global table. Configure DNS failover to point to the new DR Region's ELB.
* D. Create an Auto Scaling group and an ELB in the DR Region. Configure the DynamoDB table as a global table. Create an Amazon CloudWatch alarm with an evaluation period of 10 minutes to invoke an AWS Lambda function that updates Amazon Route 53 to point to the DR Region's ELB.

The correct solution is **A. Create an Auto Scaling group and an ELB in the DR Region. Configure the DynamoDB table as a global table. Configure DNS failover to point to the new DR Region's ELB.**

### Detailed Breakdown of the Solution

To design an optimal cross-Region Disaster Recovery (DR) solution, the architecture must satisfy the constraint of providing **minimal downtime** (achieving a low Recovery Time Objective, or RTO).

### Why A is the Correct Choice:

This option sets up a **Warm Standby** or **Active-Active** strategy, which provides the absolute fastest recovery time during a regional outage.

1. **Pre-provisioned Infrastructure:** Having the Auto Scaling group and Elastic Load Balancer (ELB) already running in the DR Region means there is no lag time waiting for infrastructure to spin up or containers to initialize.
2. **DynamoDB Global Tables:** Global Tables provide fully managed, active-active cross-region replication. Your data is already present and continuously synchronized in the secondary Region, resulting in a backup data latency of under a second.
3. **Route 53 DNS Failover:** Amazon Route 53 health checks continuously monitor the primary Region's ELB. If the primary region goes offline, Route 53 automatically detects the failure and updates the DNS record to point to the pre-warm DR region's load balancer. This automated switchover happens within minutes, resulting in the **least possible downtime**.

### Why the Other Options are Incorrect

- **B & C. Create an AWS CloudFormation template to be launched when necessary...**
    - *Reason:* These options describe a **Pilot Light** or **Backup & Restore** strategy. Waiting for a disaster to hit before triggering CloudFormation to deploy network stacks, register target configurations, spin up virtual machines, and complete boot orchestration scripts (`User Data`) takes a significant amount of time. This introduces substantial downtime and fails the requirement for *minimal downtime*. (Additionally, Option B doesn't sync the database ahead of time, potentially leading to catastrophic data loss).
- **D. ...Create an Amazon CloudWatch alarm with an evaluation period of 10 minutes to invoke an AWS Lambda function...**
    - *Reason:* Relying on a CloudWatch alarm with a **10-minute evaluation period** introduces an intentional 10-minute delay *before the system even detects* that an outage has occurred. Furthermore, writing custom Lambda code to modify Route 53 resource records is less resilient and operationally heavier than using Route 53's native, fully automated health check DNS failover routing policies.

---

A company uses Amazon S3 to host its static website. The company wants to add a contact form to the webpage. The contact form will have dynamic server-side components for users to input their name, email address, phone number, and user message. The company expects fewer than 100 site visits each month. The contact form must notify the company by email when a customer fills out the form. Which solution will meet these requirements MOST cost-effectively?

* A. Host the dynamic contact form in Amazon Elastic Container Service (Amazon ECS). Set up Amazon Simple Email Service (Amazon SES) to connect to a third-party email provider.
* B. Create an Amazon API Gateway endpoint that returns the contact form from an AWS Lambda function. Configure another Lambda function on the API Gateway to publish a message to an Amazon Simple Notification Service (Amazon SNS) topic.
* C. Host the website by using AWS Amplify Hosting for static content and dynamic content. Use server-side scripting to build the contact form. Configure Amazon Simple Queue Service (Amazon SQS) to deliver the message to the company.
* D. Migrate the website from Amazon S3 to Amazon EC2 instances that run Windows Server. Use Internet Information Services (IIS) for Windows Server to host the webpage. Use client-side scripting to build the contact form. Integrate the form with Amazon WorkMail.

The correct solution is **B. Create an Amazon API Gateway endpoint that returns the contact form from an AWS Lambda function. Configure another Lambda function on the API Gateway to publish a message to an Amazon Simple Notification Service (Amazon SNS) topic.**

### Detailed Explanation

To solve this scenario, the architecture must implement **dynamic server-side component processing**, establish an automated **email notification system**, and run **MOST cost-effectively** for an incredibly small scale (**fewer than 100 site visits each month**).

### Why B is the Correct Choice:

This solution leverages a 100% **serverless execution model**, which is the most optimal choice for handling ultra-low, intermittent traffic volumes economically.

1. True Pay-As-You-Go Billing:services like Amazon API Gateway, AWS Lambda, and Amazon SNS charge strictly based on precise request volumes. Under the standard AWS Free Tier, 100 invocations a month cost **$0.00**. Even out of free tier windows, 100 requests will compute to fractions of a single cent.
2. **Server-Side Form Processing:** When a user interacts with the webpage assets hosted on Amazon S3 and fills out the contact form, a quick script issues an API post request down to your **Amazon API Gateway** endpoint. API Gateway intercepts the payload and passes it to a backend **AWS Lambda** function. Lambda securely parses the form inputs (name, email, phone, message) using dynamic server-side logic.
3. **Automated Notification Delivery:** The processing Lambda function then takes the parsed string variables and publishes them into an **Amazon SNS (Simple Notification Service)** topic. Since you can natively configure an email address as a structural protocol subscriber to an SNS topic, SNS automatically packages the form inputs and fires off a notification directly to the company inbox.

### Why the Other Options are Incorrect

- **A. Host the dynamic contact form in Amazon Elastic Container Service (Amazon ECS)...**
    - *Reason:* Running an Amazon ECS microservices container (even using AWS Fargate task provisioning) means you are continuously paying for the memory and CPU compute footprints allocated to host that active listener task 24/7. Paying to keep a container running continuously just to intercept fewer than 100 requests a month generates massive **unnecessary idle cost overhead**.
- **C. Host the website by using AWS Amplify Hosting... Configure Amazon Simple Queue Service (Amazon SQS) to deliver...**
    - *Reason:* An Amazon Simple Queue Service (SQS) resource is a *message buffering queue* intended for point-to-point decoupling between compute microservices. SQS **cannot send, package, or deliver emails** to an end-user or corporate team inbox. Sending an email from a queue structure requires attaching an active polling engine (like Lambda) linked to an email relay node (like SES).
- **D. Migrate the website from Amazon S3 to Amazon EC2 instances... Integrate the form with Amazon WorkMail.**
    - *Reason:* Migrating an entirely static asset bucket out of S3 onto a fleet of **Amazon EC2 virtual instances running Windows Server with IIS** represents a completely backwards architectural design anti-pattern. This structure reintroduces heavy administrative patching overhead and requires paying a high, fixed monthly server instance fee alongside specialized Microsoft OS licensing bills—completely destroying any concept of cost-efficiency for 100 monthly visits.

---

The correct answers are:

- **A. Configure the security group for the web tier to allow inbound HTTPS traffic from the security group for the ALB.**
- **C. Configure the security group for the database tier to allow inbound Microsoft SQL Server traffic from the security group for the application tier.**
- **E. Configure the security group for the application tier to allow inbound HTTPS traffic from the security group for the web tier.**

### Detailed Architectural Breakdown

To enforce a high level of security based on the **principle of least privilege**, security group rules must reflect a strict, linear flow of traffic. Each tier should only accept inbound connections explicitly coming from the immediately preceding tier's security group.

Furthermore, because security groups in AWS are **stateful**, if you permit an inbound request, the corresponding outbound response is automatically allowed at the tracking layer. Specifying outbound rules back to web layers for transaction traffic is unnecessary and incorrect.

Here is how the chained security group structure passes validation:

### 1. Public Entry to Web Tier (Option A)

- Inbound client web traffic hits the internet-facing Application Load Balancer (ALB).
- To restrict the web tier so it cannot bypass the ALB or accept rogue public connection attempts, the **Web Tier Security Group** must only accept inbound traffic (on Port 443/HTTPS) where the **Source is explicitly the ALB's Security Group**.

### 2. Web Tier to Application Tier (Option E)

- The presentation web tier routes dynamic computational requests down into the business logic layer.
- To ensure data integrity, the **Application Tier Security Group** should tightly lock down its boundaries to allow inbound traffic (typically HTTPS Port 443) **only if the Source is the Web Tier's Security Group**.

### 3. Application Tier to Database Tier (Option C)

- The business logic handles transaction requests and queries the relational storage tier.
- For maximum protection of sensitive records, the **Database Tier Security Group** must block all outside environments and only allow inbound Microsoft SQL Server traffic (on Port 1433) **when the Source is the Application Tier's Security Group**.

### Why the Other Options are Incorrect

- **B. Configure the security group for the web tier to allow outbound HTTPS traffic to 0.0.0.0/0.**
    - *Reason:* Opening wide outbound routes to the entire internet (`0.0.0.0/0`) from your core system layers creates a data exfiltration vector. If a bad actor compromises a web instance, wide-open outbound rules allow data to be quietly streamed out to external servers. It violates the priority of strict least-privilege security.
- **D & F. Outbound configurations back to preceding tiers (Database to Web / App to Web).**
    - *Reason:* As noted, AWS security groups are **stateful**. When the Application tier successfully queries the Database, the SQL Server instance can natively return the data payload back over the same connection without needing an explicit outbound rule. Attempting to open explicit outbound ports back up the tier chain is structurally redundant and unnecessarily widens the attack surface.
