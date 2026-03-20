# AWS Developer Associate - Quiz Set 5 (Questions 357–445)

---

**Question 357.** A developer is publishing critical log data to a log group in Amazon CloudWatch Logs. The log group was created 2 months ago. The developer must encrypt the log data by using an AWS Key Management Service (AWS KMS) key so that future data can be encrypted to comply with the company's security policy.

Which solution will meet this requirement with the LEAST effort?

A. Use the AWS Encryption SDK for encryption and decryption of the data before writing to the log group.
B. Use the AWS KMS console to associate the KMS key with the log group.
C. Use the AWS CLI aws logs create-log-group command, and specify the key Amazon Resource Name (ARN).
D. Use the AWS CLI aws logs associate-kms-key command, and specify the key Amazon Resource Name (ARN).

---

**Question 358.** A developer is working on an app for a company that has a table named Orders in Amazon DynamoDB table to store customer orders. The table uses OrderID as the partition key and there is no sort key. The developer needs to find all Orders records from customers. The developer needs a functionality that will retrieve all Orders records that contain an OrderSource attribute with the MobileApp value.

Which solution will improve the user experience in the MOST efficient way?

A. Perform a Scan operation on the Orders table. Provide a QueryFilter condition to filter to only the items where the OrderSource attribute is equal to the MobileApp value.
B. Create a local secondary index (LSI) with OrderSource as the partition key. Perform a Query operation by using the MobileApp value.
C. Create a global secondary index (GSI) with OrderSource as the partition key. Perform a Query operation by using MobileApp as the key.
D. Create a global secondary index (GSI) with OrderSource as the sort key. Perform a Query operation by using MobileApp as the key.

---

**Question 359.** A company has an application that uses an AWS Lambda function to process data. A developer must implement encryption in transit for all sensitive configuration data, such as API keys, that is stored in the application. The developer creates an AWS Key Management Service (AWS KMS) customer managed key.

What should the developer do next to meet the encryption requirement?

A. Create parameters of the String type in AWS Systems Manager Parameter Store. For each parameter, specify the KMS key ID to encrypt the parameter in transit. Reference the GetParameter API call in the Lambda environment.
B. Create an AWS Secrets Manager by using the customer managed KMS key. Create a new Lambda function and set up a Lambda layer to retrieve the values from Secrets Manager.
C. Create objects in Amazon S3 for each sensitive data field. Specify the customer managed KMS key to encrypt the objects. Configure the Lambda layer to retrieve the objects from Amazon S3 during data processing.
D. Create encrypted Lambda environment variables. Specify the customer managed KMS key to encrypt the variables. Enable encryption helpers for encryption in transit. Grant permission to the Lambda function's execution role to use the KMS key.

---

**Question 360.** A developer is building an ecommerce application. When there is a sale event, the application needs to concurrently call three third-party systems to record the sale. The developer wrote three AWS Lambda functions. There is one Lambda function for each third-party system, which contains complex integration logic.

These Lambda functions are all independent. The developer needs to design the application so each Lambda function will meet these requirements of others' success or failure.

Which solution will meet these requirements?

A. Publish the sale event from the application to an Amazon Simple Queue Service (Amazon SQS) queue. Configure the three Lambda functions to poll the queue.
B. Publish the sale event from the application to an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe the three Lambda functions to be triggered by the SNS topic.
C. Publish the sale event from the application to an Application Load Balancer (ALB). Add the three Lambda functions as ALB targets.
D. Publish the sale event from the application to an AWS Step Functions state machine. Move the logic from the three Lambda functions into the Step Functions state machine.

---

**Question 361.** A developer is writing an application, which stores data in an Amazon DynamoDB table. The developer wants to query the DynamoDB table by using the partition key and a different sort key value. The developer needs the latest data with all recent write operations.

How should the developer write the DynamoDB query?

A. Add a local secondary index (LSI) during table creation. Query the LSI by using eventually consistent reads.
B. Add a local secondary index (LSI) during table creation. Query the LSI by using strongly consistent reads.
C. Add a global secondary index (GSI) during table creation. Query the GSI by using eventually consistent reads.
D. Add a global secondary index (GSI) during table creation. Query the GSI by using strongly consistent reads.

---

**Question 362.** A developer manages an application that writes customer orders to an Amazon DynamoDB table. The table uses the customer_id as the partition key, order_id as the sort key, and order_date as an attribute. A new access pattern requires accessing data by order_date and order_id. The developer needs to implement a new AWS Lambda function to support the new access pattern.

How should the developer support the new access pattern in the MOST operationally efficient way?

A. Add a local secondary index (LSI) to the DynamoDB table that specifies order_date as the partition key and order_id as the sort key. Write the new Lambda function to query the new LSI index.
B. Write the new Lambda function to scan the DynamoDB table. In the Lambda function, write a method to retrieve and combine results by order_date and order_id.
C. Add a new global secondary index (GSI) to the DynamoDB table that specifies order_date as the partition key and order_id as the sort key. Write the new Lambda function to query the new GSI index.
D. Enable DynamoDB Streams on the table. Choose the new and old images information to write to the DynamoDB stream. Write the new Lambda function to query the DynamoDB stream.

---

**Question 363.** A developer is creating a web application for a school that stores data in Amazon DynamoDB. The ExamScores table has the following attributes: student_id, subject_name, and top_score.

Each item in the ExamScores table is identified with student_id as the partition key and subject_name as the sort key. The web application needs to display the student_id for the top scores for each school subject. The developer needs to increase the speed of the queries to retrieve the student_id for the top scorer for each school subject.

Which solution will meet these requirements?

A. Create a local secondary index (LSI) with subject_name as the partition key and top_score as the sort key.
B. Create a local secondary index (LSI) with top_score as the partition key and student_id as the sort key.
C. Create a global secondary index (GSI) with subject_name as the partition key and top_score as the sort key.
D. Create a global secondary index (GSI) with subject_name as the partition key and student_id as the sort key.

---

**Question 364.** A developer wrote an application that uses an AWS Lambda function to asynchronously generate short videos from customers. This video generation can take up to 10 minutes. After the video is generated, a URL to download the video is pushed to the customer's web browser. The customer should be able to access these videos for at least 3 hours after generation.

Which solution will meet these requirements?

A. Store the video in the /tmp folder within the Lambda execution environment. Push a Lambda function URL to the customer.
B. Store the video in an Amazon Elastic File System (Amazon EFS) file system attached to the function. Generate a pre-signed URL for the video object and push the URL to the customer.
C. Store the video in Amazon S3. Generate a pre-signed URL for the video object and push the URL to the customer.
D. Store the video in an Amazon CloudFront distribution. Generate a pre-signed URL for the video object and push the URL to the customer.

---

**Question 365.** A developer is creating an AWS Lambda function that is invoked by messages to an Amazon Simple Notification Service (Amazon SNS) topic. The messages represent customer data updates from a customer relationship management (CRM) system.

The developer wants the Lambda function to process only the messages that pertain to email address changes. Additional subscribers to the SNS topic will process any other messages.

Which solution will meet these requirements in the LEAST development effort?

A. Use Lambda event filtering to allow only messages that are related to email address changes to invoke the Lambda function.
B. Use an SNS filter policy on the Lambda function subscription to allow only messages that are related to email address changes to invoke the Lambda function.
C. Subscribe an Amazon Simple Queue Service (Amazon SQS) queue to the SNS topic. Configure the SQS queue with a filter policy to allow only messages that are related to email address changes. Connect the SQS queue to the Lambda function.
D. Configure the Lambda code to check the received message. If the message is not related to an email address change, configure the Lambda function to publish the message back to the SNS topic for the other subscribers to process.

---

**Question 366.** A developer is designing a fault-tolerant environment where client sessions will be saved.

How can the developer ensure that no sessions are lost if an Amazon EC2 instance fails?

A. Use sticky sessions with an Elastic Load Balancer target group.
B. Use Amazon SQS to save session data.
C. Use Amazon DynamoDB to perform scalable session handling.
D. Use Elastic Load Balancer connection draining to stop sending requests to failing instances.

---

**Question 367.** A developer is creating AWS CloudFormation templates to manage an application's deployment in Amazon Elastic Container Service (Amazon ECS) through AWS CodeDeploy. The developer wants to automatically deploy new versions of the application to a percentage of users before the new version becomes available for all users.

How should the developer manage the deployment of the new version?

A. Modify the CloudFormation template to include a Transform section and the AWS::CodeDeploy::BlueGreen hook.
B. Deploy the new version in a new CloudFormation stack. After testing is complete, update the application's DNS records for the new stack.
C. Run CloudFormation stack updates on the application stack to deploy new application versions when they are available.
D. Create a nested stack for the new version. Include a Transform section and the AWS::CodeDeploy::BlueGreen hook.

---

**Question 368.** A developer has written a distributed application that uses microservices. The microservices are running on Amazon EC2 instances. Because of message volume, the developer is unable to match log output from each microservice to a specific transaction. The developer needs to analyze the message flow to debug the application.

