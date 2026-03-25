# CodeSignal Test 7 - Questions

---

**Question 1.** A developer is tasked with automating the deployment of a new microservice in an ECS cluster using AWS CodeDeploy. The developer is writing the AppSpec file to instruct CodeDeploy on how to handle the deployment.

Which sets of properties are REQUIRED in the resources section to successfully deploy the microservice? (Select THREE.)

A. ContainerPort
B. ContainerName
C. alias
D. NetworkConfiguration
E. TaskDefinition
F. targetVersion

---

**Question 2.** A developer has an application that uses a Lambda function to process data from an Aurora MySQL DB instance in a Virtual Private Cloud (VPC). The database throws a MySQL: ERROR 1040: Too many connections error whenever there is a surge in incoming traffic.

Which is the most suitable solution for resolving the issue?

A. Increase the concurrency limit of the Lambda function
B. Increase the allocated memory of your function.
C. Increase the value of the max_connections parameter of the Aurora MySQL DB instance.
D. Provision an RDS Proxy between the Lambda function and the RDS database instance

---

**Question 3.** A write-heavy data analytics application is using DynamoDB database which has global secondary index. Whenever the application is performing heavy write activities on the table, the DynamoDB requests return a ProvisionedThroughputExceededException.

Which of the following is the MOST likely cause of this issue?

A. The provisioned write capacity for the global secondary index is less than the write capacity of the base table.
B. The provisioned throughput exceeds the current throughput limit for your account.
C. The provisioned write capacity for the global secondary index is greater than the write capacity of the base table.
D. The rate of requests exceeds the allowed throughput.

---

**Question 4.** An application, which already uses X-Ray, generates thousands of trace data every hour. The developer wants to use a filter expression that will limit the results based on custom attributes or keys that he specifies.

How should the developer refactor the application in order to filter the results in the X-Ray console?

A. Add the custom attributes as metadata in your segment document.
B. Include the custom attributes as new segment fields in the segment document.
C. Add the custom attributes as annotations in your segment document.
D. Create a new sampling rule based on the custom attributes.

---

**Question 5.** A Lambda function downloads the same 250 MB file between invocations and stores it in memory for processing. This leads to frequent timeouts and negatively impacts the performance of the serverless application.

Which change should be made to resolve the issue most effectively?

A. Increase the ephemeral storage size of the function.
B. Increase the timeout of the function.
C. Store the file in the /tmp directory of the execution context and reuse it on succeeding invocations.
D. Increase the memory allocation of the function.

---

**Question 6.** A developer is preparing the application specification (AppSpec) file in CodeDeploy, which will be used to deploy her Lambda functions to AWS. In the deployment, she needs to configure CodeDeploy to run a task before the traffic is shifted to the deployed Lambda function version.

Which deployment lifecycle event should she configure in this scenario?

A. BeforeInstall
B. Start
C. Install
D. BeforeAllowTraffic

---

**Question 7.** A developer has a Node.js function running in AWS Lambda. Currently, the code initializes a database connection to an Amazon RDS database every time the Lambda function is executed, and closes the connection before the function ends.

What feature in AWS Lambda will allow the developer to reuse the already existing database connection instead of initializing it each time the function is run?

A. AWS Lambda is not capable of maintaining existing database connections due to its transient data store.
B. Execution context
C. Event source mapping
D. Environment variables

---

**Question 8.** A developer is building an e-commerce application which will be hosted in an ECS Cluster. To minimize the number of instances in use, she must select a strategy which will place tasks based on the least available amount of CPU or memory.

Which of the following task placement strategy should the developer implement?

A. binpack
B. spread
C. random
D. distinctInstance

---

**Question 9.** A recruitment agency has a large collection of resumes stored in an Amazon S3 bucket. The agency wants to perform an analysis on these files, but for privacy compliance reasons, they need to ensure that certain personally identifiable information (PII) is redacted before being processed by their internal service.

Which solution can meet the requirements in the most cost-effective way?

A. Use Amazon S3 Object Lambda to redact PII before it is returned to the application.
B. Use a Lambda function to create a redacted copy of each file in a separate S3 bucket. Then, set up an Amazon S3 Access Point to serve these files.
C. Configure an Amazon S3 Access Point and set up an Amazon CloudFront distribution with a Lambda@Edge function to redact the PII as data is fetched from the S3 bucket.
D. Implement a solution with AWS Glue to transform the data and redact PII before storing it in an S3 bucket.

---

**Question 10.** A multinational e-commerce company hosts its product descriptions on an Amazon RDS database. All descriptions are originally written in English. Users can request on-demand translations via a Lambda function, which pulls the description and employs Amazon Translate's TranslateText API for the task. However, during sales of popular products, the surge in translation requests is stressing the RDS, causing increased response times.

How can a developer improve the Lambda function's response time cost-effectively without performing database optimizations?

