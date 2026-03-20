# AWS Developer Associate - Quiz Set 6 (Questions 446–557)

**Question 446.** A developer adds new dependencies to an existing AWS Lambda function. The developer cannot deploy the Lambda function because the unzipped deployment package exceeds the maximum size quota for the Lambda function. The instruction set architecture of the Lambda function is x86_64.

The developer must implement a solution to deploy the Lambda function with the new dependencies.

Which solution will meet these requirements?

A. Create a snapshot of all the dependencies. Configure the Lambda function to use the snapshot.
B. Change the instruction set architecture of the Lambda function to use an arm64 architecture.
C. Associate an Amazon Elastic Block Store (Amazon EBS) volume with the Lambda function. Store all the dependencies on the EBS volume.
D. Create and deploy a Lambda container image with all the dependencies.

---

**Question 447.** A developer is working on a project that requires regular updates to a web application's backend code. The code is stored in AWS CodeCommit. Company policy states that all code must have complete unit testing and that the test results must be available for access.

The developer needs to implement a solution that will take each change to the code repository, build the code, and run unit tests. The solution also must provide a detailed report of the test results.

Which solution will meet these requirements?

A. Configure AWS CodeDeploy to deploy code from CodeCommit and to run unit tests. Send the test results to Amazon CloudWatch metrics to view reports.
B. Configure Amazon CodeWhisperer to create the code and to run unit tests. Save the test results in an Amazon S3 bucket to generate reports.
C. Configure AWS CodeBuild to build the code and to run unit tests. Use test reporting in CodeBuild to generate and view reports.
D. Create AWS Lambda functions that run when changes are made in CodeCommit. Program the Lambda functions to build the code, run unit tests, and save the test results to a Lambda layer.

---

**Question 448.** A developer is building an application on AWS. The application has an Amazon API Gateway API that sends requests to an AWS Lambda function. The API is experiencing increased latency because the Lambda function has limited available CPU to fulfill the requests.

Before the developer deploys the API into production, the developer must configure the Lambda function to have more CPU.

Which solution will meet this requirement?

A. Increase the virtual CPU (vCPU) cores quota of the Lambda function.
B. Increase the amount of memory that is allocated to the Lambda function.
C. Increase the ephemeral storage size of the Lambda function.
D. Increase the timeout value of the Lambda function.

---

**Question 449.** A developer is creating a web application to upload and store private data. The application will encrypt private data and then will upload the data to an Amazon S3 bucket.

The developer needs to implement a solution to automatically find any unencrypted private data in the S3 bucket. The solution must monitor the security and access control of the S3 bucket and must provide a notification if there are any security issues.

Which solution will meet these requirements?

A. Use AWS Step Functions to run Amazon Athena queries. Configure Athena to find unencrypted private data and to monitor for security issues in the S3 bucket. Start the queries when new objects are added to the S3 bucket. Configure Athena to provide a notification if security issues are detected.
B. Enable Amazon Macie for the S3 bucket. Set up custom criteria to find unencrypted private data in the S3 bucket. Set up AWS User Notifications to send a notification when security issues are detected.
C. Enable Amazon Inspector for the S3 bucket. Use Amazon Inspector to scan the S3 bucket to find unencrypted private data and to monitor for security issues. Configure Amazon Inspector to provide a notification when Amazon Inspector detects security issues.
D. Create an Amazon Kinesis data stream. Configure Amazon S3 to send new object notifications to the stream. Create an AWS Lambda function that runs every 10 minutes to check the stream for unencrypted private data and to monitor for security issues. Program the Lambda function to provide a notification when security issues are detected.

---

**Question 450.** A developer has an application that uses AWS Lambda functions and AWS CloudFormation templates. Usage of the application has increased. As a result, the Lambda functions are encountering rate limit errors when they retrieve data.

The Lambda functions retrieve an advanced parameter from AWS Systems Manager Parameter Store on every call. The parameter changes only during new deployments. Because the application's usage is unpredictable, the developer needs a way to avoid the rate limiting.

Which solution will meet these requirements MOST cost-effectively?

A. Configure the Lambda functions to use a concurrency that is equal to the last month's average number of concurrent invocations.
B. Add a retry mechanism with exponential backoff to the call to Parameter Store.
C. Request a service quota increase for Parameter Store GetParameter API operations to match the expected usage of the Lambda functions.
D. Add an SSM dynamic reference as an environment variable to the Lambda functions resource in the CloudFormation templates.

---

**Question 451.** A developer is using an AWS Lambda function to process data. The developer needs to extract custom metrics about processing times from the Lambda logs. The developer needs to create graphs and alarms, set alarms, and detect issues in real time.

Which solution will meet these requirements?

A. Publish custom metric data to AWS CloudTrail by using the PutMetricData API operation. Classify and collect the metrics. Create graphs and alarms in CloudTrail for the custom metrics.
B. Use the open source client libraries provided by Amazon to generate the logs in the Amazon CloudWatch embedded metric format. Use CloudWatch to create the required graphs and alarms for the custom metrics.
C. Use Amazon CloudWatch Logs Insights to create custom metrics by querying the logs that come from the Lambda function. Use CloudWatch to create the required graphs and alarms for the custom metrics.
D. Create an Amazon Kinesis data stream to stream log events in real time from Lambda. Specify an Amazon S3 bucket as the destination for the Kinesis data stream. Use Amazon CloudWatch to visualize the log data and to set alarms.

---

**Question 452.** A developer needs to fix an AWS CodeDeploy deployment that failed. During the failed deployment, the developer received the following error message:

"The overall deployment status for this deployment failed because too many individual instances failed deployment, too few healthy instances are available for deployment, or some instances in your deployment group are experiencing problems. (Error code: HEALTH-CONSTRAINTS)"

What are the possible causes of the failed deployment? (Choose two.)

A. The CodeDeploy agent was not running on the instances that CodeDeploy was trying to deploy to.
B. The unified Amazon CloudWatch agent was not running on the instances that CodeDeploy was trying to deploy to.
C. The developer's IAM role did not have the necessary permissions to perform code deployment to the instances.
D. CodeDeploy was trying to deploy to instances that were attached to an IAM instance profile that did not have the required permissions.
E. CodeDeploy was trying to deploy to instances that were not set up with correct CodeDeploy health checks.

---

**Question 453.** A company is developing a serverless application that requires storage of sensitive API keys as environment variables for various services. The application requires the automatic rotation of the encryption keys every year.

Which solution will meet these requirements with no development effort?

A. Encrypt the environment variables by using AWS Secrets Manager. Set up automatic rotation in Secrets Manager.
B. Encrypt the environment variables by using AWS Key Management Service (AWS KMS) customer managed keys. Enable automatic key rotation.
C. Encrypt the environment variables by using AWS Key Management Service (AWS KMS) AWS managed keys. Configure a custom AWS Lambda function to automate key rotation.
D. Encrypt the environment variables by using AWS Systems Manager Parameter Store. Set up automatic rotation in Parameter Store.

---

**Question 454.** A developer built an application that uses AWS Lambda functions to process images. The developer wants to improve image processing times throughout the day.

The developer needs to create an Amazon CloudWatch Logs Insights query that shows the average, slowest, and fastest processing time in 1-minute intervals.

Which query will meet these requirements?

A. `filter @type = "REPORT" | stats avg(@duration), max(@duration), min(@duration) by bin(1m)`
B. `filter @type = "DISPLAY" | stats avg(@duration), max(@duration), min(@duration) by bin(5m)`
C. `filter @type = "STATS" | stats avg(@duration), max(@duration), min(@duration) by bin(1m)`
D. `filter @type = "PATTERN" | stats avg(@duration), max(@duration), min(@duration) by bin(1m)`

---

**Question 455.** An application stores user data in Amazon S3 buckets in multiple AWS Regions. A developer needs to find sensitive information that analyzes the user data in the S3 buckets to find sensitive information. The analysis findings from all the S3 buckets must be available in the eu-west-2 Region.

Which solution will meet these requirements with the LEAST development effort?

A. Create an AWS Lambda function to generate findings. Program the Lambda function to send the findings to another S3 bucket in eu-west-2. Use Amazon EventBridge to create rules that copy the findings to eu-west-2.
B. Configure Amazon Inspector to generate findings. Use Amazon EventBridge to create rules that copy the findings to eu-west-2.
C. Configure Amazon Macie to generate findings. Use Amazon EventBridge to create rules that copy the findings to eu-west-2.
D. Configure Amazon Macie to generate findings and to publish the findings to AWS CloudTrail. Use a CloudTrail trail to copy the results to eu-west-2.

---

**Question 456.** An application ingests data from an Amazon Kinesis data stream. The shards in the data stream are set for normal traffic.

During tests for peak traffic, the application ingests data slowly. A developer needs to adjust the data stream to handle the peak traffic.

What should the developer do to meet this requirement MOST cost-effectively?

A. Install the Kinesis Producer Library (KPL) to ingest data into the data stream.
B. Switch to on-demand capacity mode for the data stream. Specify a partition key when writing data to the data stream.
C. Decrease the amount of time that data is kept in the data stream by using the DecreaseStreamRetentionPeriod API operation.
D. Increase the shard count in the data stream by using the UpdateShardCount API operation.

---

**Question 457.** A developer is building an application that uses an AWS Lambda function to process data. The application requires minimum latency. The Lambda function must have predictable function start times. All setup activities for the execution environment must happen before invocation of the Lambda function.

Which solution will meet these requirements?

A. Increase the memory of the Lambda function to the maximum amount. Configure an Amazon EventBridge rule to schedule invocations of the Lambda function every minute to keep the execution environment active.
B. Optimize the static initialization code that runs when a new execution environment is prepared for the first time. Decrease and compress the size of the Lambda function package and the imported libraries and dependencies.
C. Increase the reserved concurrency of the Lambda function to the maximum value for unreserved account concurrency. Run any setup activities manually before the initial invocation of the Lambda function.
D. Publish a new version of the Lambda function. Configure provisioned concurrency for the Lambda function with the required minimum number of execution environments.

---

**Question 458.** A company has implemented a pipeline in AWS CodePipeline. The company is using a single AWS account and does not use AWS Organizations. The company needs to test its AWS CloudFormation templates in its primary AWS Region and a disaster recovery Region.

Which solution will meet these requirements with the MOST operational efficiency?

A. In the CodePipeline pipeline, implement an AWS CodeDeploy action for each Region to deploy and test the CloudFormation templates. Configure CodePipeline and AWS CodeBuild with appropriate permissions.
B. Configure CodePipeline to deploy and test the CloudFormation templates. Use CloudFormation StackSets to start deployment to both Regions. Configure CodeBuild and CloudFormation with appropriate permissions.
C. Configure CodePipeline to use AWS CodeBuild to deploy and test the CloudFormation templates in each Region. Update CodeBuild and CloudFormation with appropriate permissions.
D. Use the Stryk action in CodePipeline to deploy and test the CloudFormation templates in each Region.