Which combination of steps should the developer take to meet this requirement? (Choose two.)

A. Download the AWS X-Ray daemon. Install the daemon on an EC2 instance. Ensure that the EC2 instance allows UDP traffic on port 2000.
B. Configure an interface VPC endpoint to allow traffic to reach the global AWS X-Ray daemon on TCP port 443.
C. Enable AWS X-Ray. Configure AWS CloudWatch to push logs to X-Ray.
D. Add the AWS X-Ray software development kit (SDK) to the microservices. Use X-Ray to trace requests that each microservice makes.
E. Set up Amazon CloudWatch metric streams to collect streaming data from the microservices.

---

**Question 369.** A company wants to deploy AWS Lambda functions and the dependent infrastructure with minimum coding effort. The application also needs to be reliable.

Which method will meet these requirements with the LEAST operational overhead?

A. Build the application by using shell scripts to create .zip files for each Lambda function. Manually upload the .zip files to the AWS Management Console.
B. Build the application by using the AWS Serverless Application Model (AWS SAM). Use a continuous integration and continuous delivery (CI/CD) pipeline and the SAM CLI to deploy the Lambda functions.
C. Build the application by using shell scripts to create .zip files for each Lambda function. Upload the .zip files. Deploy the .zip files as Lambda functions by using the AWS CLI in a continuous integration and continuous delivery (CI/CD) pipeline.
D. Build a container for each Lambda function. Store the container images in AWS CodeArtifact. Deploy the containers as Lambda functions by using the AWS CLI in a continuous integration and continuous delivery (CI/CD) pipeline.

---

**Question 370.** A developer needs to modify an application architecture to meet new functional requirements. Application data is stored in Amazon DynamoDB and processed for analysis in a nightly batch. The system analysts do not want to wait until the next day to view the processed data and have asked to have it available in near-real time.

Which application architecture pattern would enable the data to be processed as it is received?

A. Event driven
B. Client-server driven
C. Fan-out driven
D. Schedule driven

---

**Question 371.** A company hosts its application in the us-west-1 Region. The company wants to add redundancy in the us-east-1 Region.

The application secrets are stored in AWS Secrets Manager in us-west-1. A developer needs to replicate the secrets to us-east-1.

Which solution will meet this requirement?

A. Configure secret replication for each secret. Add us-east-1 as a replication Region. Choose an AWS Key Management Service (AWS KMS) key in us-east-1 to encrypt the replicated secrets.
B. Create a new secret in us-west-1 for each secret. Set the source to be the corresponding secret in us-east-1. Choose an AWS Key Management Service (AWS KMS) key in us-west-1 to encrypt the replicated secrets.
C. Create a lifecycle rule for each secret. Set us-east-1 as the destination Region. Configure the rule to run during secret rotation. Choose an AWS Key Management Service (AWS KMS) key in us-west-1 to encrypt the replicated secrets.
D. Create a Secrets Manager lifecycle rule to replicate each secret to a new Amazon S3 bucket in us-east-1. Configure an S3 replication rule to replicate the secrets to us-east-1.

---

**Question 372.** A company runs an ecommerce application on AWS. The application stores data in an Amazon Aurora database.

A developer is adding a caching layer to the application. The caching strategy must ensure that the application always uses the most recent value for each data item.

Which caching strategy will meet these requirements?

A. Implement a TTL strategy for every item that is saved in the cache.
B. Implement a write-through strategy for every item that is created and updated.
C. Implement a lazy loading strategy for every item that is loaded.
D. Implement a read-through strategy for every item that is loaded.

---

**Question 373.** A company has a serverless application that uses Amazon API Gateway backed by AWS Lambda proxy integration. The company is developing several backend APIs. The company needs a landing page to provide an overview of navigation to the APIs.

A developer creates a new LandingPage resource and a new GET method that uses mock integration.

What should the developer do next to meet these requirements?

A. Configure the integration request mapping template with Content-Type of text/html and statusCode of 200. Configure the integration response mapping template with Content-Type of application/json. In the integration response mapping template, include the LandingPage HTML code that references the APIs. Configure the integration response mapping template with Content-Type of text/html and statusCode of 200.
B. Configure the integration request mapping template with Content-Type of application/json. In the integration request mapping template, include the LandingPage HTML code that references the APIs. Configure the integration response mapping template with Content-Type of text/html and statusCode of 200.
C. Configure the integration request mapping template with Content-Type of application/json and statusCode of 200. Configure the integration response mapping template with Content-Type of text/html. In the integration response mapping template, include the LandingPage HTML code that references the APIs. Configure the integration response mapping template with Content-Type of application/json and statusCode of 200.
D. Configure the integration request mapping template with Content-Type of text/html. In the integration request mapping template, include the LandingPage HTML code that references the APIs. Configure the integration response mapping template with Content-Type of application/json and statusCode of 200.

---

**Question 374.** A developer creates an AWS Lambda function that is written in Java. During testing, the Lambda function does not work how the developer expected. The developer wants to use tracing capabilities to troubleshoot the problem.

Which AWS service should the developer use to accomplish this goal?

A. AWS Trusted Advisor
B. Amazon CloudWatch
C. AWS X-Ray
D. AWS CloudTrail

---

**Question 375.** A company is developing an application that will be accessed through the Amazon API Gateway REST API. Registered users should be the only ones who can access certain resources of this API. The token being used should expire automatically and needs to be refreshed periodically.

How can a developer meet these requirements?

A. Create an Amazon Cognito identity pool, configure the Amazon Cognito Authorizer in API Gateway, and use the temporary credentials generated by the identity pool.
B. Create and maintain a database record for each user with a corresponding token and use an AWS Lambda authorizer in API Gateway.
C. Create an Amazon Cognito user pool, configure the Cognito Authorizer in API Gateway, and use the identity or access token.
D. Create an IAM user for each API user, attach an invoke permissions policy to the API, and use an IAM authorizer in API Gateway.

---

**Question 376.** A company used AWS to develop an application for customers. The application includes an Amazon API Gateway that invokes AWS Lambda functions. The Lambda functions process data and store the data in Amazon DynamoDB tables.

The company must monitor the entire application to identify potential bottlenecks in the architecture that can negatively affect customers.

Which solution will meet this requirement with the LEAST development effort?

A. Instrument the application with AWS X-Ray. Inspect the service map to identify errors and issues.
B. Configure Lambda exceptions and additional logging to Amazon CloudWatch. Use CloudWatch Logs Insights to query the logs.
C. Configure API Gateway to log responses to Amazon CloudWatch. Create a metric filter for the TooManyRequestsException error message.
D. Use Amazon CloudWatch metrics for the DynamoDB tables to identify all the ProvisionedThroughputExceededException error messages.

---

**Question 377.** A company launched an online portal to announce a new product that the company will release in 6 months. The portal requests that users enter an email address to receive communications about the product. The company needs to create a REST API that will store the email addresses in Amazon DynamoDB. The developer will deploy the Lambda function by using the AWS Serverless Application Model (AWS SAM). The developer must provide access to the Lambda function over HTTP.

Which solutions will meet these requirements with the LEAST additional configuration? (Choose two.)

A. Expose the Lambda function by using function URLs.
B. Expose the Lambda function by using a Gateway Load Balancer.
C. Expose the Lambda function by using a Network Load Balancer.
D. Expose the Lambda function by using AWS Global Accelerator.
E. Expose the Lambda function by using Amazon API Gateway.

---

**Question 378.** A company has a website that displays a daily newsletter. When a user visits the website, an AWS Lambda function processes the browser's request and queries the company's on-premises database to obtain the current newsletter. The newsletters are stored in English. The Lambda function uses the Amazon Translate TranslateText API operation to translate the newsletters, and the translation is displayed to the user.

Due to an increase in popularity, the website's response time has slowed. The database is overloaded. The company cannot change the database and needs a solution that improves the response time of the Lambda function.

Which solution meets these requirements?

A. Change to asynchronous Lambda function invocation.
B. Cache the translated newsletters in the Lambda/tmp directory.
C. Enable TranslateText API caching.
D. Change the Lambda function to use parallel processing.

---

**Question 379.** A developer is monitoring an application that runs on an Amazon EC2 instance. The developer has configured a custom Amazon CloudWatch metric with data granularity of 1 second. If any issues occur, the developer wants to be notified within 30 seconds by Amazon Simple Notification Service (Amazon SNS).

What should the developer do to meet this requirement?

A. Configure a high-resolution CloudWatch alarm.
B. Set up a custom CloudWatch dashboard.
C. Use Amazon CloudWatch Logs Insights.
D. Change to a default CloudWatch metric.

---

**Question 380.** A company has a web application that contains an Amazon API Gateway REST API. A developer has created an AWS CloudFormation template for the initial deployment of the application. The developer has deployed the application successfully as part of an AWS CodePipeline continuous integration and continuous delivery (CI/CD) process.

