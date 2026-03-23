# CodeSignal Test 4 - Questions

---

**Question 1.** A developer wants to perform additional processing on newly-inserted items in Amazon DynamoDB using AWS Lambda. In order to implement this requirement, the developer will have to use DynamoDB Streams to automatically send the new items to a Lambda table for processing.

Given the scenario, what steps should be performed by the developer to implement this to his/her Lambda functions? (Select TWO.)

A. Create a trigger for a Firehose stream that uses a Lambda function for data processing.
B. Create an SNS topic to capture new records from DynamoDB.
C. Select AWSLambdaBasicExecutionRole managed policy as the function's execution role.
D. Create an event source mapping in Lambda to send records from your stream to a Lambda function.
E. Select AWSLambdaDynamoDBExecutionRole managed policy as the function's execution role.

---

**Question 2.** You currently have an IAM user for working in the development environment using shell scripts that call the AWS CLI. The EC2 instance that you are using already contains the access key credential set and an IAM role, which are used to run the CLI and access the development environment. You were given a new set of access credentials for a new IAM role that allows you to access and manage the production environment.

Which of the following is the EASIEST way to switch from one role to another?

A. Store the production access key credentials set in the user data of the instance and call this whenever you need to access the production environment.
B. Create a new profile for the role in the AWS CLI configuration file then append the --profile parameter along with the new profile name, whenever you run the CLI command.
C. Create a new instance profile in the AWS CLI configuration file then append the --profile parameter along with the new profile name, whenever you run the CLI command.
D. Store the production access key credentials set in the instance metadata and call this whenever you need to access the production environment.

---

**Question 3.** A web application is currently using an on-premises Microsoft SQL Server 2019 Enterprise Edition database. Your manager instructed you to migrate the application to Elastic Beanstalk and the database to RDS for SQL Server. For additional security, you must configure your database to automatically encrypt the actual data before it is written to storage, and automatically decrypt data when the data is read from storage.

Which of the following services will you use to achieve this?

A. Use IAM DB Authentication.
B. Enable RDS Encryption.
C. Enable Transparent Data Encryption (TDE).
D. Use Microsoft SQL Server Windows Authentication.

---

**Question 4.** You are developing an online game where the app preferences and game state of the player must be synchronized across devices. It should also allow multiple users to synchronize and collaborate shared data in real time.

Which of the following is the MOST appropriate solution that you should implement in this scenario?

A. Integrate AWS Amplify to your mobile app.
B. Integrate Amazon Cognito Sync to your mobile app.
C. Integrate Amazon Pinpoint to your mobile app.
D. Integrate AWS AppSync to your mobile app.

---

**Question 5.** A developer recently deployed a serverless application, which consists of a Lambda function, API Gateway, and DynamoDB using the sam deploy CLI command. The Lambda function is invoked through the API Gateway and then processes and stores the API Gateway data in a DynamoDB table with an average time of 20 minutes. However, there are a lot of discrepancies in the terminated Lambda invocations that happen every day, which is causing a decrease in performance.

Which of the following options is the MOST likely root cause of this problem?

A. The serverless application should be deployed using the sam publish CLI command instead.
B. The concurrent execution limit has been reached.
C. The Lambda function contains a recursive code and has been running for over 15 minutes.
D. The failed Lambda invocations have been running for over 15 minutes and reached the maximum execution time.

---

**Question 6.** A developer is utilizing AWS X-Ray to generate a visual representation of the requests flowing through their enterprise web application. Since the application interacts with multiple services, all requests must be traced in X-Ray, including any downstream calls made to AWS resources.

Which of the following actions should the developer perform in this scenario?

A. Use X-Ray SDK to generate segment documents with subsegments and send them to the X-Ray daemon, which will buffer them and upload to the X-Ray API in batches.
B. Install AWS X-Ray on the different services that communicate with the application including the AWS resources that the application calls.
C. Pass multiple trace segments as a parameter of PutTraceSegments API.
D. Use AWS X-Ray SDK to upload a trace segment by executing PutTraceSegments API.

---

**Question 7.** A company is in the process of integrating their on-premises data center to their cloud infrastructure in AWS. One of the requirements is to integrate the on-premises Lightweight Directory Access Protocol (LDAP) directory service to their AWS VPC using IAM.

Which of the following provides the MOST suitable solution to implement if the identity store that they are using is not compatible with SAML?

A. Implement the AWS IAM Identity Center service to manage access between AWS and your LDAP.
B. Set up an IAM policy that references the LDAP identifiers and AWS credentials.
C. Create IAM roles to rotate the IAM credentials whenever LDAP credentials are updated.
D. Create a custom Identity Broker Application in your on-premises data center and use STS to issue short-lived AWS credentials.

---