A. Use AWS Step Functions with a Parallel state to concurrently run multiple instances of the Lambda function for translation.
B. Use the /tmp storage in the Lambda function to cache recently translated product descriptions.
C. Store the results of the TranslateText API in an Amazon DynamoDB Accelerator (DAX) cluster.
D. Update the Lambda function to use asynchronous invocation. Push the translation requests to an Amazon SQS queue and then process them in batches.

---

**Question 11.** A commercial bank is developing an online auction application with a DynamoDB database that will allow customers to bid for real estate properties from the comforts of their homes. The application should allow multiple users to submit their bids simultaneously at the auction. The opening bid entered by the staff must be at least the minimum acceptable price established by the bank prior to the auction. The application logic has already been implemented but the DynamoDB database calls should also be tailored to meet the requirements.

Which of the following is the MOST effective solution that will satisfy the requirement in this scenario?

A. Use DynamoDB Streams and a Lambda function to track the current bid price and compare against all of the new bids submitted by the customers
B. Configure the database calls of the application to use conditional updates and conditional writes with a condition expression that will check if the new bid submitted by the customer is greater than the current bid.
C. Enable DynamoDB Transactions to automatically check the minimum acceptable price as well as the current and new bid price.
D. Use an optimistic locking strategy in your database calls to ensure that the new bid submitted by the customer is greater than the current bid.

---

**Question 12.** Your serverless AWS Lambda functions are integrated with Amazon API Gateway using Lambda proxy integration. The API caching feature is enabled in the API Gateway with a TTL value of 300 seconds. A client would like to fetch the latest data from your endpoints every time a request is sent and invalidate the existing cache.

What should the client do in order to get the latest data?

A. Have the client send a request with the Cached: False header.
B. Modify cache TTL value to a shorter period.
C. Have the client send a request with the Cache-Control: max-age=0 header.
D. Override API caching by allowing the client to send requests to the endpoint directly.

---

**Question 13.** A serverless application, which is composed of multiple Lambda functions, has been deployed using AWS SAM. A developer was instructed to easily manage the deployments of the functions using CodeDeploy. When there is a new deployment, 10 percent of the incoming traffic should be shifted to the new version every 10 minutes until all traffic is shifted from the old version.

What should the developer do to properly deploy the functions that satisfies this requirement?

A. Deploy the functions using an All-at-once deployment configuration.
B. Deploy the functions using a Canary deployment configuration.
C. Deploy the functions using a Linear deployment configuration.
D. Deploy the functions using an Immutable deployment configuration.

---

**Question 14.** You are developing an online game where the app preferences and game state of the player must be synchronized across devices. It should also allow multiple users to synchronize and collaborate shared data in real time.

Which of the following is the MOST appropriate solution that you should implement in this scenario?

A. Integrate Amazon Pinpoint to your mobile app.
B. Integrate Amazon Cognito Sync to your mobile app.
C. Integrate AWS Amplify to your mobile app.
D. Integrate AWS AppSync to your mobile app.

---

**Question 15.** A developer wants to track the number of visitors on their website, which has a DynamoDB database. This is primarily used to give a rough idea on how many people visit the site whenever they launch a new advertisement, which means it can tolerate a slight over-counting or undercounting of website visitors.

Which of the following will satisfy the requirement with MINIMAL configuration?

A. Use conditional writes to update the counter item in the DynamoDB table only if the item has a unique primary key and the new value is greater than the current value.
B. Use atomic counters to increment the counter item in the DynamoDB table for every new visitor.
C. Use conditional writes to update the counter item in the DynamoDB table and set the ReturnConsumedCapacity parameter to TOTAL.
D. Enable DynamoDB Streams to track the number of new visitors.

---

**Question 16.** A company is legally obligated to keep transaction records containing Personally Identifiable Information (PII) for a duration of five years. These records are stored in Amazon S3. To handle data redaction, the company has developed Lambda functions with naming conventions starting as RedactPII-[role], where [role] represents different roles. The company wants to provide varying levels of redaction based on each role, ensuring each user only sees the necessary data. Only a single copy of the records should be maintained.

Which combination of actions will achieve the given requirements? (Select THREE.)

A. Use the GetObject API to retrieve the redacted data.
B. Set up an S3 event notification to invoke the corresponding RedactPII-[role] function in response to GET requests.
C. Set up S3 Replication for the bucket.
D. Use the GetObjectLegalHold API to retrieve the redacted data.
E. Create an S3 Access Point for each user role.
F. Configure an S3 Object Lambda Access Point for each S3 Access Point name. Associate the RedactPII-[role] Lambda functions with the corresponding S3 Object Lambda Access Point.

---

**Question 17.** A developer has been instructed to configure Cross-Region Replication (CRR) to their S3 bucket as part of the company's disaster recovery plan. She is using the put-bucket-replication AWS CLI to enable CRR on the bucket but it fails whenever she attempts to issue the command. However, the same command works for the other S3 buckets.

Which of the following options is the MOST likely reason for this issue?

