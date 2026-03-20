# AWS Developer Associate - Quiz Set 2 (Questions 76–150)

---

**Question 76.** A company is developing a serverless application that consists of various AWS Lambda functions behind Amazon API Gateway APIs. A developer needs to automate the deployment of Lambda function code. The developer will deploy updated Lambda functions with AWS CodeDeploy. The deployment must minimize the exposure of potential errors to end users. When the application is in production, the application cannot tolerate any downtime outside the specified maintenance window. Which deployment configuration will meet these requirements with the LEAST deployment time?

A. Use the AWS CodeDeploy in-place deployment configuration for the Lambda functions. Shift all traffic immediately after deployment.
B. Use the AWS CodeDeploy linear deployment configuration to shift 10% of the traffic every minute.
C. Use the AWS CodeDeploy all-at-once deployment configuration to shift all traffic to the updated versions immediately.
D. Use the AWS CodeDeploy predefined canary deployment configuration to shift 10% of the traffic immediately and shift the remaining traffic after 5 minutes.

---

**Question 77.** A developer needs to store configuration variables for an application. The developer needs to set an expiration date and time for the configuration. The developer wants to receive notifications before the configuration expires. Which solution will meet these requirements with the LEAST operational overhead?

A. Create a standard parameter in AWS Systems Manager Parameter Store. Set Expiration and ExpirationNotification policy types.
B. Create a standard parameter in AWS Systems Manager Parameter Store. Create an AWS Lambda function to expire the configuration and to send Amazon Simple Notification Service (Amazon SNS) notifications.
C. Create an advanced parameter in AWS Systems Manager Parameter Store. Set Expiration and ExpirationNotification policy types.
D. Create an advanced parameter in AWS Systems Manager Parameter Store. Create an Amazon EC2 instance with a cron job to expire the configuration and to send notifications.

---

**Question 78.** A developer creates an AWS Lambda function that retrieves and groups data from several public API endpoints. The Lambda function is connected to a VPC. An internet gateway is attached to the VPC. The VPC uses the default network ACL and security group configurations. The developer finds that the Lambda function can no longer access the public API. The developer has ensured that the public API is accessible, but the Lambda function cannot connect to the API. How should the developer fix the connection issue?

A. Ensure that the network ACL allows outbound traffic to the public internet.
B. Ensure that the security group allows outbound traffic to the public internet.
C. Ensure that outbound traffic from the private subnet is routed to a public NAT gateway.
D. Ensure that outbound traffic from the private subnet is routed to a new internet gateway.

---

**Question 79.** A company is developing an ecommerce application that uses Amazon API Gateway APIs. The application uses AWS Lambda as a backend. The company needs to test the code in a dedicated, monitored test environment before the company releases the code to the production environment. Which solution will meet these requirements?

A. Use a single stage in API Gateway. Create a Lambda function for each environment. Configure API clients to send a query parameter that indicates the environment and the specific Lambda function.
B. Use multiple stages in API Gateway. Create a single Lambda function for all environments. Add different code blocks for different environments in the Lambda function based on Lambda environment variables.
C. Use multiple stages in API Gateway. Create a Lambda function for each environment. Configure API Gateway stage variables to route traffic to the Lambda function in different environments.
D. Use a single stage in API Gateway. Configure API clients to send a query parameter that indicates the environment. Add different code blocks for different environments in the Lambda function to match the value of the query parameter.

---

**Question 80.** A developer is working on a web application that uses Amazon DynamoDB as its data store. The application has two DynamoDB tables: one table that is named artists and one table that is named songs. The artists table has artistName as the partition key. The songs table has songName as the partition key and artistName as the sort key. The table usage pattern requires retrieval of multiple songs and artists in a single database operation from the webpage. The developer needs a way to retrieve this information with minimal network traffic and optimal performance. Which solution will meet these requirements?

A. Perform a BatchGetItem operation that returns items from the two tables. Use the list of songName/artistName keys for the songs table and the list of artistName key for the artists table.
B. Create a local secondary index (LSI) on the songs table that uses artistName as the partition key. Perform a query operation for each artistName key. Perform a query operation for each artistName on the artists table.
C. Perform a BatchGetItem operation on the songs table that uses the songName/artistName keys. Perform a BatchGetItem operation on the artists table that uses artistName as the key.
D. Perform a Scan operation on each table that filters by the list of songName/artistName for the songs table and the list of artistName in the artists table.

---

**Question 81.** A developer is creating an AWS Lambda function. The Lambda function will consume messages from an Amazon Simple Queue Service (Amazon SQS) queue. The developer wants to integrate unit testing as part of the function's continuous integration and continuous delivery (CI/CD) process. How can the developer test the function?

A. Create an AWS CloudFormation template that creates an SQS queue and deploys the Lambda function. Create a stack from the template during the CI/CD process. Invoke the deployed function. Verify the output.
B. Create an SQS event for tests. Use a test that consumes messages from the SQS queue during the function's CI/CD process.
C. Create an SQS queue for tests. Use this SQS queue in the application's unit test. Run the unit tests during the CI/CD process.
D. Use the aws lambda invoke command with a test event during the CI/CD process.

---

**Question 82.** A company has a front-end application that runs on four Amazon EC2 instances behind an Elastic Load Balancer (ELB) in a production environment that is provisioned by AWS Elastic Beanstalk. A developer needs to deploy and test new application code while updating the Elastic Beanstalk platform from the current version to a newer version of Node.js. The solution must result in zero downtime for the application. Which solution will meet these requirements?

A. Clone the production environment to a different platform version. Deploy the new application code, and test the environment. Swap the environment URLs after the verification fails.
B. Deploy the new application code in an all-at-once deployment to the existing EC2 instances. Test the code. Redeploy the previous code if verification fails.
C. Perform an immutable update to deploy the new application code to new EC2 instances. Serve traffic to the new instances after they pass health checks.
D. Use a rolling deployment for the new application code. Apply the code to a subset of EC2 instances until the tests pass. Redeploy the previous code if the tests fail.

---

**Question 83.** A developer is creating an AWS Lambda function. The Lambda function needs an external library to connect to a third-party solution. The external library is a collection of files with a total size of 100 MB. The developer needs to make the external library available to the Lambda execution environment and reduce the Lambda package space. Which solution will meet these requirements with the LEAST operational overhead?

A. Create a Lambda layer. Create the external library. Configure the Lambda function to use the layer.
B. Create an Amazon S3 bucket. Upload the external library into the S3 bucket. Mount the S3 bucket folder in the Lambda function. Import the library by using the proper folder in the mount point.
C. Load the external library to the Lambda function's /tmp directory during deployment of the Lambda package. Import the library from the /tmp directory.
D. Create an Amazon Elastic File System (Amazon EFS) volume. Upload the external library into the EFS volume. Mount the EFS volume in the Lambda function. Import the library by using the proper folder in the mount point.

---

**Question 84.** A developer is integrating Amazon ElastiCache in an application. The cache will store data from a database. The cached data must populate real-time dashboards. Which caching strategy will meet these requirements?

A. A read-through cache
B. A write-behind cache
C. A lazy-loading cache
D. A write-through cache

---