---

**Question 459.** A developer is implementing a serverless application by using AWS CloudFormation to provision Amazon S3 web hosting, Amazon API Gateway, and AWS Lambda functions. The Lambda function source code key of the zipped source code is specified in the CloudFormation resource in the template. The S3 object key of the zipped source code is specified in the CloudFormation resource in the template.

The developer notices that there are no changes to the Lambda function every time the CloudFormation stack is updated.

How can the developer resolve this issue?

A. Create a new Lambda function alias before updating the CloudFormation stack.
B. Change the S3 object key or the S3 version in the CloudFormation template before updating the CloudFormation stack.
C. Upload the zipped source code to another S3 bucket before updating the CloudFormation stack.
D. Associate a code signing configuration with the Lambda function before updating the CloudFormation stack.

---

**Question 460.** A developer is building an application that processes a stream of user-supplied data. The data stream must be consumed by multiple Amazon EC2 based processing applications in parallel and in real time. Each processor must be able to resume without losing data if there is a service interruption. The application architect plans to add other processors in the near future, and wants to minimize the amount of data duplication involved.

Which solution will satisfy these requirements?

A. Publish the data to Amazon Simple Queue Service (Amazon SQS).
B. Publish the data to Amazon Data Firehose.
C. Publish the data to Amazon EventBridge.
D. Publish the data to Amazon Kinesis Data Streams.

---

**Question 461.** A developer is using AWS CloudFormation to deploy an AWS Lambda function. The developer needs to set the timeout parameter of the environment parameter of the template. The template contains mappings for EnvironmentData for each environment's timeout value. The Environment parameter and EnvironmentData mappings are as follows:

Environment parameter:
```
Parameters:
  Environment:
    Type: String
    AllowedValues:
      - dev
      - test
      - prod
    Description: The name of the deployment environment.
```

EnvironmentData mappings:
```
Mappings:
  EnvironmentData:
    dev:
      Timeout: 30
    test:
      Timeout: 45
    prod:
      Timeout: 90
```

Which solution will meet these requirements?

A. Timeout: `!GetAtt [EnvironmentData, !Ref Environment, Timeout]`
B. Timeout: `!FindInMap [EnvironmentData, !Ref Environment, Timeout]`
C. Timeout: `!Select [EnvironmentData, !Ref Environment, Timeout]`
D. Timeout: `!ForEach [EnvironmentData, !Ref Environment, Timeout]`

---

**Question 462.** A company's AWS accounts are in an organization in AWS Organizations. An application in Account A uses environment variables that are stored as parameters in AWS Systems Manager Parameter Store. A developer is creating a new application in Account B that needs to use the same environment variables.

The application in Account B needs to access the parameters in Account A without duplicating the parameters into Account B.

Which solution will meet these requirements with the LEAST operational overhead?

A. Configure the application in Account B to use credentials for an IAM user in Account A that has access to the parameters.
B. Create an assumable IAM role in Account A. Grant the role the permission to access the parameters. Configure cross-account resource sharing for the parameters by using AWS Resource Access Manager (AWS RAM).
C. Configure cross-account resource sharing for the parameters by using AWS Resource Access Manager (AWS RAM).
D. Write a script to share the parameters for the parameters by using AWS Resource Access Manager (AWS RAM).

---

**Question 463.** A developer is creating an application that uses an Amazon DynamoDB table. The developer needs to develop code that reads all records that were added to the table during the previous day, creates HTML reports, and pushes the reports into third-party storage. The item size varies from 1 KB to 4 KB, and the index structure is defined with the date. The developer needs to minimize the read capacity that the application requires from the DynamoDB table.

Which DynamoDB API operation should the developer use in the code to meet these requirements?

A. Query
B. Scan
C. BatchGetItem
D. GetItem

---

**Question 464.** A company has an application that uses an Amazon Cognito user pool for authentication. A developer needs to add a new REST API that will use the user pool to authenticate requests.

Which solution will meet this requirement with the LEAST development effort?

A. Create a new API key and a usage plan. Associate the API key with the REST API with the usage plan. Reference the authorization header that contains the Cognito token. Authenticate requests based on the token value.
B. Create a Cognito authorizer for the user pool. Attach the authorizer to the API. Deploy the API.
C. Create an AWS Lambda token authorizer. Reference the authorization header in the event payload. Authenticate requests based on the token value.
D. Create an AWS Lambda request authorizer. Reference the authorization header in the event payload. Authenticate requests by using the header value in a request to the Cognito API.

---

**Question 465.** A developer manages encryption keys in AWS Key Management Service (AWS KMS). The developer must ensure that all encryption keys can be deleted immediately when the keys are no longer required. The developer wants a solution that is highly available and does not require manual management for compute infrastructure.

Which solution will meet these requirements?

A. Use AWS KMS managed keys. When the keys are no longer required, schedule the keys for immediate deletion.
B. Use customer managed keys with imported key material. When the keys are no longer required, delete the imported key material.
C. Use customer managed keys. When the keys are no longer required, delete the key material.
D. Use customer managed keys and an AWS CloudHSM key store. When the keys are no longer required, schedule the keys for immediate deletion.

---

**Question 466.** A company has an ecommerce application. The application's API sends order data to an Amazon Simple Queue Service (Amazon SQS) queue so the file can be processed. A developer needs to enrich the order data before the application sends the order to a fulfillment system.

Which solution will meet this requirement with the LEAST development effort?

A. Create an AWS Lambda function to poll the SQS queue, read and enrich the data, and send the enriched data to the fulfillment system. Create an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe the Lambda function to the SNS topic.
B. Create an AWS Step Functions state machine. Configure an Amazon EventBridge rule to run the state machine when new objects are published to the SQS queue. Map the orders to the state machine to perform data enrichment and to invoke the fulfillment system.
C. Create an Amazon EXB job to read messages from the SQS queue. Configure the job to enrich the order data. Create an Amazon EventBridge EXB job to enrich the order data. Specify an Amazon S3 bucket as the destination location. Configure the SQS queue as a source for the pipe.
D. Create an Amazon EventBridge Pipes that uses enrichment. Configure the SQS queue as a source for the pipe.

---

**Question 467.** An application interacts with Amazon Aurora to store and track customer information. The primary database is set up with multiple read replicas for improving the performance of the read queries. However, one of the Aurora replicas is receiving most or all of the traffic, while the other Aurora replica remains idle.

How can this issue be resolved?

A. Disable application-level DNS caching.
B. Enable application-level DNS caching.
C. Enable application pooling
D. Disable application pooling

---

**Question 468.** A company runs a new application on AWS Elastic Beanstalk. The company needs to deploy updates to the application. The updates must not cause any downtime for application users.

The deployment must forward a specified percentage of incoming client traffic to a new application version during an evaluation period.

Which deployment type will meet these requirements?

A. rolling
B. traffic-splitting
C. in-place
D. immutable

---

**Question 469.** A developer is launching a global application that needs to serve content to multiple countries. The developer needs to serve the content based on the country of each user and the user's primary language. The developer must ensure that content is served reliably and with low latency.

Which solution will meet these requirements?

A. Create an Amazon API Gateway REST API. Create an AWS Global Accelerator standard accelerator to resolve requests to the API. Configure endpoint groups on the accelerator. Attach listeners for each country and language.
B. Store the content in a centralized Amazon S3 bucket. Enable S3 Transfer Acceleration on the bucket. Create an Amazon Route 53 hosted zone that includes the endpoint for the S3 bucket. Create records in Route 53 that use geoproximity and geolocation routing policies.
C. Create an Amazon API Gateway REST API. Connect the REST API to AWS WAF. Use geo match statements and regex match statements to allow or deny requests based on web request evaluations.
D. Configure an Amazon CloudFront distribution that uses the application as the origin. Configure the distribution to forward the Accept-Language header and the CloudFront-Viewer-Country header to the origin.

---

**Question 470.** A developer has an AWS Lambda function that needs to access an Amazon DynamoDB table named DailyOrders. The Lambda function must be able to perform read operations on the table. The Lambda function must not be able to perform write operations on the table.

The developer needs to create an IAM policy to associate with the Lambda function's execution role.

Which IAM policy statement will meet these requirements?

A.
```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Action": [
      "dynamodb:BatchGetItems",
      "dynamodb:GetItem",
      "dynamodb:Query",
      "dynamodb:Scan",
      "dynamodb:BatchWriteItem",
      "dynamodb:PutItem",
      "dynamodb:UpdateItem"
    ],
    "Resource": "arn:aws:dynamodb:eu-east-1:321456987012:table/DailyOrders"
  }]
}
```

B.
```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Action": [
      "dynamodb:GetItem",
      "dynamodb:PutItem",
      "dynamodb:Query",
      "dynamodb:Scan"
    ],
    "Resource": "arn:aws:dynamodb:eu-east-1:321456987012:table/DailyOrders"
  }]
}
```

C.
```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Deny",
    "Action": [
      "dynamodb:Query",
      "dynamodb:Scan",
      "dynamodb:PutItem",
      "dynamodb:UpdateItem"
    ],
    "Resource": "arn:aws:dynamodb:eu-east-1:321456987012:table/DailyOrders"
  }]
}
```

D.
```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Action": [
      "dynamodb:BatchGetItem",
      "dynamodb:GetItem",
      "dynamodb:Query",
      "dynamodb:Scan"
    ],
    "Resource": "arn:aws:dynamodb:eu-east-1:321456987012:table/DailyOrders"
  }]
}
```

---

**Question 471.** A developer is working on a new authorization mechanism for an application. The developer must create an Amazon API Gateway API and must test JSON Web Tokens (JWT) authorization on the API.

The developer must use the built-in authorizer and must avoid managing the code with custom logic. The developer needs to define an API route that is available at /auth to set the authorizer configuration.

Which solution will meet these requirements?

A. Create a WebSocket API and the /auth route. Configure and attach the JWT authorizer to the API. Deploy the API.
B. Create a WebSocket API and the /auth route. Create a Lambda authorizer. Attach the Lambda authorizer to the API. Deploy the API.
C. Create an HTTP API and the /auth route. Create and configure an AWS Lambda authorizer. Attach the Lambda authorizer to the API. Deploy the API.
D. Create an HTTP API and the /auth route. Configure the JWT authorizer. Attach the JWT authorizer to the /auth route. Deploy the API.

---

**Question 472.** A company is creating a new application that gives users the ability to upload and share short video files. The average size of the video files is 10 MB. After a user uploads a file, a message needs to be placed into an Amazon Simple Queue Service (Amazon SQS) queue so the file can be processed. The files need to be accessible for processing within 5 minutes.

Which solution will meet these requirements MOST cost-effectively?