A. Amazon S3 Object Lock is enabled in the bucket.
B. Versioning is not enabled in the bucket.
C. S3 Transfer Acceleration is not enabled in the bucket.
D. The bucket should be configured as a static web hosting first.

---

**Question 18.** An application experiences a sluggish response whenever there is a surge in requests involving read queries. The developer has already attempted to improve performance by optimizing the queries. However, the problem still persists even after applying the change. The application is hosted in an Amazon ECS Cluster and uses a MySQL database backed by Amazon RDS.

Which of the following could the developer do to resolve the performance issue? (Select TWO.)

A. Replace the database with Amazon MemoryDB for Redis.
B. Implement a Multi-AZ deployment configuration for the RDS DB instance.
C. Implement database caching using Amazon ElastiCache.
D. Set up read replicas for the RDS database instance and route read queries to these replicas.
E. Cache the database response using Amazon CloudFront.

---

**Question 19.** A developer is building a web application which requires a multithreaded event-based key/value cache store that will cache result sets from database calls. You need to run large nodes with multiple cores for your cache layer and it should scale up or down as the demand on your system increases and decreases.

Which is the MOST suitable service that you should use?

A. AWS Greengrass
B. Amazon CloudFront
C. Amazon ElastiCache for Redis
D. Amazon ElastiCache for Memcached

---

**Question 20.** A recently deployed Lambda function has an intermittent issue in processing customer data. You enabled the active tracing option in order to detect, analyze, and optimize performance issues of your function using the X-Ray service.

Which of the following environment variables are used by AWS Lambda to facilitate communication with X-Ray? (Select TWO.)

A. AUTO_INSTRUMENT
B. _AWS_XRAY_DEBUG_MODE
C. _X_AMZN_TRACE_ID
D. AWS_XRAY_CONTEXT_MISSING
E. AWS_XRAY_TRACING_NAME

---

**Question 21.** A developer is creating a real-time auction app for second-hand cars using Kinesis Data Streams to ingest bids. The auction rules are as follows:

- A bid must be processed only once.
- An ECS instance consumer must process bids in the same order they were received.

Which solution will meet the requirement?

A. Replace the stream with an SQS FIFO queue and use the SendMessage API to write bids. Provide a unique Id in the MessageDeduplicationId parameter for each bid request.
B. Replace the stream with an SQS FIFO queue and use the SendMessageBatch API to write bids. Provide a unique Id in the MessageDeduplicationId parameter for each bid request.
C. Embed a unique ID in each bid record. Use Kinesis PutRecord API to write bids. Assign a timestamp-based value for the SequenceNumberForOrdering parameter.
D. Embed a unique ID in each bid record. Use Kinesis PutRecords API to write bids. Assign a timestamp-based value for the PartitionKey parameter.

---

**Question 22.** A developer has recently deployed an application, which is hosted in an Auto Scaling group of EC2 instances and processes data from an Amazon Kinesis Data Stream. Each of the EC2 instances has exactly one KCL worker processing one Kinesis data stream which has 10 shards. Due to performance issues, the systems operations team has resharded the data stream to increase the number of open shards to 20.

What is the maximum number of running EC2 instances that should ideally be kept to maintain application performance?

A. 30
B. 40
C. 20
D. 10

---

**Question 23.** A transcoding media service is being developed in AWS. Photos uploaded to Amazon S3 will trigger Step Functions to coordinate a series of processes that will perform image analysis tasks. The final output should contain the input plus the result of the final state to conform to the application's logic flow.

What should the developer do?

A. Declare a ResultPath field filter on the Amazon States Language specification.
B. Declare an InputPath field filter on the Amazon States Language specification.
C. Declare a Parameters field filter on the Amazon States Language specification.
D. Declare an OutputPath field filter on the Amazon States Language specification.

---

**Question 24.** Your application is processing one Kinesis data stream which has four shards, and each instance has one KCL worker. To scale up processing in your application, you reshard your stream to increase the number of open shards to six.

What is the MAXIMUM number of EC2 instances that you should launch to achieve optimum performance?

A. 12
B. 6
C. 5
D. 3

---

**Question 25.** A developer is instructed to set up a new serverless architecture composed of AWS Lambda, API Gateway, and DynamoDB in a single stack. The new architecture should allow the developer to locally build, test, and debug serverless applications.

Which of the following should the developer use to satisfy the above requirement?

A. AWS Systems Manager
B. AWS Serverless Application Model (AWS SAM)
C. AWS Elastic Beanstalk
D. AWS CloudFormation

---

**Question 26.** A company wants to centrally organize login credentials for its internal application. The application prompts users to change passwords every 30 days. Expired login credentials must be removed automatically, and an email notification should be sent to the users when their passwords are about to expire. A developer must create a solution with the least amount of development effort.

Which solution meets the requirements?

