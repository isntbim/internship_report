---
title: "Week 9 Worklog"
date: "r Sys.Date()"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---



### Week 9 Objectives:

* Design and integrate conversational and event-driven components using Amazon Lex and Amazon SNS.
* Work with managed data and caching services such as DynamoDB and ElastiCache, and automate deployments for EKS-based workloads.
* Apply governance and scalability practices through Service Quotas, IAM-based usage controls, and EKS Blueprints.
* Build and operate serverless and containerized applications, and evaluate storage performance across S3 and EFS.
* Implement S3 security controls and build a basic data lake pipeline using Glue, Athena, and QuickSight.

### Tasks carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |------------|-----------------| ----------------------------------------- |
| 2   | - **Configure an Amazon Lex Chatbot** <br>&emsp; + Deploy the base application and necessary APIs for the chatbot <br>&emsp; + Create a new chatbot instance in Amazon Lex <br>&emsp; + Enhance the chatbot's functionality and conversational flow <br>&emsp; + Develop a Lambda function to handle the bot's fulfillment logic <br>&emsp; + Publish the chatbot to make it available for use <br> - **Implement a Publish/Subscribe Messaging Model with Amazon SNS** <br>&emsp; + Deploy the initial infrastructure using a SAM template <br>&emsp; + Create an Amazon SNS Topic to handle message publication <br>&emsp; + Develop a customer notification service to subscribe to the topic <br>&emsp; + Create a customer accounting service as another subscriber <br>&emsp; + Implement an "extraordinary rides" service with message filtering <br>&emsp; + Update the primary management service to publish messages to the SNS topic <br>&emsp; + Test the fan-out functionality and message filtering rules | 11/03/2025 | 11/03/2025      | Amazon Lex Chatbot: <br> <https://000058.awsstudygroup.com/> <br> Messaging with Amazon SNS: <br> <https://000059.awsstudygroup.com/> |
| 3   | - **Work with Amazon DynamoDB** <br>&emsp; + Create a table and perform basic data operations like write, read, and update <br>&emsp; + Query data from the table <br>&emsp; + Create and query a Global Secondary Index <br>&emsp; + Manage a table using AWS CloudShell <br>&emsp; + Interact with DynamoDB using Python, covering operations like creating tables, managing data, and performing queries and scans <br> - **Work with Amazon ElastiCache for Redis** <br>&emsp; + Create an ElastiCache subnet group <br>&emsp; + Create an ElastiCache cluster with both cluster mode disabled and enabled <br>&emsp; + Grant access and connect to a cluster node <br>&emsp; + Use the AWS SDK to connect to an ElastiCache cluster <br>&emsp; + Perform data operations using the AWS SDK, such as get/set strings, manage hashes, use publish/subscribe, and interact with streams <br> - **Build a CI/CD Pipeline for an EKS Cluster** <br>&emsp; + Prepare the environment with an IAM User, a Cloud9 workspace, and install Kubernetes tools <br>&emsp; + Configure an IAM role for the EKS cluster <br>&emsp; + Create an EKS cluster and test the deployment of a sample application <br>&emsp; + Set up AWS CodePipeline and CodeBuild with necessary service roles and permissions <br>&emsp; + Create a pipeline to automate the deployment process from a source code repository <br>&emsp; + Test the CI/CD pipeline by making a code change | 11/04/2025 | 11/04/2025      | Amazon DynamoDB Workshop: <br> <https://000060.awsstudygroup.com/> <br> Amazon ElastiCache Workshop: <br> <https://000061.awsstudygroup.com/> <br> EKS CI/CD Workshop: <br> <https://000062.awsstudygroup.com/> |
| 4   | - **Manage Service Quotas** <br>&emsp; + View and manage service quotas from a central location <br>&emsp; + Request a service quota increase through the Service Quotas console <br> - **Implement Resource Usage and Cost Management with IAM** <br>&emsp; + Create IAM groups and users for managing access <br>&emsp; + Apply a policy to restrict resource creation by AWS Region <br>&emsp; + Implement a policy to limit the allowed EC2 instance families <br>&emsp; + Update policies to restrict allowed EC2 instance sizes <br>&emsp; + Create and assign a policy to limit the types of EBS volumes that can be created <br> - **Deploy and Manage an EKS Cluster using EKS Blueprints** <br>&emsp; + Prepare the environment by creating a VPC, an EC2 instance, and installing necessary tools <br>&emsp; + Configure an IAM role for the EKS Blueprints setup <br>&emsp; + Create an EKS Blueprints and a CDK project <br>&emsp; + Build a deployment pipeline to create and manage the cluster <br>&emsp; + Manage team access to the cluster using Infrastructure as Code (IaC) <br>&emsp; + Configure and test add-ons such as the Cluster Autoscaler <br>&emsp; + Deploy workloads to the cluster using ArgoCD | 11/05/2025 | 11/05/2025      | Service Quotas Workshop: <br> <https://000063.awsstudygroup.com/> <br> IAM Resource Management: <br> <https://000064.awsstudygroup.com/> <br> EKS Blueprints Workshop: <br> <https://000065.awsstudygroup.com/> |
| 5   | - **Build a Serverless Web Application using Lambda and API Gateway** <br>&emsp; + Create a Cloud9 instance and a CodeCommit repository for the project <br>&emsp; + Deploy the frontend application using AWS Amplify Console <br>&emsp; + Deploy the backend infrastructure, including Lambda functions and an API Gateway <br>&emsp; + Populate a DynamoDB table with sample data <br>&emsp; + Implement a system for handling ride times with backend and frontend deployments <br>&emsp; + Develop a photo processing system using Lambda for chroma keying and photo-compositing <br> - **Transition a Monolithic Application to Microservices using Docker and AWS Fargate** <br>&emsp; + Create a CloudFormation stack and set up the environment <br>&emsp; + Containerize a monolithic application using Docker <br>&emsp; + Deploy the containerized application using AWS Fargate <br>&emsp; + Configure an Application Load Balancer and an ECS Service <br>&emsp; + Create a new task definition revision and update the ECS service <br>&emsp; + Build a Docker image for a new microservice and create its task definition and ECS service <br> - **Evaluate Storage Performance on AWS** <br>&emsp; + Launch a CloudFormation template and configure security groups <br>&emsp; + Connect to an EC2 instance for testing <br>&emsp; + Optimize S3 throughput and test sync commands for efficient data transfer <br>&emsp; + Analyze and optimize S3 performance for small file and copy operations <br>&emsp; + Optimize EFS IOPS and evaluate the impact of I/O size and sync frequency <br>&emsp; + Investigate the effects of multi-threading on EFS performance | 11/06/2025 | 11/06/2025      | Serverless Web Application: <br> <https://000066.awsstudygroup.com/> <br> Microservices with Fargate: <br> <https://000067.awsstudygroup.com/> <br> Storage Performance Evaluation: <br> <https://000068.awsstudygroup.com/> |
| 6   | - **Implement S3 Security Best Practices** <br>&emsp; + Launch a CloudFormation template and secure network access <br>&emsp; + Generate access keys and connect to an EC2 instance <br>&emsp; + Require HTTPS and SSE-S3 encryption for data in transit and at rest <br>&emsp; + Block public ACLs and configure S3 Block Public Access settings <br>&emsp; + Restrict access to an S3 VPC Endpoint <br>&emsp; + Use AWS Config to detect public buckets <br>&emsp; + Utilize Amazon Access Analyzer for S3 <br> - **Build a Data Lake with Your Data** <br>&emsp; + Create a Cloud9 instance and prepare a dataset for upload to S3 <br>&emsp; + Use AWS DataBrew for data profiling, cleaning, and transformation <br>&emsp; + Ingest data with AWS Glue by configuring roles and creating a data catalog <br>&emsp; + Transform data to Parquet format <br>&emsp; + Query data using Amazon Athena with basic and advanced queries like joins and views <br>&emsp; + Visualize data with Amazon QuickSight by connecting datasets and building a dashboard | 11/07/2025 | 11/07/2025      | S3 Security Best Practices: <br> <https://000069.awsstudygroup.com/> <br> Data Lake Workshop: <br> <https://000070.awsstudygroup.com/> |