A. Write the files to Amazon S3 Glacier Deep Archive. Add the S3 location of the files to the SQS queue.
B. Write the files to Amazon S3 Standard. Add the S3 location of the files to the SQS queue.
C. Write the files to an Amazon Elastic Block Store (Amazon EBS) General Purpose SSD volume. Add the EBS location of the files to the SQS queue.
D. Write messages that contain the contents of the uploaded files to the SQS queue.

---

**Question 473.** A developer is updating the code for an AWS Lambda function to add new capabilities. The Lambda function has version aliases for production and development environments that run separate versions of the function. The developer needs to configure a staging environment for the Lambda function to handle invocations to both the development version and the production version.

Which solution will meet these requirements?

A. Create a weighted alias that references the production version of the function and the updated version of the function.
B. Add a Network Load Balancer. Add the production version of the function and updated version of the function as targets.
C. Use AWS CodeDeploy to create a linear traffic shifting deployment.
D. Create a tag for the Lambda function that contains the production version and updated version of the code.

---

**Question 474.** A gaming company has deployed a web portal on AWS Elastic Beanstalk. The company sometimes needs to deploy new versions three or four times in a day. The company needs to deploy new features for all users as quickly as possible. The solution must minimize performance impact and must maximize availability.

What solution will meet these requirements?

A. Use a rolling deployment policy to deploy to Amazon EC2 instances.
B. Use an immutable deployment policy to deploy to Amazon EC2 instances.
C. Use an all-at-once deployment policy to deploy to Amazon EC2 instances.
D. Use a canary deployment strategy to deploy changes to Amazon EC2 instances.

---

**Question 475.** An AWS Lambda function generates a 1 MB JSON file and then uploads it to an Amazon S3 bucket daily. The file contains sensitive information, so the developer must ensure that it is encrypted before uploading to the bucket.

Which of the following modifications should the developer make to ensure that the data is encrypted before uploading it to the bucket?

A. Use the default AWS Key Management Service (AWS KMS) key for Amazon S3 in the Lambda function code.
B. Use the S3 managed key and the GenerateDataKey API to encrypt the file in the Lambda function code.
C. Use the GenerateDataKey API, then use that data key to encrypt the file in the Lambda function code.
D. Use an AWS Key Management Service (AWS KMS) customer managed key for Amazon S3 in the Lambda function code.

---

**Question 476.** An Amazon Data Firehose delivery stream is receiving customer data that contains personally identifiable information. A developer needs to remove pattern-based customer identifiers from the data and store the modified data in an Amazon S3 bucket.

What should the developer do to meet these requirements?

A. Implement Firehose data transformation as an AWS Lambda function. Configure the function to remove the customer identifiers. Set an Amazon S3 bucket as the destination of the delivery stream.
B. Launch an Amazon EC2 instance. Set the EC2 instance as the destination of the delivery stream. Run an application on the EC2 instance to remove the customer identifiers. Store the transformed data in an Amazon S3 bucket.
C. Create an Amazon OpenSearch Service instance. Set the OpenSearch Service instance as the destination of the delivery stream. Use the search and replace to remove the customer identifiers. Export the data to an Amazon S3 bucket.
D. Create an AWS Step Functions workflow to remove the customer identifiers. As the last step in the workflow, store the transformed data in an Amazon S3 bucket. Set the workflow as the destination of the delivery stream.

---

**Question 477.** A developer has deployed an AWS Lambda function that is subscribed to an Amazon Simple Notification Service (Amazon SNS) queue. The developer must implement a solution to add a dead-letter queue for each Lambda function invocation to an Amazon Simple Queue Service (Amazon SQS) queue.

Which solution will meet this requirement?

A. Configure the SQS queue as a dead-letter queue for the Lambda function.
B. Create a filter that uses the AWS SDK to call the SQS SendMessage operation to add the invocation details to the SQS queue. Add the code to the end of the Lambda function.
C. Add two asynchronous invocation destinations to the Lambda function: one destination for successful invocations and one destination for failed invocations. Configure the SQS queue as the destination for each type. Create an Amazon CloudWatch alarm based on the DestinationDeliveryFailures metric to catch any message that cannot be delivered.
D. Add a single asynchronous invocation destination to the Lambda function to capture successful invocations. Configure the SQS queue as the destination. Create an Amazon CloudWatch alarm based on the DestinationDeliveryFailures metric to catch any message that cannot be delivered.

---

**Question 478.** A developer needs to configure an AWS Lambda function to make HTTP POST requests to an internal application. The application is in the same AWS account that hosts the function. The internal application runs on Amazon EC2 instances in a private subnet within a VPC.

Which solution will meet these requirements?

A. Configure a VPC endpoint to connect to the private subnet. Attach the endpoint to the Lambda function.
B. Attach the Lambda function to the VPC and to the private subnet.
C. Configure a VPN connection between the Lambda function and the private subnet. Attach the VPN to the Lambda function.
D. Configure the VPC route table to include the Lambda function's IP address.

---

**Question 479.** A developer is writing a mobile application that allows users to view images from an S3 bucket. The users must be able to log in with their Amazon login, as well as supported social media accounts.

How can the developer provide this authentication functionality?

A. Use Amazon Cognito with web identity federation.
B. Use Amazon Cognito with SAML-based identity federation.
C. Use IAM access keys and secret keys in the application code to allow Get* on the S3 bucket.
D. Use AWS STS AssumeRole in the application code and assume a role with Get* permissions on the S3 bucket.

---

**Question 480.** A developer is building an ecommerce application that uses multiple AWS Lambda functions. Each function performs a specific step in a customer order workflow, such as order processing and inventory management. The developer must ensure that the Lambda functions run in a specific order.

Which solution will meet this requirement with the LEAST operational overhead?

A. Configure an Amazon Simple Queue Service (Amazon SQS) queue to contain messages about each step a function must perform. Configure the Lambda functions to run sequentially based on the order of messages in the SQS queue.
B. Configure an Amazon Simple Notification Service (Amazon SNS) topic to contain notifications about each step a function must perform. Subscribe the Lambda functions to the SNS topic. Use subscription filters based on the step each function must perform.
C. Use an AWS Step Functions state machine to invoke the Lambda functions in a specific order.
D. Configure Amazon EventBridge Scheduler schedules to invoke the Lambda functions in a specific order.

---

**Question 481.** A company generates SSL certificates from a third-party provider. The company imports the certificates into AWS Certificate Manager (ACM) to use with public applications. A developer must implement a solution to notify the company's security team 90 days before a certificate expires. The company already has configured an Amazon Simple Queue Service (Amazon SQS) queue. The company also has configured an Amazon Simple Notification Service (Amazon SNS) topic that has the security team's email address as a subscriber.

Which solution will provide the security team with the required notification about certificates?

A. Create an Amazon EventBridge rule that specifies the ACM Certificate Approaching Expiration event type. Set the SNS topic as a target of the EventBridge rule's target.
B. Create an AWS Lambda function to search for all certificates that are expiring within 90 days. Program the Lambda function to send each certificate's Amazon Resource Name (ARN) in the notification to the SNS topic queue. Create an Amazon CloudWatch alarm based on the DestinationDeliveryFailures metric to catch any message that cannot be delivered.
C. Create an AWS Step Functions workflow that is invoked by each certificate's expiration notification event type. Create an AWS Lambda function to send each certificate's Amazon Resource Name (ARN) to the SNS topic. Set the Lambda function as a step in the Step Functions workflow.
D. Configure AWS Config with the acm-certificate-expiration-check managed rule to run every 24 hours. Create an Amazon EventBridge rule that includes an event pattern that specifies the Config Rules Compliance Change detail type. Set the SNS topic as a target of the EventBridge rule's target.

---

**Question 482.** A company has an Amazon API Gateway REST API that integrates with an AWS Lambda function. The API's development stage references a development alias of the Lambda function named dev.

A developer needs make a production alias of the Lambda function named prod available through the API.

Which solution meets these requirements?

A. Create a new method on the API. Name the method production. Configure the method to include a stage variable that points to the prod Lambda function alias.
B. Create a new method on the API. Name the method production. Configure an integration request on the API's development stage that points to the prod Lambda function alias.
C. Deploy the API to a new stage named production. Configure the stage to include a stage variable that points to the prod Lambda function alias.
D. Deploy the API to a new stage named production. Configure an integration request on the API's production stage that points to the prod Lambda function alias.

---

**Question 483.** A developer published a change to a new version of an AWS Lambda function. The developer must route 50% of the traffic to the new version and 90% of the traffic to the current version. What is the most operationally efficient approach to route traffic to the different versions of the Lambda function?

A. Create two Amazon Route 53 records with a simple routing policy to route traffic to the different versions of the Lambda function. Add a canary release that will override the version variable 50% of the time. Deploy and test the Lambda function through the API Gateway stage.
B. Create an Amazon API Gateway API with a POST method. Add a stage variable that assigns the stage variable to the Lambda function. Set the event source mappings for the Lambda function. In the mappings, set the weight to 90% for the current version and 50% for the new version.
C. Create a new stage for the REST API. Add a GET method to a resource that is integrated with the new Lambda function version. Set the event source mappings for the Lambda function. In the mappings, set the weight to 90% for the current version and 50% for the new version.
D. Update the Lambda integration of the existing GET method to point to the updated version of the Lambda function. Deploy the new version.

---

**Question 484.** An application is experiencing performance issues based on increased demand. This increased demand is on read-only historical records pulled from an Amazon RDS-hosted database with custom views and queries. A developer must improve performance without changing the database structure.

Which approach will improve performance and MINIMIZE management overhead?

A. Deploy Amazon DynamoDB, move all the data, and point to DynamoDB.
B. Deploy Amazon ElastiCache (Redis OSS) and cache the data for the application.
C. Deploy Memcached on Amazon EC2 and cache the data for the application.
D. Deploy Amazon DynamoDB Accelerator (DAX) on Amazon RDS to improve cache performance.

---

**Question 485.** In a move toward using microservices, a company's management team has asked all development teams to build their services so that API requests depend only on that service's data store. One team is building a Payments service which has its own database; the service needs data that originates in the Accounts database. Both are using Amazon DynamoDB.

What approach will result in the simplest, decoupled, and reliable method to get near-real time updates from the Accounts database?

A. Use AWS Glue to perform frequent ETL updates from the Accounts database to the Payments database.
B. Use Amazon ElastiCache in Payments, with the cache updated by triggers in the Accounts database.
C. Use Amazon Data Firehose to deliver all changes from the Accounts database to the Payments database.
D. Use Amazon DynamoDB Streams to deliver all changes from the Accounts database to the Payments database.

---