A. Store the credentials as Standard Parameters in AWS Systems Manager (SSM) Parameter Store and configure Expiration and ExpirationNotification policies. Create an Amazon EventBridge rule that sends Amazon SNS email notifications.
B. Use AWS Secrets Manager to store user credentials. Create a Lambda function that runs periodically to send Amazon SNS email notifications for passwords nearing expiration.
C. Store the credentials as Advanced Parameters in AWS Systems Manager (SSM) Parameter Store and configure Expiration and ExpirationNotification policies. Create an Amazon EventBridge rule that sends Amazon SNS email notifications.
D. Use AWS Secrets Manager to store user credentials and turn on automatic rotation.

---

**Question 27.** A code that runs on a Lambda function performs a BatchItem call from a DynamoDB table. The function runs three times every week. You noticed that the application kept receiving a ProvisionedThroughputExceededException error for 10 seconds most of the time.

How should you handle this error?

A. Reduce the frequency of requests using error retries and exponential backoff.
B. Create a Local Secondary Index (LSI) to the existing DynamoDB table to increase the provisioned throughput.
C. Enable DynamoDB Accelerator (DAX) to reduce response times from milliseconds to microseconds.
D. Refactor the code in the Lambda function to optimize its performance.

---

**Question 28.** An application performs various workflows and processes long-running tasks that take a long time to complete. Users are complaining that the application is unresponsive since the workflow substantially increases the time it takes to complete a user request. The development team is looking for a managed solution that can handle background tasks efficiently, scale automatically, and integrate seamlessly with the existing application deployed on Elastic Beanstalk.

Which of the following is the BEST way to improve the performance of the application?

A. Spawn a worker process locally in the EC2 Instances and process the tasks asynchronously.
B. Use a multicontainer docker environment in Elastic Beanstalk to process the long-running tasks asynchronously.
C. Use an Amazon ECS Cluster with a Fargate launch type to process the tasks asynchronously.
D. Use an Elastic Beanstalk worker environment to process the tasks asynchronously.

---

**Question 29.** A mobile game has a serverless backend in AWS which is composed of Lambda, API Gateway, and DynamoDB. It writes 500 items per second to the DynamoDB table and the size is 1.5 KB per item. The table has a provisioned WCU of 500 but the write requests are still being throttled by DynamoDB.

What is the MOST suitable solution in order to rectify this throttling issue?

A. Implement database caching with an ElastiCache cluster.
B. Increase the WCU to 300.
C. Enable DynamoDB Accelerator (DAX).
D. Use strong consistency in the write operations.

---

**Question 30.** A developer has enabled API Caching on his application endpoints in Amazon API Gateway. For testing purposes, he wants to fetch the latest data, and not the cache data, whenever he sends a GET request with a Cache-Control: max-age=0 header to a specific resource.

Which of the following policies will allow him to invalidate the cache for requests?

A.
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "execute-api:*"
      ],
      "Resource": [
        "arn:aws:execute-api:region:account-id:stage/name/GET/resource-path-specifier"
      ]
    }
  ]
}
```

B.
```json
{
  "Version": "2019-09-17",
  "Statement": [
    {
      "Effect": "Deny",
      "Action": [
        "execute-api:*"
      ],
      "Resource": [
        "arn:aws:execute-api:region:account-id:stage/name/GET/resource-path-specifier"
      ]
    }
  ]
}
```

C.
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "execute-api:InvalidateCache"
      ],
      "Resource": [
        "arn:aws:execute-api:region:account-id:stage/name/GET/resource-path-specifier"
      ]
    }
  ]
}
```

D.
```json
{
  "Version": "2019-09-17",
  "Statement": [
    {
      "Effect": "Deny",
      "Action": [
        "execute-api:InvalidateCache"
      ],
      "Resource": [
        "arn:aws:execute-api:region:account-id:stage/name/GET/resource-path-specifier"
      ]
    }
  ]
}
```

---

**Question 31.** A software engineer is building a serverless application in AWS consisting of Lambda, API Gateway, and DynamoDB. She needs to implement a custom authorization scheme that uses a bearer token authentication strategy such as OAuth or SAML, to determine the caller's identity.

Which of the Features of API Gateway is the MOST suitable one that she should use to build this feature?

A. Cross-Account Lambda Authorizer
B. Resource Policy
C. Cross-Origin Resource Sharing (CORS)
D. Lambda Authorizers

---

**Question 32.** A developer is building an AI-based traffic monitoring application using Lambda in AWS. Due to the complexity of the application, the developer must do certain modifications such as the way Lambda runs the function's setup code and how the invocation events are read from the Lambda runtime API.

In this scenario, which feature of Lambda should you take advantage of to meet the above requirement?

A. Custom Runtime
B. DLQ
C. Lambda@Edge
D. Layers

---

**Question 33.** A startup has an urgent requirement to deploy their new Node.JS application to AWS. You were assigned to perform the deployment to a service where you don't need to worry about the underlying infrastructure that runs the application. The service must also automatically handle provisioning, load balancing, scaling, and application health monitoring.

Which service will you use to easily deploy and manage the application?