### Week 9 Achievements:

* Designed conversational and messaging workflows by configuring an Amazon Lex chatbot, wiring Lambda for fulfillment, and implementing a publish/subscribe model with Amazon SNS and multiple subscriber services.

* Worked with managed data and cache services:
  * Practiced core DynamoDB operations, Global Secondary Indexes, CloudShell table management, and Python-based interactions.
  * Created and connected to ElastiCache for Redis clusters, using the SDK to perform operations such as strings, hashes, publish/subscribe, and streams.

* Automated Kubernetes-based deployments by provisioning EKS clusters, configuring IAM roles, and building CI/CD pipelines with CodePipeline and CodeBuild to deploy sample applications from source changes.

* Applied governance and quota management:
  * Reviewed and adjusted AWS Service Quotas for capacity needs.
  * Implemented IAM policies to control resource usage by Region, EC2 instance family/size, and EBS volume types.

* Used EKS Blueprints and Infrastructure as Code to prepare networking, configure cluster roles, manage team access, and deploy add-ons like Cluster Autoscaler and workloads via ArgoCD.

* Built and evaluated application architectures:
  * Developed a serverless web application using Lambda, API Gateway, DynamoDB, Amplify, and CodeCommit, including ride time handling and photo processing flows.
  * Transitioned a monolithic application to microservices with Docker and AWS Fargate, fronted by an Application Load Balancer and ECS services.

* Analyzed storage performance on AWS by testing S3 throughput and sync patterns, exploring small-file operations, and tuning EFS IOPS, I/O size, sync frequency, and multi-threading impact.

* Strengthened S3 security posture:
  * Enforced HTTPS and SSE-S3 encryption, blocked public access via ACLs and Block Public Access, and restricted traffic to an S3 VPC Endpoint.
  * Used AWS Config and Access Analyzer to detect and review potentially public or misconfigured buckets.

* Built a simple data lake workflow by staging data in S3, transforming it with DataBrew and Glue into Parquet, querying with Athena, and creating visualizations in QuickSight.