**Question 8.** A company uses AWS Systems Manager (SSM) Parameter Store to manage configuration details for multiple applications. The parameters are currently stored in the Standard tier. The company wants its operations team to be notified if there are sensitive parameters that haven't been rotated within 90 days.

Which must be done to meet the requirement?

A. Convert the sensitive parameters from Standard tier into Advanced tier. Set a NoChangeNotification policy with a value of 90 days. Use Amazon EventBridge (Amazon CloudWatch Events) to send a notification via Amazon SNS.
B. Configure a NoChangeNotification policy with a value of 90 days. Use Amazon EventBridge (Amazon CloudWatch Events) to send a notification via Amazon SNS.
C. Set up an Amazon EventBridge (Amazon CloudWatch Events) event pattern that captures SSM Parameter-related events. Use Amazon SNS to send notifications.
D. Convert the sensitive parameters from Standard tier into Advanced tier. Set a ExpirationNotification policy with a value of 90 days. Use Amazon EventBridge (Amazon CloudWatch Events) to send a notification via Amazon SNS.

---

**Question 9.** A developer is planning to build a serverless Rust application in AWS using AWS Lambda and Amazon DynamoDB. Much to his disappointment, AWS Lambda does not natively support the Rust programming language.

Can the developer still proceed with creating serverless Rust applications in AWS given the situation above?

A. Yes. The developer can submit a request ticket to AWS so that they can provide him a Lambda runtime environment that supports Rust.
B. Yes. The developer can create a custom runtime for Rust applications and bootstrap it to an AWS Lambda function.
C. Yes. The developer will just have to use AWS Fargate instead of AWS Lambda.
D. No. The developer will have to wait for a new support release in AWS Lambda.

---

**Question 10.** A product design firm has adopted a remote work policy and wants to provide employees with access to a suite of CAD applications through EC2 Spot Instances. These instances will be deployed using a CloudFormation template. The development team must be able to securely obtain software license keys in the template each time it is needed.

Which solution meets this requirement while offering the most cost-effective approach?

A. Embed the license keys in the Mapping section of the CloudFormation template. Let users choose the correct license key using the Parameter section. Enable the NoEcho attribute on the parameter.
B. Pass the license key in the Parameter section of the CloudFormation template during stack creation. Enable the NoEcho attribute on the parameter.
C. Store the license key as a SecureString in AWS Systems Manager (SSM) Parameter Store. Use the ssm-secure dynamic reference to retrieve the secret in the CloudFormation template.
D. Store the license key as a secret in AWS Secrets Manager. Use the secretsmanager dynamic reference to retrieve the secret in the CloudFormation template.

---

**Question 11.** A developer is planning to add a global secondary index in a DynamoDB table. This will allow the application to query a specific item that can span all of the data in the base table, across all partitions.

Which of the following should the developer consider when using this type of index? (Select TWO.)

A. Queries or scans on this index consume capacity units from the index, not from the base table.
B. When you query this index, you can choose either eventual consistency or strong consistency.
C. Queries on this index support eventual consistency only.
D. Queries or scans on this index consume read capacity units from the base table.
E. For each partition key value, the total size of all indexed items must be 10 GB or less.

---

**Question 12.** A company is using a combination of CodeBuild, CodePipeline, and CodeDeploy services for its continuous integration and continuous delivery (CI/CD) pipeline on AWS. They want someone to perform a code review before a revision is allowed into the next stage of a pipeline. If the action is approved, the pipeline execution resumes, but if it is not, then the pipeline execution will not continue.

Which is the MOST suitable solution to implement in this scenario?

A. Implement a manual approval actions configuration in CodePipeline. Send the approval request to an SQS Queue.
B. Remodel the pipeline using AWS Serverless Application Model (AWS SAM).
C. Implement a manual approval actions configuration in CodePipeline. Send the approval request to an SNS Topic.
D. Split the processes into different Task states using Step Functions. Use a Wait state to set a timeout for approval.

---

**Question 13.** An Elastic Beanstalk application becomes inaccessible for several minutes whenever a failed deployment is rolled back. A developer should recommend a strategy that will have the least impact on the application's availability if the deployment fails. Teams must be able to revert changes quickly as well.

Which deployment method should the developer suggest?

A. Rolling with Additional Batches
B. Rolling
C. All at Once
D. Blue/Green

---

**Question 14.** A developer has a Node.js function running in AWS Lambda. Currently, the code initializes a database connection to an Amazon RDS database every time the Lambda function is executed, and closes the connection before the function ends.

What feature in AWS Lambda will allow the developer to reuse the already existing database connection instead of initializing it each time the function is run?

A. AWS Lambda is not capable of maintaining existing database connections due to its transient data store.
B. Execution context
C. Environment variables
D. Event source mapping

---