The CloudFormation template contains the following resource types:
- AWS::ApiGateway::RestApi
- AWS::ApiGateway::Resource
- AWS::ApiGateway::Method
- AWS::ApiGateway::Stage
- AWS::ApiGateway::Deployment

The developer adds a new resource to the REST API with additional methods and redeploys the template. CloudFormation reports that the deployment is successful and the stack is in the UPDATE_COMPLETE state. However, calls to all new methods are returning 404 (Not Found) errors.

What should the developer do to make the new methods available?

A. Specify the disable-rollback option with the stack update operation.
B. Unset the CloudFormation stack failure options.
C. Add an action to CodePipeline to run the aws apigateway create-deployment AWS CLI command.
D. Add an action to CodePipeline to run the aws cloudfront create-invalidation AWS CLI command.

---

**Question 381.** A developer updates an AWS Lambda function that an Amazon API Gateway API uses. The API is the backend for a web application.

The developer needs to test the updated Lambda function before deploying the Lambda function to production. The testing must not affect production users of the web application.

Which solution will meet these requirements in the MOST operationally efficient way?

A. Create a canary release deployment for the existing API Gateway stage. Deploy the API to the existing stage. Test the updated Lambda function by using the existing URL.
B. Update the API Gateway API endpoint to private. Deploy the changes to the existing API Gateway stage. Test the updated Lambda function by using the existing URL.
C. Create a new test API stage in API Gateway. Add stage variables to deploy the updated Lambda function to only the test stage. Test the API by using the test stage URL.
D. Create a new AWS CloudFormation stack to deploy a copy of the entire production API and Lambda function. Use the stack's API URL to test the updated Lambda function.

---

**Question 382.** A developer wants the ability to roll back to a previous version of an AWS Lambda function in the event of errors caused by a new deployment.

How can the developer achieve this with MINIMAL impact on users?

A. Change the application to use an alias that points to the current version. Deploy the new version of the code. Update the alias to direct 10% of users to the newly deployed version. If too many errors are encountered, point the alias back to the previous version.
B. Change the application to use an alias that points to the current version. Deploy the new version of the code. Update the alias to direct 10% of users to the newly deployed version. If too many errors are encountered, point the alias back to the previous version.
C. Do not make any changes to the deployment. Deploy the new version of the code. If too many errors are encountered, point the application back to the previous version by using the version number in the Amazon Resource Name (ARN).
D. Create three aliases: new, existing, and router. Point the existing alias to the current version. Make the router alias direct 100% of users to the existing alias. Update the application to use the router alias. Deploy the new version of the code. Update the router alias to direct 10% of users to the new alias. If too many errors are encountered, send 100% of traffic to the existing alias.

---

**Question 383.** A company maintains a REST service using Amazon API Gateway and the API Gateway native API key validation. The company recently launched a new registration page, which allows users to sign up for the service. The registration page creates a new API key by using the CreateApiKey API and sends the new key to the user. When the user attempts to call the API using this key, the user receives a 403 Forbidden error. Existing users are unaffected and can still call the API.

What code deployment will grant these new users access to the API?

A. The createDeployment method must be called so the API can be redeployed to include the newly created API key.
B. The updateAuthorizer method must be called to update the API's authorizer to include the newly created API key.
C. The importApiKeys method must be called to import all newly created API keys into the current stage of the API.
D. The createUsagePlanKey method must be called to associate the newly created API key with the correct usage plan.

---

**Question 384.** A company uses an AWS CloudFormation template to deploy and manage its AWS infrastructure. The CloudFormation template creates Amazon VPC security groups and Amazon EC2 security groups.

A manager finds out that some engineers modified the security groups of a few EC2 instances for testing purposes. A developer needs to determine what modifications occurred.

Which solution will meet this requirement?

A. Add a Conditions section in the source YAML file of the template. Run the CloudFormation stack.
B. Perform a drift detection operation on the CloudFormation stack.
C. Execute a change set for the CloudFormation stack.
D. Use Amazon Detective to detect the modifications.

---

**Question 385.** An IAM role is attached to an Amazon EC2 instance that explicitly denies access to all Amazon S3 API actions. The EC2 instance credentials file specifies the IAM access key and secret access key, which allow full administrative access.

Given that multiple modes of IAM access are present for this EC2 instance, which of the following is correct?

A. The EC2 instance will only be able to list the S3 buckets.
B. The EC2 instance will only be able to list the contents of one S3 bucket at a time.
C. The EC2 instance will be able to perform all actions on any S3 bucket.
D. The EC2 instance will not be able to perform any S3 action on any S3 bucket.

---

**Question 386.** A company uses an AWS Lambda function to transfer files from an Amazon S3 bucket to the company's SFTP server. The Lambda function connects to the SFTP server by using credentials such as username and password. The company uses Lambda environment variables to store these credentials.

A developer needs to implement encrypted username and password credentials.

Which solution will meet these requirements?

A. Remove the user credentials from the Lambda environment. Implement IAM database authentication.
B. Move the user credentials from Lambda environment variables to AWS Systems Manager Parameter Store.
C. Move the user credentials from Lambda environment variables to AWS Key Management Service (AWS KMS).
D. Move the user credentials from the Lambda environment to an encrypted .txt file. Store the file in an S3 bucket.

---

**Question 387.** A developer is creating a new batch application that will run on an Amazon EC2 instance. The application requires read access to an Amazon S3 bucket. The developer needs to follow security best practices to grant S3 read access to the application.

Which solution meets these requirements?

A. Add the permissions to an IAM policy. Attach the policy to a role. Attach the role to the EC2 instance profile.
B. Add the permissions inline to an IAM group. Attach the group to the EC2 instance profile.
C. Add the permissions to an IAM policy. Attach the policy to a user. Attach the user to the EC2 instance profile.
D. Add the permissions to an IAM policy. Use IAM web identity federation to access the S3 bucket with the policy.

---

**Question 388.** A company has an application that receives batches of orders from partners every day. The application uses an AWS Lambda function to process the batches.

If a batch contains no orders, the Lambda function must publish to an Amazon Simple Notification Service (Amazon SNS) topic as soon as possible.

Which combination of steps will meet this requirement with the LEAST implementation effort? (Choose two.)

A. Update the existing Lambda function's code to send an Amazon CloudWatch custom metric for the number of orders in a batch for each partner.
B. Create a new Lambda function as an Amazon Kinesis Data Streams consumer. Configure the new Lambda function to track orders and to publish to the SNS topic when a batch contains no orders.
C. Set up an Amazon CloudWatch alarm that will send a notification to the SNS topic when the value of the custom metric is 0.
D. Schedule a new Lambda function to analyze Amazon CloudWatch metrics every 24 hours to identify batches that contain no orders. Configure the Lambda function to publish to the SNS topic.
E. Modify the existing Lambda function to log orders to an Amazon Kinesis data stream.

---

**Question 389.** A developer has an application that uses an Amazon DynamoDB table with a configured local secondary index (LSI). During application testing, the DynamoDB table metrics report a ProvisionedThroughputExceededException error message. The number of requests made by the test suite did not exceed the table's provisioned capacity limits.

What is the cause of this issue?

A. The data in the table's partition key column is not evenly distributed.
B. The LSI's capacity is different from the table's capacity.
C. The application is not implementing exponential backoff retry logic while interacting with the DynamoDB API.
D. The application has the IAM permission to query the DynamoDB table but not to query the LSI.

---

**Question 390.** A developer manages a website that distributes its content by using Amazon CloudFront. The website's static artifacts are stored in an Amazon S3 bucket.

The developer deploys some changes and can see the new artifacts in the S3 bucket. However, the changes do not appear on the webpage that the CloudFront distribution delivers.

How should the developer resolve this issue?

A. Configure S3 Object Lock to update to the latest version of the files every time an S3 object is updated.
B. Configure the S3 bucket to clear all objects from the bucket before new artifacts are uploaded.
C. Set CloudFront to invalidate the cache after the artifacts have been deployed to Amazon S3.
D. Set CloudFront to modify the distribution origin after the artifacts have been deployed to Amazon S3.

---

**Question 391.** A company has a development team that uses AWS CodeCommit repositories in multiple AWS accounts. The team is expanding to include developers who work in various locations.

The company must ensure that the developers have secure access to the repositories.

Which solution will meet these requirements in the MOST operationally efficient way?

A. Configure IAM roles for each developer and grant access individually.
B. Configure permission sets in AWS IAM Identity Center to grant access to the accounts.
C. Share AWS access keys with the development team for direct repository access.
D. Use public SSH keys for authentication to the CodeCommit repositories.

---

**Question 392.** A developer received the following error message during an AWS CloudFormation deployment:

DELETE_FAILED (The following resource(s) failed to delete: [ASGInstanceRole12345678].)

Which action should the developer take to resolve this error?

