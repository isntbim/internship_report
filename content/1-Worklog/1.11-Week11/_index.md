---
title: "Week 11 Worklog"
date: "`r Sys.Date()`"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---



### Week 11 Objectives:

* Attend AWS community event to learn about advanced cloud services and best practices.
* Build serverless text service infrastructure with DynamoDB table design and IAM role configuration.
* Implement database retrieval functions with pagination support and filter expressions.
* Develop in-memory caching system and API request validation logic.
* Integrate Amazon Bedrock Agent for AI-generated paragraph content.
* Configure monitoring and debugging tools for serverless applications.
* Develop GraphQL APIs using AWS AppSync with DynamoDB resolvers.

### Tasks carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
|-----|------| ---------- |-----------------| ------------------ |
| 2   | - **Attending "AWS Cloud Mastery Series #2" event** | 11/17/2025 | 11/17/2025 |
| 3   | - **Initialize AWS serverless infrastructure for text service:** <br>&emsp; + Create DynamoDB table `wordsntexts` with a string partition key to store words and paragraphs <br>&emsp; + Configure IAM execution role permissions for `dynamodb:Scan`, `dynamodb:Query`, and CloudWatch logging <br>&emsp; + Set up the initial Lambda handler structure and establish `boto3` database connection objects <br><br> - **Implement database retrieval algorithms:** <br>&emsp; + Develop `fetch_words_from_db` using scan operations with `LastEvaluatedKey` for pagination <br>&emsp; + Develop `fetch_paragraph_from_db` applying filter expressions for content type and length attributes | 11/18/2025 | 11/18/2025 |
| 4   | - **Implement caching mechanisms and data processing logic:** <br>&emsp; + Design an in-memory global cache dictionary with a 300-second TTL to reduce database scan frequency <br>&emsp; + Implement `get_random_words` logic to retrieve data from cache or DB and perform random sampling <br>&emsp; + Implement `get_paragraph` logic to handle length clamping (1-3) and split content strings into word lists <br><br> - **Develop API request validation and response formatting:** <br>&emsp; + Create a custom `Decimal_encoder` class to properly serialize DynamoDB numeric types for JSON output <br>&emsp; + Add input validation blocks for query parameters `type` and `count` to handle `TypeError`s and `ValueError`s <br>&emsp; + Standardize JSON response structures to include appropriate HTTP status codes and headers | 11/19/2025 | 11/19/2025 |
| 5   | - **Integrate Amazon Bedrock Agent for generative capabilities:** <br>&emsp; + Update IAM permissions to include `bedrock:InvokeAgent` and associate with Agent ID `HUEBUXSALX` <br>&emsp; + Initialize the `bedrock-agent-runtime` client and implement the `invoke_agent` call with session management <br>&emsp; + Develop logic to process streaming response payloads and decode byte chunks into a unified string <br><br> - **Conduct prompt engineering and model experimentation:** <br>&emsp; + Design trigger prompts to ensure the Agent returns three paragraphs separated by blank lines <br>&emsp; + Experiment with different underlying models to ensure consistent formatting for the split logic <br>&emsp; + Implement parsing logic to separate the AI output | 11/20/2025 | 11/20/2025 |
| 6   | - **Monitor and Debug Serverless Applications with CloudWatch and X-Ray** <br>&emsp; + Analyze Lambda function logs in CloudWatch to identify and troubleshoot execution errors <br>&emsp; + Define and implement custom metrics to track application-specific performance data <br>&emsp; + Configure CloudWatch Alarms to trigger notifications based on critical metric thresholds <br>&emsp; + Enable AWS X-Ray tracing to visualize service maps and identify latency bottlenecks <br><br> - **Develop GraphQL APIs with AWS AppSync and DynamoDB Resolvers** <br>&emsp; + Prepare the AppSync environment and configure DynamoDB as a data source <br>&emsp; + Implement resolvers to perform Write and Read operations for individual data items <br>&emsp; + Configure Update and Delete resolvers to manage data modification lifecycles <br>&emsp; + Execute Scan and Query operations to facilitate bulk data retrieval via the API <br>&emsp; + Design and implement complex object resolvers to handle nested data structures | 11/21/2025 | 11/21/2025 | CloudWatch and X-Ray Monitoring: <br> <https://000085.awsstudygroup.com/> <br> AppSync GraphQL APIs: <br> <https://000086.awsstudygroup.com/> |


### Week 11 Achievements:

* Attended the "AWS Cloud Mastery Series #2" event to learn about advanced AWS services and best practices.

* Built serverless infrastructure for a typing practice text service application:
  * Created DynamoDB table `wordsntexts` with string partition key to store approximately 64,726 words and paragraphs.
  * Configured IAM execution role with permissions for DynamoDB Scan/Query operations and CloudWatch logging.
  * Set up Lambda handler (128 MB memory, 15s timeout) with `boto3` database connection objects.

* Implemented database retrieval algorithms:
  * Developed `fetch_words_from_db` using DynamoDB scan operations with `LastEvaluatedKey` pagination.
  * Created `fetch_paragraph_from_db` with filter expressions for content type and length attributes (short: 10-25 words, medium: 25-60 words, long: 60+ words).

* Optimized application performance and implemented request handling:
  * Designed in-memory caching system with 300-second TTL to reduce DynamoDB scan frequency for expected load of ~500 requests/hour.
  * Implemented `get_random_words` and `get_paragraph` functions with random sampling and length clamping (1-3).
  * Created custom `Decimal_encoder` class for proper JSON serialization of DynamoDB numeric types.
  * Added input validation for query parameters `type` and `count` to handle `TypeError`s and `ValueError`s.
  * Standardized JSON response structures with appropriate HTTP status codes and headers.

* Integrated Amazon Bedrock Agent for generative AI paragraph generation:
  * Updated IAM permissions to include `bedrock:InvokeAgent` and configured access to Agent ID `HUEBUXSALX`.
  * Initialized `bedrock-agent-runtime` client with session management for `invoke_agent` calls.
  * Developed streaming response processing logic to decode byte chunks into unified strings.
  * Designed trigger prompts to generate three paragraphs separated by blank lines for future daily challenge feature.
  * Implemented parsing logic to separate AI output.

* Configured monitoring and debugging capabilities for serverless applications:
  * Analyzed Lambda execution logs in CloudWatch to identify and troubleshoot errors.
  * Defined custom CloudWatch metrics to track application-specific performance data.
  * Configured CloudWatch Alarms with critical metric thresholds for error rates and duration monitoring.
  * Enabled AWS X-Ray tracing to visualize service maps and identify latency bottlenecks.

* Developed GraphQL APIs with AWS AppSync:
  * Set up AppSync environment and configured DynamoDB as a data source.
  * Implemented resolvers for Write, Read, Update, and Delete operations.
  * Configured Scan and Query resolvers for bulk data retrieval via the API.
  * Designed complex object resolvers to handle nested data structures and relationships.