**Question 85.** A developer is creating an AWS Serverless Application Model (AWS SAM) template. The AWS SAM template contains the definition of multiple AWS Lambda functions, an Amazon S3 bucket, and an Amazon CloudFront distribution. One of the Lambda functions runs on Lambda@Edge in the CloudFront distribution. The S3 bucket is configured as an origin for the CloudFront distribution. When the developer deploys the AWS SAM template in the us-east-1 Region, the creation of the stack fails. Which of the following could be the reason for this issue?

A. CloudFront distributions can be created only in the us-east-1 Region.
B. Lambda@Edge functions can be created only in the us-east-1 Region.
C. A single AWS SAM template cannot contain multiple Lambda functions.
D. The CloudFront distribution and the S3 bucket cannot be created in the same Region.

---

**Question 86.** An organization is storing large files in Amazon S3, and is writing a web application to display meta-data about the files to end-users. Based on the metadata a user selects an object to download. The organization needs a mechanism to index the files and provide single-digit millisecond latency retrieval for the metadata. What AWS service should be used to accomplish this?

A. Amazon DynamoDB
B. Amazon EC2
C. AWS Lambda
D. Amazon RDS

---

**Question 87.** A company must deploy all its Amazon RDS DB instances by using AWS CloudFormation templates as part of AWS CodePipeline continuous integration and continuous delivery (CI/CD) automation. The primary password for the DB instance must be automatically generated as part of the deployment process. Which solution will meet these requirements with the LEAST development effort?

A. Create an AWS Lambda-backed CloudFormation custom resource. Write Lambda code that generates a secure string. Return the value of the secure string as a data field of the custom resource response object. Use the CloudFormation Fn::GetAtt intrinsic function to get the value of the secure string. Use the value to create the DB instance.
B. Use the AWS CodeBuild action of CodePipeline to generate a secure string by using the following AWS CLI command: aws codepipeline get-pipeline. Pass the CloudFormation parameter with the NoEcho attribute set to true. Use the parameter reference to create the DB instance.
C. Create an AWS Lambda-backed CloudFormation custom resource. Write Lambda code that generates a secure string. Create secrets in AWS Secrets Manager. Use the CloudFormation Fn::GetAtt intrinsic function to get a value of the secure string. Use the secretsmanager dynamic reference to create the DB instance.
D. Use the AWS::SecretsManager::Secret resource to generate a secure string. Store the string as a secret in AWS Secrets Manager. Use the secretsmanager dynamic reference to use the value stored in the secret to create the DB instance.

---

**Question 88.** A developer is developing an application that uses signed requests (Signature Version 4) to call other AWS services. The developer has created a canonical request, has created the string to sign, and has calculated signing information. Which methods could the developer use to complete a signed request? (Choose two.)

A. Add the signature to an HTTP header that is named Authorization.
B. Add the signature to a session cookie.
C. Add the signature to an HTTP header that is named Authentication.
D. Add the signature to a query string parameter that is named X-Amz-Signature.
E. Add the signature to an HTTP header that is named WWW-Authenticate.

---

**Question 89.** A company's developer is building a static website to be deployed in Amazon S3 for a production environment. The website integrates with an Amazon Aurora PostgreSQL database by using an AWS Lambda function. The website that is deployed to production will use a Lambda alias that points to a specific version of the Lambda function. The company must rotate the database credentials every 2 weeks. Lambda functions that the company deployed previously must use the most recent credentials. Which solution will meet these requirements?

A. Store the database credentials in AWS Secrets Manager. Turn on rotation. Write code in the Lambda function to retrieve the credentials from Secrets Manager.
B. Include the database credentials as part of the Lambda function code. Update the credentials periodically and deploy the updated Lambda function.
C. Use Lambda environment variables. Update the environment variables when new credentials are available.
D. Store the database credentials in AWS Systems Manager Parameter Store. Turn on rotation. Write code in the Lambda function to retrieve the credentials from Systems Manager Parameter Store.

---

**Question 90.** A developer has written code for an application and wants to share it with other developers on the team to receive feedback. The shared application code needs to be stored long-term with multiple versions and batch change tracking. Which AWS service should the developer use?

A. AWS CodeBuild
B. Amazon S3
C. AWS CodeCommit
D. AWS Cloud9

---

**Question 91.** A real-time messaging application uses Amazon API Gateway WebSocket APIs with backend HTTP service. A developer needs to build a feature in the application to identify a client that keeps connecting to and disconnecting from the WebSocket connection. The developer also needs the ability to remove the client. Which combination of changes should the developer make to the application to meet these requirements? (Choose two.)

A. Switch to HTTP APIs in the backend service.
B. Switch to REST APIs in the backend service.
C. Use the callback to disconnect the client from the backend service.
D. Add code to track the client status in Amazon ElastiCache in the backend service.
E. Implement $connect and $disconnect routes in the backend service.

---

**Question 92.** A developer is writing an application for a company. The application will be deployed on Amazon EC2 and will use an Amazon RDS for Microsoft SQL Server database. The company's security team requires that database credentials are rotated at least weekly. How should the developer configure the database credentials for this application?

A. Create a database user. Store the user name and password in an AWS Systems Manager Parameter Store secure string parameter. Enable rotation of the AWS Key Management Service (AWS KMS) key that is used to encrypt the parameter.
B. Enable IAM authentication for the database. Create a database user for use with IAM authentication. Enable password rotation.
C. Create a database user. Store the user name and password in an AWS Secrets Manager secret that has daily rotation enabled.
D. Use the EC2 user data to create a database user. Provide the user name and password in environment variables to the application.

---

**Question 93.** A developer maintains a critical business application that uses Amazon DynamoDB as the primary data store. The DynamoDB table contains millions of documents and receives 30-60 requests each minute. The developer needs to perform processing in near-real time on the documents when they are added or updated in the DynamoDB table. How can the developer implement this feature with the LEAST amount of change to the existing application code?

A. Set up a cron job on an Amazon EC2 instance. Run a script every hour to query the table for changes and process the documents.
B. Enable a DynamoDB stream on the table. Invoke an AWS Lambda function to process the documents.
C. Update the application to send a PutEvents request to Amazon EventBridge. Create an EventBridge rule to invoke an AWS Lambda function to process the documents.
D. Update the application to synchronously process the documents directly after the DynamoDB write.

---

**Question 94.** A company has hundreds of AWS Lambda functions that the company's QA team needs to test by using the Lambda function URLs. A developer needs to configure the authentication of the Lambda function URLs to allow access so that the QA IAM group can invoke the Lambda functions by using the public URLs. Which solution will meet these requirements?

A. Create a CLI script that loops on the Lambda functions to add a Lambda function URL with the AWS_IAM auth type. Run another script to create an IAM identity-based policy that allows the lambda:InvokeFunctionUrl action to all the Lambda function Amazon Resource Names (ARNs). Attach the policy to all the Lambda function Amazon Resource Names (ARNs).
B. Create a CLI script that loops on the Lambda functions to add a Lambda function URL with the NONE auth type. Run another script to create an IAM resource-based policy that allows the lambda:InvokeFunctionUrl action to all the Lambda function Amazon Resource Names (ARNs). Attach the policy to the QA IAM group's Amazon Resource Name (ARN).
C. Create a CLI script that loops on the Lambda functions to add a Lambda function URL with the AWS_IAM auth type. Run another script to create an IAM identity-based policy that allows the lambda:InvokeFunctionUrl action to all the Lambda function Amazon Resource Names (ARNs). Attach the policy to the QA IAM group.
D. Create a CLI script that loops on the Lambda functions to add a Lambda function URL with the NONE auth type. Run another script to loop on the Lambda functions to create an IAM identity-based policy that allows the lambda:InvokeFunctionUrl action from the QA IAM group's Amazon Resource Name (ARN).

