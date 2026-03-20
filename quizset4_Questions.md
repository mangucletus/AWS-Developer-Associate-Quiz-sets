# AWS Developer Associate - Quiz Set 4 (Questions 326–443)

**Question 326.** Given the following AWS CloudFormation template:

Description: Creates a new Amazon S3 bucket for shared content. Uses a random bucket name to avoid conflicts.

Resources:
  ContentBucket:
    Type: AWS::S3::Bucket
Outputs:
  ContentBucketName:
    Value: !Ref ContentBucket

What is the MOST efficient way to reference the new Amazon S3 bucket from another AWS CloudFormation template?

A. Add an Export declaration to the Outputs section of the original template and use ImportValue in other templates.
B. Add Exported: true to the ContentBucket in the original template and use ImportResource in other templates.
C. Create a custom AWS CloudFormation resource that gets the bucket name from the ContentBucket resource of the first stack.
D. Use Fn::Include to include the existing template in other templates and use the ContentBucket resource directly.

---

**Question 327.** A developer has built an application that inserts data into an Amazon DynamoDB table. The table is configured to use provisioned capacity. The application is deployed on a burstable nano Amazon EC2 instance. The application logs show that the application has been failing because of a ProvisionedThroughputExceededException error.
Which actions should the developer take to resolve this issue? (Choose two.)

A. Move the application to a larger EC2 instance.
B. Increase the number of read capacity units (RCUs) that are provisioned for the DynamoDB table.
C. Reduce the frequency of requests to DynamoDB by implementing exponential backoff.
D. Increase the frequency of requests to DynamoDB by decreasing the retry delay.
E. Change the capacity mode of the DynamoDB table from provisioned to on-demand.

---

**Question 328.** A company has deployed an application on AWS Elastic Beanstalk. The company has configured the Auto Scaling group that is associated with the Elastic Beanstalk environment to have five Amazon EC2 instances. If the capacity is fewer than four EC2 instances during the deployment, application performance degrades. The company is using the all-at-once deployment policy.
What is the MOST cost-effective way to solve the deployment issue?

A. Change the Auto Scaling group to six desired instances.
B. Change the deployment policy to traffic splitting. Specify an evaluation time of 1 hour.
C. Change the deployment policy to rolling with additional batch. Specify a batch size of 1.
D. Change the deployment policy to rolling. Specify a batch size of 2.

---

**Question 329.** A developer is planning to use an Amazon API Gateway and AWS Lambda to provide a REST API. The developer will have three distinct environments to manage: development, test, and production.
How should the application be deployed while minimizing the number of resources to manage?

A. Create a separate API Gateway and separate Lambda function for each environment in the same Region.
B. Assign a Region for each environment and deploy API Gateway and Lambda to each Region.
C. Create one API Gateway with multiple stages with one Lambda function with multiple aliases.
D. Create one API Gateway and one Lambda function, and use a REST parameter to identify the environment.

---

**Question 330.** A developer registered an AWS Lambda function as a target for an Application Load Balancer (ALB) using a CLI command. However, the Lambda function is not being invoked when the client sends requests through the ALB.
Why is the Lambda function not being invoked?

A. A Lambda function cannot be registered as a target for an ALB.
B. A Lambda function can be registered with an ALB using AWS Management Console only.
C. The permissions to invoke the Lambda function are missing.
D. Cross-zone is not enabled on the ALB.

---

**Question 331.** A developer is creating an AWS Lambda function that will connect to an Amazon RDS for MySQL instance. The developer wants to store the database credentials. The database credentials need to be encrypted and the database password needs to be automatically rotated.
Which solution will meet these requirements?

A. Store the database credentials as environment variables for the Lambda function. Set the environment variables to rotate automatically.
B. Store the database credentials in AWS Secrets Manager. Set up managed rotation on the database credentials.
C. Store the database credentials in AWS Systems Manager Parameter Store as secure string parameters. Set up managed rotation on the parameters.
D. Store the database credentials in the X-Amz-Security-Token parameter. Set up managed rotation on the parameter.

---

**Question 332.** A developer wants to reduce risk when deploying a new version of an existing AWS Lambda function. To test the Lambda function, the developer needs to split the traffic between the existing version and the new version of the Lambda function.
Which solution will meet these requirements?

A. Configure a weighted routing policy in Amazon Route 53. Associate the versions of the Lambda function with the weighted routing policy.
B. Create a function alias. Configure the alias to split the traffic between the two versions of the Lambda function.
C. Create an Application Load Balancer (ALB) that uses the Lambda function as a target. Configure the ALB to split the traffic between the two versions of the Lambda function.
D. Create the new version of the Lambda function as a Lambda layer on the existing version. Configure the layer to split the traffic between the two layers.

---

**Question 333.** A developer is writing a web application that allows users to sign in. The application will run on Amazon EC2 instances behind an Application Load Balancer (ALB). The instances are in an Auto Scaling group across multiple Availability Zones.
How can the developer ensure that users stay signed in when the Auto Scaling group is scaled down?

A. Enable sticky sessions on the ALB target group.
B. Create an Amazon DynamoDB table. Configure the application to use the DynamoDB table to store session state such as login status.
C. Create an Amazon Elastic Block Store (Amazon EBS) volume. Use EBS Multi-Attach to attach the volume to all instances in the Auto Scaling group. Configure the application to use the volume to store session state such as login status.
D. Enable deregistration delay on the ALB target group.

---

**Question 334.** A developer is troubleshooting an application in an integration environment. In the application, an Amazon Simple Queue Service (Amazon SQS) queue consumes messages and then an AWS Lambda function processes the messages. The Lambda function transforms the messages and makes an API call to a third-party service. There has been an increase in application usage. The third-party API frequently returns an HTTP 429 Too Many Requests error message. The error message prevents a significant number of messages from being processed successfully.
How can the developer resolve this issue?

A. Increase the SQS event source's batch size setting.
B. Configure provisioned concurrency for the Lambda function based on the third-party API's documented rate limits.
C. Increase the retry attempts and maximum event age in the Lambda function's asynchronous configuration.
D. Configure maximum concurrency on the SQS event source based on the third-party service's documented rate limits.

---

**Question 335.** A company has a three-tier application that is deployed in Amazon Elastic Container Service (Amazon ECS). The application is using an Amazon RDS for MySQL DB instance. The application performs more database reads than writes. When this performance degradation occurs, the DB instance's ReadLatency metric in Amazon CloudWatch increases suddenly.
How should a developer modify the application to improve performance?

A. Use Amazon ElastiCache to cache query results.
B. Scale the ECS cluster to contain more ECS instances.
C. Add read capacity units (RCUs) to the DB instance.
D. Modify the ECS task definition to increase the task memory.

---

**Question 336.** A developer is writing an application to encrypt files outside of AWS before uploading the files to an Amazon S3 bucket. The encryption must be symmetric and must be performed inside the application.
How can the developer implement the encryption in the application to meet these requirements?

A. Create a data key in AWS Key Management Service (AWS KMS). Use the AWS Encryption SDK to encrypt the files.
B. Create a Hash-Based Message Authentication Code (HMAC) key in AWS Key Management Service (AWS KMS). Use the AWS Encryption SDK to encrypt the files.
C. Create a data key pair in AWS Key Management Service (AWS KMS). Use the AWS Encryption SDK to encrypt the files.
D. Create a data key in AWS Key Management Service (AWS KMS). Use the AWS CLI to encrypt the files.

---

**Question 337.** A developer is working on an application that is deployed on an Amazon EC2 instance. The developer needs a solution that will securely transfer files from the application to an Amazon S3 bucket.
What should the developer do to meet these requirements in the MOST secure way?

A. Create an IAM user. Create an access key for the IAM user. Store the access key in the application's environment variables. Associate the IAM role to access the specific Amazon S3 API calls the application requires. Configure the S3 bucket policy to allow access for the EC2 instance ID.
B. Create an IAM role. Configure the IAM role to access the specific Amazon S3 API calls the application requires. Associate the IAM role with the EC2 instance.
C. Configure an S3 bucket policy for the S3 bucket. Configure the S3 bucket policy to allow access for the EC2 instance ID.
D. Configure an S3 bucket policy for the S3 bucket. Configure the S3 bucket policy to allow access for the EC2 instance ID.

---

**Question 338.** A developer created a web API that receives requests by using an internet-facing Application Load Balancer (ALB) with an HTTPS listener. The developer configures an Amazon Cognito user pool and wants to ensure that every request to the API is authenticated through Amazon Cognito.
What should the developer do to meet this requirement?

A. Add a listener rule to the listener to return a fixed response if the Authorization header is missing. Set the fixed response to 401 Unauthorized. Create an authentication action for the listener rules of the ALSet. Set the OnUnauthenticatedRequest field to "deny."
B. Create an authentication action for the listener rules of the ALB. Configure all API methods to be forwarded to the ALB endpoint. Create an authorizer of the COGNITO_USER_POOLS type. Configure every API method to use that authorizer.
C. Create a new target group that includes an AWS Lambda function target that validates the Authorization header by using Amazon Cognito. Associate the new target group with the listener.
D. Create a new target group that includes an AWS Lambda function target that validates the Authorization header by using Amazon Cognito. Associate the new target group with the listener.

---

**Question 339.** A company recently deployed an AWS Lambda function. A developer notices an increase in the function throttle metrics in Amazon CloudWatch.
What are the MOST operationally efficient solutions to reduce the function throttling? (Choose two.)

A. Migrate the function to Amazon Elastic Kubernetes Service (Amazon EKS).
B. Increase the maximum age of events in Lambda.
C. Increase the function's reserved concurrency.
D. Add the lambda:GetFunctionConcurrency action to the execution role.
E. Request a service quota change for increased concurrency.

---

**Question 340.** A company is creating a REST service using an Amazon API Gateway with AWS Lambda integration. The service must run different versions for testing purposes.
What would be the BEST way to accomplish this?

A. Use an X-Version header to denote which version is being called and pass that header to the Lambda function(s).
B. Create an API Gateway Lambda authorizer to route API clients to the correct API version.
C. Create an API Gateway resource policy to isolate versions and provide context to the Lambda function(s).
D. Deploy the API versions as unique stages with unique endpoints and use stage variables to provide further context.

---

**Question 341.** A developer is building a serverless application by using AWS Serverless Application Model (AWS SAM) on multiple AWS Lambda functions. When the application is deployed, the developer wants to shift 10% of the traffic to the new deployment of the application for the first 10 minutes after deployment. If there are no issues, all traffic must switch over to the new version.
Which change to the AWS SAM template will meet these requirements?

A. Set the Deployment Preference Type to Canary10Percent10Minutes. Set the AutoPublishAlias property to the Lambda alias.
B. Set the Deployment Preference Type to Linear10PercentEvery10Minutes. Set the AutoPublishAlias property to the Lambda alias.
C. Set the Deployment Preference Type to Canary10Percent10Minutes. Set the PreTraffic and PostTraffic properties to the Lambda alias.
D. Set the Deployment Preference Type to Linear10PercentEvery10Minutes. Set the PreTraffic and PostTraffic properties to the Lambda alias.

---

**Question 342.** A company is using AWS CodePipeline to deliver one of its applications. The delivery pipeline is triggered by changes to the main branch of an AWS CodeCommit repository and uses AWS CodeBuild to implement the test and build stages of the process and AWS CodeDeploy to deploy the application. The pipeline has been operating successfully for several months and there have been no modifications. Following a recent change to the application's source code, AWS CodeDeploy has not deployed the updated application as expected.
What are the possible causes? (Choose two.)

A. The change was not made in the main branch of the AWS CodeCommit repository.
B. One of the earlier stages in the pipeline failed and the pipeline has terminated.
C. One of the Amazon EC2 instances in the company's AWS CodePipeline cluster is inactive.
D. The AWS CodePipeline is incorrectly configured and is not invoking AWS CodeDeploy.
E. AWS CodePipeline does not have permissions to access AWS CodeCommit.

---

**Question 343.** An AWS Lambda function is running in a company's shared AWS account. The function needs to perform an additional ec2:DescribeInstances action that is directed at the company's development accounts. A developer must configure the required permissions across the accounts.
How should the developer configure the permissions to adhere to the principle of least privilege?