**Question 486.** A developer compresses a Lambda function and packages the result as a .zip file. The developer uses the Functions page on the Lambda console to attempt to upload the packaged .zip file. When pushing the package to Lambda, the console returns the following error:
An error occurred (RequestEntityTooLargeException) when calling the UpdateFunctionCode operation: Request must be smaller than 69905067 bytes for the GetObject operation.

Which solutions can the developer use to publish the code? (Choose two.)

A. Upload the package to Amazon S3. Use the update-function-code AWS CLI command to update the Lambda function with the S3 location.
B. Create an AWS Support ticket to increase the package size limit on the account.
C. Use the update-function-code AWS CLI command. Pass the --zipfile parameter.
D. Repackage the Lambda function as a Docker container image to Amazon Elastic Container Registry (Amazon ECR). Create a new Lambda function by using the Lambda console. Reference the image that is deployed to Amazon ECR.
E. Sign the .zip file digitally. Create a new Lambda function by using the Lambda console. Update the configuration of the new Lambda function to include the Amazon Resource Name (ARN) of the code signing configuration.

---

**Question 487.** A company runs an application on Amazon EC2 instances in an Auto Scaling group. The application experiences variable loads throughout each day. The company needs to collect detailed metrics from the EC2 instances to right-size the instances. The company also wants to monitor custom application metrics to ensure the application is performing efficiently.

Which solution will meet these requirements?

A. Install the AWS X-Ray agent on the instances. Configure the agent to collect the EC2 instance metrics and the custom application metrics.
B. Install the Amazon CloudWatch agent on the instances. Configure the agent to collect the EC2 instance metrics and the custom application metrics.
C. Install the AWS SDK in the application's code. Update the application to use the AWS SDK to collect and publish the EC2 instance metrics and the custom application metrics.
D. Configure AWS CloudTrail to capture and analyze the EC2 instance metrics and the custom application metrics.

---

**Question 488.** A company is launching a feature that uses an HTTP API built with Amazon API Gateway and AWS Lambda. An API Gateway endpoint performs several independent tasks that run in a Lambda function. The independent tasks can take up to 10 minutes in total to finish running.

Users report that the endpoint sometimes returns an HTTP 604 status code. The Lambda function invocations are successful.

Which solution will stop the endpoint from returning the HTTP 504 status code?

A. Increase the Lambda function's timeout value.
B. Increase the reserved concurrency of the Lambda function.
C. Increase the memory that is available to the Lambda function.
D. Refactor the Lambda function to start an AWS Step Functions state machine.

---

**Question 489.** A developer is testing an AWS Lambda function that has an event source of an Amazon Simple Queue Service (Amazon SQS) queue. The developer notices that some of the messages the Lambda function processes re-appear in the queue while the messages are being processed.

The developer must correct this behavior.

Which solution will meet this requirement?

A. Increase the timeout of the Lambda function.
B. Increase the visibility timeout of the SQS queue.
C. Increase the memory allocation of the Lambda function.
D. Increase the batch size in the event source mapping.

---

**Question 490.** A developer created reusable code that several AWS Lambda functions need to use. The developer bundled the code into a zip archive. The developer needs to deploy the code to AWS and update the Lambda functions to use the code.

Which solution will meet this requirement in the MOST operationally efficient way?

A. Upload the zip archive to Amazon S3. Configure an import path on the Lambda functions to point to the zip archive.
B. Create a new Lambda function that contains and runs the shared code. Update the existing Lambda functions to invoke the new Lambda function synchronously.
C. Create a Lambda layer that contains the zip archive. Attach the Lambda layer to the Lambda functions.
D. Create a Lambda container image that includes the shared code. Use the container image as a Lambda base image for all the functions.

---

**Question 491.** A team has an Amazon API Gateway REST API that consists of a single resource and a GET method that is backed by an AWS Lambda integration. A developer needs to set up a process to test the new version in production before using the new version in production. The tests must not affect the production REST API.

Which solution will meet these requirements with the LEAST operational overhead?

A. Create a new REST API. Add a resource, and add a Lambda integration to the updated version of the Lambda function. Deploy the new version.
B. Create a new stage for the REST API. Add a stage variable. Assign the stage variable to the Lambda function. Set the API Gateway stage to point to the prod Lambda function alias. Deploy and test the Lambda function through the API Gateway stage.
C. Create a new REST API. Add a resource that is integrated with the new Lambda function version. Assign the stage variable to the new Lambda function alias. Deploy and test the Lambda function through the API Gateway stage.
D. Update the Lambda integration of the existing GET method to point to the updated version of the Lambda function. Deploy the new version.

---

**Question 492.** A company runs continuous integration/continuous delivery (CI/CD) pipelines for its application on AWS CodePipeline. A developer must incorporate unit tests as part of the pipelines before staging the artifacts for testing.

How should the developer incorporate unit tests as part of CI/CD pipelines?

A. Create a separate CodePipeline pipeline to run unit tests.
B. Update the AWS CodeBuild buildspec specification to include a phase to run unit tests.
C. Use the AWS CodeDeploy agent on an Amazon EC2 instance to run the unit tests.
D. Create a testing branch in a git repository for the pipelines to run unit tests.

---

**Question 493.** A developer is troubleshooting a three-tier application, which is deployed on Amazon EC2 instances. There is a connectivity problem between the application and the database servers.

Which AWS services or tools should be used to identify the faulty component? (Choose two.)

A. AWS CloudTrail
B. AWS Trusted Advisor
C. Amazon VPC Flow Logs
D. Network access control lists
E. AWS Config rules

---

**Question 494.** A developer is making changes to a custom application that uses AWS Elastic Beanstalk. Which solutions will update the Elastic Beanstalk environment with the new application version after the developer completes the changes? (Choose two.)

A. Package the application code into a tar file. Use the AWS Management Console to create a new application version from the tar file. Deploy the packaged application.
B. Package the application code into a tar file. Use the AWS Management Console to create a new application version from the tar file. Update the environment.
C. Package the application code into a .zip file. Use the AWS CLI to create a new application version from the .zip file and to update the environment.
D. Package the application code into a tar file. Use the AWS Management Console to create a new application version from the .zip file. Rebuild the environment by using the AWS CLI.
E. Package the application code into a .zip file. Use the AWS Management Console to create a new application version from the .zip file. Rebuild the environment.

---

**Question 495.** A developer needs to write an AWS CloudFormation template on a local machine and deploy a CloudFormation stack to AWS.

What must the developer do to complete these tasks?

A. Install the AWS CLI. Configure the AWS CLI by using an IAM user name and password.
B. Install the AWS CLI. Configure the AWS CLI by using an SSH key.
C. Install the AWS CLI. Configure the AWS CLI by using an IAM user access key and secret key.
D. Install an AWS software development kit (SDK). Configure the SDK by using an X.509 certificate.

---

**Question 496.** A developer is updating an Amazon API Gateway REST API to have a mock endpoint. The developer wants to update the integration request mapping template so the endpoint will respond to mock integration requests with specific HTTP status codes based on various conditions.

Which statement will meet these requirements?

A.
#if{ $input.params('integration') == "mock" }
"statusCode": 404
#else
"statusCode": 500
#end

B.
#if{ $input.params('scope') == "internal" }
"statusCode": 200
#else
"statusCode": 500
#end

C.
#if{ $input.path("integration") }
"statusCode": 200
#else
"statusCode": 404
#end

D.
#if( $context.integration.status)
"statusCode": 200
#else
"statusCode": 500
#end

---

**Question 497.** A large company has its application components distributed across multiple AWS accounts. The company needs to collect and visualize trace data across these accounts.

What should be used to meet these requirements?

A. AWS X-Ray
B. Amazon CloudWatch
C. Amazon VPC flow logs
D. Amazon OpenSearch Service

---

**Question 498.** A developer must cache dependent artifacts from Maven Central, a public package repository, as part of an application's build pipeline. The build pipeline has an AWS CodeArtifact repository where artifacts of the build are published. The developer needs a solution that requires minimum changes to the build pipeline.

Which solution meets these requirements?

A. Modify the existing CodeArtifact repository to associate an upstream repository with the public package repository.
B. Create a new CodeArtifact repository that has an external connection to the public package repository.
C. Create a new CodeArtifact domain that contains a new repository that has an external connection to the public package repository.
D. Modify the CodeArtifact repository resource policy to allow artifacts to be fetched from the public package repository.

---

**Question 499.** A developer is creating an AWS Step Functions state machine to handle an order processing workflow. When the state machine receives an order, the state machine pauses until the order has been confirmed. A record that is added to an Amazon DynamoDB table when an order is confirmed.

The developer must complete the order processing workflow.

Which solution will meet this requirement?

A. Update the state machine to query the DynamoDB table by using the DynamoDB GetItem state to determine whether a record exists. If the record does not exist, wait 5 minutes and check again.
B. Subscribe an AWS Lambda function to the DynamoDB table stream. Configure the Lambda function to run when a new record is added to the table. When the Lambda function receives the appropriate record, stop the redrive execution command on the running state machine invocation and start a new invocation.
C. Subscribe an AWS Lambda function from the DynamoDB table stream. Configure the Lambda function to continuously poll the DynamoDB table for the appropriate record and to return when a record exists. Configure the Lambda function state machine invocation. When the Lambda function times out, start a new invocation.
D. Invoke an AWS Lambda function from the state machine. Configure the Lambda function to continuously poll the DynamoDB table for the appropriate record and to return when a record exists. Configure the state machine invocation. When the Lambda function times out, start a new invocation.

---

**Question 500.** A developer is writing a web application that must share secure documents with end users. The documents are stored in a private Amazon S3 bucket. The application must allow only authenticated users to download specific documents when requested, and only for a duration of 15 minutes.

How can the developer meet these requirements?

A. Copy the documents to a separate S3 bucket that has a lifecycle policy for deletion after 15 minutes.
B. Create a presigned S3 URL using the AWS SDK with an expiration time of 15 minutes.
C. Use server-side encryption with AWS KMS managed keys (SSE-KMS) and download the documents using HTTPS.
D. Modify the S3 bucket policy to only allow specific users to download the documents. Revert the change after 15 minutes.

---

**Question 501.** A company is developing a set of AWS Lambda functions to process data. The Lambda functions need to use a common third-party library as a dependency. The library is frequently updated with new features and bug fixes. The company wants to ensure that the Lambda functions always use the latest version of the library.

Which solution will meet these requirements in the MOST operationally efficient way?

A. Store the dependency and the function code in an Amazon S3 bucket.
B. Create a Lambda layer that includes the library. Attach the layer to each Lambda function.
C. Install the dependency in an Amazon Elastic File System (Amazon EFS) file system. Attach the file system to each Lambda function.
D. Create a new Lambda function to load the library. Configure the existing Lambda functions to invoke the new Lambda function when the existing functions need to use the library.

---

**Question 502.** A company's application includes an Amazon DynamoDB table for product orders. The table has a primary partition key of orderId and has no sort key. The company is adding a new feature that requires the application to query the table by using the customerId attribute.

