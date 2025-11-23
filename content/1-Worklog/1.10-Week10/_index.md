---
title: "Week 10 Worklog"
date: "`r Sys.Date()`"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---



### Week 10 Objectives:

* Deploy and manage applications with Red Hat OpenShift Service on AWS (ROSA) and implement a basic CI/CD workflow.
* Build and analyze an analytics platform on AWS using streaming ingestion, Glue, EMR, Athena, QuickSight, and Redshift.
* Create business dashboards and monitor network and account activity with Amazon QuickSight, VPC Flow Logs, and delegated billing access.
* Develop and deploy cloud applications using AWS CDK, event-driven architectures with SNS/SQS, and Lambda-based serverless patterns.
* Build serverless web application stacks with API Gateway, Lambda, DynamoDB, Cognito, and CloudFront, including SSL and authentication.
* Implement order processing and CI/CD pipelines for serverless applications using SQS, SNS, SAM, and CodePipeline.

### Tasks carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- |-----------------| ----------------------------------------- |
| 2   | - **Deploy Applications with Red Hat OpenShift Service on AWS (ROSA)** <br>&emsp; + Enable ROSA and install the necessary command-line tools <br>&emsp; + Create and configure an OpenShift cluster on AWS <br>&emsp; + Deploy a sample application onto the OpenShift cluster <br>&emsp; + Set up a basic CI/CD workflow using CodeCommit, CodeBuild, and CodePipeline <br>&emsp; + Configure a CI/CD workflow specifically for the application deployment <br><br> - **Build an Analytics Platform on AWS** <br>&emsp; + Ingest and store streaming data using Amazon Kinesis Firehose <br>&emsp; + Catalog data using AWS Glue Crawlers to populate the Glue Data Catalog <br>&emsp; + Transform data using AWS Glue interactive sessions, Glue Studio, and DataBrew <br>&emsp; + Process large-scale data with Amazon EMR <br>&emsp; + Analyze data interactively with Amazon Athena and in real-time with Kinesis Data Analytics <br>&emsp; + Visualize data by creating dashboards in Amazon QuickSight <br>&emsp; + Serve data using AWS Lambda and build a data warehouse with Amazon Redshift | 11/10/2025 | 11/10/2025      | ROSA Hands-on Lab: <br> <https://000071.awsstudygroup.com/> <br> Analytics Platform: <br> <https://000072.awsstudygroup.com/> |
| 3   | - **Getting Started with Amazon QuickSight** <br>&emsp; + Prepare data and build an initial dashboard with various chart types like line charts, pie charts, and pivot tables <br>&emsp; + Enhance the dashboard by applying formatting, adding new visuals, and including detailed data tables <br>&emsp; + Create an interactive dashboard by configuring filters, filter actions, and navigation actions before publishing <br><br> - **Monitor Network Infrastructure with VPC Flow Logs** <br>&emsp; + Create and enable VPC Flow Logs to capture IP traffic information for a VPC <br>&emsp; + Publish flow log data to Amazon CloudWatch Logs <br>&emsp; + Monitor and analyze the collected network traffic data to diagnose security group rules and understand traffic patterns <br><br> - **Delegate Access to the AWS Billing Console** <br>&emsp; + Create an IAM user group and enable access to the billing console <br>&emsp; + Define a custom IAM policy to grant specific billing and cost management permissions <br>&emsp; + Attach the policy to the IAM user group to delegate access <br>&emsp; + Test the configured permissions by having a user from the group access the billing console | 11/11/2025 | 11/11/2025      | Amazon QuickSight Guide: <br> <https://000073.awsstudygroup.com/> <br> VPC Flow Logs Lab: <br> <https://000074.awsstudygroup.com/> <br> AWS Billing Console: <br> <https://000075.awsstudygroup.com/> |
| 4   | - **Develop an Application using AWS CDK** <br>&emsp; + Set up the environment by creating an IAM Role and launching an EC2 instance <br>&emsp; + Configure the development environment using VSCode <br>&emsp; + Use CDK to create an application architecture with API Gateway, ELB, and ECS <br>&emsp; + Integrate Lambda and S3 into the architecture <br>&emsp; + Implement nested stacks for better organization and reusability <br><br> - **Build an Event-driven Architecture with SNS and SQS** <br>&emsp; + Deploy the necessary infrastructure and configure an event generator <br>&emsp; + Implement a simple publish/subscribe model using an SNS topic and an SQS queue <br>&emsp; + Apply message filtering to an SNS subscription to route specific messages <br>&emsp; + Use advanced message filtering techniques to handle more complex routing logic <br><br> - **Develop a Serverless Application with AWS Lambda** <br>&emsp; + Create a Lambda function for image processing triggered by S3 events <br>&emsp; + Set up an S3 bucket and an IAM policy for the Lambda function <br>&emsp; + Test the Lambda function's operations for image resizing <br>&emsp; + Create a DynamoDB table to store data <br>&emsp; + Write data to the DynamoDB table using a Lambda function | 11/12/2025 | 11/12/2025      | AWS CDK Development: <br> <https://000076.awsstudygroup.com/> <br> Event-driven Architecture Lab: <br> <https://000077.awsstudygroup.com/> <br> Serverless Lambda Guide: <br> <https://000078.awsstudygroup.com/> |
| 5   | - **Build a Serverless Frontend to Call API Gateway** <br>&emsp; + Deploy the front-end application <br>&emsp; + Create a DynamoDB table <br>&emsp; + Deploy Lambda functions for writing, listing, and deleting items <br>&emsp; + Configure API Gateway methods and enable CORS <br>&emsp; + Test the APIs using Postman and the front-end <br><br> - **Deploy a Serverless Application with SAM** <br>&emsp; + Deploy the front-end application <br>&emsp; + Create a DynamoDB table <br>&emsp; + Deploy Lambda functions for listing, writing, deleting, and resizing images <br>&emsp; + Configure GET, POST, and DELETE methods in API Gateway <br>&emsp; + Test the APIs using Postman and the front-end <br><br> - **Implement Serverless Authentication with Amazon Cognito** <br>&emsp; + Create a Cognito User Pool <br>&emsp; + Create an API and a corresponding Lambda function <br>&emsp; + Test the authentication flow with a front-end application <br><br> - **Configure SSL for a Serverless Application** <br>&emsp; + Create a domain and a Route 53 hosted zone <br>&emsp; + Request an SSL certificate using AWS Certificate Manager <br>&emsp; + Create a CloudFront distribution to serve the application over HTTPS | 11/13/2025 | 11/13/2025      | Serverless Frontend with API Gateway: <br> <https://000079.awsstudygroup.com/> <br> Serverless Application with SAM: <br> <https://000080.awsstudygroup.com/> <br> Cognito Authentication Lab: <br> <https://000081.awsstudygroup.com/> <br> SSL Configuration: <br> <https://000082.awsstudygroup.com/> |
| 6   | - **Implement Order Processing with SQS and SNS** <br>&emsp; + Create an SQS queue and an SNS topic <br>&emsp; + Create a DynamoDB table for orders <br>&emsp; + Develop Lambda functions for checking out, managing, handling, and deleting orders <br>&emsp; + Test the order processing flow <br><br> - **Build a CI/CD Pipeline for a Serverless Application** <br>&emsp; + Create a Git repository for the SAM pipeline <br>&emsp; + Configure a SAM pipeline with AWS CodePipeline <br>&emsp; + Create a Git repository for the front-end <br>&emsp; + Build a pipeline for the front-end deployment <br>&emsp; + Test the web application's functionality | 11/14/2025 | 11/14/2025      | Order Processing with SQS and SNS: <br> <https://000083.awsstudygroup.com/> <br> CI/CD Pipeline for Serverless: <br> <https://000084.awsstudygroup.com/> |