A. Create an IAM role in the shared account. Add the ec2:DescribeInstances permission to the role. Establish a trust relationship between the development accounts for this role. Update the Lambda function IAM role in the shared account by adding the ec2:DescribeInstances permission to the role.
B. Create an IAM role in the development accounts. Add the ec2:DescribeInstances permission to the role. Establish a trust relationship with the shared account for this role. Update the Lambda function IAM role in the shared account by adding the iam:AssumeRole permissions.
C. Create an IAM role in the shared account. Add the ec2:DescribeInstances permission to the role. Establish a trust relationship with the development accounts for this role. Update the Lambda function IAM role in the shared account by adding the iam:AssumeRole permissions.
D. Create an IAM role in the development accounts. Add the ec2:DescribeInstances permission to the role. Establish a trust relationship with the shared account for this role. Update the Lambda function IAM role in the shared account by adding the ec2:DescribeInstances permission to the role.

---

**Question 344.** A developer is building a new application that will be deployed on AWS. The developer has initialized a new project for the application using the AWS Cloud Development Kit (AWS CDK) cdk init command. The developer must write unit tests for the infrastructure as code (IaC) templates that the AWS CDK generates. The developer must also run a validation tool across all constructs in the CDK application to ensure that all critical security configurations are activated.
Which combination of actions will meet these requirements with the LEAST development overhead? (Choose two.)

A. Use a unit testing framework to write custom unit tests against the cdk.out file that the AWS CDK generates. Run the unit tests in a continuous integration and continuous delivery (CI/CD) pipeline that is invoked after any commit to the repository.
B. Use the CDK assertions module to integrate unit tests with the application. Run the unit tests in a continuous integration and continuous delivery (CI/CD) pipeline that is invoked after any commit to the repository.
C. Use the CDK runtime context to set key-value pairs that must be present in the cdk.out file that the AWS CDK generates. Fail the stack synthesis if any violations are present.
D. Write a script that searches the application for specific key configuration strings. Configure the script to produce a report if any violations are present.
E. Use the CDK Aspects class to create custom rules to apply to the CDK application. Fail the stack synthesis if any violations are present.

---

**Question 345.** An online sales company is developing a serverless application that runs on AWS. The application uses an AWS Lambda function that calculates order success rates and stores the data in an Amazon DynamoDB table. A developer wants an efficient solution to invoke the Lambda function every 15 minutes.
Which solution will meet this requirement with the LEAST development effort?

A. Create an Amazon EventBridge rule that has a rate expression that will run the rule every 15 minutes. Add the Lambda function as the target of the EventBridge rule.
B. Create an AWS Systems Manager document that has a script that runs the Lambda function on Amazon EC2. Use a Systems Manager Run Command task to run the shell script every 15 minutes.
C. Create an AWS Step Functions state machine. Configure the state machine to invoke the Lambda function execution by using a Wait state. Set the interval to 15 minutes.
D. Provision a small Amazon EC2 instance. Set up a cron job that invokes the Lambda function every 15 minutes.

---

**Question 346.** A company deploys a photo-processing application to an Amazon EC2 instance. The application needs to process each photo within 5 seconds. If processing takes longer than 5 seconds, the company's development team must receive a notification.
How can a developer implement the required time measurement and notification with the LEAST operational overhead?

A. Create an Amazon CloudWatch custom metric. Each time a photo is processed, publish the processing time as a metric value. Create a CloudWatch alarm that is based on a static threshold of 5 seconds. Notify the development team by using an Amazon Simple Notification Service (Amazon SNS) topic.
B. Create an Amazon Simple Queue Service (Amazon SQS) queue. Each time a photo is processed, publish the processing time to the queue. Create an application to consume from the queue and to determine whether any values are greater than 5 seconds. Notify the development team by using an Amazon Simple Notification Service (Amazon SNS) topic.
C. Create an Amazon CloudWatch custom metric. Each time a photo is processed, publish the processing time as a metric value. Create a CloudWatch alarm that enters ALARM state if any values are more than 5 seconds. Notify the development team by sending an Amazon Simple Email Service (Amazon SES) message.
D. Create an Amazon Kinesis data stream. Each time a photo is processed, publish the processing time to the data stream. Create an Amazon CloudWatch alarm that enters ALARM state if any values are more than 5 seconds. Notify the development team by using an Amazon Simple Notification Service (Amazon SNS) topic.

---

**Question 347.** A company is using AWS Elastic Beanstalk to manage web applications that are running on Amazon EC2 instances. A developer needs to make configuration changes. The developer must deploy the changes to new instances only.
Which types of deployment can the developer use to meet this requirement? (Choose two.)

A. All at once
B. Immutable
C. Rolling
D. Blue/green
E. Rolling with additional batch

---

**Question 348.** A developer needs to use Amazon DynamoDB to store customer orders. The developer's company requires all customer data to be encrypted at rest with a key that the company generates.
What should the developer do to meet these requirements?

A. Create the DynamoDB table with encryption set to None. Code the application to use the key to decrypt the data when the application reads from the table. Code the application to use the key to encrypt the data when the application writes to the table.
B. Store the key by using AWS Key Management Service (AWS KMS). Choose an AWS KMS customer managed key during creation of the DynamoDB table. Provide the Amazon Resource Name (ARN) of the AWS KMS key.
C. Store the key by using AWS Key Management Service (AWS KMS). Choose an AWS KMS key with default encryption. Include the kms:Encrypt parameter with the Amazon Resource Name (ARN) of the AWS KMS key when using the application.
D. Store the key by using AWS Key Management Service (AWS KMS). Choose an AWS KMS AWS managed key during creation of the DynamoDB table. Provide the Amazon Resource Name (ARN) of the AWS KMS key.

---

**Question 349.** A developer is creating an AWS Lambda function that will generate and export a file. The function requires 100 MB of temporary storage for temporary files while running. These files will not be needed after the function is complete.
How can the developer MOST efficiently handle the temporary files?

A. Store the files in Amazon Elastic Block Store (Amazon EBS) and delete the files at the end of the Lambda function.
B. Copy the files to Amazon Elastic File System (Amazon EFS) and delete the files at the end of the Lambda function.
C. Store the files in the /tmp directory and delete the files at the end of the Lambda function.
D. Copy the files to an Amazon S3 bucket with a lifecycle policy to delete the files.

---

**Question 350.** A company uses Amazon DynamoDB as a data store for its order management system. The company's frontend application stores orders in a DynamoDB table. The DynamoDB table is configured to send change events to a DynamoDB stream. An AWS Lambda function processes the orders based on data from the DynamoDB stream. An operational review reveals that the order quantity equal to 0 groups the results in 1-day periods.
What should the developer do to implement the dashboard?

A. Grant the Lambda function's execution role permissions to upload logs to Amazon CloudWatch Logs. Implement a CloudWatch Logs Insights query that selects the number of unique customers for orders with order quantity equal to 0 and groups the results in 1-day periods. Add the CloudWatch Logs Insights query to a CloudWatch dashboard.
B. Use Amazon Athena to query AWS CloudTrail API logs for API calls. Implement an Athena query that selects the number of unique customers for orders with order quantity equal to 0 and groups the results in 1-day periods. Add the Athena query to the Amazon CloudWatch dashboard.
C. Configure the Lambda function to send events for the DynamoDB stream of the DynamoDB table to a CloudWatch dashboard. Create a CloudWatch alarm that groups the number of unique customers for orders with order quantity equal to 0 in 1-day periods. Add the CloudWatch alarm to a CloudWatch dashboard.
D. Configure the Lambda function to send events for the DynamoDB stream of the DynamoDB table to Amazon CloudWatch Logs. Create a CloudWatch metric filter that groups the number of unique customers for orders with order quantity equal to 0 in 1-day periods. Add the CloudWatch filter alarm to a CloudWatch dashboard.

---

**Question 351.** A developer needs to troubleshoot an AWS Lambda function in a development environment. The Lambda function is configured in VPC mode and needs to connect to Amazon RDS for SQL Server DB instance. The DB instance is deployed in a private subnet and accepts connections by using port 1433.
When the developer tests the function, the function reports an error when it tries to connect to the database.
Which combination of checks should the developer do to diagnose this issue? (Choose two.)

A. Check that the function's security group has outbound access on port 1433 to the DB instance's security group. Check that the DB instance's security group has inbound access on port 1433 from the function's security group.
B. Check that the function's security group has inbound access on port 1433 from the DB instance's security group. Check that the DB instance's security group has outbound access on port 1433 to the function's security group.
C. Check that the VPC is set up for a NAT gateway. Check that the DB instance has the public access option enabled.
D. Check that the function's execution role permissions include rds:ModifyDBInstance, rds:DescribeDBInstances, and rds:DescribeDBSecurityGroups for the DB instance. Check that the function's execution role permissions include ec2:CreateNetworkInterface, ec2:DescribeNetworkInterfaces, ec2:DeleteNetworkInterface.

---

**Question 352.** A developer needs to launch a new Amazon EC2 instance by using the AWS CLI.
Which AWS CLI command should the developer use to meet this requirement?

A. aws ec2 bundle-instance
B. aws ec2 start-instances
C. aws ec2 confirm-product-instance
D. aws ec2 run-instances

---

**Question 353.** A developer needs to manage AWS infrastructure as code and must be able to deploy multiple identical copies of the infrastructure, stage changes, and revert to previous versions.
Which approach addresses these requirements?

A. Use cost allocation reports and AWS OpsWorks to deploy and manage the infrastructure.
B. Use Amazon CloudWatch metrics and alerts along with resource tagging to deploy and manage the infrastructure.
C. Use AWS Elastic Beanstalk and AWS CodeCommit to deploy and manage the infrastructure.
D. Use AWS CloudFormation and AWS CodeCommit to deploy and manage the infrastructure.

---

**Question 354.** A developer is working on an AWS Lambda function that accesses Amazon DynamoDB. The Lambda function must retrieve an item and update some of its attributes, or create the item if it does not exist. The Lambda function has access to the primary key.
Which IAM permissions should the developer request for the Lambda function to achieve this functionality?

A. dynamodb:DeleteItem, dynamodb:GetItem, dynamodb:PutItem
B. dynamodb:UpdateItem, dynamodb:GetItem, dynamodb:DescribeTable
C. dynamodb:GetRecords, dynamodb:PutItem, dynamodb:UpdateTable
D. dynamodb:UpdateItem, dynamodb:GetItem, dynamodb:PutItem

---

**Question 355.** A developer has built a market application that stores pricing data in Amazon DynamoDB with Amazon ElastiCache in front. The prices of items in the market change frequently. Sellers have begun complaining that, after they update the price of an item, the price does not actually change in the product listing.
What could be causing this issue?

A. The cache is not being invalidated when the price of the item is changed.
B. The price of the item is being retrieved using a write-through ElastiCache cluster.
C. The DynamoDB table was provisioned with insufficient read capacity.
D. The DynamoDB table was provisioned with insufficient write capacity.

**Question 356.** A company requires that all applications running on Amazon EC2 use IAM roles to gain access to AWS services. A developer is modifying an application that currently relies on IAM user access keys stored in environment variables to access Amazon DynamoDB tables using boto, the AWS SDK for Python.

The developer associated a role with the same permissions as the IAM user to the EC2 instance, then deleted the IAM user. When the application was restarted, the AWS AccessDeniedException messages started appearing in the application logs. The developer was able to use their personal account on the server to run DynamoDB API commands using the AWS CLI.

What is the MOST likely cause of the exception?

A. IAM policies might take a few minutes to propagate to resources.
B. Disabled environment variable credentials are still being used by the application.
C. The AWS SDK does not support credentials obtained using an instance role.
D. The instance's security group does not allow access to http://169.254.169.254.

---

**Question 357.** A company has an existing application that has hardcoded database credentials. A developer needs to modify the existing application. The application is deployed in two AWS Regions with an active-passive failover configuration to meet company's disaster recovery strategy. The developer needs a solution to store the credentials outside the code. The solution must comply with the company's disaster recovery strategy.

Which solution will meet these requirements in the MOST secure way?

A. Store the credentials in AWS Secrets Manager in the primary Region. Enable secret replication to the secondary Region. Update the application to use the Amazon Resource Name (ARN) based on the Region.
B. Store the credentials in AWS Systems Manager Parameter Store in the primary Region. Enable parameter replication to the secondary Region. Update the application to use the Amazon Resource Name (ARN) based on the Region.
C. Store credentials in a config file. Upload the config file to an S3 bucket in the primary Region. Enable Cross-Region Replication (CRR) to an S3 bucket in the secondary region. Update the application to access the config file from the S3 bucket based on the Region.
D. Store credentials in a config file. Upload the config file to an Amazon Elastic File System (Amazon EFS) file system. Update the application to use the Amazon EFS file system Regional endpoints to access the config file in the primary and secondary Regions.

