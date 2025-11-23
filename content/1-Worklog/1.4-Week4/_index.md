---
title: "Week 4 Worklog"
date: "'r Sys.Date() '"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---



### Week 4 Objectives:

* Learn to configure Amazon RDS databases with VPC setup, security groups, and backup operations.
* Study scalable web application deployment using Auto Scaling Groups and Application Load Balancers.
* Understand monitoring techniques with CloudWatch metrics, logs, alarms, and dashboards.
* Explore hybrid DNS solutions using Route 53 Resolver for enterprise networking.
* Develop AWS CLI skills for automated resource management across S3, EC2, VPC, and IAM.
* Practice building CI/CD pipelines with CodeCommit, CodeBuild, CodeDeploy, and CodePipeline.
* Implement automated backup strategies using AWS Backup with lifecycle policies.
* Learn containerized application deployment with Docker on AWS and container registries.
* Study VM migration workflows including import/export operations between environments.
* Build serverless applications using AWS Lambda and API Gateway with IAM configuration.
* Understand security monitoring using AWS Security Hub with multi-service integration.

### Tasks carried out this week:
| Day | Task                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Start Date | Completion Date | Reference Material                                                                                                                                                                     |
| --- |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| ---------- |-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 2   | - **Configure and Manage a Relational Database with Amazon RDS:** <br>&emsp; + Create a VPC, security groups for EC2 and RDS, and a DB subnet group <br>&emsp; + Launch an EC2 instance and create an RDS database instance <br>&emsp; + Deploy a sample application on the EC2 instance to connect to the RDS database <br>&emsp; + Perform backup and restore operations for the RDS instance <br>&emsp; + Practice resource cleanup by deleting the created resources <br><br> - **Deploy and configure a scalable web application using Auto Scaling:** <br>&emsp; + Set up the necessary network infrastructure, including a VPC, subnets, and security groups <br>&emsp; + Create an EC2 Launch Template to define the configuration for new instances <br>&emsp; + Configure a Target Group and an Application Load Balancer to manage and distribute incoming traffic <br>&emsp; + Create and configure an Auto Scaling Group to automatically manage the number of EC2 instances <br>&emsp; + Test various scaling solutions, including manual, scheduled, and dynamic scaling policies <br>&emsp; + Clean up all created AWS resources to avoid ongoing charges <br><br> - **Monitor and Analyze AWS Resources with CloudWatch:** <br>&emsp; + Explore and analyze metrics from various AWS services using search and math expressions <br>&emsp; + Investigate and query log data using CloudWatch Logs Insights <br>&emsp; + Create a Metric Filter to extract data from log events for monitoring <br>&emsp; + Configure a CloudWatch Alarm to trigger notifications based on a specific metric threshold <br>&emsp; + Build a custom CloudWatch Dashboard to visualize key metrics and alarms <br>&emsp; + Perform a cleanup of all created resources, including alarms and dashboards  | 29/09/2025 | 29/09/2025      | Amazon RDS: <br> <https://000005.awsstudygroup.com/> <br> Auto Scaling Group: <br> <https://000006.awsstudygroup.com/> <br> CloudWatch Metrics <br> <https://000008.awsstudygroup.com/> |
| 3   | - **Implement a Hybrid DNS Solution with Route 53 Resolver:** <br>&emsp; + Prepare the lab environment by deploying foundational infrastructure using a CloudFormation template <br>&emsp; + Deploy a Microsoft Active Directory instance to simulate an on-premises DNS server <br>&emsp; + Create a Route 53 Resolver outbound endpoint to forward DNS queries from the VPC <br>&emsp; + Configure Route 53 Resolver rules to direct DNS queries to the appropriate resolver <br>&emsp; + Set up a Route 53 Resolver inbound endpoint to allow the on-premises network to query VPC resources <br>&emsp; + Test the hybrid DNS name resolution and then clean up all deployed resources <br><br> - **Manage AWS Services using the Command Line Interface (CLI):** <br>&emsp; + Install and configure the AWS CLI with an access key, secret key, and default region <br>&emsp; + Practice using the CLI to view and describe resources in various services like S3, SNS, and IAM <br>&emsp; + Perform Amazon S3 operations, such as creating buckets and managing objects, via the command line <br>&emsp; + Create and manage VPC components, including an Internet Gateway, using CLI commands <br>&emsp; + Launch, describe, and terminate an Amazon EC2 instance entirely from the command line <br>&emsp; + Clean up all resources created during the lab to avoid incurring costs | 30/09/2025 | 30/09/2025      | Route 53 Resolver: <br> <https://cloudjourney.awsstudygroup.com/> <br> AWS CLI: <br> <https://000011.awsstudygroup.com/>                                                               |
| 4   | - **Build a CI/CD Pipeline to Automate Application Deployment:** <br>&emsp; + Create a version control repository using AWS CodeCommit to store the application's source code <br>&emsp; + Configure a build project with AWS CodeBuild to compile, test, and package the application <br>&emsp; + Set up a deployment group and application in AWS CodeDeploy to manage the deployment process <br>&emsp; + Create a unified CI/CD pipeline with AWS CodePipeline to orchestrate the entire workflow <br>&emsp; + Test the end-to-end pipeline by pushing a code change and verifying the automated deployment <br>&emsp; + Clean up all AWS resources created during the lab to avoid unnecessary charges <br><br> - **Automate EC2 Instance Backups with AWS Backup:** <br>&emsp; + Deploy the necessary infrastructure, including a new VPC and an EC2 instance, using a CloudFormation template <br>&emsp; + Create a backup plan in AWS Backup to define backup frequency, retention policies, and lifecycle rules <br>&emsp; + Configure notification settings to receive alerts on the status of backup jobs <br>&emsp; + Test the backup and restore process to ensure data can be successfully recovered <br>&emsp; + Clean up all resources, including the CloudFormation stack and any created backups | 01/10/2025 | 01/10/2025      | AWS IAM Identity Center: <br> <https://000012.awsstudygroup.com/> <br> AWS Backup: <br> <https://000013.awsstudygroup.com/>                                                            |
| 5   | - **Deploy a Dockerized Application on AWS:** <br>&emsp; + Configure the necessary AWS infrastructure, including a VPC, security groups, and IAM roles <br>&emsp; + Launch an Amazon RDS instance to serve as the application's database <br>&emsp; + Set up an EC2 instance and install the required dependencies for running the application <br>&emsp; + Deploy and test the application on the EC2 instance using a Docker image <br>&emsp; + Redeploy the application using Docker Compose to manage multiple containers <br>&emsp; + Push the Docker image to a container registry, such as Amazon ECR or Docker Hub <br>&emsp; + Clean up all created AWS resources to avoid incurring further charges <br><br> - **Migrate a Virtual Machine to and from AWS:** <br>&emsp; + Export a virtual machine from an on-premises environment <br>&emsp; + Upload the exported virtual machine image to an Amazon S3 bucket <br>&emsp; + Import the virtual machine from S3 into AWS to create a new Amazon Machine Image (AMI) <br>&emsp; + Deploy a new EC2 instance from the imported AMI <br>&emsp; + Export an existing EC2 instance back to an S3 bucket <br>&emsp; + Clean up all created resources, including the S3 bucket and EC2 instance | 02/10/2025 | 02/10/2025      | Docker on AWS: <br> <https://000015.awsstudygroup.com/> <br> VM Import/Export: <br> <https://000014.awsstudygroup.com/>                                                                |
| 6   | - **Deploy a Serverless Application with Lambda and API Gateway:** <br>&emsp; + Prepare and zip the Lambda deployment package, ensuring it includes the function's source code and all required dependencies <br>&emsp; + Define and create an IAM role with the necessary execution permissions and a trust policy that allows Lambda to assume the role <br>&emsp; + Create the Lambda function in the AWS Console, specifying the runtime and uploading the zipped deployment package <br>&emsp; + Build an HTTP API endpoint using Amazon API Gateway and configure its integration to invoke the Lambda function <br>&emsp; + Deploy the API Gateway to a stage and test the end-to-end serverless application by accessing the public URL <br>&emsp; + Clean up all associated resources, including the API Gateway, the Lambda function, and the IAM role, to prevent ongoing costs <br><br> - **Aggregate and Prioritize Security Findings with AWS Security Hub:** <br>&emsp; + Enable AWS Security Hub to begin aggregating security data from various AWS services <br>&emsp; + Review the integrated dashboard to visualize security alerts and findings <br>&emsp; + Organize and prioritize security detections from services like Amazon GuardDuty, Inspector, and Macie <br>&emsp; + Explore the summarized risks presented in interactive charts and tables | 03/10/2025 | 03/10/2025      | AWS Lambda: <br> <https://000016.awsstudygroup.com/> <br> AWS Security Hub: <br> <https://000018.awsstudygroup.com/> |