A. Contact AWS Support to report an issue with the Auto Scaling Groups (ASG) service.
B. Add a DependsOn attribute to the ASGInstanceRole12345678 resource in the CloudFormation template. Then delete the stack.
C. Modify the CloudFormation template to retain the ASGInstanceRole12345678 resource. Then manually delete the resource after the stack.
D. Add a force parameter when calling CloudFormation with the role-arn of ASGInstanceRole12345678.

---

**Question 393.** A company is running a critical application on Amazon Elastic Container Service (Amazon ECS) by using Amazon EC2 instances. The company needs to migrate the application to Amazon ECS on AWS Fargate. A developer is configuring Fargate and the ECS capacity providers to make the change.

Which solution will meet these requirements with the LEAST downtime during migration?

A. Use the PutClusterCapacityProviders API operation to associate the ECS cluster with the FARGATE and FARGATE_SPOT capacity provider strategies. Use FARGATE as Provider 1 with a base value. Use FARGATE_SPOT as Provider 2 for failover.
B. Use the CreateCapacityProvider API operation to associate the ECS cluster with the FARGATE and FARGATE_SPOT capacity provider strategies. Use FARGATE as Provider 1 with a base value. Use FARGATE_SPOT as Provider 2 for failover.
C. Use the PutClusterCapacityProviders API operation to associate the ECS cluster with the FARGATE and FARGATE_SPOT capacity provider strategies. Use FARGATE_SPOT as Provider 1 with a base value. Use FARGATE as Provider 2 for failover.
D. Use the CreateCapacityProvider API operation to associate the ECS cluster with the FARGATE and FARGATE_SPOT capacity provider strategies. Use FARGATE_SPOT as Provider 1 with a base value. Use FARGATE as Provider 2 for failover.

---

**Question 394.** A company has a web application that is hosted on AWS. The application is behind an Amazon CloudFront distribution. A developer needs to monitor the error rates and anomalies of the CloudFront distribution as frequently as possible.

Which combination of steps should the developer take to meet these requirements? (Choose two.)

A. Stream the CloudFront distribution logs to an Amazon S3 bucket. Detect anomalies and error rates by using Amazon Kinesis Data Streams.
B. Enable real-time logs on the CloudFront distribution. Create a data stream in Amazon Kinesis Data Streams. Subscribe to the Kinesis data stream to receive the logs.
C. Set up Amazon Kinesis Data Streams to send the logs to Amazon OpenSearch Service by using an AWS Lambda function. Make a dashboard in OpenSearch Dashboards.
D. Stream the CloudFront distribution logs to Amazon Kinesis Data Firehose.
E. Set up Route 53 health checks to monitor the application's availability. Turn on AWS CloudTrail logs for all the AWS services that the application uses. Send the logs to Amazon S3 bucket.

---

**Question 395.** A developer creates an Amazon DynamoDB table. The table has OrderID as the partition key and NumberOfItemsPurchased as the sort key. The data type of the partition key and the sort key is Number.

When the developer queries the table, the results are sorted by NumberOfItemsPurchased in ascending order. The developer needs the query results to be sorted by NumberOfItemsPurchased in descending order.

Which solution will meet this requirement?

A. Create a local secondary index (LSI) on the NumberOfItemsPurchased sort key.
B. Change the sort key from NumberOfItemsPurchased to NumberOfItemsPurchasedDescending.
C. In the Query operation, set the ScanIndexForward parameter to false.
D. In the Query operation, set the KeyConditionExpression parameter to false.

---

**Question 396.** A developer needs to use a code template to create an automated deployment of an application onto Amazon EC2 instances. The template must be configured to support repeated deployment, installation, and updates of resources for the application. The template must be able to create identical environments and roll back to previous versions.

Which solution will meet these requirements?

A. Use AWS Amplify for automatic deployment templates. Use a traffic-splitting deployment to copy any deployments. Manually remove any resources created by Amplify, if necessary.
B. Use AWS CodeBuild for automatic deployment. Upload the required AppSpec file template. Save the appspec.yml file in the home directory of the deployment folder of the service. Save the EC2 instances for the deployment.
C. Use AWS CloudFormation to create an infrastructure template in JSON format to deploy the EC2 instances and to start the application. Call the scripts directly from the template.
D. Use AWS AppSync to deploy the application. Upload the template as a GraphQL schema. Specify the EC2 instances for deployment, and use resolvers as a version control mechanism and to roll back to the deployments.

---

**Question 397.** A developer has a continuous integration and continuous delivery (CI/CD) pipeline that uses AWS CodeBuild. The build artifacts are stored in an Amazon S3 bucket. The builds happen frequently and retrieve many dependencies from CodeArtifact each time.

The builds have been slow because of the time it takes to transfer dependencies. The developer needs to improve build performance by reducing the number of dependencies that are retrieved for each build.

A. Specify an Amazon S3 cache in CodeBuild. Add the S3 cache folder path to the buildspec.yaml file for the build project.
B. Specify a local cache in CodeBuild. Add the CodeArtifact repository name to the buildspec.yaml file for the build project.
C. Specify a local cache in CodeBuild. Add the cache path to the buildspec.yaml file for the build project.
D. Retrieve the buildspec.yaml file directly from CodeArtifact. Add the CodeArtifact repository name to the buildspec.yaml file for the build project.

---

**Question 398.** A company that has large online business uses an Amazon DynamoDB table to store sales data. The company enabled Amazon DynamoDB Streams on the table. The value of the TransactionStatus attribute must be tracked. The value of the TransactionStatus attribute is stored in a TransactionStatus attribute in the table.

The company wants to be notified of failed sales where the Price attribute is above a specific threshold. A developer needs to set up notification for the failed sales.

Which solution will meet these requirements with the LEAST development effort?

A. Create an event source mapping between DynamoDB Streams and an AWS Lambda function. Configure the Lambda function to use Lambda event filtering to invoke the Lambda function only if sales fail when the price is above the specified threshold. Configure the Lambda function to publish the data to an Amazon Simple Notification Service (Amazon SNS) topic.
B. Create an event source mapping between DynamoDB Streams and an AWS Lambda function. Configure the Lambda function to check if sales fail when the price is above the specified threshold. Subscribe the Lambda function to the SNS topic.
C. Create an event source mapping between DynamoDB Streams and an Amazon Simple Notification Service (Amazon SNS) topic. Use event filtering to publish to the SNS topic if sales fail when the price is above the specified threshold.
D. Create an Amazon CloudWatch alarm to monitor the DynamoDB Streams sales data. Configure the alarm to publish to an Amazon Simple Notification Service (Amazon SNS) topic if sales fail due to the price being above the specified threshold.

---

**Question 399.** An AWS Lambda function is invoked asynchronously to process events. Occasionally, the Lambda function fails to process some messages. A developer finds the bug and wants to collect and analyze these failed events.

What should the developer do to meet these requirements with the LEAST development effort?

A. Add logging statements for all events in the Lambda function. Filter AWS CloudTrail logs for errors.
B. Configure the Lambda function to send messages to an AWS Step Functions workflow with retries for failed events.
C. Add a dead-letter queue to send messages to an Amazon Simple Queue Service (Amazon SQS) standard queue.
D. Add a dead-letter queue to send messages to an Amazon Simple Notification Service (Amazon SNS) FIFO topic.

---

**Question 400.** A company has an application that needs to configure in-transit encryption for Amazon S3 bucket for object storage. A developer needs to ensure that the S3 objects containing personal data need to be encrypted at rest using a customer managed key. Objects must be encrypted at rest, and data needs to be encrypted at rest using AWS Key Management Service (AWS KMS) keys, which can be rotated on demand.

Which combination of steps will meet these requirements? (Choose two.)

A. Write an S3 bucket policy to allow only encrypted connections over HTTPS by using permissions boundary.
B. Configure an S3 bucket policy to enable client-side encryption for the objects containing personal data by using an AWS KMS customer managed key.
C. Configure the application to encrypt the objects by using an AWS KMS customer managed key before uploading the objects containing personal data to Amazon S3.
D. Write an S3 bucket policy to allow only encrypted connections over HTTPS by using the aws:SecureTransport condition.
E. Configure S3 Block Public Access settings for the S3 bucket to allow only encrypted connections over HTTPS.

---

**Question 401.** A company has a monolithic desktop-based application that processes images. A developer is converting the application into an AWS Lambda function by using Python. Currently, the desktop application runs every 5 minutes to process the latest image from an Amazon S3 bucket. The desktop application completes the image processing task within 1 minute.

During testing on AWS, the developer notices that the Lambda function runs at the specified 5-minute interval. However, the Lambda function takes more than 2 minutes to complete the image processing task. The developer needs a solution that will improve the Lambda function's performance.

Which solution will meet this requirement?

A. Update the instance type of the Lambda function to a compute optimized instance with at least eight virtual CPU (vCPU).
B. Update the configuration of the Lambda function to use the latest Python runtime.
C. Increase the memory that is allocated to the Lambda function.
D. Configure a reserved concurrency on the Lambda function.