**Question 15.** A company is legally obligated to keep transaction records containing Personally Identifiable Information (PII) for a duration of five years. These records are stored in Amazon S3. To handle the data redaction, the company has developed Lambda functions with naming conventions starting as RedactPII-[role], which represents different roles. The company wants to provide varying levels of access based on each role so that only a single role only sees the necessary data. Only a single copy of the records should be maintained.

Which combination of actions will achieve the given requirements? (Select THREE.)

A. Create an S3 Access Point for each user role.
B. Use the GetObjectLegalHold API to retrieve the redacted data.
C. Set up S3 Replication for the bucket.
D. Set up an S3 event notification to invoke the corresponding RedactPII-[role] Lambda function in response to GET requests.
E. Use the GetObject API to retrieve the redacted data.
F. Configure an S3 Object Lambda Access Point for each S3 Access Point name. Associate the RedactPII-[role] Lambda functions with the corresponding S3 Object Lambda Access Point.

---

**Question 16.** A company has an application hosted in an ECS Cluster that heavily uses an RDS database. A developer needs to closely monitor how the different processes on a DB instance use the CPU, the percentage of the CPU bandwidth, and the total memory consumed by each process to ensure application performance.

Which of the following is the MOST suitable solution that the developer should implement?

A. Develop a shell script that collects and publishes custom metrics to CloudWatch which tracks the real-time CPU utilization of the RDS instance.
B. Track the CPUs and MEMs metrics which are readily available in the Amazon RDS console.
C. Use Enhanced Monitoring in RDS.
D. Use CloudWatch to track the CPU Utilization of your database.

---

**Question 17.** The infrastructure of an application is designed such that a producer sends data to a consumer via HTTPS. The consumer may sometimes take a while to process the messages and cause them not to be acknowledged immediately. This can result in unexpected timeouts and cause messages not to be processed. To resolve this issue, a developer discovers that duplicate messages are still not being processed properly.

What should the developer do to ensure that messages are durably delivered and prevent duplicate messages? (Select TWO.)

A. Use a delay queue.
B. Configure the producer to set deduplication IDs for the messages.
C. Increase the number of consumers polling from your standard queue.
D. Increase the timeout for the acknowledgement response.
E. Create a FIFO queue as a replacement for the standard queue.

---

**Question 18.** A developer is planning to use the AWS Elastic Beanstalk console to run the AWS X-Ray daemon on the EC2 instances in her application environment. She will use X-Ray to construct a service map to help identify issues with her application and provide insight on which application component to optimize. The environment is using a default Elastic Beanstalk instance profile.

Which IAM managed policy does Elastic Beanstalk use for the X-Ray daemon to upload data to X-Ray?

A. AWSXRayDaemonWriteAccess
B. AWSXRayFullAccess
C. AWSXRayElasticBeanstalkWriteAccess
D. AWSXRayReadOnlyAccess

---

**Question 19.** A web application hosted in Elastic Beanstalk has a configuration file named `.ebextensions/debugging.config` which has the following content:

```
option_settings:
  aws:elasticbeanstalk:xray:
    XRayEnabled: true
```

For its database test, it uses RDS with Multi-AZ deployment and Read Replicas. There is a new requirement to record calls that your application makes to internal and external HTTP web APIs. The tracing information should also include the actual SQL database queries made by the application, which can be searched using the filter expressions in the X-Ray Console.

Which of the following should you do to satisfy the above task?

A. Add metadata in the segment document.
B. Add metadata in the subsegment section of the segment document.
C. Add annotations in the segment document.
D. Add annotations in the subsegment section of the segment document.

---

**Question 20.** A financial mobile application has a serverless backend API which consists of DynamoDB, Lambda, and Cognito. Due to the confidential financial transactions handled by the mobile application, there is a new requirement to add a second authentication method that doesn't rely solely on user name and password.

Which of the following is the MOST suitable solution that the developer should implement?

A. Use Cognito with SNS to allow additional authentication via SMS.
B. Create a custom application that integrates with Amazon Cognito which implements the second layer of authentication.
C. Use a new IAM policy to a user pool in Cognito.
D. Integrate multi-factor authentication (MFA) to a user pool in Cognito to protect the identity of your users.

---

**Question 21.** You have two users concurrently accessing a DynamoDB table and submitting updates. If a user will modify a specific item in the table, she needs to make sure that the update operation will not affect another user's attempt to modify the same item. You have to ensure that your update operations will only succeed if the item attributes meet one or more expected conditions.

Which of the following DynamoDB features should you use in this scenario?

A. Projection Expressions
B. Conditional Writes
C. Update Expressions
D. Batch Operations

---

**Question 22.** A leading insurance firm is hosting its customer portal in Elastic Beanstalk, which has an RDS database in AWS. The support team in your company discovered a lot of SQL injection attempts and cross-site scripting attacks on the portal, which is starting to affect the production environment.

Which of the following services should you implement to mitigate this attack?