Which solution will provide this query functionality?

A. Change the existing primary key by setting customerId as the sort key.
B. Create a new global secondary index (GSI) on the table with a partition key of customerId.
C. Create a new local secondary index (LSI) on the table with a partition key of customerId.
D. Create a new local secondary index (LSI) on the table with a partition key of orderId and a sort key of customerId.

---

**Question 503.** A company hosts applications on premises. The on-premises servers generate audit logs that are available through an HTTP endpoint. The company needs an automated solution to regularly ingest and store large volumes of audit data from the on-premises servers. The company also needs to perform queries on the audit data. Which solution will meet these requirements in the MOST operationally efficient way?

A. Export the audit logs. Upload the logs to Amazon S3. Import the logs to an Amazon RDS DB instance.
B. Create an AWS Lambda function to call the HTTP endpoint to fetch audit logs. Configure an Amazon EventBridge scheduled rule to invoke the Lambda function. Configure the Lambda function to push the logs to AWS CloudTrail Lake.
C. Use AWS DataSync to transfer audit logs to an Amazon S3 bucket. Load the logs into an Amazon S3 bucket. Use Amazon Athena to query the bucket.
D. Install the Amazon CloudWatch agent on the on-premises servers. Give the agent the ability to push audit logs to CloudWatch. Use CloudWatch Insights to query the logs.

---

**Question 504.** A developer is building an application that includes an AWS Lambda function that is written in .NET Core. The Lambda function's code needs to interact with Amazon DynamoDB tables and Amazon S3 buckets. The developer must minimize the Lambda function's deployment time and invocation duration. Which solution will meet these requirements?

A. Increase the Lambda function's memory.
B. Include the entire AWS SDK for .NET in the Lambda function's deployment package.
C. Include only the AWS SDK for .NET modules for DynamoDB and Amazon S3 in the Lambda function's deployment package.
D. Configure the Lambda function to download the AWS SDK for .NET from an S3 bucket at runtime.

---

**Question 505.** A development team has an Amazon API Gateway REST API that is backed by an AWS Lambda function. Users have reported performance issues for the Lambda function. The development team identified the source of the issues as a cold start of the Lambda function. The development team needs to reduce the time needed for the Lambda function to initialize. Which solution will meet this requirement?

A. Change the Lambda concurrency to reserved concurrency.
B. Increase the timeout of the Lambda function.
C. Increase the memory allocation of the Lambda function.
D. Configure provisioned concurrency for the Lambda function.

---

**Question 506.** A video streaming company has a pipe in Amazon EventBridge Pipes that uses an Amazon Simple Queue Service (Amazon SQS) queue as an event source. The pipe publishes all source events to a target EventBridge event bus. Before events are published, the pipe uses an AWS Lambda function to retrieve the stream status of each event from a database and adds the stream status to each source event. The company wants the pipe to publish events to the event bus only if the video stream has a status of ready. Which solution will meet these requirements?

A. Add a filter step to the pipe that will match on a stream status of ready.
B. Update the Lambda function to return only video streams that have a status of ready.
C. Include a filter for a status of ready in all EventBridge rules that subscribe to the event bus.
D. Add an input transformer to the pipe output that filters streams that have a status of ready.

---

**Question 507.** A developer needs to build a workflow to handle messages that are sent to an Amazon Simple Queue Service (Amazon SQS) queue. When a message reaches the queue, the workflow must implement a delay before message delivery to allow sufficient time to process the message. Which solution will meet this requirement in the MOST operationally efficient way?

A. Create an AWS Step Functions state machine to process the SQS queue. Use a Wait state to delay the Lambda function's processing for the required number of seconds after message delivery to the SQS queue. Use Amazon EventBridge to invoke the state machine every 5 minutes.
B. Configure the Lambda function to poll the SQS queue. Update the Lambda code to include a custom attribute that contains a future time when the message should be fully processed. Update the Lambda code to fully process messages when the custom attribute's future time has been reached.
C. Set the DelaySeconds value of the SQS queue to be the number of seconds required to delay delivery of the messages. Add an event source mapping for the Lambda function. Specify the SQS queue as a source.
D. Set the Visibility Timeout value of the SQS queue to be the number of seconds required to delay delivery of the messages. Add an event source mapping for the Lambda function. Specify the SQS queue as a source.

---

**Question 508.** A company is building an application to accept data from customers. The data must be encrypted at rest and in transit. The application system uses an Amazon API Gateway REST API that resolves to AWS Lambda functions. The Lambda functions store the data in an Amazon Aurora MySQL DB cluster. The application worked properly during testing. A developer configured an Amazon CloudFront distribution with field-level encryption that uses an AWS Key Management Service (AWS KMS) key. After the configuration of the distribution, the application behaved unexpectedly. All the data in the database changed from plaintext to ciphertext. The developer must ensure that the data is not stored in the database as the ciphertext from the CloudFront field-level encryption. Which solution will meet these requirements?

A. Change the CloudFront Viewer protocol policy from "HTTP and HTTPS" to "HTTPS only."
B. Add a Lambda function to decrypt the data fields before saving the data to the database.
C. Enable encryption on the DB cluster by using the same KMS key that is used in CloudFront.
D. Request and deploy a new SSL certificate to use with the CloudFront distribution.

---

**Question 509.** A company offers a business-to-business software service that runs on dedicated infrastructure deployed in each customer's AWS account. Before a feature release, the company needs to run integration tests on real AWS test infrastructure. The test infrastructure consists of Amazon EC2 instances and an Amazon RDS database. A developer must set up a continuous delivery process that will provision the test infrastructure across the different AWS accounts. The developer then must run the integration tests. Which solution will meet these requirements with the LEAST administrative effort?

A. Use AWS CodeDeploy with AWS CloudFormation StackSets to deploy the infrastructure. Use Amazon CodeGuru to run the tests.
B. Use AWS CodePipeline with AWS CloudFormation StackSets to deploy the infrastructure. Use AWS CodeBuild to run the tests.
C. Use AWS CodePipeline with AWS CloudFormation change sets to deploy the infrastructure. Use a CloudFormation custom resource to run the tests.
D. Use AWS Serverless Application Model (AWS SAM) templates with AWS CloudFormation change sets to deploy the infrastructure. Use AWS CodeDeploy to run the tests.

---

**Question 510.** A developer is creating an application that uses an AWS Lambda function to transform and load data from an Amazon S3 bucket. When the developer tests the application, the developer finds that some invocations of the Lambda function are slower than others. The developer needs to update the Lambda function to have predictable invocation durations that run with low latency. Any initialization activities, such as loading libraries and instantiating clients, must run during allocation time rather than during actual function invocations. Which combination of steps will meet these requirements? (Choose two.)

A. Create a schedule group in Amazon EventBridge Scheduler to invoke the Lambda function.
B. Configure provisioned concurrency for the Lambda function to have the necessary number of execution environments.
C. Use the $LATEST version of the Lambda function.
D. Configure reserved concurrency for the Lambda function to have the necessary number of execution environments.
E. Deploy changes, and publish a new version of the Lambda function.

---

**Question 511.** A developer created an AWS Lambda function named ProcessMessages. The Lambda function is invoked asynchronously when a message is published to an Amazon Simple Notification Service (Amazon SNS) topic named InputTopic. The developer uses a second SNS topic named ErrorTopic to handle alerts of failures for the ProcessMessages Lambda function. The developer wants to receive notifications when the ProcessMessages Lambda function fails to process a message. Which solution will meet this requirement?

A. Configure a subscription for the ErrorTopic SNS topic. Create a filter policy for the ProcessMessages Lambda function. Specify the Amazon Resource Name (ARN) of the ErrorTopic as the endpoint.
B. Configure a failure destination for the ProcessMessages Lambda function. Specify the Amazon Resource Name (ARN) of the ErrorTopic SNS topic as the endpoint.
C. Configure a trigger for the ProcessMessages Lambda function. Specify the ErrorTopic SNS as the trigger. Configure a filter policy on the topic for failures. Specify the Lambda function as the endpoint.
D. Configure a delivery policy on the ErrorTopic SNS topic. Configure a filter policy for failures. Specify the Lambda function as the endpoint.

---

**Question 512.** A company is developing a new application that uses Amazon EC2, Amazon S3, and AWS Lambda resources. The company wants to allow employees to use their existing on-premises Active Directory. Each employee must have access to the same level of AWS resources that is based on their Active Directory group membership. Which solution will meet these requirements with the LEAST operational overhead?

A. Configure AWS Directory Service for Microsoft Active Directory to create an Active Directory in AWS Directory Service. Establish a trust relationship with the on-premises Active Directory. Configure IAM roles and trust policies to give the employees access to the AWS resources.
B. Use LDAP to directly integrate the on-premises AWS Identity and Access Management (IAM). Map AWS Identity and Access Management (IAM) groups to AWS resources for the employees.
C. Create a custom identity broker to authenticate users into the on-premises Active Directory. Configure the identity broker to use AWS Security Token Service (AWS STS) to grant authorized users IAM role-based access to the AWS resources.
D. Configure Amazon Cognito to federate users into the on-premises Active Directory. Use Cognito user pools to manage user identities and to manage user access to the AWS resources.

---

**Question 513.** A company has an Amazon DynamoDB table that contains records of users who have signed up for a trial of the company's product. The company is using a spreadsheet to track data about the product trial. The spreadsheet is automatically updated with the latest information when individual trial begins, are updated, or are deleted. The company wants to ensure the spreadsheet always has the most current data. Which solution will meet these requirements?

A. Create a DynamoDB Accelerator (DAX) cluster from the table. Set the view type to old image. Create an AWS Lambda function that uses the cluster data to update the spreadsheet. Subscribe the Lambda function to the cluster.
B. Create a DynamoDB Accelerator (DAX) cluster from the table. Set the view type to new image. Create an AWS Lambda function that uses the cluster data to update the spreadsheet. Subscribe the Lambda function to the cluster.
C. Enable a DynamoDB stream for the table. Set the view type to new image. Create an AWS Lambda function that uses the stream data to update the spreadsheet. Subscribe the Lambda function to the stream.
D. Enable a DynamoDB stream for the table. Set the view type to old image. Create an AWS Lambda function that uses the stream data to update the spreadsheet. Subscribe the Lambda function to the stream.

---

**Question 514.** A company generates SSL certificates from a third-party provider. The company imports the certificates into AWS Certificate Manager (ACM) to use the certificates. A developer must implement a solution to notify the company's security team 90 days before an imported certificate expires. The company already has configured an Amazon Simple Queue Service (Amazon SQS) queue. The company also has configured an Amazon Simple Notification Service (Amazon SNS) topic that has the security team's email address as a subscriber. Which solution will provide the security team with the required notifications about certificates?