---

**Question 358.** A developer is receiving HTTP 400: ThrottlingException errors intermittently when calling the Amazon CloudWatch API. When a call fails, no data is retrieved. What best practice should first be applied to address this issue?

A. Contact AWS Support for a limit increase.
B. Use the AWS CLI to get the metrics.
C. Analyze the applications and remove the API call.
D. Retry the call with exponential backoff.

---

**Question 359.** An application needs to use the IP address of the client in its processing. The application has been moved into AWS and has been placed behind an Application Load Balancer (ALB). However, all the client IP addresses now appear to be the same. The application must maintain the ability to scale horizontally.

Based on this scenario, what is the MOST cost-effective solution to this problem?

A. Remove the application from the ALB. Delete the ALB and change Amazon Route 53 to direct traffic to the instance running the application.
B. Remove the application from the ALCreate a Classic Load Balancer in its place. Direct traffic to the application using the HTTP protocol.
C. Alter the application code to inspect the X-Forwarded-For header. Ensure that the code can work properly if a list of IP addresses is passed in the header.
D. Alter the application code to inspect a custom header. Alter the client code to pass the IP address in the custom header.

---

**Question 360.** A developer is designing a serverless application that customers use to select seats for a concert venue. Customers send the ticket requests to an Amazon API Gateway API with an AWS Lambda function that acknowledges the order and generates an order ID. The application includes two additional Lambda functions: one for inventory management and one for payment processing. The design requires these two Lambda functions run in parallel and write the order to an Amazon Dynamo DB table. The application must provide seats to customers according to the following requirements: If a seat is accidently sold to multiple customers, the application must refund the extra customers. In these cases, the application must process the payment for only the first order. However, if the first order is rejected during payment processing, the application must process the payment for the second order. Which solution will meet these requirements?

A. Send the order ID to an Amazon Simple Notification Service (Amazon SNS) FIFO topic that fans out to one Amazon Simple Queue Service (Amazon SQS) FIFO queue for inventory management and another SQS FIFO queue for payment processing.
B. Change the Lambda function that generates the order ID to initiate the Lambda function for inventory management. Then initiate the Lambda function for payment processing.
C. Send the order ID to an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe the Lambda functions for inventory management and payment processing to the topic.
D. Deliver the order ID to an Amazon Simple Queue Service (Amazon SQS) queue. Configure the Lambda functions for inventory management and payment processing to poll the queue.

---

**Question 361.** An application uses AWS X-Ray to generate a large amount of trace data on an hourly basis. A developer wants to use filter expressions to limit the returned results through user-specified custom attributes.

How should the developer use filter expressions to filter the results in X-Ray?

A. Add custom attributes as annotations in the segment document.
B. Add custom attributes as metadata in the segment document.
C. Add custom attributes as new segment fields in the segment document.
D. Create new sampling rules that are based on custom attributes.

---

**Question 362.** A startup s photo-sharing site is deployed in a VPC. An ELB distributes web traffic across two subnets. ELB session stickiness is configured to use the AWS-generated session cookie, with a session TTL of 5 minutes. The webserver Auto Scaling Group is configured as: min-size=4, max-size=4. The startups preparing for a public launch, by running load-testing software installed on a single EC2 instance running in us-west-2.

After 60 minutes of load-testing, the webserver logs show:

Which recommendations can help ensure load-testing HTTP requests are evenly distributed across the four webservers? (Choose two.)

A. Launch and run the load-tester EC2 instance from us-east-1 instead.
B. Re-configure the load-testing software to re-resolve DNS for each web request.
C. Use a 3rd-party load-testing service which offers globally-distributed test clients.
D. Configure ELB and Auto Scaling to distribute across us-west-2a and us-west-2c.
E. Configure ELB session stickiness to use the app-specific session cookie.

---

**Question 363.** An application is real-time processing millions of events that are received through an API. What service could be used to allow multiple consumers to process the data concurrently and MOST cost-effectively?

A. Amazon SNS with fanout to an SQS queue for each application
B. Amazon SNS with fanout to an SQS FIFO (first-in, first-out) queue for each application
C. Amazon Kinesis Firehose
D. Amazon Kinesis Data Streams

---

**Question 364.** A company uses AWS CloudFormation to deploy an application that uses an Amazon API Gateway REST API with AWS Lambda function integration. The application uses Amazon DynamoDB for data persistence. The application has three stages: development, testing, and production. Each stage uses its own DynamoDB table. The changes were successful in the development and testing stages. A developer needs to route 20% of the traffic to the new production API with the next production release.

The developer creates a method for an API resource. Which approach will meet these requirements?

A. Update 20% of the planned changes to the production stage. Deploy the new production stage. Monitor the results. Repeat this process five times to test all planned changes.
B. Update the Amazon Route 53 DNS record entry for the production stage API to use a weighted routing policy. Set the weight of the first policy to 20. Change the alias of the second policy to reference the testing stage API. Deploy the API to the production stage.
C. Deploy an Application Load Balancer (ALB) in front of the REST API. Change the production API Amazon Route 53 record to point traffic to the ALB. Register the production and testing targets as targets of the ALB with weights of 80% and 20%, respectively.
D. Configure canary settings for the production stage API. Change the percentage of traffic directed to canary deployment to 20%. Make the planned updates to the production stage. Deploy the changes.

---

**Question 365.** A developer has created a data collection application that uses Amazon API Gateway, AWS Lambda, and Amazon S3. The application's users periodically upload data and wait for the validation status to be reflected on a processing dashboard. The process is complex and time-consuming for large files.

Some users are uploading dozens of large files and have to wait and refresh the processing dashboard to see if the files have been validated. The developer must refactor the application to immediately update the validation result on the user's dashboard without reloading the full dashboard. What is the MOST operationally efficient solution that meets these requirements?

A. Integrate the client with an API Gateway WebSocket API. Save the user-uploaded files with the WebSocket connection ID to the collection status to the connection ID when the processing is complete to initiate an update of the user interface.
B. Launch an Amazon EC2 micro instance, and set up a WebSocket server. Send the user-uploaded file and user detail to the EC2 instance for processing. Use the WebSocket server to send updates to the user interface when the file is processed.
C. Save the user's email address along with the user-uploaded file. When the validation process is complete, send an email notification through Amazon Simple Notification Service (Amazon SNS) to the user interface.
D. Save the user-uploaded file and user detail to Amazon DynamoDB. Use Amazon DynamoDB Streams with Amazon Simple Notification Service (Amazon SNS) push notifications to notify the browser to update the user interface.

---

**Question 366.** A company's developer is creating an application that uses Amazon API Gateway. The company wants to ensure that only users in the Sales department can use the application. The users authenticate to the application by using federated credentials from a third-party identity provider (IdP) through Amazon Cognito. The developer has set up an attribute mapping to map an attribute that is named Department and to pass the attribute to a custom AWS Lambda authorizer.

To test the access limitation, the developer sets their department in the IdP and attempts to log in. Again, the developer is denied access. The developer checks the logs and discovers that the developer's access token does not have a department value of Engineering.

Which of the following is a possible reason that the developer's department is still being reported as Engineering instead of Sales?

A. Authorization caching is enabled in the custom Lambda authorizer.
B. Authorization caching is enabled on the Amazon Cognito user pool.
C. The Lambda role for the custom Lambda authorizer does not have a Department tag.
D. The IAM role for the Amazon Cognito user pool does not have a Department tag.

---

**Question 367.** A company has migrated an application to Amazon EC2 instances. Automatic scaling is working well for the application user interface. However, to deliver shipping requests to the company's warehouse staff is encountering issues. Duplicate shipping requests are arriving, and some requests are lost or arriving out of order.

The company must avoid duplicate shipping requests and must process the requests in the order that the requests arrive. Requests are never more than 250 KB in size and take 5-10 minutes to process. If processing of the requests fails, the application must improve the reliability of the delivery and processing of the requests.

What should the developer do to meet these requirements?

A. Create an Amazon Kinesis Data Firehose delivery stream to process the requests. Create an Amazon Kinesis data application to write the requests to the Kinesis to the stream.
B. Create an AWS Lambda function to process the requests. Create an Amazon Simple Notification Service (Amazon SNS) standard queue. Set the SNS queue as an event source for the Lambda function. Modify the application to write the requests to the SNS topic.
C. Create an AWS Lambda function to process the requests. Create an Amazon Simple Queue Service (Amazon SQS) standard queue. Set the SQS queue as an event source for the Lambda function. Modify the application to write the requests to the SQS queue.
D. Create an AWS Lambda function to process the requests. Create an Amazon Simple Queue Service (Amazon SQS) FIFO queue. Set the SQS queue as an event source for the Lambda function. Modify the application to write the requests to the SQS queue.

---

**Question 368.** A developer is creating a machine learning (ML) pipeline in AWS Step Functions that contains AWS Lambda functions. The developer has configured an Amazon Simple Queue Service (Amazon SQS) queue to deliver model parameters to the ML pipeline to train ML models. The developer uploads the trained models are uploaded to an Amazon S3 bucket.

The developer needs a solution that can locally test the ML pipeline without making service integration calls to AWS Lambda functions, Amazon SQS and Amazon S3.

Which solution will meet these requirements?

A. Use the Amazon CodeGuru Profiler to analyze the Lambda functions used in the AWS Step Functions pipeline.
B. Use the AWS Step Functions Local Docker Image to run and locally test the Lambda functions.
C. Use the AWS Step Functions Serverless Application Model (AWS SAM) CLI to run and locally test the Lambda functions.
D. Use AWS Step Functions Local with mocked service integrations.

---

**Question 369.** A company runs a batch processing application by using AWS Lambda functions and Amazon API Gateway APIs with deployment stages for development, user acceptance testing, and production. A development team needs to configure the APIs in the deployment stages to connect to third-party service endpoints.

Which solution will meet this requirement?

A. Store the third-party service endpoints in Lambda layers that correspond to the stage.
B. Store the third-party service endpoints in API Gateway stage variables that correspond to the stage.
C. Encode the third-party service endpoints as query parameters in the API Gateway request URL.
D. Store the third-party service endpoint for each environment in AWS AppConfig.

---

**Question 370.** A developer is building a serverless application that runs on AWS. The developer wants to create an accelerated development workflow that deploys incremental changes to AWS for testing. The developer wants to deploy the incremental changes and does not want to fully deploy the entire application to AWS for every code commit.

What should the developer do to meet these requirements?

A. Use the AWS Serverless Application Model (AWS SAM) to build the application. Use the sam sync command to deploy the incremental changes.
B. Use the AWS Serverless Application Model (AWS SAM) to build the application. Use the sam init command to deploy the incremental changes.
C. Use the AWS Cloud Development Kit (AWS CDK) to build the application. Use the cdk synth command to deploy the incremental changes.
D. Use the AWS Cloud Development Kit (AWS CDK) to build the application. Use the cdk bootstrap command to deploy the incremental changes.

---

**Question 371.** A developer is building an application that will use an Amazon API Gateway API with an AWS Lambda backend. The team that will develop the frontend requires immediate access to the API endpoints to set up the backend application for integration, the developer needs to set up endpoints to return predefined HTTP status codes and JSON responses for the frontend team. The developer creates a method for an API resource.

Which solution will meet these requirements?

A. Set the integration type to AWS_PROXY. Configure Lambda functions to return hardcoded JSON data.
B. Set the integration type to MOCK. Configure the method's integration request and integration response to associate a JSON responses with specific HTTP status codes.
C. Set the integration type to HTTP_PROXY. Configure API Gateway to pass all requests to an external placeholder API from which the team will build.
D. Set the integration type to MOCK. Use a method request to define HTTP status codes. Use an integration request to define JSON responses.

---

**Question 372.** A developer is migrating an application to Amazon Elastic Kubernetes Service (Amazon EKS). The developer migrates the application to Amazon Elastic Container Registry (Amazon ECR) with an EKS cluster. As part of the application migration to a new backend, the developer creates a new AWS account. The developer makes configuration changes to the application to point the application to the new AWS account and to use new backend resources. The developer successfully tests the changes within the development environment by deploying the pipeline.

The Docker image in the EKS deployment are successful, but the application is still connecting to the old backend. The developer finds that the application's configuration is still referencing the original EKS cluster and not referencing the new backend resources.

Which reason can explain why the application is not connecting to the new resources?