A. Network Access Control List
B. AWS WAF
C. Amazon GuardDuty
D. AWS Firewall Manager

---

**Question 23.** A company is transitioning their systems to AWS due to the limitations of their on-premises data center. As part of this project, a developer was assigned to build a brand-new serverless architecture in AWS, which will be composed of AWS Lambda, API Gateway, and DynamoDB in a single stack. She needs a simple and reliable architecture to define dependencies such as memory and timeouts between resources and deploy all related resources together as a single, versioned entity.

Which of the following is the MOST appropriate service that the developer should use in this scenario?

A. AWS CloudFormation
B. Serverless Application Framework
C. AWS SAM
D. AWS Systems Manager

---

**Question 24.** A company has a suite of web applications that is heavily using RDS database in Multi-AZ Deployments configuration with several Read Replicas. For improved security, you were instructed to ensure that all of their database credentials, API keys, and other secrets are encrypted and rotated on a regular basis. You should also configure your applications to use the latest version of the encrypted credentials when connecting to the RDS database.

Which of the following is the MOST appropriate solution to secure the credentials?

A. Store the credentials in AWS KMS.
B. Use AWS Secrets Manager to store and encrypt the credentials and enable automatic rotation.
C. Store the credentials to Systems Manager Parameter Store with a SecureString data type.
D. Store the credentials to AWS ACM.

---

**Question 25.** A developer is creating a new global secondary index on a provisioned mode DynamoDB table. Since the application will store large quantities of data, the write capacity units must be specified for the expected capacity on both the base table and its secondary index.

Which of the following should the developer do to avoid any potential request throttling?

A. Ensure that the global secondary index's provisioned RCU is equal or greater than the RCU of the base table.
B. Ensure that the global secondary index's provisioned WCU is equal or less than the WCU of the base table.
C. Ensure that the global secondary index's provisioned RCU is equal or less than the RCU of the base table.
D. Ensure that the global secondary index's provisioned WCU is equal or greater than the WCU of the base table.

---

**Question 26.** A developer is managing a real-time fraud detection system that ingests a stream of data using Amazon Kinesis. The system works well with millisecond end-to-end latency, but the allocated shards are way underutilized based on the performance data in CloudWatch.

Which of the following is the MOST suitable solution to reduce the cost and capacity of the stream?

A. Split cold shards
B. Split hot shards
C. Merge cold shards
D. Merge hot shards

---

**Question 27.** You are a newly hired developer at a leading investment bank which uses AWS as its cloud infrastructure. One of your tasks is to develop an application that will use an S3 bucket that has the following bucket policies (two policy statements — one denying uploads unless `x-amz-server-side-encryption` is `AES256`, and another using `StringEquals` with a value of `True`).

Which of the following statements is true about uploading data to this S3 bucket?

A. The bucket will deny object uploads unless the request includes the x-amz-server-side-encryption header with a value of AoI.
B. The bucket will deny object uploads unless the request includes the x-amz-server-side-encryption header with a value of aws:kms.
C. The bucket will deny object uploads unless the request includes the x-amz-server-side-encryption header with a value of AES3298.
D. The bucket will deny object uploads unless the request includes the x-amz-server-side-encryption header with a value of True.

---

**Question 28.** You are designing the DynamoDB table that will be used by your Node.js application. It will have to handle 10 writes per second and then 20 eventually consistent reads per second where all the items have a size of 2 KB for both operations.

Which of the following are the most optimal WCU and RCU that you should provision to the table?

A. 20 RCU and 20 WCU
B. 40 RCU and 40 WCU
C. 40 RCU and 20 WCU
D. 10 RCU and 20 WCU

---

**Question 29.** A company has assigned a developer to automate its department's patch management, data synchronization, and other recurring tasks. The developer needs a service to coordinate multiple AWS services into serverless workflows.

Which of the following is the MOST cost-effective service the developer should implement in this scenario?

A. AWS Elastic Beanstalk
B. AWS Lambda
C. AWS Batch
D. AWS Step Functions

---

**Question 30.** A developer must set up a caching layer in front of the tutorialapi database. The developer should come up with a function that ensures cached data is always up-to-date. Stale records in the cache must be automatically deleted as well to prevent the build-up of extra data.

Which pseudocode best represents this caching strategy?

A.
```
save_item(item_id, item_value):
  ttl = 900
  tutorialapi.query("UPDATE MYDB Customers SET value = %s WHERE id = %s", item_value, item_id)
  cache.set(item_id, item_value, 900)
  return 'ok'
```

B.
```
save_item(item_id, item_value):
  tutorialapi.query("SELECT * FROM MYDB Customers WHERE id = %s", item_id)
  cache.delete(item_id)
  return 'ok'
```

C.
```
save_item(item_id, item_value):
  ttl = 900
  cache.set(item_id, item_value, 900)
  return 'ok'
```