A. Create an Amazon EventBridge rule that specifies the ACM Certificate Approaching Expiration event type. Set the SNS topic as the target.
B. Create an AWS Lambda function for certificates that are expiring within 90 days. Program the Lambda function to send each identified certificate's Amazon Resource Name (ARN) as a message to the SQS queue.
C. Create an AWS Step Functions workflow that is invoked by each certificate's expiration notification from AWS CloudTrail. Create an EventBridge rule that sends a message to the SQS queue every 24 hours. Create an Amazon EventBridge rule that takes an action as the Config Rules Compliance Change event type and the configured rule. Set the SNS topic as the EventBridge rule's target.
D. Configure the AWS Config with the non-certificate-expiration-check managed rule to run every 24 hours. Create an Amazon EventBridge rule that takes an action as the Config Rules Compliance Change event type and the configured rule. Set the SNS topic as the EventBridge rule's target.

---

**Question 515.** A developer has implemented an AWS Lambda function that inserts new customers into an Amazon RDS database. The function is configured to use 512 MB of RAM and is based on the following pseudo code:

```
def lambda_handler (event, context):
    db = database.connect()
    db.statement('INSERT INTO Customers (CustomerName) VALUES (event.name)')
    db.execute()
    db.close()
```

After successfully testing the function multiple times, the developer notices that the execution time is longer than expected. What should the developer do to improve performance?

A. Increase the reserved concurrency of the Lambda function.
B. Increase the size of the RDS database to facilitate an increased number of database connections each hour.
C. Move the database connection and close statement out of the handler. Place the connection in the global space.
D. Replace Amazon RDS with Amazon DynamoDB to implement control over the number of writes per second.

---

**Question 516.** A developer is troubleshooting the permissions of an application that needs to make changes to an Amazon RDS database. The developer has access to the IAM role that the application is using. Which command structure should the developer use to test the role permissions?

A. aws sts assume-role
B. aws iam attach-role-policy
C. aws ssm resume-session
D. aws rds add-role-to-db-cluster

---

**Question 517.** A company is building a social media application. A developer is modifying an AWS Lambda function that updates a database with data that tracks each user's online activity. A web application server uses the AWS SDK to invoke the Lambda function. The developer has tested the new Lambda code and is ready to deploy the code into production. However, the developer wants to allow only a small percentage of the invocations from the AWS SDK to call the new code. Which solution will meet these requirements?

A. Configure a Lambda version that has a specific weight value for the updated Lambda function.
B. Create an alias for the Lambda function. Configure a specific weight value for the updated version.
C. Create an Application Load Balancer. Specify weighted target groups for the original Lambda function and the updated Lambda function.
D. Create a Network Load Balancer. Specify weighted target groups for the original Lambda function and the updated Lambda function.

---

**Question 518.** A developer is building a three-tier web application that should be able to handle a minimum of 5000 requests per minute. Requirements state that the web tier should be completely stateless while the application maintains session state for the users. How can session data be externalized, keeping latency at the LOWEST possible value?

A. Create an Amazon ROS instance, then implement session handling at the application level to leverage a database inside the ROS database instance for session data storage.
B. Implement a shared file system solution across the underlying Amazon EC2 instances, then implement session handling at the application level to leverage the shared file system for session data storage.
C. Create an Amazon ElastiCache (Memcached) cluster, then implement session handling at the application level to leverage the cluster for session data storage.
D. Create an Amazon DynamoDB table, then implement session handling at the application level to leverage the table for session data storage.

---

**Question 519.** An AWS Lambda function that handles application requests uses the default Lambda logging mechanism to log the timestamp, processing time, and status of requests. A developer needs to create Amazon CloudWatch metrics based on the logs. The developer needs to write the metrics to a custom CloudWatch metrics namespace. Which solution will meet these requirements?

A. Use Amazon CloudWatch Logs Insights to generate custom metrics from the logs by using CloudWatch embedded metric format (EMF).
B. Use Amazon CloudWatch RUM to generate custom metrics from the logs by using CloudWatch embedded metric format (EMF).
C. Use Amazon CloudWatch Logs Insights to generate custom metrics from the logs by using JSON format.
D. Use the CloudWatch embedded metric format (EMF) for the structure of the log statements to generate custom CloudWatch metrics.

---

**Question 520.** A company has an application that processes audio files for different departments. When audio files are saved to an Amazon S3 bucket, an AWS Lambda function receives an event notification and processes the audio input. The application needs to process the audio files for each department independently. The application also needs to add the file location for each department to each department's existing Amazon Simple Queue Service (Amazon SQS) queue. Which solution will meet these requirements with no changes to the Lambda function code?

A. Configure the S3 bucket to send the event notifications to Amazon Simple Notification Service (Amazon SNS) topic. Subscribe each department's SQS queue to the SNS topic. Configure subscription filter policies.
B. Update the Lambda function to write the file location to a single shared SQS queue. Configure the shared SQS queue to send the file reference to each department's SQS queue.
C. Update the Lambda function to save the file location to the department's SQS queue independently.
D. Configure the S3 bucket to send the event notifications to each department's SQS queue.

---

**Question 521.** Two containerized microservices are hosted on Amazon EC2 ECS. The first microservice reads an Amazon RDS Aurora database instance, and the second microservice reads an Amazon DynamoDB table. How can each microservice be granted the minimum privilege?

A. Set ECS_ENABLE_TASK_IAM_ROLE to false on EC2 instance boot in ECS agent configuration file. Run the first microservice with an IAM role for ECS tasks with read-only access for the Aurora database. Run the second microservice with an IAM role for ECS tasks with read-only access to DynamoDB.
B. Set ECS_ENABLE_TASK_IAM_ROLE to false on EC2 instance boot in the ECS agent configuration file. Run the first microservice with an IAM role for ECS tasks with read-only access for the Aurora database. Grant the instance profile read-only access to the Aurora database and DynamoDB.
C. Set ECS_ENABLE_TASK_IAM_ROLE to true on EC2 instance boot in the ECS agent configuration file. Run the first microservice with an IAM role for ECS tasks with read-only access for the Aurora database. Run the second microservice with an IAM role for ECS tasks with read-only access to DynamoDB.
D. Set ECS_ENABLE_TASK_IAM_ROLE to true on EC2 instance boot in the ECS agent configuration file. Grant the instance profile role read-only access to the Aurora database and DynamoDB.

---

**Question 522.** An application that is running on Amazon EC2 instances stores data in an Amazon S3 bucket. All the data must be encrypted in transit. How can a developer ensure that all traffic to the S3 bucket is encrypted?

A. Install certificates on the EC2 instances.
B. Create a private VPC endpoint.
C. Configure the S3 bucket with server-side encryption with AWS KMS managed encryption keys (SSE-KMS).
D. Create an S3 bucket policy that denies traffic when the value for the aws:SecureTransport condition key is false.

---

**Question 523.** A company is hosting an Amazon API Gateway REST API that calls a single AWS Lambda function. The function is infrequently invoked by multiple clients at the same time. The code performance is optimal, but the company wants to optimize the startup time of the function. What can a developer do to optimize the initialization of the function?

A. Enable API Gateway caching for the REST API.
B. Configure provisioned concurrency for the Lambda function.
C. Use Lambda proxy integration for the REST API.
D. Configure AWS Global Accelerator for the Lambda function.

---

**Question 524.** A developer is building a three-tier application with an Application Load Balancer (ALB), Amazon EC2 instances, and Amazon RDS. There is an alias record in Amazon Route 53 that points to the ALB. When the developer tries to access the ALB from a laptop, the request times out. Which logs should the developer investigate to verify that the request is reaching the AWS network?

A. VPC Flow Logs
B. Amazon Route 53 logs
C. AWS Systems Manager Agent logs
D. Amazon CloudWatch agent logs

---

**Question 525.** A developer has an application that uses AWS Security Token Service (AWS STS). The application calls the STS AssumeRole API operation to provide trusted users with temporary security credentials. The application calls AWS STS at the service's default endpoint: https://sts.amazonaws.com. The application is deployed in an Asia Pacific AWS Region. The application is experiencing errors that are related to intermittent latency when the application calls AWS STS. What should the developer do to resolve this issue?

A. Update the application to use the GetSessionToken API operation.
B. Update the application to use the AssumeRoleWithSAML API operation.
C. Update the application to use a Regional STS endpoint that is closer to the application deployment.
D. Update the application to use the AssumeRoleWithWebIdentity API operation. Move the STS endpoint to a global endpoint.

---

**Question 526.** A company is launching a photo sharing application on AWS. Users use the application to upload images to an Amazon S3 bucket. When users upload images, an AWS Lambda function creates thumbnail versions of the images and stores the thumbnail versions in another S3 bucket. During development, a developer notices that the Lambda function takes more than 2 minutes to complete the thumbnail process. The company needs all images to be processed in less than 30 seconds. What should the developer do to meet these requirements?

A. Increase the virtual CPUs (VCPUs) for the Lambda function to use 10 VCPUs.
B. Change Lambda function instance type to use m6a.4xlarge.
C. Configure the Lambda function to increase the amount of memory.
D. Configure burstable performance for the Lambda function.

---

**Question 527.** A development team is designing a mobile app that requires multi-factor authentication. Which steps should be taken to achieve this? (Choose two.)

A. Use Amazon Cognito to create a user pool and create users in the user pool.
B. Send multi-factor authentication text codes to users with the Amazon SNS Publish API call in the app code.
C. Enable multi-factor authentication for the Amazon Cognito user pool.
D. Use AWS IAM to create IAM users.
E. Enable multifactor authentication for the users created in AWS IAM.

---

**Question 528.** A developer is building an application that will process messages from an Amazon Simple Queue Service (Amazon SQS) standard queue. The application needs to process the messages in an Amazon Elastic Container Service (Amazon ECS) task. Which actions will result in the MOST cost-effective processing of the messages? (Choose two.)

A. Use long polling to query the queue for new messages.
B. Use short polling to query the queue for new messages.
C. Use message batching to retrieve messages from the queue.
D. Use Amazon ElastiCache to cache messages in the queue.
E. Use an SQS FIFO queue to manage the messages.

---

**Question 529.** A developer is writing an application in AWS Lambda. To simplify testing and deployments, the developer needs the database connection string to be easily changed without modifying the Lambda code. How can this requirement be met?

A. Store the connection string as a secret in AWS Secrets Manager.
B. Store the connection string in an IAM user account.
C. Store the connection string in AWS KMS.
D. Store the connection string as a Lambda layer.

---

**Question 530.** A developer is building an image-processing application that includes an AWS Lambda function. The Lambda function moves images from one AWS service to another AWS service for image processing. For images that are larger than 2 MB, the Lambda function returns the following error: "Task timed out after 3.01 seconds." The developer needs to resolve the error without modifying the Lambda function code. Which solution will meet these requirements?