A. The developer did not successfully create the new AWS account.
B. The developer added a new tag to the Docker image.
C. The developer did not update the Docker image tag to a new version.
D. The developer pushed the changes to a new Docker image tag.

---

**Question 373.** A developer is creating an application that reads and writes to multiple Amazon S3 buckets. The application will be deployed to an Amazon EC2 instance. The developer wants to make secure API requests from the EC2 instances without the need to manage the security credentials for the application. The developer needs to apply the principle of least privilege.

Which solution will meet these requirements?

A. Create an IAM user. Create access keys and secret keys for the user. Associate the user with an IAM policy that allows s3:* permissions.
B. Associate the EC2 instance with an IAM role that has an IAM policy that allows s3:ListBucket and s3:*Object permissions for specific S3 buckets.
C. Associate the EC2 instance with an IAM role that has an IAM policy that allows AmazonS3FullAccess AWS-managed policy.
D. Store the credentials in an encrypted key file in an Amazon S3 Bucket. Configure the EC2 instance launch template to download the credentials from Amazon S3 as the instance launches. Create an AWS Lambda function to periodically update the secrets and database.

---

**Question 374.** A developer is writing an application that will retrieve sensitive data from a third-party system. The application will format the data into a PDF file. The PDF file could be more than 1 MB. The application will encrypt the data to disk using AWS Key Management Service (AWS KMS). The application will decrypt the file when a user requests to download it. The retrieval and formatting portions of the application are complete.

The developer needs to use the GenerateDataKey API to encrypt the PDF file so that the PDF file can be decrypted later. The developer needs to use an AWS KMS symmetric customer managed key for encryption.

Which solutions will meet these requirements?

A. Write the encrypted key from the GenerateDataKey API to disk for later use. Use the plaintext key from the GenerateDataKey API and a symmetric encryption algorithm to encrypt the file.
B. Write the plaintext key from the GenerateDataKey API to disk for later use. Use the encrypted key from the GenerateDataKey API to encrypt the file using the KMS Encrypt API.
C. Write the encrypted key from the GenerateDataKey API to disk for later use. Use the plaintext key from the GenerateDataKey API to encrypt the file using the KMS Encrypt API.
D. Write the plaintext key from the GenerateDataKey API to disk for later use. Use the encrypted key from the GenerateDataKey API to encrypt the file using the KMS Encrypt API.

---

**Question 375.** A company runs an application on Amazon EC2 instances. The EC2 instances open connections to an Amazon RDS for SQL Server database. A developer needs to access the credentials and wants to automatically rotate the credentials. The developer does not want to store the credentials for the database in the code.

Which solution will meet these requirements in the MOST secure way?

A. Create an IAM role that has permissions to access the database. Attach the IAM role to the EC2 instances.
B. Store the credentials as secrets in AWS Secrets Manager. Create an AWS Lambda function to update the secrets and the database. Configure an Amazon CloudWatch Events rule to invoke an AWS Lambda function to periodically update the secrets and database.
C. Store the credentials in an encrypted key file in an Amazon S3 Bucket. Configure the EC2 instance launch template to download the credentials from Amazon S3 as the instance launches. Create an AWS Lambda function to periodically update the secrets and database.
D. Store the credentials in an Amazon DynamoDB table. Configure an Amazon CloudWatch Events rule to invoke an AWS Lambda function to periodically update the secrets and database.

---

**Question 376.** A company wants to test its web application more frequently. The company deploys the application by using a separate AWS CloudFormation stack for each environment. The company deploys the same CloudFormation template to each stack as the application progresses through the development lifecycle.

A developer needs to build in notifications for the quality assurance (QA) team. The developer wants the notifications to occur for new deployments in the final preproduction environment.

Which solution will meet these requirements?

A. Create an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe the QA team to the Amazon SNS topic. Update the CloudFormation stack options to point to the SNS in the pre-production environment.
B. Create an AWS Lambda function that notifies the QA team. Create an Amazon EventBridge rule to invoke the Lambda function on the default event bus. Filter the events on the CloudFormation service and on the CloudFormation Amazon Resource Name (ARN).
C. Create an Amazon CloudWatch alarm that monitors the metrics from CloudFormation. Filter the metrics on the stack name and the stack status. Configure the CloudWatch alarm to notify the QA team.
D. Create an AWS Lambda function to notify the QA team. Configure the event source mapping to receive events from CloudFormation. Specify the filtering values to limit invocations to the desired CloudFormation stack.

---

**Question 377.** A developer manages three AWS accounts. Each account contains an Amazon RDS DB instance in a private subnet. The developer needs to define users in each database in a consistent way. The developer must ensure that the same users are created and updated later in all three accounts.

Which solution will meet these requirements with the MOST operational efficiency?

A. Create an AWS CloudFormation template. Declare the users in the template. Attach the users to the database. Deploy the template in each account.
B. Create an AWS CloudFormation template that contains a custom resource to create the users in the database. Deploy the template in each account.
C. Write a script that creates the users. Deploy an Amazon EC2 instance in each account to run the script on the databases. Run the script in each account.
D. Implement an AWS Lambda function that creates the users in the database. Provide the function with the details of all three accounts.

---

**Question 378.** A company is building a new application that runs on AWS and uses Amazon API Gateway to expose APIs. Teams of developers are working on separate components of the application in parallel. The application backend can continue the development work before the API backend development is complete.

Which solution will meet these requirements?

A. Create API Gateway resources and set the integration type to MOCK. Configure the method integration request and integration response to associate a response with an HTTP status code. Deploy the API to AWS. Deploy the API.
B. Create an AWS Lambda function that returns mocked responses and various HTTP status codes. Create API Gateway resources and set the integration type to AWS. Deploy the API to AWS. Deploy the API.
C. Create an EC2 application that returns mocked responses. Create API Gateway resources and set the integration type to HTTP_PROXY. Deploy the API to AWS. Create an API Gateway stage and deploy the API.
D. Create API Gateway resources and set the integration type to HTTP_PROXY. Add mapping templates and configure the event source mapping to the Lambda layer with the API deployment.

---

**Question 379.** An application that runs on AWS receives messages from an Amazon Simple Queue Service (Amazon SQS) queue and processes the messages in batches. The application sends the data to another SQS queue to be consumed by another legacy application. The legacy system can take up to 5 minutes to process some transaction data.

A developer wants to ensure that there are no out-of-order updates in the legacy system. The developer cannot alter the behavior of the legacy application.

Which solution will meet these requirements?

A. Use an SQS FIFO queue. Configure the visibility timeout value.
B. Use an SQS standard queue with a SendMessageBatchRequestEntry data type. Configure the DelaySeconds values.
C. Use an SQS standard queue with a SendMessageBatchRequestEntry data type. Configure the visibility timeout value.
D. Use an SQS FIFO queue. Configure the DelaySeconds value.

---

**Question 380.** A company is building a compute-intensive application that will run on a fleet of Amazon EC2 instances. The application uses attached Amazon Elastic Block Store (Amazon EBS) volumes for storing data. The Amazon EBS volumes will be created at initial deployment. The application will process sensitive information. All of the data must be encrypted. The solution should not impact the application's performance.

Which solution will meet these requirements?

A. Configure the fleet of EC2 instances to use encrypted EBS volumes to store data.
B. Configure the application to write all data to an encrypted Amazon S3 bucket.
C. Configure a custom encryption algorithm for the application that will encrypt and decrypt all data.
D. Configure an Amazon Machine Image (AMI) that has an encrypted root volume and store the data to ephemeral disks.

---

**Question 381.** A developer is updating the production version of an AWS Lambda function to fix a defect. The developer has tested the updated code in a test environment. The developer wants to slowly roll out the changes to a small subset of production users before rolling out the changes to all users. Only 10% of the users should be initially exposed to the new code in production.

Which solution will meet these requirements?

A. Update the Lambda code and create a new version of the Lambda function. Create a Lambda alias for the production version, and send 90% of the traffic to the production version, and send 10% of the traffic to the new version.
B. Create a new Lambda function for the production stage. Create a Lambda alias for the production Lambda function. Send 90% of the traffic to the production Lambda function, and send 10% of the traffic to the test Lambda function.
C. Update the Lambda code and create a new version of the Lambda function. Create a Lambda alias for the production version. Configure the traffic weights in the Lambda function versions. Send 90% of the traffic to the production Lambda function, and send 10% of the traffic to the new version.
D. Update the Lambda code and create a new version of the Lambda function. Create a Lambda alias for the production version. Configure the traffic weights in the Lambda function versions. Send 90% of the traffic to the production version, and send 10% of the traffic to the new version.

---

**Question 382.** A developer is creating an AWS Lambda function that consumes messages from an Amazon Simple Queue Service (Amazon SQS) standard queue. The developer notices that the Lambda function processes some messages multiple times.

How should developer resolve this issue MOST cost-effectively?

A. Change the Amazon SQS standard queue to an Amazon SQS FIFO queue by using the Amazon SQS message deduplication ID.
B. Set up a dead-letter queue.
C. Set the maximum concurrency limit of the AWS Lambda function to 1.
D. Change the message processing to use Amazon Kinesis Data Streams instead of Amazon SQS.

---

**Question 383.** A developer is optimizing an AWS Lambda function and wants to test the changes in a small percentage of all traffic. The Lambda function serves requests to a RE ST API in Amazon API Gateway. The developer needs to deploy their changes and perform a test in production without changing the API Gateway URL.

Which solution will meet these requirements?

A. Define a function version for the currently deployed production Lambda function. Update the API Gateway stage, define a canary release, and set the percentage of traffic to direct to the canary. Update the API Gateway endpoint to use the $LATEST version of the Lambda function. Deploy the API to the production stage.
B. Define a function version for the currently deployed production Lambda function. Create a new Lambda alias for the production stage. Upload the new Lambda function code and publish the optimized Lambda function code. Update the API Gateway endpoint to use the $LATEST version of the Lambda function. Deploy the API to the production stage.
C. Define a function version for the currently deployed production Lambda function. Create a new Lambda alias for the production stage. Upload the new Lambda function code and publish the optimized Lambda function code. Update the API Gateway stage, define a canary release, and set the percentage of traffic to direct to the canary release. Update the API Gateway endpoint to use the $LATEST version of the Lambda function. Deploy to the API Gateway stage.
D. Define a function version for the currently deployed production Lambda function. Update the API Gateway stage, define a canary release, and set the percentage of traffic to direct to the canary. Update the API Gateway endpoint to reference the Lambda function. Deploy the API to the production API Gateway stage.

---

**Question 384.** A company notices that credentials that the company uses to connect to an external software as a service (SaaS) vendor are stored in a configuration file as plaintext. The developer needs to secure the API credentials and enforce automatic credentials rotation on a quarterly basis.

Which solution will meet these requirements MOST securely?

A. Use AWS Key Management Service (AWS KMS) to encrypt the configuration file. Decrypt the configuration file when users make API calls to the SaaS vendor. Enable rotation.
B. Retrieve temporary credentials from AWS Security Token Service (AWS STS) every 15 minutes. Use the temporary credentials when users make API calls to the SaaS vendor.
C. Store the credentials in AWS Secrets Manager and enable rotation. Configure the API to have Secrets Manager access.
D. Store the credentials in AWS Systems Manager Parameter Store and enable rotation. Retrieve the credentials when users make API calls to the SaaS vendor.

---

**Question 385.** A company has an application that is hosted on Amazon EC2 instances. The application stores objects in an Amazon S3 bucket and allows users to download objects from the S3 bucket. After a developer turns on S3 Block Public Access for the S3 bucket, users report errors when they attempt to download objects. The developer needs to implement a solution so that only users who are signed in to the application can access objects in the S3 bucket.

Which combination of steps will meet these requirements in the MOST secure way? (Choose two.)

A. Create an EC2 instance profile and role with an appropriate policy. Associate the role with the EC2 instances.
B. Create an IAM user with an appropriate policy. Store the access key ID and secret access key on the EC2 instances.
C. Modify the application to use the S3 GeneratePresignedUrl API call.
D. Modify the application to use the S3 GetObject API call and to return the object handle to the user.
E. Modify the application to delegate requests to the S3 bucket.

**Question 386.** An Amazon Simple Queue Service (Amazon SQS) queue serves as an event source for an AWS Lambda function. In the SQS queue, each item corresponds to a video file that the Lambda function must convert to a smaller resolution. The Lambda function is timing out on longer video files, but the Lambda function's timeout is already configured to its maximum value. What should a developer do to avoid the timeouts without additional code changes?