D.
```
save_item(item_id, item_value):
  ttl = 500
  tutorialapi.query("SELECT MYDB Customers WHERE id = %s", item_id)
  cache.delete(item_id, item_value, 500)
  return 'ok'
```

---

**Question 31.** A development team has recently completed building their serverless application. They must zip their code artifacts, upload them to Amazon S3, produce the package template file for deployment, and deploy it to AWS.

Which command is the MOST suitable to use to automate the deployment steps?

A. aws cloudformation deploy
B. sam package
C. sam publish
D. sam deploy

---

**Question 32.** A developer is launching a Lambda function that requires access to a MySQL RDS instance that is in a private subnet.

Which of the following is the MOST secure way to achieve this?

A. Move your RDS instance to a public subnet.
B. Expose an endpoint of your RDS to the Internet using an Elastic IP.
C. Ensure that the Lambda function has proper IAM permission to access RDS.
D. Configure the Lambda function to connect to your VPC.

---

**Question 33.** Your application is hosted on an Auto Scaling group of EC2 instances with a DynamoDB database. There were a lot of data discrepancy issues where the changes made by one user were always overwritten by another user. You noticed that this usually happens whenever there are a lot of people updating the same data.

What should you do to solve this problem?

A. Use DynamoDB global tables and implement a pessimistic locking strategy.
B. Implement a pessimistic locking strategy in your application source code by designating one property to store the version number in the mapping class for your table.
C. Implement an optimistic locking strategy in your application source code by designating one property to store the version number in the mapping class for your table.
D. Use DynamoDB global tables and implement an optimistic locking strategy.

---

**Question 34.** A leading financial company has recently deployed its application to AWS using Lambda and API Gateway. However, they noticed that all metrics are being populated in their CloudWatch dashboard except for AuthentCount and CacheHitCount.

What could be the MOST likely cause of this issue?

A. The provided IAM role to their API Gateway only has read access but no write privileges to CloudWatch.
B. API Caching is not enabled in API Gateway.
C. They have not provided an IAM role to their API Gateway yet.
D. API Gateway Private Integrations has not been configured yet.

---

**Question 35.** A company has recently developed a containerized application that uses a multi-container Docker platform which supports multiple containers per instance. They need a service that automatically handles tasks such as provisioning of the resources, load balancing, auto-scaling, monitoring, and placing the containers across the cluster.

Which of the following services provides the EASIEST way to accomplish the above requirement?

A. Lambda
B. Elastic Beanstalk
C. ECS
D. EKS

---

**Question 36.** You are planning to launch a Lambda function integrated with API Gateway. It is required to specify how the incoming request data is mapped to the integration request and how the resulting integration response data is mapped to the method response.

Which of the following options is the MOST appropriate method use to meet this requirement?

A. HTTP Proxy integration
B. HTTP custom integration
C. Lambda proxy integration
D. Lambda custom integration

---

**Question 37.** A startup has recently launched a high-quality photo sharing portal using Amazon Lightroom and S3. They noticed that there are other external websites which are linking and using their photos without permission. This has caused an increase in their data transfer cost and potential revenue loss.

Which is the MOST effective method to solve this issue?

A. Enable cross-origin resource sharing (CORS) which allows cross-origin GET requests from all origins.
B. Configure the S3 bucket to remove public read access and use pre-signed URLs with expiry dates.
C. Block the IP addresses of the offending websites using Network Access Control List.
D. Use a CloudFront web distribution with signed URLs or signed cookies.

---

**Question 38.** An application running on an EC2 instance regularly fetches large amounts of data from multiple S3 buckets. A data analysis team will perform ad-hoc queries on the data. To reduce costs and optimize the process, the application requires a solution that can perform serverless queries directly on the data stored in S3 without the need to load it into a database first.

Which is the MOST suitable service that will help accomplish this requirement?

A. Amazon Athena
B. Amazon Redshift Spectrum
C. Amazon EMR
D. AWS Step Functions

---

**Question 39.** A software development company uses AWS CodePipeline as its CI/CD platform to build, test, and push deployments to its production environment. Recently, a developer created a Lambda function that will push the build details to a separate DynamoDB table. The Lambda function should be triggered after a successful build on the Pipeline.

Which of the following services will meet the specified requirement?

A. Amazon EventBridge (Amazon CloudWatch Events)
B. AWS CloudTrail Events
C. AWS CodeBuild
D. AWS Systems Manager

---

**Question 40.** Your Lambda function initializes a lot of external dependencies such as database connections and HTTP endpoints, which are required for data processing. It also fetches static data with a size of 20 MB from a third-party provider over the internet every time the function is invoked. This adds significant time in the total processing time, which greatly affects the performance of your serverless application.

Which of the following should you do to improve the performance of your function?