A. AWS CloudFormation
B. AWS CodeDeploy
C. AWS SAM
D. AWS Elastic Beanstalk

---

**Question 34.** A prototype application is hosted in an EC2 Instance, which has an assigned IAM Role to store data from both the development and production S3 buckets. The instance also has AWS CLI access/secret key installed to handle other ad hoc tasks. You assigned a new IAM Role to the instance which has the permission to access the development bucket only. However, upon testing, the instance can still store files to both buckets.

What is the MOST likely root cause of this issue?

A. The application is still using the IAM role that is configured for the AWS CLI key.
B. Due to eventual consistency, you must wait 24 hours for the change to appear across all of AWS.
C. The instance profile role of a running EC2 instance is static and can't be replaced at all.
D. The new IAM Role has an attached inline policy.

---

**Question 35.** The current application deployment process of a company is tedious and is prone to errors. They asked a developer to set up CodeDeploy as their deployment service, which can automate their application deployments on their hybrid cloud architecture.

Which of the following deployment types does CodeDeploy support? (Select TWO.)

A. Rolling deployments to ECS.
B. Blue/green deployments to ECS.
C. Blue/green deployments to on-premises servers.
D. In-place deployments to on-premises servers.
E. In-place deployments to AWS Lambda.

---

**Question 36.** A serverless application consisting of a Lambda function and a DynamoDB database is used to process Amazon S3 events. The Lambda function takes an average of three seconds to process the data and Amazon S3 publishes 10 events per second.

What is the concurrent execution that the function will have?

A. 3
B. 10
C. 13
D. 30

---

**Question 37.** A company uses AWS Systems Manager (SSM) Parameter Store to manage configuration details for multiple applications. The parameters are currently stored in the Standard tier. The company wants its operations team to be notified if there are sensitive parameters that haven't been rotated within 90 days.

Which must be done to meet the requirement?

A. Convert the sensitive parameters from Standard tier to Advanced tier. Set a NoChangeNotification policy with a value of 90 days. Use Amazon EventBridge (Amazon CloudWatch Events) to send a notification via Amazon SNS.
B. Convert the sensitive parameters from Standard tier to Advanced tier. Set an ExpirationNotification policy with a value of 90 days. Use Amazon EventBridge (Amazon CloudWatch Events) to send a notification via Amazon SNS.
C. Set up an Amazon EventBridge (Amazon CloudWatch Events) event pattern that captures SSM Parameter-related events. Use Amazon SNS to send notifications.
D. Configure a NoChangeNotification policy with a value of 90 days. Use Amazon EventBridge (Amazon CloudWatch Events) to send a notification via Amazon SNS.

---

**Question 38.** A software development company uses AWS CodePipeline as its CI/CD platform to build, test, and push deployments to its production environment. Recently, a developer created a Lambda function that will push the build details to a separate DynamoDB table. The Lambda function should be triggered after a successful build on the Pipeline.

Which of the following services will meet the specified requirement?

A. AWS CodeBuild
B. AWS CloudTrail Events
C. Amazon EventBridge (Amazon CloudWatch Events)
D. AWS Systems Manager

---

**Question 39.** A leading commercial bank has an online banking portal that is hosted in an Auto Scaling group of EC2 Instances with an Application Load Balancer in front to distribute the incoming traffic. The application has been instrumented, and the X-Ray daemon has been installed in all instances to allow debugging and troubleshooting using AWS X-Ray.

In this architecture, from which source will AWS X-Ray fetch the client IP address?

A. From the IpAddress query parameter of the request if it exists.
B. From the X-Forwarded-Host header of the request.
C. From the source IP of the IP packet.
D. From the X-Forwarded-For header of the request.

---

**Question 40.** You are a developer for a global technology company, which heavily uses AWS with regional offices in San Francisco, Manila, and Bangalore. Most of the clients of your company are using serverless computing in which you are responsible for ensuring that their applications are working efficiently.

Which of the following options are valid considerations in improving the performance of your Lambda function? (Select TWO.)

A. You have to install the X-Ray daemon in Lambda to enable active tracing.
B. Lambda automatically creates Elastic IPs that enable your function to connect securely to other resources within your private VPC.
C. An increase in memory size triggers an equivalent increase in CPU available to your function.
D. The concurrent execution limit is enforced against the sum of the concurrent executions of all function.
E. You can throttle all incoming executions and stop processing any invocations to your function by setting concurrency to false.

---

**Question 41.** An application in your development account is running in an AWS Elastic Beanstalk environment which has an attached Amazon RDS database. You noticed that if you terminate the environment, it also deletes the RDS DB instance.

In this scenario, how can you decouple your database instance from your Elastic Beanstalk environment without having any data loss?