A. Increase the memory configuration of the Lambda function.
B. Increase the visibility timeout on the SQS queue.
C. Increase the instance size of the host that runs the Lambda function.
D. Use multi-threading for the conversion.

---

**Question 387.** A company is building an application on AWS. The application's backend includes an Amazon API Gateway REST API. The company's frontend application developers cannot continue work until the backend API is ready for integration. The company needs a solution that will allow the frontend application developers to continue their work. Which solution will meet these requirements in the MOST operationally efficient way?

A. Configure mock integrations for API Gateway API methods.
B. Integrate a Lambda function with API Gateway and return a mocked response.
C. Add new API endpoints to the API Gateway stage and returns a mocked response.
D. Configure a proxy resource for API Gateway API methods.

---

**Question 388.** A company is preparing to migrate an application to the company's first AWS environment. Before this migration, 389 # A developer is creating a proof-of-concept application to validate a model for building and deploying containerized-based applications on AWS. Which combination of steps should the developer take to deploy the containerized proof-of-concept application with the LEAST operational effort? (Choose two.)

A. Package the application into a .zip file by using a command line tool. Upload the package to Amazon S3.
B. Package the application into a container image by using the Docker CLI. Upload the image to Amazon Elastic Container Registry (Amazon ECR).
C. Deploy the application to an Amazon EC2 instance by using AWS CodeDeploy.
D. Deploy the application to Amazon Elastic Kubernetes Service (Amazon EKS) on AWS Fargate.
E. Deploy the application to Amazon Elastic Container Service (Amazon ECS) on AWS Fargate.

---

**Question 389.** A company is using AWS CodePipeline to deliver one of its applications. The delivery pipeline is triggered by a change to the main branch of an AWS CodeCommit repository and uses AWS CodeBuild to implement the test and build stages of the process and AWS CodeDeploy to deploy the application. The pipeline has been operating successfully for several months and there have been no modifications. Following a recent change to the application's source code, AWS CodeDeploy has not deployed the updated application as expected. What are the possible causes? (Choose two.)

A. The change was not made in the main branch of the AWS CodeCommit repository.
B. One of the earlier stages in the pipeline failed and the pipeline has terminated.
C. One of the Amazon EC2 instances in the company's AWS CodePipeline cluster is inactive.
D. The AWS CodePipeline is incorrectly configured and is not invoking AWS CodeDeploy.
E. AWS CodePipeline does not have permissions to access AWS CodeCommit.

---

**Question 390.** A developer supports an application that accesses data in an Amazon DynamoDB table. One of the item attributes is expirationDate in the timestamp format. The application uses this attribute to find items, archive them, and remove them from the table based on the timestamp value. The application will be decommissioned soon, and the developer must find another way to implement this functionality. The developer needs a solution that will require the least amount of code to write. Which solution will meet these requirements?

A. Enable TTL on the expirationDate attribute in the table. Create a DynamoDB stream. Create an AWS Lambda function to process the stream. Use the DeleteItem API operation to delete the items based on the expirationDate attribute. Use the GetRecords API operation to get the items from the stream and process them.
B. Create two AWS Lambda functions: one to delete the items and one to process the items. Create a DynamoDB stream. Use the DeleteItem API operation to delete the items based on the expirationDate attribute. Use the GetRecords API operation to get the items from the stream and process them.
C. Create two AWS Lambda functions: one to delete the items and one to process the items. Create an Amazon EventBridge scheduled rule to invoke the Lambda functions. Use the DeleteItem API operation to delete the items based on the expirationDate attribute. Use the GetRecords API operation to get the items from the stream and process them.
D. Enable TTL on the expirationDate attribute in the table. Specify an Amazon Simple Queue Service (Amazon SQS) dead-letter queue as the target to delete the items. Create an AWS Lambda function to process the items.

---

**Question 391.** A developer needs to implement a custom machine learning (ML) library in an application. The size of the library is 15 GB. The size of the library is increasing. The application uses AWS Lambda functions. All the Lambda functions must have access to the library. Which solution will meet these requirements?

A. Save the library in Lambda layers. Attach the layers to all Lambda functions.
B. Save the library in Amazon S3. Download the library from Amazon S3 inside the Lambda function.
C. Save the library as a Lambda container image. Redeploy the Lambda functions with the new image.
D. Save the library in an Amazon Elastic File System (Amazon EFS) file system. Mount the EFS file system in all the Lambda functions.

---

**Question 392.** A developer is designing a serverless application for a game in which users register and log in through a web browser. The application makes requests on behalf of users to a set of AWS Lambda functions that run through an Amazon API Gateway HTTP API. The developer needs to implement a solution to register and log in users on the application's sign-in page. The solution must minimize operational overhead and must minimize ongoing management of user identities. Which solution will meet these requirements?

A. Create Amazon Cognito user pools for external social identity providers. Configure IAM roles for the identity pools.
B. Program the sign-in page to create users' IAM groups with the IAM roles attached to the groups.
C. Create an Amazon RDS for SQL Server DB instance to store the users and manage the permissions to the backend resources on AWS.
D. Configure the sign-in page to register and store the users and their passwords in an Amazon DynamoDB table with an attached IAM policy.

---

**Question 393.** A company has a web application that is hosted on Amazon EC2 instances. The EC2 instances are configured to stream logs to Amazon CloudWatch Logs. The company needs to receive an Amazon Simple Notification Service (Amazon SNS) notification when the number of application error messages exceeds a defined threshold within a 5-minute period. Which solution will meet these requirements?

A. Rewrite the application code to stream application logs to Amazon SNS. Configure an SNS topic to send a notification when the number of errors exceeds the defined threshold within a 5-minute period.
B. Configure a subscription filter on the CloudWatch Logs log group. Create a filter to send an SNS notification when the number of errors exceeds the defined threshold within a 5-minute period.
C. Install and configure the Amazon Inspector agent on the EC2 instances to monitor for errors. Configure Amazon Inspector to send an SNS notification when the number of errors exceeds the defined threshold within a 5-minute period.
D. Create a CloudWatch metric filter to match the application error pattern in the log data. Set up a CloudWatch alarm to send an SNS notification when the number of errors exceeds the defined threshold within a 5-minute period.

---

**Question 394.** A photo sharing application uses Amazon S3 to store image files. All user images are manually audited for inappropriate content by a third-party company. The audits are completed 1-24 hours after user upload and the results are uploaded to an Amazon DynamoDB table, which uses the S3 object key as a primary key. The database items can be queried by using a REST API created by the third-party company. An application developer needs to implement an automated process to tag all S3 objects with the results of the content audit. What should the developer do to meet these requirements in the MOST operationally efficient way?

A. Create an SQS queue with a visibility timeout of 24 hours. Configure an AWS Step Functions Wait state and set the value to 24 hours. Create an AWS Step Functions Wait Task to load all untagged S3 objects from the queue. Add the AWS Step Functions task for each item from the REST API. Tag each S3 object accordingly.
B. Create an AWS Lambda function to load all untagged S3 objects. Create and configure an Amazon EventBridge rule to run an AWS Step Functions workflow. Set the value of the Wait state to be the event that initiates the workflow. Tag each S3 object accordingly.
C. Create an Amazon EventBridge rule to run an AWS Step Functions workflow. Set the Wait state and set the value to the time it takes to receive an audit result. Create a Lambda function to call the REST API for each item from the DynamoDB table. Tag each S3 object accordingly.
D. Launch an Amazon EC2 instance. Deploy a script to the EC2 instance to use the external API to tag the S3 objects accordingly. Configure a crontab file to run the script at regular intervals.

---

**Question 395.** A company has built an AWS Lambda function to convert large image files into output files that can be used in a third-party viewer application. The company recently added a new module to the function to improve the output of the generated files. However, the new module has increased the bundle size and has increased the time that is needed to deploy changes to the function code. How can a developer increase the speed of the Lambda function deployment?

A. Use AWS CodeDeploy to deploy the function code.
B. Use Lambda layers to package and load dependencies.
C. Increase the memory size of the function.
D. Use Amazon S3 to host the function dependencies.

---

**Question 396.** A developer creates a static website for their department. The developer deploys the static assets for the website to an Amazon S3 bucket and serves the assets with Amazon CloudFront. The developer uses origin access control (OAC) on the CloudFront distribution to access the S3 bucket. The developer notices users can access the root URL and specific pages but cannot access directories without specifying a file name. For example, /products/index.html works, but /products/ returns an error. The developer needs to enable users to access directories without specifying a file name without exposing the S3 bucket publicly. Which solution will meet these requirements?

A. Update the CloudFront distribution's settings to index.html as the default root object.
B. Update the Amazon S3 bucket settings and enable static website hosting. Specify index.html as the Index document. Update the CloudFront distribution's origin to use the S3 website endpoint.
C. Create a CloudFront function that examines the request URL and appends index.html when directories are being accessed. Add the function as a viewer request CloudFront function to the CloudFront distribution's behavior.
D. Create a custom error response on the CloudFront distribution with the HTTP error code set to the HTTP 404 Not Found response code and the response page path to /index.html. Set the HTTP response code to the HTTP 200 OK response code.

---

**Question 397.** A developer is testing a RESTful application that is deployed by using Amazon API Gateway and AWS Lambda. When the developer tests the user login by using credentials that are not valid, the developer receives an HTTP 405: METHOD_NOT_ALLOWED error. The developer has verified that the test is sending the correct request for the resource. Which HTTP error should the application return in response to the request?

A. HTTP 401
B. HTTP 404
C. HTTP 503
D. HTTP 505

---

**Question 398.** A developer must use multi-factor authentication (MFA) to access data in an Amazon S3 bucket that is in another AWS account. Which AWS Security Token Service (AWS STS) API operation should the developer use with the MFA information to meet this requirement?

A. AssumeRoleWithWebIdentity
B. GetFederationToken
C. AssumeRoleWithSAML
D. AssumeRole

---

**Question 399.** A developer designed an application on an Amazon EC2 instance. The application makes API requests to objects in an Amazon S3 bucket. Which combination of steps will ensure that the application makes the API requests in the MOST secure manner? (Choose two.)

A. Create an IAM user that has permissions to the S3 bucket. Add the user to an IAM group.
B. Create an IAM role that has permissions to the S3 bucket.
C. Add the IAM role to an instance profile. Attach the instance profile to the EC2 instance.
D. Create an IAM role that has permissions to the S3 bucket. Assign the role to an IAM group.
E. Store the credentials of the IAM user in the environment variables on the EC2 instance.

---

**Question 400.** An AWS Lambda function requires read access to an Amazon S3 bucket and requires read/write access to an Amazon DynamoDB table. The correct IAM policy already exists. What is the MOST secure way to grant the Lambda function access to the S3 bucket and the DynamoDB table?

A. Attach the existing IAM policy to the Lambda function.
B. Create an IAM role for the Lambda function. Attach the existing IAM policy to the role. Attach the role to the Lambda function.
C. Create an IAM user with programmatic access. Attach the existing IAM policy to the user. Add the user access key ID and secret access key as environment variables in the Lambda function.
D. Add the AWS account root user access key ID and secret access key as encrypted environment variables in the Lambda function.

---

**Question 401.** A developer is using AWS Step Functions to automate a workflow. The workflow defines each step as an AWS Lambda function. The developer notices that runs of the Step Functions state machine fail in the GetResource task with either an IllegalArgumentException error or a TooManyRequestsException error. The developer wants the state machine to retry the GetResource task with either an IllegalArgumentException error or a TooManyRequestsException error. The state machine needs to retry the GetResource task one additional time after 10 seconds and the maximum attempts is 1. If the second attempt fails, the developer wants the state machine to stop with a TooManyRequestsException error. How can the developer implement the Lambda retry functionality without adding unnecessary complexity?

A. Add a Delay task after the GetResource task. Add a catcher to the GetResource task with an error type of TooManyRequestsException. Configure the next step to be the Delay task. Configure the Delay task to wait for an interval of 10 seconds, and a maximum attempts of 1. Configure the next step to be the GetResource task.
B. Add a catcher to the GetResource task with an error type of TooManyRequestsException. Configure the next step to be the retrier with an error type of TooManyRequestsException, an interval of 10 seconds, and a maximum attempts of 1. Configure the next step to be the GetResource task.
C. Add a retrier to the GetResource task. Rename the catcher with an error type of TooManyRequestsException, an interval of 10 seconds, and a maximum attempts of 1. Configure the next step to be the GetResource task.
D. Duplicate the GetResource task. Rename the new GetResource task to TryAgain. Add a catcher to the original GetResource task with an error type of TooManyRequestsException. Configure the next step to be the TryAgain task.