---

**Question 402.** A company uses AWS CloudFormation templates to manage infrastructure for its development, pre-production, and production environments. The company needs to scale for increasing customer demand. A developer must upgrade the Amazon RDS DB instance type to a larger instance in the pre-production environment. The developer notices that the state in the CloudFormation stack with the instance size change in the pre-production environment is in an UPDATE_ROLLBACK_FAILED state.

Which option is the cause of this issue?

A. The new instance type specified in the CloudFormation template is invalid.
B. The database was deleted or modified manually outside of the CloudFormation stack.
C. There is a syntax error in the CloudFormation template.
D. The developer has insufficient IAM permissions to provision an instance of the specified type.

---

**Question 403.** A developer needs to store files in an Amazon S3 bucket for a company's application. Each S3 object can have multiple versions. The objects must be permanently removed 1 year after object creation.

The developer creates an S3 bucket that has versioning enabled.

What must the developer do next to meet the data retention requirements?

A. Create an S3 Lifecycle rule on the S3 bucket. Configure the rule to expire current versions of objects and permanently delete noncurrent versions 1 year after object creation.
B. Create an event notification for all object creation events in the S3 bucket. Configure the event notification to invoke an AWS Lambda function. Program the Lambda function to check the object creation date and to delete the object if the object is older than 1 year.
C. Create an event notification for all object removal events in the S3 bucket. Configure the event notification to invoke an AWS Lambda function. Program the Lambda function to check the object creation date and to delete the object if the object is older than 1 year.
D. Create an S3 Lifecycle rule on the S3 bucket. Configure the rule to delete expired object delete markers and permanently delete noncurrent versions 1 year after object creation.

---

**Question 404.** A company uses AWS X-Ray to monitor a serverless application. The components of the application have different request properties. The background processes such as application health checks, polling, and connection maintenance generate high volumes of read-only requests.

Currently, the default X-Ray sampling rules are universal for all requests. Only the first request each second and a random sample of 5% of additional requests are recorded. This setup is not helping the company review the requests based on service or request type.

A developer must create custom rules to trace the user interactions and transactions without wasting effort recording monitoring background tasks.

Which solution will meet these requirements?

A. Disable sampling for high-volume read-only requests. Sample at a lower rate for all requests that handle user interactions or transactions. Sample high-volume read-only requests at a higher rate.
B. Disable sampling and trace all requests for requests that handle user interactions or transactions. Sample high-volume read-only requests at a higher rate.
C. Disable sampling and trace all requests for requests that handle user interactions or transactions. Sample high-volume read-only requests at a lower rate.
D. Disable sampling for high-volume read-only requests. Sample at a higher rate for all requests that handle user interactions or transactions.

---

**Question 405.** A developer uses an AWS Lambda function in an application to edit users' uploaded photos. The developer needs to divide the user traffic between the original version of the Lambda function and the new version of the Lambda function.

Which combination of steps will meet these requirements? (Choose two.)

A. Publish a version of the original Lambda function. Make the necessary changes to the Lambda code. Publish a new version of the Lambda function.
B. Use AWS CodeBuild to update the Lambda function. Configure CodeBuild to incrementally shift traffic from the original Lambda function to the new Lambda function.
C. Update the original version of the Lambda function to add a function URL. Make the necessary changes to the Lambda code. Configure the integration response mapping template with Content-Type of application/json and statusCode of 200.
D. Create an alias for the Lambda function. Configure weighted routing on the alias. Specify a 10% weight for the new Lambda function version.
E. Create an alias that points to the original function URL. Configure the alias to be a weighted alias that also includes the additional function URL. Divide traffic between the two function URLs.

---

**Question 406.** A company had an Amazon RDS for MySQL DB instance that was named mysql-db. The DB instance was deleted within the past 90 days.

A developer needs to find which IAM user or role deleted the DB instance in the AWS environment.

Which solution will provide this information?

A. Retrieve the AWS CloudTrail events for the resource mysql-db where the event name is DeleteDBInstance. Inspect the log events.
B. Retrieve the Amazon CloudWatch log events from the most recent log stream within the rds/mysql-db log group. Inspect the log events.
C. Retrieve the AWS X-Ray trace summaries. Filter by services with the name mysql-db. Inspect the ErrorRootCauses values within each summary.
D. Retrieve the AWS Systems Manager deletions inventory. Filter the inventory by deletions that have a TypeName value of RDS. Inspect the deletion details.

---

**Question 407.** A company migrates the on-premises MySQL database to an Amazon RDS for MySQL database. The developer's solution must not use long-term credentials.

Which solution will meet these requirements?

A. Enable IAM database authentication on the RDS for MySQL DB instance. Create an IAM role that has the minimum required permissions. Assign the role to the application.
B. Store the MySQL credentials as secrets in AWS Secrets Manager. Create an IAM role that has the minimum required permissions to retrieve the secrets. Assign the role to the application.
C. Configure the MySQL credentials as environment variables that are available at runtime for the application.
D. Store the MySQL credentials as SecureString parameters in AWS Systems Manager Parameter Store. Create an IAM role that has the minimum required permissions to retrieve the parameters. Assign the role to the application.

---

**Question 408.** A developer is creating an application that must transfer expired items from Amazon DynamoDB to Amazon S3. The developer set up the DynamoDB table to automatically delete items based on a specific TTL. The application must process the items in DynamoDB and then must store the expired items in Amazon S3. The entire process, including item processing and storage in Amazon S3, will take 5 minutes.

Which solution will meet these requirements with the LEAST operational overhead?

A. Configure DynamoDB Accelerator (DAX) to query for expired items based on the TTL. Save the results to Amazon S3.
B. Configure DynamoDB Streams to invoke an AWS Lambda function. Program the Lambda function to process the items and to store the expired items in Amazon S3.
C. Deploy a custom application on an Amazon Elastic Container Service (Amazon ECS) cluster on Amazon EC2 instances. Program the application to process the items and to store the expired items in Amazon S3.
D. Create an Amazon EventBridge rule to invoke an AWS Lambda function. Program the Lambda function to process the items and to store the expired items in Amazon S3.

---

**Question 409.** A developer has an application that uses WebSocket APIs in Amazon API Gateway. The developer wants to use an API Gateway Lambda authorizer.

The developer needs to add credential caching and reduce repeated usage of secret keys and authorization tokens on every request.

Which combination of steps should the developer take to meet these requirements? (Choose two.)

A. Use a token-based Lambda authorizer.
B. Use a request parameter-based Lambda authorizer.
C. Configure an integration request mapping template to reference the context map from the APIGateway Lambda authorizer.
D. Configure an integration request mapping template to reference the identity API key value from the API Gateway Lambda authorizer.
E. Use VPC endpoint policies for the WebSocket APIs.

---

**Question 410.** A developer builds a serverless application on AWS by using Amazon API Gateway, AWS Lambda functions, and Amazon Route 53. During testing, the developer notices errors and wants to immediately locate the root cause.

To identify the errors, the developer needs to search all the application's logs.

What should the developer do to meet these requirements with the LEAST operational overhead?

A. Set up API Gateway health checks to monitor the application's availability. Use the CloudWatch PutMetricData API operation to publish the logs to CloudWatch. Search and query the logs by using Amazon Athena.
B. Set up Route 53 health checks to monitor the application's availability. Turn on AWS CloudTrail logs for all the AWS services that the application uses. Send the logs to a specified Amazon S3 bucket. Use Amazon Athena to search and analyze the logs.
C. Configure all the application's AWS services to publish a real-time feed of log events to an Amazon Kinesis Data Firehose delivery stream. Configure the delivery stream to use Amazon OpenSearch Service by using an AWS Lambda function. Make a dashboard in OpenSearch Dashboards.
D. Set up Route 53 health checks to monitor the application's availability. Turn on AWS CloudTrail Logs for all the AWS services that the application uses. Use CloudWatch Logs Insights to search and analyze the logs.

---

**Question 411.** A developer needs to freeze changes to an AWS CodeCommit repository before a production release. The developer will work on new features while a quality assurance (QA) team tests the release. The QA testing and all bug fixes must take place in isolation from the main branch. After the release, the developer must merge the features into the main branch.

Which solution will meet these requirements?

A. Create a release branch from the latest Git commit that will be in the release. Apply fixes to the release branch. Continue developing new features, and merge the features into the main branch. Merge the release branch into the main branch after the release.
B. Create a Git tag on the latest Git commit that will be in the release. Continue developing new features, and merge the features into the main branch. Merge the release branch into the main branch after the release. Rebase the release branch onto the main branch.
C. Create a release branch from the latest Git commit that will be in the release. Continue developing new features, and merge the features into the main branch. Apply fixes to the main branch. Update the Git tag for the release to be to the latest commit on the release branch after the release. Rebase the release branch after the release.
D. Create a Git tag on the latest Git commit that will be in the release. Continue developing new features, and merge the features into the main branch. Apply the Git commits for fixes to the Git tag for the release.