### Week 4 Achievements:

* Successfully configured and managed Amazon RDS databases:
  * VPC setup with security group configuration
  * DB subnet group creation and EC2-RDS integration
  * Application deployment with database connectivity
  * Backup and restore operations implementation

* Deployed scalable web applications using Auto Scaling infrastructure:
  * Network infrastructure setup with VPC, subnets, and security groups
  * EC2 Launch Template configuration for standardized instances
  * Application Load Balancer and Target Group implementation
  * Auto Scaling Group configuration with scaling policies

* Implemented comprehensive monitoring with CloudWatch services:
  * Metrics exploration using search and math expressions
  * Log data analysis with CloudWatch Logs Insights
  * Custom alarm configuration with notification thresholds
  * Interactive dashboard development for visualization

* Configured hybrid DNS solutions using Route 53 Resolver:
  * CloudFormation-based infrastructure deployment
  * Microsoft Active Directory integration for simulation
  * Outbound and inbound endpoint configuration
  * Bidirectional name resolution testing

* Developed AWS CLI proficiency for automated resource management:
  * CLI installation and configuration with access credentials
  * Multi-service resource management (S3, SNS, IAM)
  * S3 operations including bucket and object management
  * EC2 instance lifecycle management through CLI

* Built automated CI/CD pipelines using AWS developer services:
  * Version control repository setup with AWS CodeCommit
  * Build project configuration with AWS CodeBuild
  * Deployment automation using AWS CodeDeploy
  * End-to-end pipeline orchestration with CodePipeline

* Implemented automated backup strategies with AWS Backup:
  * Infrastructure deployment using CloudFormation templates
  * Backup plan creation with lifecycle policies
  * Notification configuration for backup job monitoring
  * Disaster recovery testing through backup processes

* Deployed containerized applications using Docker on AWS:
  * AWS infrastructure configuration including VPC and IAM roles
  * RDS database integration for containerized applications
  * Docker image deployment and testing on EC2 instances
  * Container registry operations with Amazon ECR

* Completed VM migration workflows between environments:
  * Virtual machine export from on-premises systems
  * S3-based image storage and transfer operations
  * VM import processes for AMI creation
  * EC2 instance deployment from imported images

* Built serverless applications using AWS Lambda and API Gateway:
  * Lambda deployment package preparation and configuration
  * IAM role creation with execution permissions
  * Function deployment and runtime configuration
  * API Gateway endpoint creation and Lambda integration

* Configured centralized security monitoring with AWS Security Hub:
  * Security Hub enablement for multi-service data aggregation
  * Dashboard utilization for security alert visualization
  * Security finding organization from GuardDuty, Inspector, and Macie
  * Risk analysis using interactive charts and tables