---

**Question 402.** A developer is creating a serverless application that uses an AWS Lambda function. The developer will use AWS CloudFormation to deploy the application. The application will write logs to Amazon CloudWatch Logs. The developer has created a log group in a CloudFormation template for the application to use. The developer needs to modify the CloudFormation template to make the name of the log group available to the application at runtime. Which solution will meet this requirement?

A. Use the AWS::Include transform in CloudFormation to provide the log group's name to the application.
B. Pass the log group's name to the application in the user data section of the CloudFormation template.
C. Use the CloudFormation template's Mappings section to specify the log group's name for the application.
D. Pass the log group's Amazon Resource Name (ARN) as an environment variable to the Lambda function.

---

**Question 403.** A developer is creating an Amazon DynamoDB table by using the AWS CLI. The DynamoDB table must use server-side encryption with an AWS owned encryption key. How should the developer create the DynamoDB table to meet these requirements?

A. Create an AWS Key Management Service (AWS KMS) customer managed key. Provide the key's Amazon Resource Name (ARN) in the KMSMasterKeyId parameter during creation of the DynamoDB table.
B. Create an AWS Key Management Service (AWS KMS) AWS managed key. Provide the key's Amazon Resource Name (ARN) in the KMSMasterKeyId parameter during creation of the DynamoDB table.
C. Create an AWS owned key. Provide the key's Amazon Resource Name (ARN) in the KMSMasterKeyId parameter during creation of the DynamoDB table.
D. Create the DynamoDB table with the default encryption options.

---

**Question 404.** A company has an application that runs across multiple AWS Regions. The application is experiencing performance issues at irregular intervals. A developer must use AWS X-Ray to implement distributed tracing for the application to troubleshoot the root cause of the performance issues. What should the developer do to meet this requirement?

A. Use the X-Ray console to add annotations for AWS services and user-defined services.
B. Use the Region annotation that X-Ray adds automatically for AWS services. Add Region annotation for user-defined services.
C. Use the X-Ray daemon to add annotations for AWS services and user-defined services.
D. Use Region annotation that X-Ray adds automatically for user-defined services. Configure X-Ray to add Region annotation for AWS services.

---

**Question 405.** A company runs an application on AWS. The application uses an AWS Lambda function that is configured with Amazon Simple Queue Service (Amazon SQS) queue called high priority queue as the event source. 406 # A developer is updating the Lambda function with another SQS queue called low priority queue as the event source. The Lambda function must always read up to 10 simultaneous messages from the high priority queue before processing messages from low priority queue. The Lambda function must be limited to 100 simultaneous invocations. Which solution will meet these requirements?

A. Set the event source mapping batch size to 10 for the high priority queue and to 90 for the low priority queue.
B. Set the delivery delay to 0 seconds for the high priority queue and to 10 seconds for the low priority queue.
C. Set the event source mapping maximum concurrency to 10 for the high priority queue and to 90 for the low priority queue.
D. Set the event source mapping batch window to 10 for the high priority queue and to 90 for the low priority queue.

---

**Question 406.** A data visualization company wants to strengthen the security of its core applications. The applications are deployed on AWS across its development, staging, pre-production, and production environments. The company needs to encrypt all of its stored sensitive credentials. The sensitive credentials need to be automatically rotated. A version of the sensitive credentials need to be stored for each environment. Which solution will meet these requirements in the MOST operationally efficient way?

A. Configure AWS Secrets Manager to store different copies of the same credentials across multiple environments.
B. Create a new parameter version in AWS Systems Manager Parameter Store for each environment. Store the environment-specific credentials in the parameter version.
C. Configure the environment variables in the application code. Use different names for each environment type.
D. Configure AWS Secrets Manager to create a new secret for each environment type. Store the environment-specific credentials in the secret.

---

**Question 407.** A developer is investigating an issue in part of a company's application. In the application, messages are sent to an Amazon Simple Queue Service (Amazon SQS) queue. The AWS Lambda function polls the SQS queue and sends email messages by using Amazon Simple Email Service (Amazon SES). Users have been receiving duplicate email messages during periods of high traffic. Which reasons could explain the duplicate email messages? (Choose two.)

A. Standard SQS queues support at-least-once message delivery.
B. Standard SQS queues support exactly-once processing, so the duplicate email messages are because of user error.
C. Amazon SES has the DomainKeys Identified Mail (DKIM) authentication incorrectly configured.
D. The SQS queue's visibility timeout is lower than or the same as the Lambda function's timeout.
E. The Amazon SES bounce rate metric is too high.

---

**Question 408.** A developer is deploying A company's application to Amazon EC2 instances. The application generates gigabytes of files each day. The files are rarely accessed, but the files must be available to the application's users within minutes of a request during the first year of storage. The company must retain the files for 7 years. How can the developer implement the solution to meet these requirements MOST cost-effectively?

A. Store the files in an Amazon S3 bucket. Use the S3 Glacier Instant Retrieval storage class. Create an S3 Lifecycle policy to transition the files to the S3 Glacier Deep Archive storage class after 1 year.
B. Store the files in an Amazon S3 bucket. Use the S3 Standard storage class. Create an S3 Lifecycle policy to transition the files to the S3 Glacier Deep Archive storage class after 1 year.
C. Store the files on an Amazon Elastic Block Store (Amazon EBS) volume. Create an Amazon Data Lifecycle Manager (Amazon DLM) to transition the files to the S3 Glacier Deep Archive storage class after 1 year.
D. Store the files on an Amazon Elastic File System (Amazon EFS) mount. Configure EFS lifecycle management to transition the files to the EFS Standard- Infrequent Access (Standard-IA) storage class after 1 year.

---

**Question 409.** A company's developer has deployed an application in AWS by using AWS CloudFormation. The CloudFormation stack includes parameters in AWS Systems Manager Parameter Store that the application can modify as configuration settings. The application can modify the parameter values. When the developer updated the stack to create additional resources with tags, the developer noted that the parameter values were reset and that the values ignored the latest changes made by the application. The developer needs to change the way the company deploys the CloudFormation stack to prevent the parameter values from being reset. Which solution will meet these requirements with the LEAST development effort?

A. Modify the CloudFormation stack to set the deletion policy to Retain for the parameter.
B. Create an Amazon DynamoDB table as a resource in the CloudFormation stack to hold configuration data for the application. Migrate the parameters that the application is modifying from Parameter Store to the DynamoDB table.
C. Create an Amazon RDS DB instance as a resource in the CloudFormation stack. Create a table in the database for parameter configuration. Migrate the parameters that the application is modifying from Parameter Store to the configuration table.
D. Modify the CloudFormation stack policy to deny updates on Parameter Store parameters.

---

**Question 410.** A company has a social media application that receives large amounts of traffic. User posts and interactions are continuously updated in an Amazon RDS database. The data changes frequently, and the data types can be complex. The application must read requests with minimal latency. The application's current architecture struggles to deliver these rapid data updates efficiently. The company needs a solution to improve the application's performance. Which solution will meet these requirements?

A. Use Amazon DynamoDB Accelerator (DAX) in front of the RDS database to provide a caching layer for the high volume of rapidly changing data.
B. Set up Amazon S3 Transfer Acceleration on the RDS database to enhance the speed of data transfer from the databases to the application.
C. Add an Amazon CloudFront distribution in front of the RDS database to provide a caching layer for the high volume of rapidly changing data.
D. Create an Amazon ElastiCache for Redis cluster. Update the application code to use a write-through caching strategy and read the data from Redis.

---

**Question 411.** A developer created an AWS Lambda function that performs a series of operations that involve multiple AWS services. The function's duration time is higher than normal. To determine the cause of the issue, the developer must investigate traffic between the services without changing the function code. Which solution will meet these requirements?

A. Enable AWS X-Ray active tracing in the Lambda function. Review the logs in X-Ray.
B. Configure AWS CloudTrail. View the trail logs that are associated with the Lambda function.
C. Review the AWS Config logs in Amazon CloudWatch.
D. Review the Amazon CloudWatch logs that are associated with the Lambda function.

---

**Question 412.** A company has on-premises data centers that run an image processing service. The service consists of containerized applications that run on Kubernetes clusters. All the applications have access to the same NFS share for files and data storage. The company is running out of NFS capacity in the data centers and needs to migrate to AWS as soon as possible. The Kubernetes clusters are highly available on AWS. Which combination of steps will meet these requirements? (Choose two.)

A. Transfer the information that is in the NFS share to an Amazon Elastic Block Store (Amazon EBS) volume. Upload the container images to Amazon Elastic Container Registry (Amazon ECR).
B. Transfer the information that is in the NFS share to an Amazon Elastic File System (Amazon EFS) volume. Upload the container images to Amazon Elastic Container Registry (Amazon ECR).
C. Create an Amazon Elastic Container Service (Amazon ECS) cluster to run the applications. Configure each node of the cluster to mount the Amazon Elastic Block Store (Amazon EBS) volume at the required path for the container images.
D. Create an Amazon Elastic Kubernetes Service (Amazon EKS) cluster to run the applications. Configure each node of the cluster to mount the Amazon Elastic Block Store (Amazon EBS) volume at the required path for the container images.
E. Create an Amazon Elastic Kubernetes Service (Amazon EKS) cluster to run the applications. Configure each node of the cluster to mount the Amazon Elastic File System (Amazon EFS) volume at the required path for the container images.

---

**Question 413.** A company has an analytics application that uses an AWS Lambda function to process transaction data asynchronously. A developer notices that asynchronous invocations of the Lambda function sometimes fail. When failed Lambda function invocations occur, the developer wants to invoke a second Lambda function to handle errors and log details. Which solution will meet these requirements?

A. Configure a Lambda function destination with a failure condition. Specify Lambda function as the destination type. Specify the error-handling Lambda function's Amazon Resource Name (ARN) as the resource.
B. Enable AWS X-Ray active tracing on the initial Lambda function. Configure X-Ray to capture stack traces of the failed invocations. Invoke the error-handling Lambda function including the stack traces in the subject object.
C. Configure a Lambda function trigger with a failure condition. Specify Lambda function as the destination type. Specify the error-handling Lambda function's Amazon Resource Name (ARN) as the resource.
D. Create a status check alarm on the initial Lambda function. Configure the alarm to invoke the error-handling Lambda function when the alarm is initiated. Ensure that the alarm passes the stack trace in the event object.

---

**Question 414.** A company introduced a new feature that should be accessible to only a specific group of premium customers. A developer needs the ability to turn the feature on and off in response to performance and feedback. The developer needs a solution to manage and deploy these configurations quickly without causing any disruptions. What should the developer do to meet these requirements?

A. Use AWS AppConfig to manage the feature configuration and to validate and deploy changes. Use feature flags to turn the feature on and off.
B. Use AWS Secrets Manager to securely manage and validate the feature configurations. Enable lifecycle rules to turn the feature on and off.
C. Use AWS Config to manage the feature configuration and validation. Set up AWS Config rules to turn the feature on and off based on predefined conditions.
D. Use AWS Systems Manager Parameter Store to store and validate the configuration settings for the feature. Enable lifecycle rules to turn the feature on and off.

---

**Question 415.** A developer needs approval from a product owner before the developer can deploy code for an application to production. The developer uses AWS CodePipeline to deploy the application. The developer configures an Amazon Simple Notification Service (Amazon SNS) topic to send notifications to the product owner. Which solution is the MOST operationally efficient way for the developer to receive approval from the product owner?

A. Add a new stage to the CodePipeline before the production deployment. Add a manual approval action to the new stage. Specify the SNS topic's Amazon Resource Name (ARN) to notify the product owner.
B. Develop an AWS Step Functions state machine that sends a notification to the product owner and accepts an approval. Add an AWS Step Functions action to the CodePipeline before the production deployment. Add the state machine as the action to the new stage.
C. Add a manual approval action to the existing production deployment stage in CodePipeline. Specify the SNS topic's Amazon Resource Name (ARN) to notify the product owner.
D. Edit the settings in CodePipeline. Create a new notification rule. Specify manual approval as the event that initiates the notification. Create a new notification target. Specify the SNS topic to notify the product owner. Save the notification rule.