A. Use the blue/green deployment strategy to decouple the Amazon RDS instance from your Elastic Beanstalk environment. Create an RDS DB snapshot of the database and enable deletion protection. Create a new Elastic Beanstalk environment with the necessary information to connect to the Amazon RDS instance. Before terminating the old Elastic Beanstalk environment, remove its security group rule first before proceeding.
B. Use the blue/green deployment strategy to decouple the Amazon RDS instance from your Elastic Beanstalk environment. Create an RDS DB snapshot of the database and enable deletion protection. Create a new Elastic Beanstalk environment with the necessary information to connect to the Amazon RDS instance. Before terminating the old Elastic Beanstalk environment, remove its security group rule first before proceeding.
C. Use a Canary deployment strategy to decouple the Amazon RDS instance from your Elastic Beanstalk environment. Create an RDS DB snapshot of the database and enable deletion protection. Create a new Elastic Beanstalk environment with the necessary information to connect to the Amazon RDS instance and delete the old environment.
D. Use a Canary deployment strategy to decouple the Amazon RDS instance from your Elastic Beanstalk environment. Create an RDS DB snapshot of the database and then create a new Elastic Beanstalk environment with the necessary information to connect to the Amazon RDS instance.

---

**Question 42.** The operating cost of a serverless application is quite high and you are instructed to look for ways to lower the costs. As part of its processing, a Lambda function sends 100 strongly consistent reads per second to a DynamoDB table which has a provisioned RCU of 5440. The average size of items stored in the database is 17 KB.

Which of the following is the MOST suitable action that should you do to make the application more cost-effective while maintaining its performance?

A. Switch the table from using provisioned mode to on-demand mode.
B. Set the provisioned RCU to 1600.
C. Decrease the provisioned RCU to 800.
D. Implement exponential backoff.

---

**Question 43.** A company is re-architecting its legacy application to use AWS Lambda and DynamoDB. The table is provisioned to have 10 read capacity units, and each item has a size of 4 KB.

How many eventual and strong consistent read requests can the table handle per second?

A. 5 strongly consistent reads and 20 eventually consistent reads per second
B. 10 strongly consistent reads and 5 eventually consistent reads per second
C. 20 strongly consistent reads and 10 eventually consistent reads per second
D. 10 strongly consistent reads and 20 eventually consistent reads per second

---

**Question 44.** A company has developed a Lambda function that will send status updates to a third-party provider for analytics. You need to schedule this function to run every 30 minutes.

Which of the following is the MOST manageable and cost-effective way of setting up this task?

A. Enable scheduling on the AWS Console of your Lambda function. Define a schedule to run it at 30-minute intervals.
B. Integrate Amazon EventBridge (Amazon CloudWatch Events) with Lambda, which will automatically trigger the function every 30 minutes.
C. Use the Task Scheduler of your Windows PC to trigger the Lambda function every 30 minutes.
D. Launch an EC2 Instance that has a cron job that triggers the Lambda function every 30 minutes.

---

**Question 45.** A web application running in Amazon Elastic Beanstalk reads and writes a large number of related items in DynamoDB and processes each item one at a time. The network overhead of these transactions causes degradation in the application's performance. You were instructed by your manager to quickly refactor the application but without introducing major code changes such as implementing concurrency management or multithreading.

Which of the following solutions is the EASIEST method to implement that will improve the application performance in a cost-effective manner?

A. Upgrade the EC2 instances to a higher instance type.
B. Refactor the application to use DynamoDB transactional read and write APIs.
C. Use DynamoDB Batch Operations API for GET, PUT, and DELETE operations.
D. Enable DynamoDB Streams.

---

**Question 46.** A company decided to re-use the same Lambda function for multiple stages of their API, but the function should read data from a different Amazon DynamoDB table depending on which stage is being called. In order to accomplish this, they instructed the developer to pass configuration parameters to a Lambda function through mapping templates in API Gateway.

Which of the following is the MOST suitable solution that the developer should use to meet this requirement?

A. Set up traffic shifting with Lambda Aliases.
B. Create environment variables in the Lambda function.
C. Use Stage Variables.
D. Set up an API Gateway Private Integration to the Lambda function.

---

**Question 47.** A mobile game has a serverless backend consisting of an API Gateway backed by Lambda functions and a DynamoDB table in provisioned capacity mode, where player data is stored. While the game has maintained a consistent level of traffic, recent growth in the player base has caused response times to slow down. To improve performance, the developer wants to reduce the number of database queries for data that rarely changes.

What approach can the developer take to achieve this goal cost-effectively and with less development overhead?

A. Set up an Amazon DynamoDB Accelerator (DAX) caching layer in front of the DynamoDB table.
B. Create an Amazon MemoryDB for Redis database in front of the DynamoDB table to cache data.
C. Use DynamoDB Session Handler to handle the saving and retrieval of player data.
D. Switch the DynamoDB table's capacity mode to On-demand.

---

**Question 48.** The developer has built a real-time IoT device monitoring application that leverages Amazon Kinesis Data Stream to ingest data. The application uses several EC2 instances for processing. Recently, the developer has observed a steady increase in the rate of data flowing into the stream, indicating that the stream's capacity must be scaled up to sustain optimal performance.