A. Increase the CPU allocation of the function by submitting a service limit increase ticket to AWS.
B. Allocate more memory to your function.
C. Place the database and HTTP initialization logic outside the Lambda function handler and store the external files in the /tmp directory.
D. Use unreserved concurrency for your function.

---

**Question 41.** A startup has recently launched their new mobile game and is gaining a lot of new users everyday. The founders plan to add a new feature which will enable cross-device syncing of user profile data across mobile devices to improve the user experience.

Which of the following services should they use to meet this requirement?

A. Cognito Sync
B. AWS Amplify
C. Cognito Identity Pools
D. Cognito User Pools

---

**Question 42.** You are a developer for a global technology company which heavily uses AWS with regional offices in San Francisco, Manila, and Bangalore. Most of the clients of your company are using serverless computing in which you are responsible for ensuring that their applications are working efficiently.

Which of the following options are valid considerations in improving the performance of your Lambda function? (Select TWO.)

A. You can throttle all incoming executions and stop processing any invocations to your function by setting concurrency to false.
B. An increase in memory size triggers an equivalent increase in CPU available to your function.
C. The concurrent execution limit is enforced against the sum of the concurrent executions of all functions.
D. You have to install the X-Ray daemon in Lambda to enable active tracing.
E. Lambda automatically creates Elastic IPs that enable your function to connect securely to other resources within your private VPC.

---

**Question 43.** A developer is building an AI-based traffic monitoring application using Lambda in AWS. Due to the complexity of the application, the developer must do certain modifications such as the way Lambda runs the setup code and how the invocation events are read from the Lambda runtime API.

In this scenario, which feature of Lambda should you take advantage of to meet the above requirement?

A. Lambda@Edge
B. DLQ
C. Custom Runtime
D. Layers

---

**Question 44.** A developer has recently deployed an application, which is hosted in an Auto Scaling group of EC2 instances and processes data from an Amazon Kinesis Data Stream which has 10 shards. Due to performance issues, the systems operations team has increased the data stream to increase the number of open shards to 10.

What is the maximum number of running EC2 instances that should ideally be kept to maintain application performance?

A. 20
B. 40
C. 30
D. 10

---

**Question 45.** A developer is writing a CloudFormation template which will be used to deploy a simple Lambda function to AWS. The function to be deployed is made in Python with just 3 lines of codes which can be written inline in the template.

Which parameter of the AWS::Lambda::Function resource should the developer use to place the Python code in the template?

A. Handler
B. Code
C. CodeUri
D. ZipFile

---

**Question 46.** A software engineer is building a serverless application in AWS consisting of Lambda, API Gateway, and DynamoDB. She needs to implement a custom token authorization scheme that uses a bearer token authentication strategy such as OAuth or SAML to determine the caller's identity.

Which of the features of API Gateway is the MOST suitable one that she should use to build this feature?

A. Cross-Origin Resource Sharing (CORS)
B. Resource Policy
C. Lambda Authorizers
D. Cross-Account Lambda Authorizer

---

**Question 47.** A developer has just finished writing a serverless application using AWS SAM (Serverless Application Model) on a local machine. There is a SAM template ready and the corresponding Lambda function code in a directory. The developer now wants to deploy this application to AWS.

Which combination of steps should the developer follow to successfully deploy the SAM application? (Select THREE.)

A. Build the SAM template in an Amazon EC2 instance.
B. Package the SAM application for deployment.
C. Deploy the SAM template from an Amazon EC2 bucket.
D. Build the SAM template using the AWS SDK for AWS CodeDeploy.
E. Deploy the SAM template from AWS CodePipeline.
F. Build the SAM template in the local environment.

---

**Question 48.** An aerospace engineering company has recently migrated to AWS for their cloud architecture. They are using CloudFormation and AWS SAM as deployment services for both of their monolithic and serverless applications. There is a new requirement where you have to dynamically install packages, create files, and start services on your EC2 instances upon the deployment of the application stack using CloudFormation.

Which of the following helper scripts should you use in this scenario?

A. cfn-init
B. cfn-get-metadata
C. cfn-signal
D. cfn-hup

---

**Question 49.** The company that you are working for recently decided to migrate and transform their monolithic application on-premises to a Lambda application. It is your responsibility to ensure that application works effectively in AWS.

Which of the following are the best practices in developing Lambda functions? (Select TWO.)

A. Take advantage of Execution Context reuse to improve the performance of your function.
B. Use recursive code.
C. Include the core logic in the Lambda handler.
D. Use AWS Lambda Environment Variables to pass operational parameters to your function.
E. Use Amazon Inspector for troubleshooting.

---

**Question 50.** A developer is managing an application hosted in EC2, which stores data in an S3 bucket. The application also uses HTTPS for secure communication. To comply with the new security policy, the developer must ensure that the data is encrypted at rest using an encryption key that is provided and managed by the company. The change must also provide AES-256 encryption to their data.