---

**Question 95.** A developer needs to build an AWS CloudFormation template that self-populates the AWS Region variable that deploys the CloudFormation template. What is the MOST operationally efficient way to determine the Region in which the template is being deployed?

A. Use the AWS::Region pseudo parameter.
B. Require the Region as a CloudFormation parameter.
C. Find the Region from the AWS::StackId pseudo parameter by using the Fn::Split intrinsic function.
D. Dynamically import the Region by referencing the relevant parameter in AWS Systems Manager Parameter Store.

---

**Question 96.** A company is creating an application that processes .csv files from Amazon S3. A developer has created an S3 bucket. The developer has also created an AWS Lambda function to process the .csv files from the S3 bucket. Which combination of steps will invoke the Lambda function when a .csv file is uploaded to Amazon S3? (Choose two.)

A. Create an Amazon EventBridge rule. Configure the rule with a pattern to match the S3 object created event.
B. Schedule an Amazon EventBridge rule to run a new Lambda function to scan the S3 bucket.
C. Add a trigger to the existing Lambda function. Set the trigger type to EventBridge. Select the Amazon EventBridge rule.
D. Create a new Lambda function to scan the S3 bucket for recently added S3 objects.
E. Add S3 Lifecycle rules to invoke the existing Lambda function.

---

**Question 97.** A developer is working on an ecommerce website. The developer wants to review server logs without logging in to each of the application servers individually. The website runs on multiple Amazon EC2 instances, is written in Python, and needs to be highly available. How can the developer update the application to meet these requirements with MINIMUM changes?

A. Rewrite the application to be cloud native and to run on AWS Lambda, where the logs can be reviewed in Amazon CloudWatch.
B. Set up centralized logging by using Amazon OpenSearch Service, Logstash, and OpenSearch Dashboards.
C. Scale down the application to one large EC2 instance where only one instance is recording logs.
D. Install the unified Amazon CloudWatch agent on the EC2 instances. Configure the agent to push the application logs to CloudWatch.

---

**Question 98.** A team is developing an application that is deployed on Amazon EC2 instances. During testing, the EC2 instances are unable to access an Amazon S3 bucket. Which steps should the team take to troubleshoot this issue? (Choose two.)

A. Check whether the policy that is assigned to the IAM role that is attached to the EC2 instances grants access to Amazon S3.
B. Check the S3 bucket policy to validate the access permissions for the S3 bucket.
C. Check whether the policy that is assigned to the IAM user that is attached to the EC2 instances grants access to Amazon S3.
D. Check the security groups that are assigned to the EC2 instances. Make sure that a rule is not blocking the access to Amazon S3.
E. Check the S3 Lifecycle policy to validate the permissions that are assigned to the S3 bucket.

---

**Question 99.** A company has an image storage web application that runs on AWS. The company hosts the application on Amazon EC2 instances. The Auto Scaling group acts as the target group for an Application Load Balancer (ALB) and uses an Amazon S3 bucket to store the images for sale. The company wants developers to develop a feature to test system requests. The feature will direct requests to a separate target group that hosts a new beta version of the application. Which solution will meet this requirement with the LEAST effort?

A. Create a new ALB. Update the ALB routing rule with a condition that looks for a cookie named version that has a value of beta. Update the test system code to use this cookie to test the beta version of the application.
B. Create a new ALB. Auto Scaling group, and target group for the beta version of the application. Use the alternate Route 53 record for the new ALB endpoint in the test system requests to test the beta version of the application.
C. Create a new Auto Scaling group and target group for the beta version of the application. Update the ALB routing rule with a condition that looks for a cookie named version that has a value of beta. Update the test system code to use this cookie to test the beta version of the application.
D. Create a new Auto Scaling group and target group for the beta version of the application. Use the CloudFront with Lambda@Edge to determine which specific request will go to the new ALB. Use the CloudFront endpoint in the test system requests to test the beta version of the application.

---

**Question 100.** A company is providing read access to objects in an Amazon S3 bucket for different customers. The company uses IAM permissions to restrict access to the S3 bucket. The customers can access only their own files. Due to a regulation requirement, the company needs to enforce encryption in transit for interactions with Amazon S3. Which solution will meet these requirements?

A. Add a bucket policy to the S3 bucket to deny S3 actions when the aws:SecureTransport condition is equal to false.
B. Add a bucket policy to the S3 bucket to deny S3 actions when the s3:x-amz-acl condition is equal to public-read.
C. Add an IAM policy to the IAM users to enforce the usage of the AWS SDK.
D. Add an IAM policy to the IAM users that allows S3 actions when the s3:x-amz-acl condition is equal to bucket-owner-read.

---

**Question 101.** A developer wants to use AWS Elastic Beanstalk to test a new version of an application in a test environment. Which deployment method offers the FASTEST deployment?

A. Immutable
B. Rolling
C. Rolling with additional batch
D. All at once

---

**Question 102.** A developer is updating several AWS Lambda functions and notices that all the Lambda functions share the same custom libraries. The developer wants to centralize all the libraries, update the libraries in a convenient way, and keep the libraries versioned. Which solution will meet these requirements with the LEAST development effort?

A. Create an AWS CodeArtifact repository that contains all the custom libraries.
B. Create a custom container image for the Lambda functions to save all the custom libraries.
C. Create a Lambda layer that contains all the custom libraries.
D. Create an Amazon Elastic File System (Amazon EFS) file system to store all the custom libraries.

---

**Question 103.** A company has a web application that runs on Amazon EC2 instances with a custom Amazon Machine Image (AMI). The application runs in the us-east-1 Region, and the company needs to deploy the application to the us-west-1 Region. An attempt to update the AWS CloudFormation stack in us-west-1 fails. An error message states that the AMI ID does not exist. A developer must resolve this error with a solution that uses the least amount of operational overhead. Which solution meets these requirements?

A. Change the AWS CloudFormation templates for us-east-1 and us-west-1 to use an AWS AMI. Relaunch the stack for both Regions.
B. Copy the custom AMI from us-east-1 to us-west-1. Update the AWS CloudFormation template for the us-west-1 stack to refer to AMI ID for the copied AMI. Relaunch the stack.
C. Create a new AWS CloudFormation template to launch the stack in us-west-1 with an AMI that is available in us-west-1.
D. Manually deploy the application outside AWS CloudFormation in us-west-1.

---

**Question 104.** A company is updating an application to move the backend of the application from Amazon EC2 instances to a serverless model. The application and the DB instance are deployed in a private subnet in a single VPC on AWS. The company needs to connect AWS Lambda functions to the DB instance. Which solution will meet these requirements?

A. Create Lambda functions inside the VPC with the AWSLambdaBasicExecutionRole policy attached to the Lambda execution role. Modify the RDS security group to allow inbound access from the Lambda security group.
B. Create Lambda functions inside the VPC with the AWSLambdaVPCAccessExecutionRole policy attached to the Lambda execution role. Modify the RDS security group to allow inbound access from the Lambda security group.
C. Create Lambda functions with the AWSLambdaBasicExecutionRole policy attached to the Lambda execution role. Create an interface VPC endpoint for Lambda functions. Create an interface endpoint policy to allow the lambda:InvokeFunction action from the Lambda function's Amazon Resource Name (ARN).
D. Create Lambda functions with the AWSLambdaVPCAccessExecutionRole policy attached to the Lambda execution role. Create an interface VPC endpoint for Lambda functions. Create an interface endpoint policy to allow the lambda:InvokeFunction action from the Lambda function's Amazon Resource Name (ARN).