What should the developer do to increase the capacity of the stream?

A. Merge every shard in the stream.
B. Integrate Amazon Data Firehose with the Amazon Kinesis Data Stream to increase the capacity of the stream.
C. Split every shard in the stream.
D. Upgrade the instance type of the EC2 instances.

---

**Question 49.** A company is developing a serverless website that consists of images, videos, HTML pages, and JavaScript files. There is also a requirement to serve the files with lowest possible latency to its global users.

Which combination of services should be used in this scenario? (Select TWO.)

A. Amazon EC2
B. Amazon Glacier
C. Amazon Elastic File System
D. Amazon CloudFront
E. Amazon S3

---

**Question 50.** A full-stack developer has developed an application written in Node.js to host an upcoming mobile game tournament. The developer has decided to deploy the application using AWS Elastic Beanstalk because of its ease-of-use. Upon experimenting, he learned that he could configure the webserver environment with several resources.

Which of the following services can the developer configure with Elastic Beanstalk? (Select THREE.)

A. Amazon CloudFront
B. Amazon Athena
C. Amazon CloudWatch
D. Amazon EC2 Instance
E. AWS Lambda
F. Application Load Balancer

---

**Question 51.** To improve their information security management system (ISMS), a company recently released a new policy which requires all database credentials to be encrypted and be automatically rotated to avoid unauthorized access.

Which of the following is the MOST appropriate solution to secure the credentials?

A. Enable IAM DB authentication which rotates the credentials by default.
B. Create an IAM Role which has full access to the database. Attach the role to the services which require access.
C. Create a parameter to the Systems Manager Parameter Store using the PutParameter API with a type of SecureString.
D. Create a secret in AWS Secrets Manager and enable automatic rotation of the database credentials.

---

**Question 52.** A global financial company has hundreds of users from all over the world that regularly upload terabytes of transactional data to a centralized S3 bucket. You noticed that there are some users from different parts of the globe that take a lot of time to upload their data, which causes delays in the processing. You need to improve data throughput and ensure consistently fast data transfer to the S3 bucket regardless of the user's location.

Which of the following features should you use to satisfy the above requirement?

A. Amazon S3 Transfer Acceleration
B. AWS Transfer for SFTP
C. CloudFront
D. AWS Direct Connect

---

**Question 53.** You are a software developer for a multinational investment bank which has a hybrid cloud architecture with AWS. To improve the security of their applications, they decided to use AWS Key Management Service (KMS) to create and manage their application keys across a wide range of AWS services. You were given the responsibility to integrate AWS KMS with the financial applications of the company.

Which of the following are the recommended steps to locally encrypt data using AWS KMS? (Select TWO.)

A. Erase the encrypted data key from memory and store the plaintext data key alongside the locally encrypted data.
B. Use the GenerateDataKeyWithoutPlaintext operation to get a data encryption key then use the plaintext data key in the response to encrypt data locally.
C. Encrypt data locally using the Encrypt operation.
D. Use the GenerateDataKey operation to get a data encryption key then use the plaintext data key in the response to encrypt data locally.
E. Erase the plaintext data key from memory and store the encrypted data key alongside the locally encrypted data.

---

**Question 54.** A DynamoDB table has several top-level attributes such as Id, course_id, course_title, price, rating and many others. The database queries of your application returns all of the item attributes by default but you only want to fetch specific attributes such as the course_id and price per request.

As the developer, how can you refactor your application to accomplish this requirement?

A. Use expression attribute names
B. Use condition expressions
C. Use projection expression
D. Use filter expressions

---

**Question 55.** A developer is building an online game in AWS which will be using a NoSQL database with DynamoDB. Each player data has an average size of 3.5 KB and it is expected that the game will send 150 eventually consistent read requests per second.

How many Read Capacity Units (RCU) should the developer provision to the table?

A. 300
B. 600
C. 150
D. 75

---

**Question 56.** A company is using CloudFront to serve their static contents to their users around the globe. They are receiving a number of bad reviews from their customers because it takes a lot of time to log in to their website. Sometimes, their users are also getting HTTP 504 errors which is why the developer was instructed to fix HTTP errors immediately.

Which of the following combination of options should the developer use together to set up a cost-effective solution for this scenario? (Select TWO.)

A. Configure an origin failover by creating an origin group with two origins. Specify one as the primary origin and the other as the second origin which CloudFront automatically switches to when the primary returns specific HTTP status code failure responses.
B. Launch your application to multiple AWS regions to serve your global users. Use a Route 53 record with latency routing policy to route incoming traffic to the region with the best latency to the user.
C. Add a Cache-Control max-age directive to your objects in CloudFront and specify the longest practical value for max-age to increase the cache hit ratio of your CloudFront distribution.
D. Launch your application to multiple and geographically disperse VPCs on various AWS regions then create a transit VPC to easily connect resources. Use the AWS Serverless Application Model (SAM) service to improve the overall application performance.
E. Customize the content that the CloudFront web distribution delivers to your users using Lambda@Edge functions that allows your Lambda functions to execute the authentication process in AWS locations closer to the users.