---

**Question 412.** A developer is setting up AWS CodePipeline for a new application. During each build, the developer must generate a test report.

Which solution will meet this requirement?

A. Create an AWS CodeBuild build project that runs tests. Configure the buildspec file with the test report information.
B. Create an AWS CodeDeploy deployment that runs tests. Configure the AppSpec file with the test report information.
C. Run the builds on an Amazon EC2 instance that has AWS Systems Manager Agent (SSM Agent) installed and activated.
D. Create a repository in AWS CodeArtifact. Select the test report template.

---

**Question 413.** A developer built an application by using multiple AWS Lambda functions. The Lambda functions must access dynamic configuration data at runtime. The data is maintained in a 6 KB JSON document in AWS AppConfig. The configuration data needs to be updated without requiring the redeployment of the application.

What should the developer do to meet these requirements with the LEAST development effort?

A. Migrate the document from AWS AppConfig to a Lambda environment variable. Read the document at the runtime.
B. Configure the AWS AppConfig Agent Lambda extension. Access the dynamic configuration data by calling the extension on a local host.
C. Use the AWS X-Ray SDK to call the AWS AppConfig APIs. Retrieve the configuration file at runtime.
D. Migrate the configuration file to a Lambda deployment package. Read the file from the file system at runtime.

---

**Question 414.** A developer has AWS Lambda functions that need to access a company's internal data libraries and reference data. Separate teams manage the libraries and the data. The teams must be able to update and upload new data independently. The Lambda functions are connected to the company's central VPC.

Which solution will provide Lambda functions with access to the libraries and data?

A. Attach an Amazon Elastic Block Store (Amazon EBS) volume to the Lambda functions by using EBS Multi-Attach in the central VPC. Update the Lambda function execution roles to give the functions access to the EBS volume. Write the Lambda function code to reference the files in the EBS volume in the /tmp folder.
B. Compress the libraries and reference data in a Lambda /tmp folder. Update the Lambda function code to reference the files in the /tmp folder.
C. Set up an Amazon Elastic File System (Amazon EFS) file system with mount targets in the central VPC. Update the Lambda function execution roles to give the functions access to the EFS file system. Update the Lambda functions to mount the EFS file system. Update the Lambda function execution roles to give the functions to access the EFS file system.
D. Set up an Amazon FSx for Windows File Server file system with mount targets in the central VPC. Configure the Lambda functions to mount the Amazon FSx file system. Update the Lambda function execution roles to give the functions to access the FSx file system.

---

**Question 415.** A company has an application that uses an AWS Lambda function to consume messages from an Amazon Simple Queue Service (Amazon SQS) queue. The SQS queue is configured with a dead-letter queue. Due to a defect in the application, AWS Lambda failed to process some messages. A developer fixed the bug and wants to process the failed messages again.

How should the developer resolve this issue?

A. Use the SendMessageBatch API to send messages from the dead-letter queue to the original SQS queue.
B. Use the ChangeMessageVisibility API to configure messages in the dead-letter queue to be visible in the original SQS queue.
C. Use the StartMessageMoveTask API to move messages from the dead-letter queue to the original SQS queue.
D. Use the PurgeQueue API to remove messages from the dead-letter queue and return the messages to the original SQS queue.

---

**Question 416.** A developer is working on an application that will be deployed on AWS. The developer needs to test and debug the code locally. The code is packaged and stored in an Amazon S3 bucket.

How can the developer test and debug the code locally with the LEAST amount of configuration?

A. Create an application and a deployment group in AWS CodeDeploy. For the compute platform, specify the local machine as the individual instance for the deployment. For the repository type, specify that the application is stored in Amazon S3. Start the deployment to test on the local machine.
B. Create a repository in AWS CodeArtifact. Publish the application code package to the repository. Before deployment, create an upstream repository to test and validate the code.
C. Create a build project in AWS CodeBuild. In AWS CodePipeline, add a stage and an action. For the provider, specify CodeBuild and link the build project. View the build log to see the test results.
D. Install the AWS CodeDeploy agent locally to validate the deployment package. Run the codedeploy-local command. Specify the S3 bucket where the code package is located by using the --bundle-location option.

---

**Question 417.** A developer is creating an application on Amazon Elastic Container Service (Amazon ECS). The developer needs to configure the application parameters. The developer must configure the maximum number of simultaneous connections and maximum number of transactions per second.

The maximum number of connections and transactions can change in the future. The developer needs a solution that can automatically deploy these changes to the application, as needed, without causing downtime.

Which solution will meet these requirements?

A. Make the configuration changes for the application. Use AWS CodeDeploy to create a deployment configuration. Deploy the ECSCanary10Percent15Minutes launch type in the properties section of the ECS resource. Deploy the application by using CodeDeploy.
B. Bootstrap the application to use the AWS Cloud Development Kit (AWS CDK). Make the configuration changes. Specify the ECSCanary10Percent20Minutes as the deployment strategy. Deploy the changes by using AWS CodeDeploy.
C. Install the AWS AppConfig agent on Amazon ECS. Configure an IAM role with access to AWS AppConfig. Make the deployment changes by using AWS AppConfig.
D. Create an AWS Lambda function to make the configuration changes. Create an Amazon CloudWatch alarm that monitors the Lambda function when it has been updated. Deploy the changes by using AWS CodeDeploy.

---

**Question 418.** A developer has built an application running on AWS Lambda using AWS Serverless Application Model (AWS SAM).

What is the correct sequence of steps to successfully deploy the application?

A. 1. Build the SAM template in Amazon EC2. 2. Package the SAM template to Amazon EBS storage. 3. Deploy the SAM template from Amazon EBS.
B. 1. Build the SAM template locally. 2. Package the SAM template onto Amazon S3. 3. Deploy the SAM template from Amazon S3.
C. 1. Build the SAM template locally. 2. Deploy the SAM template from Amazon S3. 3. Package the SAM template for use.
D. 1. Build the SAM template locally. 2. Package the SAM template to AWS CodeCommit. 3. Deploy the SAM template to CodeCommit.

---

**Question 419.** A developer needs to deploy the code for a new application on an AWS Lambda function. The application needs a deployment file that is 500 MB to run the business logic.

Which solution will meet these requirements?

A. Compress the application code and dependencies into a .zip file. Directly upload the .zip file as a deployment package for the Lambda function instead of copying the code.
B. Compress the application code and dependencies into a .zip file. Upload the .zip file to an Amazon S3 bucket. Configure the Lambda function to run the code from the .zip file in the S3 bucket.
C. Package the application code and dependencies into a container image. Upload the image to an Amazon S3 bucket. Configure the Lambda function to run the code in the container.
D. Package the application code and dependencies into a container image. Push the image to an Amazon Elastic Container Registry (Amazon ECR) repository. Deploy the image to the Lambda function.

---

**Question 420.** A company is developing a publicly accessible single-page application. The application makes calls from a web user browser to backend services to provide a user interface to customers. The application depends on a third-party web service exposed as an HTTP API. The web client must provide an API key to the third-party web service by using the HTTP header as part of the HTTP request. The company's API key must not be exposed to the users of the web application.

Which solution will meet these requirements MOST cost-effectively?

A. Use Amazon API Gateway to create a private REST API. Create an HTTP integration to integrate with the third-party HTTP API. Add the company's API key to the HTTP headers list of the integration request configuration.
B. Use Amazon API Gateway to create a public REST API. Create a Lambda proxy integration. Make calls to the third-party HTTP API from the Lambda function. Pass the company's API key as an HTTP request header.
C. Use Amazon API Gateway to create a REST API. Create an HTTP integration to integrate with the third-party HTTP API. Add the company's API key to the HTTP headers list of the integration request configuration.
D. Use Amazon API Gateway to create a REST API. Create an AWS Lambda integration. Make calls to the third-party HTTP API from the Lambda function. Pass the company's API key as an HTTP request header.

---

**Question 421.** A developer is setting up the deployment of application stacks to new test environments by using the AWS Cloud Development Kit (AWS CDK). The application contains the code for several AWS Lambda functions that will be deployed as assets. Each Lambda function is defined by using the AWS CDK Lambda construct library.

The developer has already successfully deployed the application stacks in the first account by running the cdk deploy command. The developer is preparing to deploy to the beta environment in a second account for the first time.

Which command should the developer run before redeployment to resolve this error?

A. cdk synth
B. cdk bootstrap
C. cdk init
D. cdk destroy

---

**Question 422.** A developer is automating a new application deployment with AWS Serverless Application Model (AWS SAM). The new application has one AWS Lambda function and one Amazon S3 bucket. The Lambda function must access the S3 bucket to only read objects.

How should the developer configure AWS SAM to grant the necessary read privileges to the S3 bucket?