Which of the following actions should the developer take to achieve this? (Select TWO.)

A. Use SSL to encrypt the data while in transit to Amazon S3.
B. Implement Amazon S3 server-side encryption with Amazon S3-Managed Encryption Keys.
C. Implement Amazon S3 server-side encryption with AWS KMS Keys (SSE-KMS).
D. Implement Amazon S3 server-side encryption with customer-provided keys (SSE-C).
E. Encrypt the data on the client-side before sending to Amazon S3 using their own master key.

---

**Question 51.** You are a software developer for a multinational investment bank which has a hybrid cloud architecture with AWS. To improve the security of their applications, they decided to use AWS Key Management Service (KMS) to create and manage their encryption keys across a wide range of AWS services. You were given the responsibility to integrate AWS KMS with the financial applications of the company.

Which of the following are the recommended steps to locally encrypt data using AWS KMS that you should follow? (Select TWO.)

A. Use the GenerateDataKeyWithoutPlaintext operation to get a data encryption key then use the plaintext data key in the response to encrypt data locally.
B. Encrypt data locally using the Encrypt operation.
C. Erase the plaintext data key from memory and store the encrypted data key alongside the locally encrypted data.
D. Use the GenerateDataKey operation to get a data encryption key then use the plaintext data key in the response to encrypt data locally.
E. Erase the encrypted data key from memory and store the plaintext data key alongside the locally encrypted data.

---

**Question 52.** An e-commerce application, which is hosted in an ECS Cluster, contains the connection string of an external database and other sensitive configuration files. Since the application accepts credit card payments, the company has to meet strict security compliance which requires that the database credentials are encrypted and periodically rotated.

Which of the following should you do to comply to the requirements?

A. Store the database credentials in an encrypted ecs.config configuration file.
B. Store the database credentials in AWS Secrets Manager and enable rotation.
C. Store the database credentials as a secure string parameter in Systems Manager Parameter Store.
D. Store the database credentials in an encrypted dockerrun.aws.json configuration file.

---

**Question 53.** In the next financial year, a company has decided to develop a completely new version of its legacy application that will utilize Node.js and GraphQL. The new architecture aims to offer an end-to-end view of requests as they traverse the application and display a map of the underlying components. To achieve this, the application will be hosted in an Auto Scaling group of Linux EC2 instances behind an Application Load Balancer (ALB) and instrumented to send trace data to the AWS X-Ray.

Which of the following options is the MOST suitable to satisfy this requirement?

A. Enable AWS X-Ray tracing on the ASG's launch template.
B. Use a user data script to install the X-Ray daemon.
C. Enable AWS Web Application Firewall (WAF) on the ALB to monitor web requests.
D. Refactor your application to send segment documents directly to X-Ray by using the PutTraceSegments API.

---

**Question 54.** You were recently hired by a media company that is planning to build a news portal using Elastic Beanstalk and DynamoDB database, which contains a few data. There is already an existing DynamoDB table that has an attribute of ArticleName which acts as the partition key. You are instructed to develop a feature that will query the articles and news data, other than the existing one. The feature also requires strong read consistency to fetch the most up-to-date data.

Which of the following solutions should you implement?

A. Create a Local Secondary Index that uses the ArticleName attribute and a different sort key.
B. Create a Global Secondary Index which uses the ArticleName attribute and your alternative sort key as projected attributes.
C. Create a new DynamoDB table with a Local Secondary Index that uses the ArticleName attribute with a different sort key. Migrate the data from the existing table to the new table.
D. Create a Global Secondary Index that uses the ArticleName attribute and a different sort key.

---

**Question 55.** A developer has recently launched a new API Gateway service which is integrated with AWS Lambda. He enabled API caching and per-key cache invalidation features in the API Gateway to comply with the requirement of the front-end and back-end development teams which will use the API. The front-end team will have to invalidate an existing cache entry in some scenarios and some of the front-end application teams will fetch the latest data from the integration endpoint.

Which of the following should the developer do in order to invalidate the cache in API Gateway?

A. Send a request with the Cache-Control: no-cache header.
B. Send a request with the Cache-Control: max-age=0 header.
C. Configure the front-end application to clear the browser cache before fetching data from API Gateway.
D. Send a request with the Cache-Control: INVALIDATE_CACHE header.

---

**Question 56.** A company has an application hosted in an On-Demand EC2 instance in your VPC. The developer has been instructed to create a shell script that fetches the instance's associated public and private IP addresses.

What should the developer do to complete this task?

A. Get the public and private IP addresses from the instance metadata service using the `http://169.254.169.254/latest/meta-data/` endpoint.
B. Get the public and private IP addresses from Amazon CloudWatch.
C. Get the public and private IP addresses from the instance user data service using the `http://169.254.169.254/latest/user-data/` endpoint.
D. Get the public and private IP addresses from AWS CloudTrail.