---

**Question 57.** A developer is managing a distributed system that consists of an Application Load Balancer, an SQS queue, and an Auto Scaling group of EC2 instances. The system has been integrated with CloudFront to better serve clients worldwide. To enhance the security of the in-flight data, the developer was instructed to establish an end-to-end SSL connection between the origin and the end-users.

Which TWO options will allow the developer to meet this requirement using CloudFront? (Select TWO.)

A. Configure the Origin Protocol Policy to use HTTPS only
B. Configure your ALB to only allow traffic on port 443 using an SSL certificate from AWS Config.
C. Associate a Web ACL using AWS Web Application Firewall (WAF) with your CloudFront Distribution.
D. Set up an Origin Access Control (OAC) setting
E. Configure the Viewer Protocol Policy to use HTTPS only

---

**Question 58.** A developer has recently completed a new version of a serverless application that is ready to be deployed using AWS SAM. There is a requirement that the traffic should shift from the previous Lambda function to the new version in the shortest time possible, but you still don't want to shift traffic all-at-once immediately.

Which deployment configuration is the MOST suitable one to use in this scenario?

A. CodeDeployDefault.LambdaAllAtATime
B. CodeDeployDefault.LambdaLinear10PercentEvery1Minute
C. CodeDeployDefault.LambdaCanary10PercentSMinutes
D. CodeDeployDefault.LambdaLinear10PercentEvery2Minutes

---

**Question 59.** A financial mobile application has a serverless backend API which consists of DynamoDB, Lambda, and Cognito. Due to the confidential financial transactions handled by the mobile application, there is a new requirement provided by the company to add a second authentication method that doesn't rely solely on user name and password.

Which of the following is the MOST suitable solution that the developer should implement?

A. Use a new IAM policy to a user pool in Cognito.
B. Use Cognito with SNS to allow additional authentication via SMS.
C. Integrate multi-factor authentication (MFA) to a user pool in Cognito to protect the identity of your users.
D. Create a custom application that integrates with Amazon Cognito which implements the second layer of authentication.

---

**Question 60.** A developer is creating an analytics REST API service that is powered by API Gateway. Analysts from a separate AWS account must interact with the service through an IAM role. The IAM role already has a policy that grants permission to invoke the execute-api:Invoke action.

What else should the developer do to meet the requirement without too much overhead?

A. Set AWS_IAM as the method authorization type for the API. Attach a resource policy to the API that grants permission to the specified IAM role to invoke the execute-api:Invoke action.
B. Create a Lambda function authorizer for the API. In the Lambda function, write a logic that verifies the requester's identity by extracting the information from the context object.
C. Create an API Key for the API. Attach a resource policy to the API that grants permission to the specified IAM role to invoke the GetAPIKeys action.
D. Create a Cognito User Pool authorizer. Add the IAM role to the user pool. Authenticate the requester's identity using Cognito. Ask the analysts to pass the token returned by Cognito in their request headers.

---

**Question 61.** A company has launched a new serverless application using AWS Lambda. The app ran smoothly for a few weeks until it was featured on a popular website. As its popularity grew, so did the number of users receiving an error. Upon viewing the Lambda function's monitoring graph, the developer discovered a lot of throttled invocation requests.

What can the developer do to troubleshoot this issue? (Select THREE.)

A. Use exponential backoff in the application.
B. Deploy the Lambda function in VPC
C. Request a service quota increase
D. Use a compiled language like Golang to improve the function's performance
E. Configure reserved concurrency
F. Increase Lambda function timeout

---

**Question 62.** Your Lambda function initializes a lot of external dependencies such as database connections and HTTP endpoints, which are required for data processing. It also fetches static data with a size of 20 MB from a third-party provider over the internet every time the function is invoked. This adds significant time in the total processing, which greatly affects the performance of their serverless application.

Which of the following should you do to improve the performance of your function?

A. Allocate more memory to your function.
B. Increase the CPU allocation of the function by submitting a service limit increase ticket to AWS.
C. Use unreserved concurrency for your function.
D. Place the database and HTTP initialization logic outside the Lambda function handler and store the external files in the /tmp directory.

---

**Question 63.** You recently deployed an application to a newly created AWS account, which uses two identical Lambda functions to process ad-hoc requests. The first function processes incoming requests efficiently but the second one has a longer processing time even though both of the functions have exactly the same code. Based on your monitoring, the Throttles metric of the second function is greater than the first one in Amazon CloudWatch.

Which of the following are possible solutions that you can implement to fix this issue? (Select TWO.)

A. Set the concurrency execution limit of both functions to 500.
B. Set the concurrency execution limit of the second function to 0.
C. Set the concurrency execution limit of both functions to 450.
D. Decrease the concurrency execution limit of the first function.
E. Configure the second function to use an unreserved account concurrency.