A. Increase the Lambda function's timeout value.
B. Configure the Lambda function to not move images that are larger than 2 MB.
C. Request a concurrency quota increase for the Lambda function.
D. Configure provisioned concurrency for the Lambda function.

**Question 531.** A developer has an application container, an AWS Lambda function, and an Amazon Simple Queue Service (Amazon SQS) queue. The Lambda function uses the SQS queue as an event source. The Lambda function makes a call to a third-party machine learning API when the function is invoked. The response from the third-party API can take up to 60 seconds to return. The Lambda function's timeout value is currently 65 seconds. The developer has noticed that the Lambda function sometimes processes duplicate messages from the SQS queue. What should the developer do to ensure that the Lambda function does not process duplicate messages?

A. Configure the Lambda function with a larger amount of memory.
B. Configure an increase in the Lambda function's timeout value.
C. Configure the SQS queue's delivery delay value to be greater than the maximum time it takes to call the third-party API.
D. Configure the SQS queue's visibility timeout value to be greater than the maximum time it takes to call the third-party API.

---

**Question 532.** A company has an application running on Amazon EC2 instances. The application needs to use dynamic feature flags that will be shared with other applications. The application must poll on an interval for new feature flag values. The values must be cached when they are retrieved. Which solution will meet these requirements in the MOST operationally efficient way?

A. Store the feature flag values in AWS Secrets Manager. Configure an Amazon ElastiCache node to cache the values by using a lazy loading strategy in the application. Update the application to poll for the values on an interval from ElastiCache.
B. Store the feature flag values in an Amazon DynamoDB table. Configure DynamoDB Accelerator (DAX) to cache the values by using a lazy loading strategy in the application. Update the application to poll for the values on an interval from DynamoDB.
C. Store the feature flag values in AWS AppConfig. Configure AWS AppConfig Agent on the EC2 instance to poll for the values on an interval. Configure the application to use the AWS SDK to retrieve the values from AppConfig Agent.
D. Store the feature flag values in AWS Systems Manager Parameter Store. Configure the application to poll on an interval. Configure the application to use the AWS SDK to retrieve the values from Parameter Store and to store the values in memory.

---

**Question 533.** A team deploys an AWS CloudFormation template to update a stack that already included an Amazon DynamoDB table. However, before the deployment of the update, the team changed the name of the DynamoDB table on the template by mistake. The DeletionPolicy attribute for all resources has the default value. What will be the result of this mistake?

A. CloudFormation will create a new table and will delete the existing table.
B. CloudFormation will create a new table and will keep the existing table.
C. CloudFormation will overwrite the existing table and will rename the existing table.
D. CloudFormation will keep the existing table and will not create a new table.

---

**Question 534.** A developer is deploying an application on an Amazon Elastic Container Service (Amazon ECS) cluster that uses AWS Fargate. The developer is using a Docker container with an Ubuntu image. The developer needs to implement a solution to store application data that is available from multiple ECS tasks. The application data must remain accessible after the container is terminated. Which solution will meet these requirements?

A. Attach an Amazon FSx for Windows File Server volume to the container definition.
B. Specify the DockerVolumeConfiguration parameter in the ECS task definition to attach a Docker volume.
C. Create an Amazon Elastic File System (Amazon EFS) file system. Specify the mountPoints attribute and the efsVolumeConfiguration attribute in the ECS task definition.
D. Create an Amazon Elastic Block Store (Amazon EBS) volume. Specify the mount point configuration in the ECS task definition.

---

**Question 535.** A developer is creating an AWS Lambda function that needs network access to private resources in a VPC. Which solution will provide this access with the LEAST operational overhead?

A. Attach the Lambda function to the VPC through private subnets. Create a security group that allows network access to the private resources. Associate the security group with the Lambda function.
B. Configure the Lambda function to route traffic through a VPN connection. Create a security group that allows network access to the private resources. Associate the security group with the Lambda function.
C. Configure a VPC endpoint connection for the Lambda function. Set up the VPC endpoint to route traffic through a NAT gateway.
D. Configure an AWS PrivateLink endpoint for the private resources. Configure the Lambda function to reference the PrivateLink endpoint.

---

**Question 536.** A developer needs to automate deployments for a serverless, event-based workload. The developer needs to create standardized templates to define the infrastructure and to test the functionality of the workload locally before deployment. The developer already uses a pipeline in AWS CodePipeline. The developer needs to incorporate any other infrastructure changes into the existing pipeline. Which solution will meet these requirements?

A. Create an AWS Serverless Application Model (AWS SAM) template. Configure the pipeline stages in CodePipeline to run the necessary AWS SAM CLI commands to deploy the serverless workload.
B. Create an AWS Step Functions workflow template based on the infrastructure by using the Amazon States Language. Start the Step Functions state machine from the existing pipeline.
C. Use the existing pipeline workflow to build a pipeline for AWS CloudFormation stacks.
D. Create an AWS Serverless Application Model (AWS SAM) template. Use an automated script to deploy the serverless workload by using the AWS SAM CLI deploy command.

---

**Question 537.** A developer is creating a stock trading application. The developer needs a solution to send text messages to application users to confirm when a trade has been completed. The solution must deliver messages in the order a user makes stock trades. The solution must not send duplicate messages. Which solution will meet these requirements?

A. Configure the application to publish messages to an Amazon Data Firehose delivery stream. Configure the delivery stream to have a destination of each user's mobile phone number that is passed in the trade confirmation message.
B. Create an Amazon Simple Queue Service (Amazon SQS) FIFO queue. Use the SendMessageOut API call to send the trade confirmation messages to the queue. Use the SendMessageOut API to send the messages to users by using the information provided in the trade confirmation message.
C. Create a pipe in Amazon EventBridge Pipes. Connect the application to the pipe as a source. Configure the pipe to use each user's mobile phone number as a target. Configure the pipe to send incoming events to the users.
D. Create an Amazon Simple Notification Service (Amazon SNS) topic. Configure an event source mapping for the SNS topic. Configure the application to use the AWS SDK to publish notifications to the SNS topic to send SMS messages to the users.

---

**Question 538.** A developer is deploying a new Node.js AWS Lambda function that is not connected to a VPC. The Lambda function needs to connect to and query an Amazon Aurora database that is not publicly accessible. The developer is expecting unpredictable surges in database traffic. What should the developer do to give the Lambda function access to the database?

A. Configure the Lambda function to use an Amazon RDS proxy.
B. Configure a NAT gateway. Attach the NAT gateway to the Lambda function.
C. Enable public access on the Aurora database. Configure a security group on the database to allow outbound access for the database engine's port.
D. Enable VPC access for the Lambda function. Attach the Lambda function to a new security group that does not have rules.

---

**Question 539.** A company uses two AWS accounts: production and development. The company stores data in an Amazon S3 bucket that is in the production account. The data is encrypted with an AWS Key Management Service (AWS KMS) customer managed key. The company plans to copy the data to another S3 bucket in the development account. A developer needs to use a KMS key to encrypt the data in the S3 bucket that is in the development account. The KMS key in the development account must be accessible from the production account. Which solution will meet these requirements?

A. Replicate the customer managed KMS key from the production account to the development account. Specify the production account in the key policy.
B. Create a new customer managed KMS key in the development managed account. Specify the production account in the key policy.
C. Replicate a new AWS managed KMS key for Amazon S3 from the production account to the development account. Specify the production account in the key policy.
D. Replicate the default AWS managed KMS key for Amazon S3 from the production account to the development account. Specify the production account in the key policy.

---

**Question 540.** A developer is using AWS CodeDeploy to launch an application onto Amazon EC2 instances. The application deployment fails during testing. The developer notices an IAM_ROLE_PERMISSIONS error code in Amazon CloudWatch logs. What should the developer do to resolve the error?

A. Ensure that the deployment group is using the correct role name for the CodeDeploy service role.
B. Attach the AWSCodeDeployRoleECS policy to the CodeDeploy service role.
C. Attach the AWSCodeDeployRole policy to the CodeDeploy service role.
D. Ensure the CodeDeploy agent is installed and running on all instances in the deployment group.

---

**Question 541.** A company wants to send notifications to customers to advertise a sale on the company's products. The company needs to use Amazon Simple Notification Service (Amazon SNS) FIFO topics. The company needs to examine the rate at which the topics send notifications and the latency with which the topics send notifications. Which solution will meet these requirements with the MOST operational efficiency?

A. Use AWS X-Ray. Enable active tracing for Amazon SNS.
B. Use the Amazon CloudWatch NumberOfNotificationsFailed metric.
C. Use AWS CloudTrail to log all Amazon SNS API calls.
D. Use Amazon GuardDuty. Enable runtime monitoring.

---

**Question 542.** A cloud-based video surveillance company is developing an application that analyzes video files. After the application analyzes the files, the company can discard the files. The company stores the files in an Amazon S3 bucket. The files are 1 GB in size on average. No file is larger than 2 GB. An AWS Lambda function processes one file for each video file that is processed. The processing is way IO intensive, and the application must read each file multiple times. Which solution will meet these requirements in the MOST performance-optimized way?

A. Attach an Amazon Elastic Block Store (Amazon EBS) volume that is larger than 2 GB to the Lambda function. Copy the files from the S3 bucket to the EBS volume.
B. Attach an Elastic Network Adapter (ENA) to the Lambda function. Use the ENA to read the video files from the S3 bucket.
C. Increase the ephemeral storage to 2 GB. Lambda the files from the S3 bucket to the /tmp directory of the Lambda function.
D. Configure the Lambda function to read from the S3 bucket directly.

---

**Question 543.** A company has an AWS Step Functions state machine named myStateMachine. The company configured a service role for Step Functions. The developer must ensure that only the myStateMachine state machine can assume the service role. Which statement should the developer add to the trust policy to meet this requirement?

A. "Condition": {
"ArnLike": {
"aws:SourceArn": "arn:aws:states:ap-south-1:11111111111:stateMachine:myStateMachine"
}}

B. "Condition": {
"ArnLike": {
"aws:SourceArn": "arn:aws:states:ap-south-1:*:stateMachine:myStateMachine"
}}

C. "Condition": {
"StringEquals": {
"aws:SourceAccount": "11111111111"
}}

D. "Condition": {
"StringNotFoundEquals": {
"aws:SourceArn": "arn:aws:states:ap-south-1:11111111111:stateMachine:myStateMachine"
}}

---

**Question 544.** A company stores customer credit reports in an Amazon S3 bucket. An analytics service uses standard Amazon S3 GET requests to access the reports. A developer must implement a solution to redact personally identifiable information (PII) from the reports before the reports reach the analytics service. Which solution will meet this requirement with the MOST operational efficiency?