**Question 416.** A developer is building a serverless application on AWS for a workflow that processes high volumes of data. In the workflow, an AWS Step Functions state machine invokes several AWS Lambda functions. One of the Lambda functions occasionally fails because of timeout errors during periods of high demand. The developer must ensure that the workflow automatically retries the failed function invocation if a timeout error occurs. Which solution will meet this requirement?

A. Add a Retry field in the Step Functions state machine definition. Configure the state machine with the maximum number of retry attempts and the timeout error type to retry on.
B. Add a Timeout field in the Step Functions state machine definition. Configure the state machine with the maximum number of retry attempts.
C. Add a Fail state to the Step Functions state machine definition. Configure the state machine with the maximum number of retry attempts.
D. Update the Step Functions state machine to pass the invocation request to an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe a Lambda function to the SNS topic. Configure the Lambda function with the maximum number of retry attempts for a timeout error type.

---

**Question 417.** A company runs a serverless application on AWS. The application includes an AWS Lambda function. The Lambda function processes data and stores the data in an Amazon RDS for PostgreSQL database. A developer created a user credentials in the database for the application. The developer needs to use AWS Secrets Manager to manage the user credentials. The password must be rotated on a regular basis. The solution needs to ensure that there is high availability and no downtime for the application during secret rotation. Which should the developer do to meet these requirements?

A. Configure managed rotation with the single user rotation strategy.
B. Configure managed rotation with the alternating users rotation strategy.
C. Configure automatic rotation with the single user rotation strategy.
D. Configure automatic rotation with the alternating users rotation strategy.

---

**Question 418.** A company runs an application on AWS. The application consists of a static website that is hosted on Amazon S3. The application includes Amazon API Gateway APIs that invoke AWS Lambda functions. During a period of high traffic on the application, users reported that the application was slow at irregular intervals. There were no failed requests. A developer needs to find the slow executions across all the Lambda functions. Which solution will meet these requirements?

A. Perform a query across all the Lambda function log groups by using Amazon CloudWatch Logs Insights. Filter on type of report, descending by Lambda function execution duration.
B. Enable AWS CloudTrail Insights on the account where the Lambda functions are running. After CloudTrail Insights has finished processing, review CloudTrail Insights to find the anomalous functions.
C. Enable AWS X-Ray for all the Lambda functions. Configure an X-Ray insight on a group that includes all the Lambda functions. After the X-Ray insight has finished processing, review the X-Ray logs.
D. Set up AWS Glue to crawl through the logs in Amazon CloudWatch Logs for the Lambda functions. Configure an AWS Glue job to transfer the logs data to a structured format and store the data into Amazon S3. Use the Amazon CloudWatch dashboard to visualize the slowest functions based on the duration.

---

**Question 419.** A company is building a serverless application on AWS. The application uses Amazon API Gateway and AWS Lambda. The company wants to deploy the application to its development, test, and production environments. Which solution will meet these requirements with the LEAST development effort?

A. Use API Gateway stage variables and create Lambda aliases to reference environment-specific resources.
B. Use Amazon Elastic Container Service (Amazon ECS) to deploy the application to the environments.
C. Duplicate the code for each environment. Deploy the code to a separate API Gateway stage.
D. Use AWS Elastic Beanstalk to deploy the application to the environments.

---

**Question 420.** A developer uses AWS CloudFormation to deploy an Amazon API Gateway API and an AWS Step Functions state machine. The state machine must reference the API Gateway API after the CloudFormation template is deployed. The developer needs a solution that uses the state machine to reference the API Gateway endpoint. Which solution will meet these requirements MOST cost-effectively?

A. Configure the CloudFormation template to reference the API endpoint in the DefinitionSubstitutions property for the AWS::StepFunctions::StateMachine resource.
B. Configure the CloudFormation template to store the API endpoint in an environment variable for the AWS::StepFunctions::StateMachine resource. Configure the state machine to reference the environment variable.
C. Configure the CloudFormation template to store the API endpoint in a standard AWS::SecretsManager::Secret resource. Configure the state machine to reference the resource.
D. Configure the CloudFormation template to store the API endpoint in a standard AWS::AppConfig::ConfigurationProfile resource. Configure the state machine to reference the resource.

---

**Question 421.** A developer is building an application on AWS. The application includes an AWS Lambda function that processes messages from an Amazon Simple Queue Service (Amazon SQS) queue. The Lambda function sometimes fails or times out. The developer needs to figure out why the Lambda function fails to process some messages. Which solution will meet these requirements with the LEAST operational overhead?

A. Increase the maximum timeout of the Lambda function to 15 minutes. Check the AWS CloudTrail event history for error details.
B. Increase the visibility timeout of the SQS queue. Check logs in Amazon CloudWatch Logs for error details.
C. Create a dead-letter queue. Configure the Lambda function to send the failed messages to the dead-letter queue.
D. Create an Amazon DynamoDB table. Update the Lambda function to send the failed messages to the DynamoDB table.

---

**Question 422.** A developer needs to deploy an application in three AWS Regions by using AWS CloudFormation. Each Region will use an AWS Elastic Beanstalk environment with an Application Load Balancer (ALB). The developer wants to use AWS Certificate Manager (ACM) to deploy SSL certificates to each ALB. Which solution will meet these requirements?

A. Create a certificate in ACM in any one of the Regions. Import the certificate into the ALB that is in each Region.
B. Create a global certificate in ACM. Update the CloudFormation template to deploy the global certificate to each ALB.
C. Create a certificate in ACM in each Region. Import the certificate into the ALB for each Region.
D. Create a certificate in ACM in the us-east-1 Region. Update the CloudFormation template to deploy the certificate to each ALB.

---

**Question 423.** A company needs to deploy all its cloud resources by using AWS CloudFormation templates. A developer must create an Amazon Simple Notification Service (Amazon SNS) automatic notification to help enforce this rule. The developer creates an SNS topic and shares the email address of the company's security team to the SNS topic. The security team must receive a notification immediately if an IAM role is created without the use of CloudFormation. Which solution will meet this requirement?

A. Create an AWS Lambda function to filter events from CloudTrail if a role was created without CloudFormation. Configure the Lambda function to publish to the SNS topic. Create an Amazon EventBridge schedule to run the Lambda function every 15 minutes.
B. Create an AWS Fargate task in Amazon Elastic Container Service (Amazon ECS) to filter events from CloudTrail if a role was created without CloudFormation. Configure the Fargate task to publish to the SNS topic. Create an Amazon EventBridge schedule to run the Fargate task every 15 minutes.
C. Launch an Amazon EC2 instance that includes a script to filter events from CloudTrail if a role was created without CloudFormation. Configure the script to publish to the SNS topic. Create a cron job to run the script on the EC2 instance every 15 minutes.
D. Create an Amazon EventBridge rule to filter events from CloudTrail if a role was created without CloudFormation. Specify the SNS topic as the target of the EventBridge rule.

---

**Question 424.** A company is adopting serverless computing for some of its new services. A development team needs to create a serverless infrastructure by using AWS Serverless Application Model (AWS SAM). All infrastructure must be deployed by using AWS CloudFormation templates. What should the development team do to meet these requirements?

A. Add a Resources section to the CloudFormation templates that contains AWS::Lambda::Function resources.
B. Add a Mappings section to the CloudFormation templates that contains AWS::Serverless::Function and AWS::Serverless::API.
C. Add a Transform section to the CloudFormation templates. Use the AWS SAM syntax to define the resources.
D. Add a Parameters section to the CloudFormation templates that specifies the relevant AWS SAM Globals section.

---

**Question 425.** A developer is building an application that invokes AWS Lambda functions asynchronously to process events. The developer notices that a Lambda function fails to process some events at random times. The developer needs to investigate the failed events and capture the events that the Lambda function fails to process. Which solution will meet these requirements?

A. Add an Amazon EventBridge rule for the Lambda function. Configure the EventBridge rule to react to failed events and to store the events in an Amazon DynamoDB table.
B. Configure the Lambda function with a dead-letter queue based in Amazon Kinesis. Update the Lambda function's execution role with the required permissions.
C. Configure the Lambda function with an Amazon Simple Queue Service (Amazon SQS) dead-letter queue. Update the Lambda function's execution role with the required permissions.
D. Configure the Lambda function with an Amazon Simple Queue Service (Amazon SQS) FIFO dead-letter queue. Update the Lambda function's execution role with the required permissions.

---

**Question 426.** A company has a serverless application for its ecommerce website. The application includes a REST API in Amazon API Gateway that invokes an AWS Lambda function. The Lambda function processes data and stores the data in Amazon DynamoDB table. The Lambda function calls a third-party application API to process the order. During peak usage when the API calls exceeds a certain threshold, the third-party stock application sometimes fails and returns error messages. The company needs a solution that will not overwhelm the third-party stock application. Which solution will meet these requirements?

A. Configure the REST API in API Gateway to route the requests directly into DynamoDB. Configure a DynamoDB intrinsic function to perform the transformation. Set up a DynamoDB stream to key on it.
B. Configure the REST API in API Gateway to route the requests directly into an Amazon Simple Queue Service (Amazon SQS) queue. Configure the Lambda function with a reserved concurrency equal to the third-party stock application's threshold. Set the Lambda function to process the messages from the SQS queue.
C. Configure the REST API in API Gateway to route the requests directly into an Amazon Simple Notification Service (Amazon SNS) topic. Set up a Lambda function to subscribe to the SNS topic. Set the Lambda function to process the messages from the SNS topic.
D. Configure the REST API in API Gateway to route the requests directly into Amazon Athena. Configure the transformation by using SQL. Set up a Lambda function to subscribe to the SNS topic. Delete the Lambda function and the third-party stock application API. Delete the DynamoDB table.

---

**Question 427.** A company hosts its application on AWS. The application runs on an Amazon Elastic Container Service (Amazon ECS) cluster that uses AWS Fargate. The cluster runs behind an Application Load Balancer. The application stores data in an Amazon Aurora database. A developer encrypts and manages database credentials inside the application. The company wants to use a more secure credential storage method and implement periodic credential rotation. Which solution will meet these requirements with the LEAST operational overhead?

A. Migrate the secret credentials to Amazon RDS parameter groups. Encrypt the parameter by using an AWS Key Management Service (AWS KMS) key. Turn on secret rotation. Use IAM policies and roles to grant Amazon ECS KMS permissions to access the parameter groups.
B. Migrate the credentials to AWS Systems Manager Parameter Store. Encrypt the parameter by using an AWS Key Management Service (AWS KMS) key. Turn on secret rotation. Use IAM policies and roles to grant Amazon ECS KMS permissions to access the parameter groups.
C. Migrate the credentials to ECS Fargate environment variables. Encrypt the credentials by using an AWS Key Management Service (AWS KMS) key. Use IAM policies and roles to grant Amazon ECS Fargate permissions to access AWS Secrets Manager.
D. Migrate the credentials to AWS Secrets Manager. Encrypt the credentials by using an AWS Key Management Service (AWS KMS) key. Turn on secret rotation. Use IAM policies and roles to grant Amazon ECS Fargate permissions to access AWS Secrets Manager.

---

**Question 428.** A company has a mobile app. The app includes an Amazon API Gateway REST API that invokes AWS Lambda functions. The Lambda functions process data from the app. The company needs to conduct these tests with a subset of users before deployment. The tests must not affect other users of the app. Which solution will meet these requirements with the LEAST amount of operational effort?

A. Create a new version of each Lambda function with a weighted alias. Update the new weighted alias Amazon Resource Name (ARN) in the REST API.
B. Create a new REST API in API Gateway. Set up a Lambda proxy integration to connect to multiple Lambda functions. Enable canary settings on the deployment stage. Specify a smaller percentage of API traffic to go to the new version of the Lambda function.
C. Create a new version of each Lambda function. Define a predefined canary deployment in AWS CodeDeploy to slowly shift the traffic to the new versions automatically.
D. Create a new version of each Lambda function. Set up a Lambda proxy integration to connect to multiple Lambda functions. Specify the necessary parameters and properties in API Gateway. Enable canary settings on the deployment stage. Specify a smaller percentage of API traffic to go to the new version of the Lambda function.

---

**Question 429.** A developer works for A company that only has a single pre-production AWS account with an AWS CloudFormation Serverless Application Model (AWS SAM) stack. The developer made changes to an existing AWS Lambda function specified in the stack and additional Amazon Simple Notification service (Amazon SNS) topics. The developer wants to do a one-time deploy of the changes to test if the changes are working. The developer does not want to impact the existing pre-production application that is currently being used by other teams as a release pipeline. Which solution will meet these requirements?