---

**Question 105.** A software company is launching a multimedia application. The application will allow guest users to access sample content before the users decide if they want to create an account to gain full access. The company wants to implement an authentication process that can identify users who have already created an account. The company also needs to keep track of the number of guest users who eventually create an account. Which combination of steps will meet these requirements? (Choose two.)

A. Create an Amazon Cognito identity pool. Configure the identity pool to allow unauthenticated users. Exchange user tokens for temporary credentials that allow all users to assume a role.
B. Create an Amazon Cognito identity pool. Configure the identity pool to allow unauthenticated users. Exchange unique identity for temporary credentials that allow all users to assume a role.
C. Create an Amazon CloudFront distribution. Configure the distribution to allow unauthenticated users. Exchange user tokens for temporary credentials that allow all users to assume a role.
D. Create a role for unauthenticated users that allows access to only the sample content. Create a role for authenticated users that allows access to only the sample content.
E. Allow all users to access the sample content by default. Create a role for authenticated users that allows access to all content.

---

**Question 106.** A company stores its data in data tables in a series of Amazon S3 buckets. The company received an alert that customer credit card information may have been exposed in a data table on one of the company's public applications. A developer needs to identify all potential exposures within the application environment. Which solution will meet these requirements?

A. Use Amazon Athena to run a job on the S3 buckets that contain the affected data. Filter the findings by using the SensitiveData:S3Object/Financial finding type.
B. Use Amazon Macie to run a job on the S3 buckets that contain the affected data. Filter the findings by using the SensitiveData:S3Object/Financial finding type.
C. Use Amazon Macie to run a job on the S3 buckets that contain the affected data. Filter the findings by using the SensitiveData:S3Object/Personal finding type.
D. Use Amazon Athena to run a job on the S3 buckets that contain the affected data. Filter the findings by using the SensitiveData:S3Object/Personal finding type.

---

**Question 107.** An ecommerce website uses an AWS Lambda function and an Amazon RDS for MySQL database for an order fulfillment service. The service needs to return order confirmation immediately. During a marketing campaign that caused an increase in the number of orders, the website's operations team noticed errors for "too many connections" from Amazon RDS. However, the RDS DB cluster metrics are healthy, CPU metrics are fine, and memory metrics are still available. What should a developer do to resolve the issue?

A. Initialize the database connection outside the handler function. Increase the max_user_connections value on the parameter group of the DB cluster. Restart the DB cluster.
B. Initialize the database connection outside the handler function. Use RDS Proxy instead to connect to the DB cluster.
C. Use Amazon Simple Queue Service (Amazon SQS) FIFO queues to queue the orders. Ingest the orders into the database. Set the Lambda function's concurrency to a value that equals the number of available database connections.
D. Use Amazon Simple Queue Service (Amazon SQS) FIFO queues to queue the orders. Ingest the orders into the database. Set the Lambda function's concurrency to a value that is less than the number of available database connections.

---

**Question 108.** A social media application uses the AWS SDK for JavaScript on the frontend to get user credentials from AWS Security Token Service (AWS STS). The application stores its assets in an Amazon S3 bucket. The application serves its content by using an Amazon CloudFront distribution with the origin set to the S3 bucket. The current configuration has the application to make the SDK calls are stored in plaintext in a JSON file within the application code. The developer needs to implement a solution to get user credentials without having any credentials hardcoded in the application code. Which solution will meet these requirements?

A. Add a Lambda@Edge function to the distribution. Invoke the function on viewer request. Add permissions to the function's execution role to allow the function to access AWS STS. Move all SDK calls from the frontend into the function.
B. Add a CloudFront function to the distribution. Invoke the function on viewer request. Add permissions to the function's execution role to allow the function to access AWS STS. Move all SDK calls from the frontend into the function.
C. Add a Lambda@Edge function to the distribution. Invoke the function on viewer request. Move the credentials from the JSON file into the function. Move all SDK calls from the frontend into the function.
D. Add a CloudFront function to the distribution. Invoke the function on viewer request. Move the credentials from the JSON file into the function. Move all SDK calls from the frontend into the function.

---

**Question 109.** A developer is creating an application. New users of the application must be able to create an account and register by using their own social media accounts. Which AWS service or resource should the developer use to meet these requirements?

A. IAM role
B. Amazon Cognito identity pools
C. Amazon Cognito user pools
D. AWS Directory Service

---

**Question 110.** A company uses AWS Lambda functions and an Amazon S3 trigger to process images into an S3 bucket. A recent production deployment, the development team observed that the development S3 buckets invoked the production environment Lambda functions. These invocations caused unwanted execution of development S3 files by using production Lambda functions. The development team must follow security best practices. Which solution will meet these requirements?

A. Update the Lambda execution role for the production Lambda function to add a policy that allows the execution role to read from only the production environment S3 bucket.
B. Move the development and production environments into separate AWS accounts. Add a resource policy to each Lambda function to allow only the production environment S3 bucket to invoke the function.
C. Add a resource policy to the production Lambda function to allow only the production environment S3 bucket to invoke the function.
D. Move the development and production environments into separate AWS accounts. Update the Lambda execution role for each function to add a policy that allows the execution role to read from the S3 bucket that is within the same account.

---

**Question 111.** A company has an AWS Lambda function that processes incoming requests from an Amazon API Gateway. The API call also invokes the Lambda function. A developer updates the Lambda function to handle more details related to the incoming requests. The developer wants to deploy the new Lambda function for more testing by other developers with no impact to customers that use the API. Which solution will meet these requirements with the LEAST operational overhead?

A. Create a new version of the Lambda function. Create a new stage on API Gateway with integration to the new Lambda version. Share the new API Gateway stage URL with the other developers for testing.
B. Update the existing Lambda alias used by API Gateway integration request to use the hotfix alias. Deploy the API Gateway to a new stage. Share the new API Gateway stage URL with the other developers for testing.
C. Create a new version of the Lambda function. Create and deploy a second Lambda function to filter incoming requests. The filtering Lambda function will invoke the new Lambda version of the code. For other requests, the filtering Lambda function will invoke the old Lambda version.
D. Modify the Lambda function by fixing the code. Test the Lambda function. Create the alias hotfix. Point the alias to the new Lambda version. Deploy the API Gateway to a new stage. Share the new API Gateway stage URL with the other developers for testing.

---

**Question 112.** A developer is creating an AWS Lambda function in VPC mode. An Amazon S3 event will invoke the Lambda function when an object is added to an S3 bucket. All Lambda resources must have access to the result files and log file. Each log entry must also be appended to the same shared log file. The developer needs a solution that uses the LEAST number of AWS services. Which solution should the developer use to meet these requirements?