---

**Question 57.** Your request to increase your account's concurrent execution limit to 2000 has been recently approved by AWS. There are 10 Lambda functions running in your account and you already specified a concurrency execution limit on one function at 400 and on another function at 200.

Which of the following statements are TRUE in this scenario? (Select TWO.)

A. The remaining 1400 concurrent executions will be shared among the other 8 functions.
B. The combined allocated 600 concurrent execution will be shared among the 2 functions.
C. The unreserved concurrency pool is 600.
D. You can still set a concurrency execution limit of 1400 to a third Lambda function.
E. You can still set a concurrency execution limit of 1300 to a third Lambda function.

---

**Question 58.** A serverless application, which uses a DynamoDB database, is experiencing throttling issues during peak times. To troubleshoot the problem, you were instructed to get the total number of write capacity units consumed for the table and any secondary indexes whenever the UpdateItem operation is sent.

In this scenario, what is the MOST appropriate value for the ReturnConsumedCapacity parameter that you should set in the update request?

A. NONE
B. TOTAL
C. INDEXES
D. TRUE

---

**Question 59.** A company is developing a serverless website that consists of images, videos, HTML pages and JavaScript files. There is also a requirement to serve the files with lowest possible latency to its global users.

Which combination of services should be used in this scenario? (Select TWO.)

A. Amazon Glacier
B. Amazon Elastic File System
C. Amazon CloudFront
D. Amazon S3
E. Amazon EC2

---

**Question 60.** The operating cost of a serverless application is quite high and you are instructed to look for ways to lower the costs. As part of its processing, a Lambda function sends 200 strongly consistent read requests per second to a DynamoDB table which has a provisioned RCU of 5440. The average size of items stored in the database is 17 KB.

Which of the following is the MOST suitable action that you can do to make the application more cost-effective while maintaining its performance?

A. Decrease the provisioned RCU down to 800.
B. Switch the table from using provisioned mode to on-demand mode.
C. Implement exponential backoff.
D. Set the provisioned RCU to 1600.

---

**Question 61.** A developer uses AWS X-Ray to create a trace on an instrumented web application to identify any performance bottlenecks. The segment documents being sent by the application contain annotations that the developer wants to utilize in order to identify and filter out specific data from the trace.

Which of the following should the developer do in order to satisfy this requirement with minimal configuration? (Select TWO.)

A. Send trace results to an S3 bucket then query the trace output using Amazon Athena.
B. Use filter expressions via the X-Ray console.
C. Configure Sampling Rules in the AWS X-Ray Console.
D. Fetch the trace IDs and annotations using the GetTraceSummaries API.
E. Fetch the data using the BatchGetTraces API.

---

**Question 62.** A media company seeks to protect its copyrighted images from unauthorized distribution. They want images uploaded to their Amazon S3 bucket to be automatically watermarked. A developer has already prepared the Lambda function for this image processing feature.

Which option must the developer configure to automatically invoke the function at each upload?

A. Set up an Amazon S3 Event Notification to trigger the Lambda function when an ObjectCreated:Put event is detected in the bucket.
B. Use S3 Object Lambda to process images on retrieval and apply watermarks dynamically before the images are served to users.
C. Configure an S3 Lifecycle policy to transition images to the INTELLIGENT_TIERING storage class. Use S3 Inventory to generate a report of images that weren't watermarked and set up the Lambda function to process the report.
D. Enable S3 Storage Lens to monitor the bucket and configure the Lambda function to be invoked whenever the metrics indicate a new object creation.

---

**Question 63.** You are working as an IT Consultant for a top investment bank in Europe which uses several serverless applications in their AWS account. They just launched a new API Gateway service with a Lambda proxy integration and you were instructed to test out the new API. However, you are getting a Connection refused error whenever you use this invoke URL: `http://[yourdomain].execute-api.us-east-1.amazonaws.com/[lambda-proxy]` of the API Gateway.

Which of the following is the MOST likely cause of this issue?

A. You are not using FTP in invoking the API.
B. You are not using HTTP/2 in invoking the API.
C. You are not using HTTPS in invoking the API.
D. You are not using WebSocket in invoking the API.

---

**Question 64.** You are configuring the task definitions of your ECS Cluster in AWS to make sure that the tasks are scheduled on instances with enough resources to run them. It should also follow the constraints that you specified both implicitly or explicitly.

Which of the following options should you implement to satisfy the requirement which requires the LEAST amount of configuration?

A. Use a spread task placement strategy which uses the instanceId and host attributes.
B. Use a spread task placement strategy with custom placement constraints.
C. Use a binpack task placement strategy.
D. Use a random task placement strategy.