A. Use the AWS SAM CLI to package and deploy the SAM application to the pre-production AWS account. Specify the delta deployments.
B. Use the AWS SAM CLI to package and create a change set against the pre-production AWS account. Execute the change set on a new AWS account designated for a development environment.
C. Use the AWS SAM CLI to package and deploy the SAM application to a new AWS account designated for a development environment.
D. Update the CloudFormation stack in the pre-production account. Add a separate stage that points to a new AWS account designated for a development environment.

---

**Question 430.** A company built an online event platform. For each event, the company organizes quizzes and generates leaderboards that are based on the quiz scores. The company stores the leaderboard data in Amazon DynamoDB and retains the data for 30 days after an event is complete. The company then uses a scheduled job to delete the old leaderboard data. The DynamoDB table is configured with a fixed write capacity. During the months when many events occur, the DynamoDB write API requests are throttled when the scheduled delete job runs. A developer must create a long-term solution that deletes the old leaderboard data and optimizes write throughput. Which solution meets these requirements?

A. Configure a TTL attribute for the leaderboard data.
B. Use DynamoDB Streams to schedule and delete the leaderboard data.
C. Use AWS Step Functions to schedule and delete the leaderboard data.
D. Set a higher write capacity when the scheduled delete job runs.

---

**Question 431.** A company uses an AWS Lambda function that reads messages from an Amazon Simple Queue Service (Amazon SQS) standard queue. The Lambda function makes an HTTP call to a third-party API for each message. The company wants to ensure that the Lambda function does not overwhelm the third-party API with more than two concurrent requests. Which solution will meet these requirements?

A. Configure a provisioned concurrency of two on the Lambda function.
B. Configure a batch size of two on the Amazon SQS event source mapping for the Lambda function.
C. Configure Lambda event filtering to process two messages from Amazon SQS at every invocations.
D. Configure a maximum concurrency of two on the Amazon SQS event source mapping for the Lambda function.

---

**Question 432.** A company is using Amazon API Gateway to develop an API for its application on AWS. A developer needs to test and generate API responses. Other teams are required to test the API immediately. What should the developer do to meet these requirements?

A. Set up a mock integration request in API Gateway. Configure the method's integration request and integration response to associate a response with a given status code.
B. Set up the request validators in the API's OpenAPI definition file. Import the OpenAPI definitions into API Gateway to test the API.
C. Set up a gateway response for the API in API Gateway. Configure response headers with hardcoded HTTP status codes and responses.
D. Set up a request parameter-based Lambda authorizer to control access to the API. Configure the Lambda function with the necessary mapping template.

---

**Question 433.** A company is releasing a new feature. Users can request early access to the new feature by using an application form. The company expects a surge of requests when the application form becomes available. Each request will be stored as an item in an Amazon DynamoDB table. Each item will contain the user's username, the submission date, and a validation status of UNVALIDATED, VALID, or NOT VALID. Each item also will contain the user's rating of the process on a scale of 1 to 5. A user can submit one request. For the DynamoDB table, the developer must choose a partition key that will give well-distributed records across partitions. Which DynamoDB attribute will meet these requirements?

A. Username
B. Submission date
C. Validation status
D. Rating of the process on a scale of 1 to 5

---

**Question 434.** A developer is creating a publicly accessible enterprise website consisting of only static assets. The developer is hosting the website in Amazon S3 and serving the website to users through an Amazon CloudFront distribution. The users of this application must not be able to access the application content directly from an S3 bucket. All content must be served through the Amazon CloudFront distribution. Which solution will meet these requirements?

A. Create a new origin access control (OAC) in CloudFront. Configure the CloudFront distribution's origin to use the new OAC. Update the S3 bucket policy to allow CloudFront OAC with read and write access to access Amazon S3.
B. Update the CloudFront distribution's settings with Amazon S3. Enable the block all public access settings in Amazon S3. Configure the CloudFront distribution's with Amazon S3 as the origin. Update the S3 bucket policy to allow CloudFront write access.
C. Update the S3 bucket's static website settings. Enable static website hosting and specifying index and error documents. Update the CloudFront origin to use the S3 bucket's website endpoint.
D. Update the CloudFront distribution's origin to send a custom header. Update the S3 bucket policy with a condition by using the aws:RequestedTag/tag-key key. Configure the tag-key as the custom header name, and the value being matched as the header's value.

---

**Question 435.** A developer built an application that calls an external API to obtain data, processes the data, and saves the result to Amazon S3. The developer built a container image with all of the necessary dependencies to run the application. The application runs locally and requires minimal CPU and RAM resources. The developer has created an Amazon ECS cluster. The developer needs to run the application hourly in Amazon Elastic Container Service (Amazon ECS). Which solution will meet these requirements with the LEAST amount of infrastructure management overhead?

A. Add a capacity provider to manage instances.
B. Add an Amazon EC2 instance that runs the application.
C. Define a task definition with an AWS Fargate launch type.
D. Create an Amazon ECS cluster and add the managed node groups feature to run the application.

---

**Question 436.** A company runs its website on AWS. The company posts daily polls on its website and publishes the poll results next day. The website stores user responses in an Amazon DynamoDB table. After the poll results are published, the company does not need to keep the user responses. A developer needs to implement a solution that will automatically remove old user responses from the DynamoDB table. The developer adds a new expiration_date attribute to the DynamoDB table. The developer plans to use the expiration_date attribute for the automation. Which solution will meet these requirements with the LEAST development effort?

A. Create an AWS Lambda function to delete old user responses based on the expiration_date attribute. Create an Amazon EventBridge schedule to run the Lambda function daily.
B. Create an AWS Fargate task in Amazon Elastic Container Service (Amazon ECS) to delete old user responses based on the expiration_date attribute. Create an Amazon EventBridge schedule to run the Fargate task daily.
C. Create an AWS Glue job to delete old user responses based on the expiration_date attribute. Create an AWS Glue trigger schedule to run the job daily.
D. Enable TTL on the DynamoDB table and specify the expiration_date attribute. Expire old user responses by using DynamoDB TTL.

---

**Question 437.** A developer is creating a simple proof-of-concept demo by using AWS CloudFormation and AWS Lambda functions. The demo will use a CloudFormation template to deploy an existing Lambda function. The developer defined an AWS::Lambda::Function resource in a CloudFormation template. The developer needs to add the S3 bucket to the CloudFormation template. What should the developer do to meet these requirements with the LEAST development effort?

A. Add the function code in the CloudFormation template inline as the code property.
B. Add the function code in the CloudFormation template as the ZipFile property.
C. Find the S3 key for the Lambda function. Add the S3 key as the ZipFile property in the CloudFormation template.
D. Add the relevant key and bucket to the S3Bucket and S3Key properties in the CloudFormation template.

---

**Question 438.** A developer is building a microservices-based application by using Python on AWS and several AWS services. The developer must use AWS X-Ray. The developer views the service map by using the console to view the service dependencies. During testing, the developer notices that some services are missing from the service map. What can the developer do to ensure that all services appear in the X-Ray service map?

A. Modify the X-Ray Python agent configuration in each service to increase the sampling rate.
B. Instrument the application by using the AWS SDK for Python. Install the X-Ray SDK for all the services that the application uses.
C. Enable X-Ray data aggregation in Amazon CloudWatch Logs for all the services that the application uses.
D. Increase the X-Ray service map timeout value in the X-Ray console.

---

**Question 439.** A developer is building a containerized application on AWS. The application communicates with a third-party service by using API keys. The developer needs a secure way to store the API keys and pass the API keys to the containerized application. Which solutions will meet these requirements? (Choose two.)

A. Store the API keys as a SecureString parameter in AWS Systems Manager Parameter Store. Grant the application access to retrieve the value from Parameter Store.
B. Store the API keys in AWS CloudFormation templates by using base64 encoding. Pass the API keys to the application through container definition environment variables.
C. Add a new AWS CloudFormation parameter to the CloudFormation template. Pass the API keys to the application by using the container definition environment variables.
D. Embed the API keys in the application. Build the container image on-premises. Upload the container image to Amazon Elastic Container Registry (Amazon ECR).
E. Store the API keys in the application as a SecretString parameter in AWS Secrets Manager. Grant the application access to retrieve the value from Secrets Manager.

---

**Question 440.** A company runs an application on AWS. The application stores data in an Amazon DynamoDB table. Some queries are taking a long time to run. These slow queries involve an attribute that is not the table's partition key or sort key. The amount of data that the application stores in the DynamoDB table is expected to increase significantly. A developer must increase the performance of the queries. Which solution will meet these requirements?

A. Increase the page size for each request by setting the Limit parameter to be higher than the default value. Configure the application to retry any request that exceeds the throughput.
B. Create a global secondary index (GSI). Set the query attribute to be the partition key of the index.
C. Perform a parallel scan operation by issuing individual scan requests. In the parameters, specify the segment for the scan requests and the total number of segments for the parallel scan.
D. Turn on read capacity auto scaling for the DynamoDB table. Increase the maximum read capacity units (RCUs).

---

**Question 441.** A company runs a application on Amazon EC2 instances behind an Application Load Balancer. The EC2 instances run in an Auto Scaling group across multiple Availability Zones. The application needs to retrieve application secrets during the application startup and to export the secrets as environment variables. Which solution will meet these requirements with the LEAST development effort?

A. Save the secrets in a text file and store the text file in Amazon S3. Provision a customer master key. Use the key to encrypt the secrets. Enable automatic rotation. Configure an Amazon Lambda function to rotate the secrets. Configure a startup data script to read the secrets from Amazon S3 and to export the secrets as environment variables.
B. Save the secrets as strings in AWS Systems Manager Parameter Store and use the default AWS Key Management Service (AWS KMS) key. Configure an AWS Lambda function to rotate the secrets. Configure the startup and export as environment variables.
C. Save the secrets as base64 encoded strings in the application properties. Configure the startup and export as environment variables. Write a script to rotate the secrets in the application code. Write a startup data script to read the secrets from the application code and export the secrets as environment variables.
D. Store the secrets in AWS Secrets Manager. Provision a new customer master key. Use the key to encrypt the secrets. Enable automatic rotation. Configure a startup data script to read the secrets in the application code. Write a startup data script to read the secrets from Amazon S3 and to export the secrets as environment variables.

---

**Question 442.** A company is using Amazon API Gateway to invoke a new AWS Lambda function. The company has Lambda function versions in its PROD and DEV environments. In each environment, there is a Lambda function alias pointing to the corresponding Lambda function version. The company wants to configure API Gateway to enable the PROD and DEV Lambda function versions to be simultaneously and distinctly available. Which solution will meet these requirements?

A. Enable a Lambda authorizer for the Lambda function alias in API Gateway. Republish PROD and create a new stage for DEV. Create API Gateway stage variables for PROD and DEV stages. Point each stage variable to the PROD Lambda function alias and to the DEV Lambda function alias.
B. Set up a gateway response in API Gateway. Republish PROD and create a new stage for DEV. Create API gateway responses in API Gateway for PROD and DEV Lambda aliases.
C. Use an alias in API Gateway. Republish PROD and create a new stage for development. Create API gateway environment variables for PROD and DEV stages. Point each stage variable to the PROD Lambda function alias and to the DEV Lambda function alias.
D. Embed the API keys in the application. Build the container image on-premises. Create API Gateway stage variables for PROD and DEV stages. Point each stage variable to the PROD Lambda function alias and to the DEV Lambda function alias.

---

**Question 443.** A developer is working on an ecommerce platform that communicates with several third-party payment processing APIs. The third-party payment services do not provide a test environment. The developer needs to validate the ecommerce platform's integration with the third-party payment processing APIs. The developer must test the API integration code without invoking the third-party payment processing APIs. Which solution will meet these requirements?

A. Set up an Amazon API Gateway REST API with a gateway response configured for status code 200. Add response templates that include sample responses captured from the real third-party API.
B. Set up an AWS AppSync GraphQL API with a data source configured for each third-party API. Specify an integration type of Mock. Configure integration responses by using sample responses captured from the real third-party API.
C. Create an AWS Lambda function for each third-party API. Embed responses captured from the real third-party API. Configure Amazon Route 53 Resolver with an inbound endpoint for each Lambda function Amazon Resource Name (ARN).
D. Set up an Amazon API Gateway REST API for each third-party API. Specify an integration request type of Mock. Configure integration responses by using sample responses captured from the real third-party API.

---