A. Load the S3 objects into Amazon Redshift by using a COPY command. Implement dynamic data masking. Refactor the analytics service to read from Amazon Redshift.
B. Set up an S3 Object Lambda function. Attach the function to the endpoint. Integrate the endpoint with the mobile app. Use the function to call a PII redaction API.
C. Use AWS Key Management Service (AWS KMS) to implement encryption in the S3 bucket. Re-upload all the existing S3 objects. Give the kms:Decrypt permission to the analytics service.
D. Create an Amazon Simple Notification Service (Amazon SNS) topic. Implement message data protection. Refactor the analytics service to publish data access requests to the SNS topic.

---

**Question 545.** A company is using the AWS Serverless Application Model (AWS SAM) to develop a social media application. A developer needs a quick way to test AWS Lambda functions locally by using test event payloads. The developer needs the structure of these test event payloads to match the actual events that AWS services create. Which solution will meet these requirements with the LEAST development effort?

A. Create shareable test Lambda events. Use these test Lambda events for local testing.
B. Store manually created test event payloads locally. Use the sam local invoke command with the file path to the payloads.
C. Store manually created test event payloads in an Amazon S3 bucket. Use the sam local invoke command with the S3 path to the payloads.
D. Use the sam local generate-event command to create test payloads for local testing.

---

**Question 546.** A developer is building the authentication mechanism for a new mobile app. Users need to be able to sign up, sign in, and access secured backend AWS resources. Which solution will meet these requirements?

A. Use AWS Identity and Access Management Access Analyzer to generate IAM policies. Create an IAM role. Attach the policies to the role. Integrate the IAM role with an identity provider that the mobile app uses.
B. Create an IAM policy that grants access to the backend resources. Create an IAM role. Attach the policy to the role. Create an Amazon API Gateway endpoint. Attach the role to the endpoint. Integrate the endpoint with the mobile app.
C. Create an Amazon Cognito identity pool. Configure permissions by choosing a default IAM role for authenticated users or guest users in the identity pool. Create a user pool to identify the app's users. Specify the identity pool with the mobile app.
D. Create an Amazon Cognito user pool. Configure the security requirements by choosing a password policy, multi-factor authentication (MFA) requirements, and user account recovery options. Create an app client. Integrate the app client with the mobile app.

---

**Question 547.** A developer is designing an event-driven architecture. An AWS Lambda function that processes data needs to push processed data to a subset of four consumer Lambda functions. The data must be routed based on the value of one field in the data. Which solution will meet these requirements with the LEAST operational overhead?

A. Create an Amazon Simple Queue Service (Amazon SQS) queue and event source mapping for each consumer Lambda function. Add message routing logic to the data-processing Lambda function.
B. Create an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe the four consumer Lambda functions to the topic. Add message filtering logic to each consumer Lambda function. Subscribe the data-processing Lambda function to the SNS topic.
C. Create a separate Amazon Simple Notification Service (Amazon SNS) topic and subscription for each consumer Lambda function. Add message routing logic to the data-processing Lambda function to publish to the appropriate topic.
D. Create a single Amazon Simple Notification Service (Amazon SNS) topic. Subscribe the four consumer Lambda functions to the topic. Add SNS subscription filter policies to each subscription. Configure the data-processing Lambda function to publish to the topic.

---

**Question 548.** A developer is creating a new application that will give users the ability to upload documents to Amazon S3. The contents of the documents must not be accessible to any third party. Which type of encryption will meet this requirement?

A. Client-side encryption by using the S3 Encryption Client with a Raw RSA wrapping key that is stored on the user's device
B. Server-side encryption with S3 managed keys (SSE-S3)
C. Server-side encryption with AWS KMS keys (SSE-KMS)
D. Dual-layer server-side encryption with AWS KMS keys (DSSE-KMS)

---

**Question 549.** A developer is building an application that consists of many AWS Lambda functions. The Lambda functions connect to a single Amazon RDS database. The developer needs to implement a solution to store the database credentials securely. When the credentials are updated, the Lambda functions must be able to use the new credentials without requiring a code update or a configuration update. Which solution will meet these requirements?

A. Store the credentials as a secret in AWS Secrets Manager. Access the secret at runtime from within the Lambda functions.
B. Store the credentials as a secret in AWS Secrets Manager. Access the credentials in environment variables by using the containerDefinitions and valueFrom properties in reference to the secret value.
C. Store the credentials as a SecureString parameter in AWS Systems Manager Parameter Store. Add a trigger to pass the credentials to the Lambda functions each time the Lambda functions run.
D. Store the credentials as a SecureString parameter in AWS Systems Manager Parameter Store. Add a reference to the parameter in an environment variable in the Lambda functions.

---

**Question 550.** A developer is building an application that includes an Amazon CloudFront distribution and that uses AWS Lambda functions. The application includes an Amazon CloudFront distribution and uses AWS Lambda functions. The user can use a transaction across multiple fields. The data can be encrypted. Only specific parts of the application need to have the ability to decrypt the data. Which solution will meet these requirements?

A. Associate the CloudFront distribution with a Lambda@Edge function. Configure the function to perform field-level asymmetric encryption by using a user-defined RSA public key that is stored in AWS Key Management Service (AWS KMS).
B. Integrate AWS WAF with CloudFront to protect the sensitive data. Use a Lambda function and self-managed keys to perform the encryption and decryption processes.
C. Configure the CloudFront distribution to use WebSockets by forwarding all viewer request headers to the origin. Create an asymmetric AWS KMS key. Configure the CloudFront distribution to use field-level encryption. Use the AWS KMS key.
D. Configure the cache behavior in the CloudFront distribution to require HTTPS for communication between viewers and CloudFront. Configure CloudFront to require users to access the files by using either signed URLs or signed cookies.

---

**Question 551.** An application includes an Amazon DynamoDB table that is named accountIds. The GSI has a partition key of id and a global secondary index (GSI) that is named as accountIndex. The GSI has a partition key of accountId and a sort key of orderDateTime. A developer needs to create an AWS Lambda function to retrieve the orders that have an accountId >= 100. Which solution will meet these requirements by using the LEAST read capacity units?

A. Define a DynamoDB-DB request for the GetItem action with the following parameters:
{ "TableName": "orders", "Key": { "accountId": { "N": "${ accountId }" } }, "FilterExpression": "accountId >= :accountId", "ExpressionAttributeValues": { ":accountId": { "N": "100" } } }

B. Define a DynamoDB-DB request for the BatchGetItem action with the following parameters:
{ "RequestItems": { "orders": { "Keys": [ { "accountId": { "N": "${ accountId }" } } ] } } }

C. Define a DynamoDB-DB request for the Scan action with the following parameters:
{ "TableName": "orders", "IndexName": "accountIndex", "FilterExpression": "accountId >= :accountId", "ExpressionAttributeValues": { ":accountId": { "N": "100" } } }

D. Define a DynamoDB-DB request for the Query action with the following parameters:
{ "TableName": "orders", "IndexName": "accountIndex", "KeyConditionExpression": "accountId >= :accountId", "ExpressionAttributeValues": { ":accountId": { "N": "100" } } }

---

**Question 552.** A company stores data in an Amazon S3 bucket. The data is updated multiple times every day from an application that runs on a server in the company's on-premises data center. The company enables S3 Versioning on the S3 bucket. After some time, the company observes multiple versions of the same objects in the S3 bucket. The company needs the S3 bucket to keep the current version of each object and the version immediately previous to the current version. Which solution will meet these requirements?

A. Configure an S3 bucket policy to retain one newer noncurrent version of the objects.
B. Configure an S3 Lifecycle rule to retain one newer noncurrent version of the objects.
C. Enable S3 Object Lock. Configure an S3 Object Lock policy to retain one newer noncurrent version of the objects.
D. Suspend S3 Versioning. Modify the application code to check the number of object versions before updating the objects.

---

**Question 553.** A company is creating a new feature for existing software. Before the company fully releases a new version of the software, the company wants to test the feature. The company needs to gather feedback about the feature from a small group of users while the current software version remains deployed. If the testing validates the feature, the company needs to deploy the new software version to all other users at the same time. Which deployment strategy will meet these requirements?

A. All-at-once deployment
B. Canary deployment
C. In-place deployment
D. Linear deployment

---

**Question 554.** A developer has an application that runs in AWS Account A. The application must retrieve an AWS Secure Manager secret that is encrypted by an AWS Key Management Service (AWS KMS) key from AWS Account B. The application's role has permission to access the secret in Account B. The developer must add a statement to the KMS key's key policy to allow the role in Account A to use the KMS key in Account B. The permissions must grant least privilege access to the role. Which permissions will meet these requirements?

A. kms:Decrypt and kms:DescribeKey
B. secretmanager:DescribeSecret and secretmanager:GetSecretValue
C. kms.*
D. secretmanager.**

---

**Question 555.** A developer created several AWS Lambda functions that write data to a single Amazon S3 bucket. The developer configured all the Lambda functions to send logs and metrics to Amazon CloudWatch. The developer receives reports that one of the Lambda functions writes data to the bucket very slowly. The developer needs to measure the latency between the problematic Lambda function and the S3 bucket. Which solution will meet this requirement?

A. Enable AWS X-Ray on the Lambda function. In the generated trace map, select the line between Lambda and Amazon S3.
B. Query the Lambda function's log file in Amazon CloudWatch Logs Insights. Return the average of the auto-discovered @duration field.
C. Enable CloudWatch Lambda Insights on the function. View the latency graph that CloudWatch Lambda Insights provides.
D. Enable AWS X-Ray on the Lambda function. Select Amazon S3 in the latency graph to view the latency histogram.

---

**Question 556.** A company's developer needs to activate Amazon CloudWatch Logs insights for AWS Lambda functions. The SAM template includes a resource that is named CloudWatchLogGroup. How should the developer update the SAM template to activate CloudWatch Logs insights for the Lambda functions?

A. Add an parameter named CloudWatchInsightsRole that contains a value of the Amazon Resource Name (ARN) for the CloudWatchLogGroup resource.
B. Add a parameter named CloudWatchLogGroupNamePrefix that contains a value of the application name. Reference the new parameter in the CloudWatchLogGroup resource.
C. For each Lambda function, add the layer for the Lambda Insights extension and the CloudWatchLambdaInsightsExecutionRolePolicy AWS managed policy.
D. For each Lambda function, set Tracing mode to Active and add the CloudWatchLambdaInsightsExecutionRolePolicy AWS managed policy.

---

**Question 557.** A developer is designing a game that stores data in an Amazon DynamoDB table. The partition key of the table is the country of the player. After a sudden increase in the number of players in a specific country, the developer notices ProvisionedThroughputExceededException errors. What should the developer do to resolve these errors?

A. Use strongly consistent table reads.
B. Reside the primary key to use more unique identifiers.
C. Use pagination to reduce the size of the items that the queries return.
D. Use the Scan operation to retrieve the data.

---