A. Create an Amazon Elastic File System (Amazon EFS) file system. Mount the EFS file system in the Lambda function. Update the Lambda function code to download the log file, append the log entries, and upload the log file to the mount point.
B. Create an Amazon Elastic Block Store (Amazon EBS) volume. Multi-Attach enabled volume. Attach the EBS volume to all Lambda functions. Update the Lambda function code to download the log file, append the log entries, and upload the log file.
C. Create a reference to the /tmp local directory. Store the result files and log file by using the directory reference. Append the log entry to the log file.
D. Create a reference to the /opt storage directory. Store the result files and log file by using the directory reference. Append the log entry to the log file.

---

**Question 113.** A developer has designed an application to store incoming data as JSON files in Amazon S3 objects. A custom business logic in an AWS Lambda function then transforms the objects, and the Lambda function loads the data into an Amazon DynamoDB table. Recently, the workload has experienced sudden and significant changes in traffic. The flow of data to the DynamoDB table is becoming throttled. The developer needs to implement a solution to eliminate the throttling and load the data into the DynamoDB table consistently. Which solution will meet these requirements?

A. Refactor the Lambda function into two functions. Configure one function to transform the data and one function to load the data into DynamoDB. Create an Amazon Simple Queue Service (Amazon SQS) queue in between the functions to hold the items as messages and to invoke the second function.
B. Turn on auto scaling for the DynamoDB table. Use Amazon CloudWatch to monitor the table's read and write capacity metrics and to track consumed capacity.
C. Create an alias for the Lambda function. Configure provisioned concurrency for the application to use. Use Amazon CloudWatch to monitor the Lambda function invocations.
D. Refactor the Lambda function into two functions. Configure one function to store the data in the DynamoDB table. Configure the second function to process the data and update the items after the data is stored. Create a DynamoDB stream to invoke the second function after the data is stored.

---

**Question 114.** A developer has a subscribed to the Amazon Simple Notification Service (Amazon SNS) topic for image uploads. A service will upload an image to an S3 bucket for image uploads. Each time an image is uploaded, the service needs to send an email notification and create the thumbnail. The developer needs to configure the image processing and email notifications setup. Which solution will meet these requirements?

A. Create an Amazon Simple Notification Service (Amazon SNS) topic. Configure S3 event notifications with a destination of the SNS topic. Subscribe the Lambda function to the SNS topic. Create an email notification subscription to the SNS topic.
B. Create an Amazon Simple Notification Service (Amazon SNS) topic. Configure S3 event notifications with a destination of the SNS topic. Subscribe the Lambda function to the SNS topic. Create an Amazon Simple Queue Service (Amazon SQS) queue. Subscribe the SQS queue to the SNS topic. Create an email notification subscription to the SQS queue.
C. Create an Amazon Simple Queue Service (Amazon SQS) queue. Configure S3 event notifications with a destination of the SQS queue. Subscribe the Lambda function to the SQS queue. Create an email notification subscription to the SQS queue.
D. Create an Amazon Simple Queue Service (Amazon SQS) queue. Send S3 event notifications to Amazon EventBridge. Create an EventBridge rule that runs a Lambda function when images are uploaded to the S3 bucket. Create an email notification subscription to the SQS queue. Create an EventBridge rule that sends notifications to the SQS queue.

---

**Question 115.** A developer is leveraging a Border Gateway Protocol (BGP)-based AWS VPN connection to connect from on-premises to Amazon EC2 instances in the developer's account. The developer is able to access an EC2 instance in subnet A, but is unable to access an EC2 instance in subnet B in the same VPC. Which logs can the developer use to verify whether the traffic is reaching subnet B?

A. VPN logs
B. BGP logs
C. VPC Flow Logs
D. AWS CloudTrail logs

---

**Question 116.** A developer has written an application that runs on Amazon EC2 instances. The developer is adding functionality for the application to write objects to an Amazon S3 bucket. Which policy must the developer modify to allow the instances to write these objects?

A. The IAM policy that is attached to the EC2 instance profile role
B. The session policy that is applied to the EC2 instance role session
C. The AWS Key Management Service (AWS KMS) key policy that is attached to the EC2 instance profile role
D. The Amazon VPC endpoint policy

---

**Question 117.** A developer is building an application that uses Amazon DynamoDB. The developer wants to retrieve multiple specific items from the database with a single API call. Which DynamoDB API call will meet these requirements with the MINIMUM impact on the database?

A. BatchGetItem
B. GetItem
C. Scan
D. Query

---

**Question 118.** An e-commerce web application that shares session state on-premises is being migrated to AWS. The application must be fault tolerant, natively highly scalable, and any service interruption should not affect the user experience. What is the best option to store the session state?

A. Store the session state in Amazon ElastiCache.
B. Store the session state in Amazon CloudFront.
C. Store the session state in Amazon S3.
D. Enable session stickiness using elastic load balancers.

---

**Question 119.** A company needs to design a plan for a web service application. The application will provide a REST endpoint that clients can call. Where possible, the application should use caching features provided by AWS to limit the number of requests to the backend service. The application backend will receive a small amount of traffic only. Which approach should the developer take to provide the REST endpoint MOST efficiently?

A. Create a container image. Deploy the application to Amazon Elastic Kubernetes Service (Amazon EKS). Expose the AWS Lambda functionality by using Amazon API Gateway.
B. Create an AWS Lambda function by using the AWS Serverless Application Model (AWS SAM). Expose the Lambda functionality by using Amazon API Gateway.
C. Create a container image. Deploy the application to Amazon Elastic Container Service (Amazon ECS). Expose the AWS Lambda functionality by using Amazon API Gateway.
D. Create a microservices application. Deploy the application to AWS Elastic Beanstalk. Expose the application using an Application Load Balancer.

---

**Question 120.** A company moved some of its secure files to a private Amazon S3 bucket that has no public access. The company wants to develop a serverless application that gives its employees the ability to log in and securely share the files with other users. Which AWS feature should the company use to share and access the files securely?

A. Amazon Cognito user pool
B. S3 presigned URLs
C. S3 bucket policy
D. Amazon Cognito identity pool

---

**Question 121.** A company is using an Amazon API Gateway REST API endpoint as a webhook to publish events from an on-premises source control management (SCM) system to Amazon EventBridge. The company has configured an EventBridge rule to listen for the events and to control application deployment in a central AWS account. The company needs to receive the same events across multiple receiver AWS accounts. How can a developer meet these requirements without changing the configuration of the SCM system?

A. Deploy the API Gateway REST API to all the required AWS accounts. Use the same custom domain name for all the gateway APIs so that a single SCM webhook can be used for all accounts. Create as many SCM webhooks as the number of AWS accounts.
B. Deploy the API Gateway REST API to all the receiver AWS accounts so that a single SCM webhook can be used for all accounts. Create as many SCM webhooks as the number of AWS accounts.
C. Grant permission to the central AWS account for EventBridge to access the receiver AWS accounts. Add an EventBridge event bus on the receiver AWS accounts as the targets to the existing EventBridge rule.
D. Convert the API Gateway type from REST to HTTP API.

---

**Question 122.** A company caches session information for a web application in an Amazon DynamoDB table. The company wants an automated way to delete old items from the table. What is the simplest way to do this?

A. Write a script that deletes old records; schedule the script as a cron job on an Amazon EC2 instance.
B. Add an attribute with the expiration time; enable the Time To Live feature based on that attribute.
C. Each day, create a new table to hold session data; delete the previous day's table.
D. Add an attribute with the expiration time; name the attribute ItemExpiration.

---

