---
title: "Week 5 Worklog"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---



### Week 5 Objectives:

* Implement advanced AWS networking with VPC Peering and Transit Gateway for multi-VPC connectivity.
* Deploy full-stack applications using EC2, RDS, Auto Scaling, and CloudFront integration.
* Create serverless cost optimization solutions with AWS Lambda for automated EC2 management.
* Build CI/CD pipelines using AWS Developer Tools for automated application deployment.
* Configure hybrid cloud storage with AWS Storage Gateway for on-premises integration.
* Manage enterprise file systems with Amazon FSx and secure web applications using AWS WAF.
* Organize AWS resources effectively using Tags and Resource Groups for governance.
* Develop proficiency with both AWS Management Console and CLI operations.

### Tasks carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                                                                                                                 |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- |------------------------------------------------------------------------------------------------------------------------------------|
| 2   | - **Set up VPC Peering between two VPCs:** <br>&emsp; + Initialize CloudFormation Template to create the initial environment <br>&emsp; + Create Security Groups to control traffic to the EC2 instances <br>&emsp; + Create EC2 instances in each VPC for testing connectivity <br>&emsp; + Update Network ACLs to allow traffic between the peered VPCs <br>&emsp; + Create and accept the VPC Peering connection <br>&emsp; + Configure Route Tables to direct traffic between the peered VPCs <br>&emsp; + Enable Cross-Peer DNS for name resolution between VPCs <br><br> - **Implement a scalable network architecture with AWS Transit Gateway:** <br>&emsp; + Generate a Key Pair for secure access to instances <br>&emsp; + Initialize the environment using a CloudFormation Template <br>&emsp; + Create a Transit Gateway to act as a central network hub <br>&emsp; + Attach VPCs to the Transit Gateway to enable communication <br>&emsp; + Configure Transit Gateway Route Tables to control traffic flow <br>&emsp; + Update VPC Route Tables to route traffic through the Transit Gateway <br>&emsp; | 10/06/2025 | 10/06/2025      | VPC Peering: <br> <https://000019.awsstudygroup.com/> <br> AWS Transit Gateway: <br> <https://000020.awsstudygroup.com/>           |
| 3   | - **Deploy WordPress on AWS Cloud:** <br>&emsp; + Prepare VPC and Subnets for the network infrastructure <br>&emsp; + Create Security Groups for EC2 and Database instances to control access <br>&emsp; + Launch an EC2 instance to host the WordPress application <br>&emsp; + Launch a Database instance using Amazon RDS for the WordPress database <br>&emsp; + Install and configure WordPress on the EC2 instance <br>&emsp; + Implement Auto Scaling for the WordPress instance <br>&emsp; + Perform database backup and restore operations <br>&emsp; + Set up CloudFront for the web server to improve performance and security <br><br> - **Optimize EC2 Costs with Lambda:** <br>&emsp; + Create tags for EC2 instances to identify them for cost optimization <br>&emsp; + Create an IAM Role for the Lambda function to grant necessary permissions <br>&emsp; + Create a Lambda function to automatically stop and start EC2 instances <br>&emsp; + Test the Lambda function to ensure it is working correctly | 10/07/2025 | 10/07/2025      | WordPress on AWS: <br> <https://000021.awsstudygroup.com/> <br> Lambda Cost Optimization: <br> <https://000022.awsstudygroup.com/> |
| 4   | - **Automate Application Deployment with CI/CD Pipeline:** <br>&emsp; + Prepare the necessary resources for the CI/CD pipeline <br>&emsp; + Install and configure the CodeDeploy Agent on the EC2 instances <br>&emsp; + Create a CodeCommit repository to store the application source code <br>&emsp; + Configure CodeBuild to compile and build the application <br>&emsp; + Set up CodeDeploy to automate the deployment process <br>&emsp; + Create a CodePipeline to orchestrate the entire CI/CD workflow <br>&emsp; + Troubleshoot any issues that may arise during the pipeline execution <br><br> - **Utilize AWS Storage Gateway for hybrid cloud storage:** <br>&emsp; + Create an S3 Bucket to store data in the cloud <br>&emsp; + Set up an EC2 instance to host the Storage Gateway <br>&emsp; + Create a Storage Gateway to connect on-premises environments with AWS storage <br>&emsp; + Create File Shares on the Storage Gateway for file-based access <br>&emsp; + Mount the File Shares on an on-premises machine to access cloud storage | 10/08/2025 | 10/08/2025      | AWS CodePipeline: <br> <https://000023.awsstudygroup.com/> <br> Storage Gateway: <br> <https://000024.awsstudygroup.com/> |
| 5   | - **Manage Amazon FSx for Windows File Server:** <br>&emsp; + Create the initial environment for the file server <br>&emsp; + Create both SSD and HDD Multi-AZ file systems <br>&emsp; + Create new file shares on the file systems <br>&emsp; + Test and monitor the performance of the file systems <br>&emsp; + Enable data deduplication and shadow copies for storage optimization and data protection <br>&emsp; + Manage user sessions, open files, and user storage quotas <br>&emsp; + Enable Continuous Access share for high availability <br>&emsp; + Scale throughput and storage capacity as needed <br>&emsp; + Delete the environment to clean up resources <br>&emsp; + Reference the AWS CLI for managing the file server <br><br> - **Implement AWS Web Application Firewall (WAF):** <br>&emsp; + Create an S3 Bucket and deploy a sample web application for testing <br>&emsp; + Use AWS WAF with managed rules to protect against common threats <br>&emsp; + Create custom and advanced custom rules for specific security needs <br>&emsp; + Test new rules to ensure they are working correctly <br>&emsp; + Log requests for monitoring and analysis <br>&emsp; + Clean up all created resources to avoid ongoing charges | 10/09/2025 | 10/09/2025      | Amazon FSx: <br> <https://000025.awsstudygroup.com/> <br> AWS WAF: <br> <https://000026.awsstudygroup.com/> |
| 6   | - **Manage AWS resources using Tags and Resource Groups:** <br>&emsp; + Understand and use tags on the AWS Management Console <br>&emsp; + Create an EC2 instance with tags <br>&emsp; + Add or remove tags from existing resources <br>&emsp; + Filter resources based on tags <br>&emsp; + Learn to use tags with the AWS Command Line Interface (CLI) <br>&emsp; + Add tags to an existing EC2 resource using the CLI <br>&emsp; + Add tags to a new resource during creation using the CLI <br>&emsp; + Describe tagged resources using the CLI <br>&emsp; + Create and manage a Resource Group to organize AWS resources <br>&emsp; + Create a tag-based Resource Group <br>&emsp; + View and manage resources within a Resource Group | 10/10/2025 | 10/10/2025      | AWS Tags & Resource Groups: <br> <https://000027.awsstudygroup.com/> |


### Week 5 Achievements:

* Successfully implemented advanced AWS networking solutions:
  * VPC Peering for direct inter-VPC communication
  * Transit Gateway for centralized network hub architecture
  * Cross-VPC DNS resolution and routing configuration

* Deployed and optimized full-stack cloud applications:
  * WordPress application with RDS database integration
  * Auto Scaling and CloudFront for performance and availability
  * Serverless cost optimization using Lambda functions

* Built comprehensive DevOps automation workflows:
  * End-to-end CI/CD pipelines with AWS Developer Tools
  * Automated deployment processes with CodePipeline integration
  * Hybrid cloud storage solutions using Storage Gateway

* Configured enterprise-grade file systems and security:
  * Amazon FSx for Windows File Server with Multi-AZ deployment
  * AWS WAF implementation with custom security rules
  * Performance monitoring and storage optimization techniques

* Established effective AWS resource management practices:
  * Resource tagging strategies for cost tracking and organization
  * Resource Groups for streamlined resource governance
  * Proficient use of both AWS Console and CLI operations

* Gained hands-on experience with Infrastructure as Code using CloudFormation templates for consistent environment provisioning.