### Week 10 Achievements:

* Deployed applications with Red Hat OpenShift Service on AWS by enabling ROSA, provisioning a cluster, deploying a sample workload, and wiring a basic CI/CD workflow using CodeCommit, CodeBuild, and CodePipeline.

* Built and explored an analytics platform on AWS:
  * Ingested streaming data with Kinesis Firehose and cataloged it using AWS Glue Crawlers.
  * Transformed and processed data with Glue (Studio and interactive sessions), DataBrew, EMR, and analyzed it with Athena and Kinesis Data Analytics.
  * Visualized insights in QuickSight dashboards and served data with Lambda and Redshift-based warehousing.

* Created visualizations and improved observability:
  * Designed interactive QuickSight dashboards with multiple chart types, formatting, filters, and navigation.
  * Enabled and reviewed VPC Flow Logs in CloudWatch Logs to understand traffic patterns and validate security group behavior.
  * Delegated access to the AWS Billing Console via IAM groups and custom billing policies, then verified the delegated access.

* Developed infrastructure and applications with AWS CDK and event-driven patterns:
  * Set up a CDK development environment on EC2 with VSCode, IAM roles, and used CDK to define architectures with API Gateway, ELB, ECS, Lambda, and S3.
  * Implemented SNS + SQS event-driven flows, including basic pub/sub and advanced message filtering.
  * Created Lambda-based image processing and data persistence workflows integrated with S3 and DynamoDB.

* Built serverless application stacks end-to-end:
  * Deployed front-end applications that call API Gateway, backed by Lambda and DynamoDB, using both manual setup and SAM.
  * Configured API Gateway methods with CORS, implemented Cognito-based authentication, and tested flows from the front end and with tools like Postman.
  * Secured serverless applications with custom domains, Route 53 hosted zones, ACM certificates, and CloudFront distributions over HTTPS.

* Implemented order processing and automation for serverless workloads:
  * Built an order processing pipeline using SQS, SNS, DynamoDB, and multiple Lambda functions to handle checkout, management, and deletion flows.
  * Set up CI/CD pipelines for SAM-based backends and front-end applications with CodePipeline, connecting them to Git repositories and validating successful deployments.