**Question 123.** A company's new mobile app uses Amazon API Gateway. As the development team completes a new release of its APIs, a developer must safely and transparently roll out the API change. What is the SIMPLEST solution for the developer to use for rolling out the new API version to a limited number of users through API Gateway?

A. Create a new API in API Gateway. Direct a portion of the traffic to the new API using an Amazon Route 53 weighted routing policy.
B. Validate the new API version and promote it to production during the window of lowest expected utilization.
C. Implement an Amazon CloudWatch alarm to trigger a rollback if the observed HTTP 500 status code rate exceeds a predetermined threshold.
D. Use the canary deployment option in API Gateway. Direct a percentage of the API traffic using the canarySettings setting.

---

**Question 124.** A developer is implementing an AWS Cloud Development Kit (AWS CDK) serverless application. The developer will provision several AWS Lambda functions and Amazon API Gateway APIs during AWS CloudFormation stack creation. The developer's workstation has the AWS Serverless Application Model (AWS SAM) and the AWS CDK installed locally. How can the developer test a specific Lambda function locally?

A. Run the sam package and sam deploy commands. Create a Lambda test event from the AWS Management Console. Test the Lambda function.
B. Run the cdk synth and cdk deploy commands. Create a Lambda test event from the AWS Management Console. Test the Lambda function.
C. Run the cdk synth and sam local invoke commands with the function construct identifier and the path to the synthesized CloudFormation template.
D. Run the cdk synth and sam local start-lambda commands with the function construct identifier and the path to the synthesized CloudFormation template.

---

**Question 125.** A company has a web application that is deployed on AWS. The application uses an Amazon API Gateway and an AWS Lambda function as its backend. The application recently demonstrated an unexpected behavior. A developer examines the Lambda function code, finds an error, and modifies the code to resolve the problem. Before deploying the changes to production, the developer needs to create a new development environment to test the code changes. The developer must also prevent other developers from overwriting the code changes during the test cycle. Which combination of steps will meet these requirements with the LEAST development effort? (Choose two.)

A. Create a new stage in the current stage. Create a new method with Lambda proxy integration. Select the Lambda function. Test the backend.
B. Update the Lambda function in the API Gateway API integration request to use the hotfix alias. Deploy the API Gateway to a new stage. Add a resource and method with Lambda integration. Test the backend.
C. Modify the Lambda function by fixing the code. Test the Lambda function. Create the alias hotfix. Point the alias to the new version. Deploy the API Gateway to a new stage. Point the alias to the new version.
D. Create a new API Gateway API for the development environment. Add a resource and method with Lambda integration. Test the backend.
E. Create a new version of the Lambda function. Create the alias hotfix. Point the alias to the new version. Deploy the API Gateway to a new stage. Point the alias to the new version.

---

**Question 126.** A developer is creating a Ruby application and needs to automate the deployment, scaling, and management of an environment without requiring knowledge of the underlying infrastructure. Which service would best accomplish this task?

A. AWS CodeDeploy
B. AWS CloudFormation
C. AWS OpsWorks
D. AWS Elastic Beanstalk

---

**Question 127.** A developer has created an AWS Lambda function to provide notification through Amazon Simple Notification Service (Amazon SNS) whenever a file is uploaded to Amazon S3 that is larger than 50 MB. The developer has deployed and tested the Lambda function by using the CLI. However, when the event notification is added to the S3 bucket and a 3,000 MB file is uploaded, the Lambda function does not launch. Which of the following is a possible reason for the Lambda function's inability to launch?

A. The S3 event notification does not activate for files that are larger than 1,000 MB.
B. The resource-based policy for the Lambda function does not have the required permissions to be invoked by Amazon S3.
C. Lambda functions cannot be invoked directly from an S3 event.
D. The S3 bucket needs to be made public.

---

**Question 128.** A developer is building a highly secure healthcare application using serverless components. This application requires writing temporary data to /tmp storage on an AWS Lambda function. How should the developer encrypt this data?

A. Enable Amazon EBS volume encryption with an AWS KMS key in the Lambda function configuration so that all storage attached to the Lambda function is encrypted.
B. Set up the Lambda function with a role and key policy to access an AWS KMS key. Use the key to generate a data key used to encrypt all data prior to writing to /tmp storage.
C. Use OpenSSL to generate a symmetric encryption key on Lambda startup. Use this key to encrypt the data prior to writing to /tmp.
D. Use an on-premises hardware security module (HSM) to generate keys, where the Lambda function requests a data key from the HSM and uses that to encrypt data on all requests to the function.

---

**Question 129.** A company hosts a batch processing application on AWS Elastic Beanstalk with instances that run the most recent version of Amazon Linux. The application sorts and processes large datasets. In recent weeks, the application's performance has decreased significantly during a peak period for traffic. A developer suspects that the application issues are related to the memory usage. The developer checks the Elastic Beanstalk console and notices that memory usage is not being tracked. How should the developer gather more information about the application performance issues?

A. Configure the Amazon CloudWatch agent to push logs to Amazon CloudWatch Logs by using port 443.
B. Configure the Elastic Beanstalk .ebextensions directory to track the memory usage of the instances.
C. Configure the Amazon CloudWatch agent to track the memory usage of the instances.
D. Configure an Amazon CloudWatch dashboard to track the memory usage of the instances.

---

**Question 130.** A company is planning to use AWS CodeDeploy to deploy an application to Amazon Elastic Container Service (Amazon ECS). During the deployment of a new version of the application, the company initially must expose only 10% of live traffic to the new version of the deployed application. Then, after 15 minutes elapses, the company must route all the remaining live traffic to the new version of the application. Which CodeDeploy predefined configuration will meet these requirements?

A. CodeDeployDefault.ECSCanary10Percent15Minutes
B. CodeDeployDefault.LambdaCanary10Percent5Minutes
C. CodeDeployDefault.LambdaCanary10Percent15Minutes
D. CodeDeployDefault.ECSLinear10PercentEvery1Minutes

---

**Question 131.** A developer wants to debug an application by searching and filtering log data. The application logs are stored in Amazon CloudWatch Logs. The developer creates a new metric filter to count exceptions in the application logs. However, no results are returned from the logs. What is the reason that no filtered results are being returned?

A. A setup of the Amazon CloudWatch interface VPC endpoint is required for filtering the CloudWatch Logs in the VPC.
B. CloudWatch Logs only publishes metric data for events that happen after the filter is created.
C. The log group for CloudWatch Logs should first be streamed to Amazon OpenSearch Service before metric filtering returns the results.
D. Metric data points for logs groups can be filtered only after they are exported to an Amazon S3 bucket.

---

**Question 132.** Company A has an S3 bucket containing premier content that they intend to make available to only paid subscribers of their website. The S3 bucket currently has default permissions of all objects being private to prevent inadvertent exposure of the premier content to non-paying website visitors. How can Company A provide only-paid subscribers the ability to download a premier content file in the S3 bucket?

A. Apply a bucket policy that grants anonymous users to download the content from the S3 bucket
B. Generate a pre-signed object URL for the premier content file when a paid subscriber requests a download
C. Add a bucket policy that requires Multi-Factor Authentication for requests to access the S3 bucket objects
D. Enable server side encryption on the S3 bucket for data protection against the non-paying website visitors

---