A. Reference a second Lambda authorizer function.
B. Add a custom S3 bucket policy to the Lambda function.
C. Create an Amazon Simple Queue Service (SQS) topic for only S3 object reads. Reference the topic in the Lambda function.
D. Add the S3ReadPolicy template to the Lambda function's execution role.

---

**Question 423.** A development team wants to immediately build and deploy an application whenever there is a change to the source code.

Which approaches could be used to trigger the deployment? (Choose two.)

A. Store the source code in an Amazon S3 bucket. Configure AWS CodePipeline to start whenever a file in the bucket changes.
B. Store the source code in an encrypted Amazon EBS volume. Use AWS CodePipeline to start whenever a file in the volume changes.
C. Store the source code in an AWS CodeCommit repository. Configure AWS CodePipeline to start whenever a change is committed to the repository.
D. Store the source code in an Amazon S3 bucket. Configure AWS CodePipeline to start every 15 minutes.
E. Store the source code in an Amazon EC2 instance's ephemeral storage. Configure the instance to start AWS CodePipeline whenever there are changes to the source code.

---

**Question 424.** A developer is building an application integrating an Amazon API Gateway with an AWS Lambda function. When calling the API, the developer receives the following error:

Wed Nov 08 01:13:00 UTC 2017 : Method completed with status: 502

What should the developer do to resolve the error?

A. Change the HTTP endpoint of the API to an HTTPS endpoint.
B. Change the format of the payload sent to the API Gateway.
C. Change the format of the Lambda function response to the API call.
D. Change the authorization header in the API call to access the Lambda function.

---

**Question 425.** A developer is building various microservices for an application that will run on Amazon EC2 instances. The developer needs to monitor the end-to-end view of the requests between the microservices and debug any issues in the various microservices.

What should the developer do to accomplish these tasks?

A. Use Amazon CloudWatch to aggregate the microservices' logs and metrics, and build the monitoring dashboard.
B. Use AWS CloudTrail to aggregate the microservices' logs and metrics, and build the monitoring dashboard.
C. Use the AWS X-Ray SDK to add instrumentation in all the microservices, and monitor using the X-Ray service map.
D. Use AWS Health to monitor the health of all the microservices.

---

**Question 426.** A developer is building a microservice that uses AWS Lambda to process messages from an Amazon Simple Queue Service (Amazon SQS) queue. The Lambda function calls external APIs to search the database and load the data before loading the data into an Amazon Redshift data warehouse. The SQS queue can handle a maximum of 1,000 messages per second.

During initial testing, the Lambda function repeatedly inserted duplicate data into the Amazon Redshift table. The duplicate data led to a problem with data analysis. All duplicate messages were submitted to the queue within 1 minute of each other.

How should the developer resolve this issue?

A. Create an SQS FIFO queue. Enable message deduplication on the SQS FIFO queue.
B. Reduce the maximum Lambda concurrency that the SQS queue can invoke.
C. Use Lambda's temporary storage to keep track of processed message identifiers.
D. Configure a message group ID for every sent message. Enable message deduplication on the SQS standard queue.

---

**Question 427.** A company has an application that uses an Amazon API Gateway API to invoke an AWS Lambda function. The application is latency sensitive.

A developer needs to configure the Lambda function to reduce the cold start time that is associated with default scaling.

What should the developer do to meet these requirements?

A. Publish a new version of the Lambda function. Configure provisioned concurrency. Set the provisioned concurrency limit to meet the company requirements.
B. Increase the Lambda function's memory to the maximum amount. Increase the Lambda function's reserved concurrency limit.
C. Increase the reserved concurrency of the Lambda function to a number that matches the current production load.
D. Use Service Quotas to request an increase in the Lambda function's concurrency limit for the AWS account where the function is deployed.

---

**Question 428.** A developer is deploying an application on Amazon EC2 instances that run in Account A. The application needs to read data from an existing Amazon Kinesis data stream in Account B.

Which actions should the developer take to provide the application with access to the stream? (Choose two.)

A. Update the instance profile role in Account A with stream read permissions.
B. Create an IAM role with stream read permissions in Account B.
C. Add a trust policy to the instance profile role and IAM role in Account B to allow the instance profile role to assume the IAM role.
D. Add a trust policy to the instance profile role and IAM role in Account B to allow reads from the stream.
E. Add a resource-based policy in Account B to allow read access from the instance profile role.

---

**Question 429.** An ecommerce startup is preparing for an annual sales event. As the traffic to the company's application increases, the development team wants to be notified when the Amazon EC2 instance's CPU utilization exceeds 80%.

Which solution will meet this requirement?

A. Create a custom Amazon CloudWatch alarm that sends a notification to an Amazon SNS topic when the CPU utilization exceeds 80%.
B. Create a custom AWS CloudTrail alarm that sends a notification to an Amazon SNS topic when the CPU utilization exceeds 80%.
C. Create a cron job on the EC2 instance that invokes the --describe-instance-information command on the host instance every 15 minutes and sends the results to an Amazon SNS topic.
D. Create an AWS Lambda function that queries the AWS CloudTrail logs for the CPUUtilization metric every 15 minutes and sends a notification to an Amazon SNS topic when the CPU utilization exceeds 80%.

---

**Question 430.** A company has an application that is deployed on AWS Elastic Beanstalk. The application generates their-specific PDFs and stores the PDFs in an Amazon S3 bucket. The application is using Amazon Simple Email Service (Amazon SES) to send the PDFs by email to subscribers.

Users no longer access the PDFs after the PDFs are generated. The S3 bucket grows and contains many obsolete PDFs.

A developer must reduce the number of files in the S3 bucket by removing PDFs that are older than 90 days.

Which solution will meet this requirement with the LEAST development effort?

A. Update the application code. In the code, add a rule to scan all the objects in the S3 bucket every day and delete objects after 90 days.
B. Create an AWS Lambda function, Program the Lambda function to scan all the objects in the S3 bucket every day and to delete objects after 90 days.
C. Create an S3 Lifecycle rule for the S3 bucket to expire objects after 90 days.
D. Partition the S3 objects with a // key prefix. Create an AWS Lambda function to remove objects that have prefixes that have reached the expiration date.

---

**Question 431.** A developer is troubleshooting an application. The application includes several AWS Lambda functions that invoke Amazon API Gateway. The API Gateway's method request is set up to use an Amazon Cognito authorizer for authentication.

All the Lambda functions pass the user ID as part of the Authorization header to the API Gateway API. The API Gateway returns a 403 status code for all GET requests.

How should the developer resolve this issue?

A. Modify the client GET request to include a valid API key in the Authorization header.
B. Modify the client GET request to include a valid token in the Authorization header.
C. Update the resource policy for the API Gateway API to allow the execute-api:Invoke action.
D. Modify the client to send an OPTIONS preflight request before the GET request.

---

**Question 432.** A company processes incoming documents from an Amazon S3 bucket. Users upload documents to an S3 bucket using a web user interface. Upon receiving files in S3, an AWS Lambda function is invoked to process the files.

If the Lambda function is configured with the default settings, what will happen to the S3 event when there is a timeout exception?

A. Notification of a failed S3 event is sent as an email through Amazon SNS.
B. The S3 event is sent to the default Dead Letter Queue.
C. The S3 event is processed until it is successful.
D. The S3 event is discarded after it is retried twice.

---

**Question 433.** A developer uses Amazon S3 Event Notifications to invoke AWS Lambda functions. The Lambda function sets up a development S3 bucket, a production S3 bucket, a development Lambda function, and a production Lambda function in the same AWS account.

The developer that uploads to the development S3 bucket wrongly invokes the production Lambda function. The developer must prevent development data from affecting the production Lambda function.

What should the developer do to meet these requirements?

A. Update the execution role for the production Lambda function. Add a policy that allows the execution role to be read from only the production S3 bucket.
B. Update the S3 bucket policy for the production S3 bucket to invoke the production Lambda function. Update the S3 bucket policy for the development S3 bucket to invoke the development Lambda function.
C. Separate the development environment and the production environment into their own AWS accounts. Update the execution role for each Lambda function. Add a resource policy that allows the execution role to only read from the S3 bucket that is in the same account.
D. Separate the development environment and the production environment into their own AWS accounts. Add a resource policy to the Lambda functions to allow only S3 bucket events in the same account to invoke the functions.

---

**Question 434.** A developer is writing an application that will run on Amazon EC2 instances in an Auto Scaling group. The developer wants to externalize the session state to support the application.

Which AWS services or resources can the developer use to meet these requirements? (Choose two.)

A. Amazon DynamoDB
B. Amazon Cognito
C. Amazon ElastiCache
D. Application Load Balancer
E. Amazon Simple Queue Service (Amazon SQS)

---

**Question 435.** A company has a serverless application that uses an Amazon API Gateway API to invoke an AWS Lambda function. The company wants to test a fix for a defect in the Lambda function code. The developer wants to send 10% of the live production traffic to the updated Lambda function version.