**Question 133.** An application under development is required to store hundreds of video files. The data must be encrypted within the application prior to storage, with a unique key for each video file. How should the developer code the application?

A. Use the KMS Encrypt API to encrypt the data. Store the encrypted data key and data.
B. Use a cryptography library to generate an encryption key for the application. Use the encryption key to encrypt the data. Store the encrypted data.
C. Use the KMS GenerateDataKey API to get a data key. Encrypt the data with the data key. Store the encrypted data key and data.
D. Upload the data to an S3 bucket using server side-encryption with an AWS KMS key.

---

**Question 134.** A developer deployed an application to an Amazon EC2 instance. The application needs to know the public IPv4 address of the instance. How can the application find this information?

A. Query the instance metadata from http://169.254.169.254/latest/meta-data/.
B. Query the instance user data from http://169.254.169.254/latest/user-data/.
C. Query the Amazon Machine Image (AMI) information from http://169.254.169.254/latest/meta-data/ami/.
D. Check the hosts file of the operating system.

---

**Question 135.** A developer is writing unit tests for a new application that will be deployed on AWS. The developer wants to validate all the code with unit tests and merge the code with the main branch only when all tests pass. The developer stores the code in AWS CodeCommit and sets up AWS CodeBuild to run the unit tests. The developer needs to identify the CodeCommit event that can invoke the Lambda function to start the CodeBuild task. The developer needs to identify the CodeCommit event that can invoke the Lambda function when a pull request is created or updated. Which CodeCommit event will meet these requirements?

A. `{"detail-type": ["CodeCommit Pull Request State Change"], "detail": {"event": ["pullRequestStatusUpdated"]}}`
B. `{"detail-type": ["CodeCommit Pull Request State Change"], "detail": {"event": ["pullRequestCreated"]}}`
C. `{"detail-type": ["CodeCommit Pull Request State Change"], "detail": {"event": ["pullRequestSourceBranchUpdated", "pullRequestCreated"]}}`
D. `{"detail-type": ["CodeCommit Pull Request State Change"], "detail": {"event": ["pullRequestSourceBranchUpdated"]}}`

---

**Question 136.** A developer created an AWS Lambda function that accesses resources in a VPC. The Lambda function polls an Amazon Simple Queue Service (Amazon SQS) queue for new messages through a VPC endpoint. Then the function calculates a rolling average of the numeric values that are contained in the messages. After initial tests of the Lambda function, the developer found that the value of the rolling average stored in the function's reserved concurrency was inaccurate. How can the developer ensure the function calculates an accurate rolling average?

A. Set the function's reserved concurrency to 1. Calculate the rolling average in the function. Store the calculated rolling average in Amazon ElastiCache. When the function initializes, use the previous values from the cache to calculate the rolling average.
B. Set the function's provisioned concurrency to 1. Calculate the rolling average in the function. Store the calculated rolling average in Amazon ElastiCache. When the function initializes, use the previous values from the cache to calculate the rolling average.
C. Set the function's reserved concurrency to 1. Calculate the rolling average in the function. Store the calculated rolling average in Amazon ElastiCache. When the function initializes, use the previously stored values to calculate the rolling average.
D. Modify the function to store the values in the function's layers. When the function initializes, use the previously stored values to calculate the rolling average.

---

**Question 137.** A company runs an application on AWS. The company deployed the application on Amazon EC2 instances. The application stores data on Amazon Aurora. The application recently logged multiple application-specific custom DECRYP_ERROR errors to Amazon CloudWatch Logs. The company did not detect the issue until the automated tests that run every 30 minutes failed. A developer must implement a solution that will monitor for the custom errors and notify a development team in real time when these errors occur in the production environment. Which solution will meet these requirements with the LEAST operational overhead?

A. Configure the application to create a custom metric and to push the metric to CloudWatch. Create an AWS CloudWatch alarm. Use an Amazon Simple Notification Service (Amazon SNS) topic to send a notification.
B. Create an AWS Lambda function to run every 5 minutes to scan the CloudWatch logs for the keyword DECRYP_ERROR. Create a CloudWatch alarm. Use an Amazon Simple Notification Service (Amazon SNS) topic to send a notification.
C. Use Amazon CloudWatch Logs that has a filter pattern for DECRYP_ERROR. Create a CloudWatch alarm that has a threshold >1. Configure the alarm to send Amazon Simple Notification Service (Amazon SNS) notifications.
D. Install the Amazon CloudWatch unified agent on the EC2 instance. Configure the application to generate a metric for the DECRYP_ERROR keyword. Configure the agent to send Amazon Simple Notification Service (Amazon SNS) notifications.

---

**Question 138.** A developer creates a VPC named VPC-A that has public and private subnets. The developer also creates an Amazon RDS database inside the private subnet of VPC-A. To perform some queries, the developer creates an AWS Lambda function in the default VPC. The Lambda function has code to access the RDS database. When the Lambda function runs, an error message indicates that the function cannot connect to the RDS database. How should the developer solve this problem?

A. Modify the RDS security group. Add a rule to allow all traffic from the VPC CIDR block.
B. Redeploy the Lambda function in the same subnet as the RDS instance. Ensure that the RDS security group allows traffic from the new Lambda security group.
C. Create a security group for the Lambda function. Add a new rule in the RDS security group to allow traffic from the new Lambda security group.
D. Create an IAM role. Attach a policy that allows access to the RDS database. Attach the role to the Lambda function.

---

**Question 139.** A developer is working on an existing application that uses Amazon DynamoDB as its data store. The DynamoDB table has the following attributes: partNumber (partition key), vendor (sort key), description, productFamily, and productType. The developer analyzes the usage patterns and notices that there are application modules that frequently look for a list of products based on the productFamily and productType attributes. The developer wants to make changes to the application to improve performance of the query operations. Which solution will meet these requirements?

A. Create a global secondary index (GSI) with productFamily as the partition key and productType as the sort key.
B. Create a local secondary index (LSI) with productFamily as the partition key and productType as the sort key.
C. Recreate the table. Add partNumber as the partition key and vendor as the sort key. During table creation, add a local secondary index (LSI) with productFamily as the partition key and productType as the sort key.
D. Update the queries to use Scan operations with productFamily as the partition key and productType as the sort key.

---

**Question 140.** An engineer created an A/B test of a new feature on an Amazon CloudWatch Evidently project. The engineer configured two variations of the feature (Variation A and Variation B) for the test. The engineer wants to work exclusively with Variation A. The engineer needs to make updates so that Variation A is the only variation that appears when the engineer hits the application's endpoint. Which solution will meet this requirement?

A. Add an override to the feature. Set the identifier of the override to the engineer's user ID. Set the variation to Variation A.
B. Add an override to the feature. Set the identifier of the override to Variation A. Set the variation to 100%.
C. Add an experiment to the project. Set the identifier of the experiment to Variation B. Set the variation to 0%.
D. Add an experiment to the project. Set the identifier of the experiment to the AWS account's account ID. Set the variation to Variation A.

---

**Question 141.** A developer is configuring an application's deployment environment in AWS CodePipeline. The application code is stored in a GitHub repository. The developer wants to ensure that the repository package's unit tests run in the new deployment environment. The developer has already set the pipeline's source stage to GitHub and has specified the repository and branch to use in the deployment. Which combination of steps should the developer take next to meet these requirements with the LEAST overhead? (Choose two.)

A. Create an AWS CodeCommit project. Add the repository package's build and test commands to the project's buildspec.
B. Create an AWS CodeBuild project. Add the repository package's build and test commands to the project's buildspec.
C. Create an AWS CodeDeploy project. Add the repository package's build and test commands to the project's buildspec.
D. Add an action to the source stage. Specify the newly created project as the action provider. Specify the build artifact as the action's input artifact.
E. Add a new stage to the pipeline after the source stage. Add an action to the new stage. Specify the newly created project as the action provider. Specify the source artifact as the action's input artifact.

---

**Question 142.** A developer is creating a mobile application that will not require users to log in. What is the MOST efficient method to grant users access to AWS resources?

A. Use an identity provider to securely authenticate with the application.
B. Create an AWS Lambda function to create an IAM user when a user accesses the application.
C. Create credentials using AWS KMS and apply these credentials to users when using the application.
D. Use Amazon Cognito to associate unauthenticated users with an IAM role that has limited access to resources.

---

**Question 143.** A company is building a serverless application that uses AWS Lambda functions. The company needs to create a set of test events to test Lambda functions in a development environment. The test events will be created once and then will be used by all the developers in an IAM developer group. The test events must be editable by any of the IAM users in the IAM developer group. Which solution will meet these requirements?

A. Create and store the test events in Amazon S3 as JSON objects. Allow S3 bucket access to all IAM users.
B. Create the test events. Configure the event sharing settings to make the test events shareable.
C. Create and store the test events in Amazon DynamoDB. Allow access to DynamoDB by using IAM roles.
D. Create the test events. Configure the event sharing settings to make the test events private.

---

**Question 144.** A company has installed smart meters in all its customer locations. The smart meters measure power usage at 1-minute intervals and send the usage readings to a remote endpoint for collection. The company needs to create an endpoint that will receive the smart meter readings and store the location ID and timestamp information. The company wants to store the information and also retrieve readings based on location ID and timestamp. The company expects demand to increase significantly. The solution must not impact performance or include downtime. Which solution will meet these requirements MOST cost-effectively?

A. Store the smart meter readings in an Amazon RDS database. Create an index on the location ID and timestamp columns. Use the columns to filter on the customers' data.
B. Store the smart meter readings in an Amazon DynamoDB table. Create a composite key by using the location ID and timestamp columns. Use the columns to filter on the customers' data.
C. Store the smart meter readings in Amazon ElastiCache for Redis using a SortedSet key structure by using the location ID and timestamp columns. Use the columns to filter on the customers' data.
D. Store the smart meter readings in Amazon S3. Partition the data by using the location ID and timestamp columns. Use Amazon Athena to filter on the customers' data.

---

**Question 145.** A company has a critical application on AWS. The application exposes an HTTP API by using Amazon API Gateway. The API is integrated with an AWS Lambda function. The application uses an Amazon RDS for MySQL DB instance with 2 virtual CPUs (vCPUs) and 64 GB of RAM. Customers have reported that the API calls return errors for "too many connections." The errors occur during peak usage times that are unpredictable. The company needs to make the application resilient. The database cannot be down outside of scheduled maintenance hours. Which solution will meet these requirements?

A. Decrease the number of vCPUs for the DB instance. Increase the max_connections setting.
B. Use RDS Proxy to create a proxy that connects to the DB instance. Update the Lambda function to connect to the proxy.
C. Add a CloudWatch alarm that increases the DB instance class when the number of connections is more than 1,000.
D. Add an Amazon EventBridge rule that increases the max_connections setting of the DB instance when CPU utilization is above 75%.

---

**Question 146.** A developer is building a new application on AWS. The application uses an AWS Lambda function that retrieves information from an Amazon DynamoDB table. The developer hard coded the DynamoDB table name into the Lambda function code. The table name might change over time. The developer does not want to modify the Lambda code if the table name changes. Which solution will meet these requirements MOST efficiently?

A. Create a Lambda environment variable to store the table name. Use the standard method for the programming language to retrieve the variable.
B. Store the table name in a file. Store the file name in the /tmp folder. Use the SDK for the programming language to retrieve the table name.
C. Create a file to store the table name. Zip the file and upload the file to the Lambda layer. Use the SDK for the programming language to retrieve the table name.
D. Create a global variable that is outside the handler in the Lambda function to store the table name.

---

**Question 147.** A developer is migrating some features from a legacy monolithic application to use AWS Lambda functions instead. The application currently stores data in an Amazon Aurora DB cluster that runs in private subnets in a VPC. The AWS account has one VPC deployed. The Lambda functions and the DB cluster are deployed in the same AWS Region in the same AWS account. The developer needs to ensure that the Lambda functions can securely access the DB cluster without crossing the public internet. Which solution will meet these requirements?

A. Configure the DB cluster's public access setting to Yes.
B. Configure an Amazon RDS database proxy for the Lambda functions.
C. Configure a NAT gateway and a security group for the Lambda functions.
D. Configure the VPC, subnets, and a security group for the Lambda functions.

---

**Question 148.** A developer is incorporating AWS X-Ray into an application that handles personal identifiable information (PII). The application is hosted on Amazon EC2 instances. The application trace messages include encrypted PII and go to Amazon CloudWatch. The developer needs to ensure that no PII goes outside of the EC2 instances. Which solution will meet these requirements?

A. Manually instrument the X-Ray SDK in the application code.
B. Use the X-Ray auto-instrumentation agent.
C. Use Amazon Macie to detect and hide PII. Call the X-Ray API from AWS Lambda.
D. Use AWS Distro for Open Telemetry.

---

**Question 149.** A company has deployed an application on AWS Elastic Beanstalk. The company has configured the Auto Scaling group that is associated with the Elastic Beanstalk environment to have five Amazon EC2 instances. If the capacity is fewer than four EC2 instances during the deployment, application performance degrades. The company is using the all-at-once deployment policy. What is the MOST cost-effective way to solve the application performance issue?

A. Change the Auto Scaling group to six desired instances.
B. Change the deployment policy to traffic splitting. Specify an evaluation time of 1 hour.
C. Change the deployment policy to rolling with additional batch. Specify a batch size of 1.
D. Change the deployment policy to rolling. Specify a batch size of 2.

---

**Question 150.** A company is building a web application on AWS. When a customer sends a request, the application will generate reports and then make the reports available to the customer within one hour. Reports should be accessible to the customer for 8 hours. Some reports are larger than 1 MB. Each report is unique to the customer. The application should delete all reports that are older than 2 days. Which solution will meet these requirements with the LEAST operational overhead?

A. Generate the reports and then store the reports as Amazon DynamoDB items that have a specified TTL. Generate a URL that retrieves the reports from DynamoDB. Provide the URL to customers through the web application.
B. Generate the reports and then store the reports in an Amazon S3 bucket that uses server-side encryption. Attach the report to the S3 bucket. Generate a presigned URL that contains an expiration date. Provide the URL to customers through the web application.
C. Generate the reports and then store the reports in an Amazon S3 bucket that uses server-side encryption. Generate a presigned URL that contains an expiration date. Provide the URL to customers through the web application. Add an S3 Lifecycle policy to delete records that are older than 2 days.
D. Generate the reports and then store the reports in an Amazon RDS database with a date stamp. Provide the URL to customers through the web application. Schedule an hourly AWS Lambda function to delete database records that have expired date stamps.

---