Which combination of steps will meet these requirements? (Choose two.)

A. Publish a new version of the Lambda function that contains the updated code. Publish a new version of the Lambda function.
B. Use AWS CodeBuild to update the Lambda function. Configure CodeBuild to incrementally shift traffic from the original Lambda function to the new Lambda function.
C. Create an alias for the Lambda function. Configure weighted routing on the alias. Specify a 10% weight for the new Lambda function version.
D. Set up a routing policy on a Network Load Balancer. Configure 10% of the traffic to go to the new Lambda function version.
E. Set up a weighted routing policy by using Amazon Route 53. Configure 10% of the traffic to go to the new Lambda function version.

---

**Question 436.** A developer is creating a video search application for a global company. The video files have an average size of 2.5 TB. The video storage system must provide instant access to the video files for the first 90 days. After the first 90 days, the video files can take more than 10 minutes to load.

Which solution will meet these requirements MOST cost-effectively?

A. Upload the video files to the Amazon Elastic File System (Amazon EFS) Standard storage class for the first 90 days. After 90 days, transition the video files to the EFS Standard-Infrequent Access (Standard-IA) storage class.
B. Upload the video files to Amazon S3. Use the S3 Glacier Deep Archive storage class for the first 90 days. After 90 days, transition the video files to the Amazon S3 Glacier Flexible Retrieval storage class.
C. Use Amazon Elastic Block Store (Amazon EBS) to store the video files for the first 90 days. After 90 days, transition the video files to the Amazon S3 Glacier Deep Archive storage class.
D. Upload the video files to Amazon S3. Use the S3 Standard-Infrequent Retrieval storage class for the first 90 days. After 90 days, transition the video files to the S3 Glacier Flexible Retrieval storage class.

---

**Question 437.** A company has an ecommerce platform. A developer is designing an Amazon DynamoDB table to store customer order data for the platform. The table uses the order ID as the partition key.

The developer needs to modify the table to get all order IDs that are associated with a given customer email address in a single query. The solution must give the developer the ability to query order IDs by other item attributes in the future.

Which solution will meet these requirements?

A. Configure the partition key to use the customer email address as the sort key.
B. Update the table to use the customer email address as the partition key.
C. Create a local secondary index (LSI) with the customer email address as the sort key.
D. Create a global secondary index (GSI) with the customer email address as the partition key.

---

**Question 438.** A company has a virtual reality (VR) game. The game has a serverless backend that consists of Amazon API Gateway, AWS Lambda, and Amazon DynamoDB. Recently, the company noticed a sudden increase of new users globally. The company also noticed delays in the retrieval of user data.

Which AWS service or feature can the company use to reduce the database response time to microseconds?

A. Amazon ElastiCache
B. DynamoDB Accelerator (DAX)
C. DynamoDB auto scaling
D. Amazon CloudFront

---

**Question 439.** A developer is creating a solution to track an account's Amazon S3 buckets over time. The developer has created an AWS Lambda function that will list the account's S3 buckets and will store the list in an Amazon DynamoDB table. The developer receives a permissions error when the developer runs the function with the AWSLambdaBasicExecutionRole AWS managed policy.

Which combination of permissions should the developer use to resolve this error? (Choose two.)

A. Cross-account IAM role
B. Permission for the Lambda function to list buckets in Amazon S3
C. Permission for the Lambda function to write in DynamoDB
D. Permission for Amazon S3 to invoke the Lambda function
E. Permission for DynamoDB to invoke the Lambda function

---

**Question 440.** A company uses AWS to run its learning management system (LMS) application. The application runs on Amazon EC2 instances behind an Application Load Balancer (ALB). The application's domain name is managed in Amazon Route 53. The company wants to improve global performance for users all over the world.

Which solution will improve global performance with the LEAST operational overhead?

A. Set up an Amazon CloudFront distribution that uses the ALB as the origin. Configure Route 53 to use a DNS alias record for the application's domain name to point to the CloudFront distribution URL.
B. Launch more EC2 instances behind the ALConfigure the ALB to use session affinity (sticky sessions). Create a Route 53 alias record for the new EC2 instances.
C. Create an AWS Client VPN endpoint in the VPC. Install the VPN endpoint in the VPC. Create a Route 53 alias record for the VPN endpoint. Configure a geolocation routing policy.
D. Deploy the application to multiple Regions across the world. Create a Route 53 alias record for the ALB by using a latency-based routing policy.

---

**Question 441.** A developer hosts a static website on Amazon S3 and connects the website to an Amazon CloudFront URL.

The developer has set up a continuous integration and continuous delivery (CI/CD) pipeline. The pipeline automatically runs when changes occur in an AWS CodeCommit repository. The pipeline has a source stage and a build stage. The build stage invokes an AWS CodeBuild project that generates static files by building a buildspec.yml file. The buildspec.yml file builds the code and deploys the static files to the S3 bucket.

The pipeline runs successfully, and the latest website files are visible in the S3 bucket and at the S3 bucket URL. However, when the developer accesses the website through the CloudFront domain, the updates are not reflected on the website.

What should the developer configure the buildspec.yml file to do to resolve this issue?

A. Properly synchronize the objects in the S3 bucket with new files from the source stage.
B. Delete the previous website files in the S3 bucket and redeploy the website files.
C. Invalidate the cache for the primary CloudFront distribution.
D. Modify the cross-origin resource sharing (CORS) policy of the S3 bucket and redeploy the website files.

---

**Question 442.** A developer is working on an ecommerce application that stores data in an Amazon RDS for MySQL cluster. The developer needs to implement a caching layer for the application to retrieve information about the most viewed products.

Which solution will meet these requirements?

A. Edit the RDS for MySQL cluster by adding a cache node. Configure the cache endpoint instead of the cluster endpoint in the application.
B. Create an Amazon ElastiCache for Redis cluster. Update the application code to use the ElastiCache cluster endpoint for Redis cluster endpoint.
C. Create an Amazon DynamoDB Accelerator (DAX) cluster in front of the RDS for MySQL cluster. Configure the application to connect to the DAX endpoint instead of the RDS endpoint.
D. Configure the RDS for MySQL cluster to add a standby instance in a different Availability Zone. Configure the application to read the data from the standby instance.

---

**Question 443.** A gaming application stores scores for players in an Amazon DynamoDB table that has four attributes: user_id, user_name, user_score, and user_rank. The users are allowed to update their names. A user is authenticated by web identity federation.

Which set of conditions should be added in the policy attached to the role for the dynamodb:PutItem API call?

A.
```
"Condition": {
  "ForAllValues:StringEquals": {
    "dynamodb:LeadingKeys": [
      "${www.amazon.com/user_id}"
    ],
    "dynamodb:Attributes": [
      "user_name", "user_id"
    ]
  }
}
```

B.
```
"Condition": {
  "ForAllValues:StringEquals": {
    "dynamodb:LeadingKeys": [
      "${www.amazon.com/user_name}"
    ]
  }
}
```

C.
```
"Condition": {
  "ForAllValues:StringEquals": {
    "dynamodb:LeadingKeys": [
      "${www.amazon.com/user_id}"
    ],
    "dynamodb:Attributes": [
      "user_name", "user_id"
    ]
  }
}
```

D.
```
"Condition": {
  "ForAllValues:StringEquals": {
    "dynamodb:LeadingKeys": [
      "${www.amazon.com/user_name}"
    ],
    "dynamodb:Attributes": [
      "user_name", "user_id"
    ]
  }
}
```

---

**Question 444.** A developer is creating a database of products. Queries for frequently accessed products must have retrieval times of microseconds. To ensure data consistency, the application cache must be updated whenever products are added, changed, or deleted.

Which solution will meet these requirements?

A. Set up an Amazon DynamoDB database and a DynamoDB Accelerator (DAX) cluster. Implement a lazy loading caching strategy in the application.
B. Set up an Amazon RDS database and an Amazon ElastiCache for Redis cluster. Implement a lazy loading caching strategy with ElastiCache.
C. Set up an Amazon DynamoDB database that has an in-memory cache. Implement a lazy loading caching strategy in the application.
D. Set up an Amazon RDS database and an Amazon DynamoDB Accelerator (DAX) cluster. Specify a TTL setting for the DAX cluster.

---

**Question 445.** A developer is creating a script to automate the deployment process for a serverless application. The developer wants to use an existing AWS Serverless Application Model (AWS SAM) template for the application.

What should the developer use for the project? (Choose two.)

A. Call aws cloudformation package to create the deployment package. Call aws cloudformation deploy to deploy the package afterward.
B. Call sam package to create the deployment package. Call sam deploy to deploy the package afterward.
C. Call aws s3 cp to upload the AWS SAM template to Amazon S3. Call aws lambda update-function-code to create the application.
D. Create a ZIP package locally and call aws serverlessrepo create-application to create the application.
E. Create a ZIP package and upload it to Amazon S3. Call aws cloudformation create-stack to create the application.

---
