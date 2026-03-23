# CodeSignal Test 2 - Questions

**Question 1.** A developer is building the cloud architecture of an application which will be hosted in a large EC2 instance. The application will process the data and it will upload results to an S3 bucket.

Which of the following is the SAFEST way to implement this architecture?

A. Store the access keys in the instance then use the AWS SDK to upload the results to S3.
B. Install the AWS CLI then use it to upload the results to S3.
C. Use an IAM Role to grant the application the necessary permissions to upload data to S3.
D. Use an IAM Inline Policy to grant the application the necessary permissions to upload data to S3.

---

**Question 2.** A prototype application is hosted in an EC2 instance, which has an assigned IAM Role to store data from both the development and production S3 buckets. The instance also has AWS CLI access/secret key installed to handle other ad hoc tasks. You assigned a new IAM Role to the instance which has the permission to access the development bucket only. However, upon testing, the instance can still store files to both buckets.

What is the MOST likely root cause of this issue?

A. The instance profile role of a running EC2 instance is static and can't be replaced at all.
B. The application is still using the IAM role that is configured for the AWS CLI key.
C. Due to eventual consistency, you must wait 24 hours for the change to appear across all of AWS.
D. The new IAM Role has an attached inline policy.

---

**Question 3.** An organization has a serverless application using AWS Lambda, Amazon API Gateway. Recently, the DevOps team discovered that the IAM roles associated with the Lambda functions had been manually modified. The organization must identify these unauthorized changes and ensure all resources are in sync with the CloudFormation stack.

Which solution will help the company identify these changes?

A. Use AWS Config to monitor updates made to the Lambda functions and IAM roles.
B. Review CloudTrail logs to trace IAM role updates for the Lambda functions.
C. Run a drift detection check on the CloudFormation stack.
D. Analyze CloudWatch Logs to identify changes to the IAM role permissions.

---

**Question 4.** A mobile game is currently being developed and needs to have an authentication service. You need to use an AWS service which provides temporary AWS credentials for users who have been authenticated via their social media logins as well as for guest users who do not require any authentication.

How can you BEST achieve this using AWS?

A. Use AWS Cognito User Pools then enable access to unauthenticated identities.
B. Use Amazon Cognito Sync.
C. Use AWS IAM Identity Center.
D. Use AWS Cognito Identity Pools then enable access to unauthenticated identities.

---

**Question 5.** You are developing a serverless application in AWS in which you have to control the code execution performance and costs of your Lambda functions. There is a requirement to increase the CPU available to your function in order to efficiently process records from an Amazon Kinesis data stream.

Which of the following is the BEST way to meet this requirement?

A. Configure the function to use unreserved account concurrency.
B. Increase the concurrent execution limit of the function.
C. Use Lambda@Edge.
D. Increase the allocated memory of the function.

---

**Question 6.** A company has a hybrid cloud architecture that connects its on-premises data center with AWS. The DevOps team has been tasked to set up the company's continuous integration and continuous delivery (CI/CD) systems. The application deployment to both Amazon EC2 instances and on-premises servers should also be automated.

Which of the following AWS service should be used to accomplish this?

A. AWS CodeBuild
B. AWS CloudFormation
C. AWS CodeDeploy
D. Amazon Kinesis

---

**Question 7.** You are hosting a website in an Amazon S3 bucket named tutorialsdojo and your users load the website using the http://tutorialsdojo.s3-website-us-east-1.amazonaws.com endpoint. You want to use JavaScript on the webpages that are stored in this bucket to be able to make authenticated GET and PUT requests. These requests are directed to the same bucket through the website.s3.amazonaws.com S3 API endpoint. However, you noticed that your web browser blocks the HTTP requests originating from your website.

What should you do to rectify this issue?

A. Enable Cross-Region Replication (CRR).
B. Enable Cross-Zone Load Balancing.
C. Enable cross-account access.
D. Enable Cross-origin resource sharing (CORS) configuration in the bucket.

---

**Question 8.** A data analytics company has installed sensors to track the number of people that goes to the mall. The data sets are collected in real-time by an Amazon Kinesis Data Stream which has a consumer that is configured to process data every other day and store the results to S3. Your team noticed that your S3 bucket is only receiving half of the data that is being sent to the Kinesis stream but after checking, you have verified that the sensors are properly sending the data to Amazon Kinesis in real-time without any issues.

Which of the following is the MOST likely root cause of this issue?

A. By default, the data records are only accessible for 24 hours from the time they are added to a Kinesis stream.
B. The Amazon Kinesis Data Stream automatically deletes duplicate data.
C. The Amazon Kinesis Data Stream has too many open shards.
D. The sensors are having intermittent connection issues.

---

**Question 9.** A serverless application consisting of a Lambda function and a DynamoDB database is used to process Amazon S3 events. The Lambda function takes an average of three seconds to process the data and Amazon S3 publishes 10 events per second.

What is the concurrent execution that the function will have?

A. 30
B. 13
C. 10
D. 3

---

**Question 10.** A developer wants to track the number of visitors on their website, which has a DynamoDB database. This is primarily used to give a rough idea on how many people visit the site whenever they launch a new advertisement, which means it can tolerate a slight over-counting or undercounting of website visitors.

Which of the following will satisfy the requirement with MINIMAL configuration?

A. Enable DynamoDB Streams to track the number of new visitors.
B. Use atomic counters to increment the counter item in the DynamoDB table for every new visitor.
C. Use conditional writes to update the counter item in the DynamoDB table only if the item has a unique primary key and the new value is greater than the current value.
D. Use conditional writes to update the counter item in the DynamoDB table and set the ReturnConsumedCapacity parameter to TOTAL.

---

**Question 11.** A company has a global multi-player game with a multi-master DynamoDB database topology which stores data in multiple AWS regions. You were assigned to develop a real-time data analytics application which will track and store the recent changes on all the tables from various regions. Only one of the newly updated items is needed to be tracked by your application.

Which of the following is the MOST suitable way to configure the data analytics application to detect and retrieve the updated database entries automatically?

A. Enable DynamoDB Streams and set the value of StreamViewType to NEW_IMAGE. Create a trigger in AWS Lambda to capture stream data and forward it to your application.
B. Enable DynamoDB Streams and set the value of StreamViewType to NEW_IMAGE. Use Kinesis Adapter in the application to consume streams from DynamoDB.
C. Enable DynamoDB Streams and set the value of StreamViewType to NEW_AND_OLD_IMAGE. Use Kinesis Adapter in the application to consume streams from DynamoDB.
D. Enable DynamoDB Streams and set the value of StreamViewType to NEW_AND_OLD_IMAGE. Create a trigger in AWS Lambda to capture stream data and forward it to your application.

---

**Question 12.** A developer is designing the cloud architecture of an internal application which will be used by about a hundred employees. She needs to ensure that the architecture is elastic enough to adequately match the supply of resources to the demand while maintaining its cost-effectiveness.

Which of the following services can provide the MOST elasticity to the architecture? (Select TWO.)

A. Amazon RDS
B. Amazon CloudFront
C. Amazon EC2 Spot Fleet
D. Amazon DynamoDB
E. AWS WAF

---

**Question 13.** A developer has instrumented an application using the X-Ray SDK to collect all data about the requests that an application serves. There is a new requirement to develop a custom debug tool which will enable them to view the full traces of their application without using the X-Ray console.

What should the developer do to accomplish this task?

A. Use the BatchGetTraces API to get the list of trace IDs of the application and then retrieve the list of traces using GetTraceSummaries API.
B. Use the GetTraceSummaries API to get the list of trace IDs of the application and then retrieve the list of traces using BatchGetTraces API.
C. Use the GetGroup API to get the list of trace IDs of the application and then retrieve the list of traces using BatchGetTraces API.
D. Use the GetServiceGraph API to get the list of trace IDs of the application and then retrieve the list of traces using GetTraceSummaries API.

---

**Question 14.** You are developing an application that will use a Lambda function, which will be invoked asynchronously. The application will be implemented with exponential back-off that will handle failures so that the requests will be retried twice before the event is discarded. If the retries fail with an unexpected error, you have to direct unprocessed events to another service which will analyze the failure.

Which of the following is the MOST suitable component that you should implement in the application architecture to meet the above requirement?

A. FIFO Queue
B. Dead Letter Queue
C. Delay Queue
D. Amazon MQ

---

**Question 15.** An application is sending thousands of log files to an S3 bucket everyday. The request to retrieve the list of objects using the AWS CLI aws s3api list-objects command is timing out due to the high volume of data being fetched. In order to rectify this issue, you have to use pagination to control the number of results returned on your request.

Which of the following parameters should you include in CLI command for this scenario? (Select TWO.)

A. --page-size
B. --summarize
C. --max-items
D. --size-only
E. --exclude

---

**Question 16.** A company has a website hosted in a multicontainer Docker environment in Elastic Beanstalk. There is a requirement to integrate the website with API Gateway, where it simply passes client-submitted method requests to the backend. It is important that the client and backend interact directly with no intervention from API Gateway after the API method is set up, except for known issues such as unsupported characters.

Which of the following integration types is the MOST suitable one to use to meet this requirement?

A. HTTP
B. AWS
C. AWS_PROXY
D. HTTP_PROXY

---

**Question 17.** A developer needs to configure the environment name, solution stack, and environment links of his application environment which will be hosted in Elastic Beanstalk.

Which configuration file should the developer add in the source bundle to meet the above requirement?

A. env.config
B. Dockerrun.aws.json
C. cron.yaml
D. env.yaml

---

**Question 18.** An online magazine is deployed in AWS and uses an Application Load Balancer, an Auto Scaling group of EC2 instances, and an RDS MySQL Database. Some of the readers are complaining about the website's sluggish performance when loading the articles. Upon checking, there is a high number of read operations in the database, which affects the website's performance.

Which of the following actions should you take to resolve the issue with minimal code change?

A. Upgrade the EC2 instances to a higher instance type.
B. Launch a large ElastiCache Cluster as a database cache for RDS and apply the required code change.
C. Create an RDS Read Replica instance and configure the application to use this for read queries.
D. Set up a multi-AZ deployments configuration in RDS.

---

**Question 19.** Using AWS SAM, a developer recently deployed a serverless application consisting of Lambda functions, API Gateway, Kinesis Data stream, and a DynamoDB table. The application has worked fine for a few days, but lately, there were a lot of ProvisionedThroughputExceeded exceptions being returned by DynamoDB. The developer also noticed that there's a sudden increase in read capacity units (RCU) usage whenever this issue happens.

How should the developer refactor the application to find items based on primary key values and use the LEAST amount of RCU?

A. Use the Query operation with eventual consistency reads.
B. Use the Scan operation with eventual consistency reads.
C. Use the Query operation with strong consistency reads.
D. Use the Scan operation with strong consistency reads.

---

**Question 20.** A company is re-architecting its legacy application to use AWS Lambda and DynamoDB. The table is provisioned to have 10 read capacity units, and each item has a size of 4 KB.

How many eventual and strong consistent read requests can the table handle per second?

A. 5 strongly consistent reads and 20 eventually consistent reads per second
B. 10 strongly consistent reads and 10 eventually consistent reads per second
C. 10 strongly consistent reads and 20 eventually consistent reads per second
D. 20 strongly consistent reads and 10 eventually consistent reads per second

---

**Question 21.** A developer is instructed to collect data on the number of times that web visitors click the advertisement link of a popular news website. A database entry containing the count will be incremented for every click. Given that the website has millions of readers worldwide, your database should be configured to provide optimal performance to capture all the click events.

What is the BEST service that the developer should implement in this scenario?

A. Take advantage of Amazon Aurora's performance speed and AUTO_INCREMENT feature for item updates.
B. Launch an Amazon Redshift for the database and apply a step count of 1 for the IDENTITY column.
C. Use Amazon RDS for the database and setup SQL AUTO_INCREMENT on your tables.
D. Set up Amazon DynamoDB for the database and implement atomic counters for UpdateItem operation of the website counter.

---

**Question 22.** A company is using AWS Organizations to manage its multiple AWS accounts which is being used by its various departments. To avoid security issues, it is of utmost importance to test the impact of service control policies (SCPs) on your IAM policies and resource policies before applying them.

Which of the following services can you use to test and troubleshoot IAM and resource-based policies?

A. AWS Config
B. Systems Manager
C. Amazon Inspector
D. IAM Policy Simulator

---

**Question 23.** A developer wants to use multi-factor authentication (MFA) to protect programmatic calls to specific AWS API operations like Amazon EC2 StopInstances. He needs to call an API where he can submit the MFA code that is associated with his MFA device. Using the temporary security credentials that are returned from the call, he can then make programmatic calls to API operations that require MFA authentication.

Which API should the developer use to properly implement this security feature?

A. AssumeRoleWithSAML
B. AssumeRoleWithWebIdentity
C. GetFederationToken
D. GetSessionToken

---

**Question 24.** A developer is instrumenting an application that will be hosted in a large On-Demand EC2 instance in AWS. All of the downstream calls invoked by the application must be traced properly, including the AWS SDK calls. A user-defined data should also be present to expedite the troubleshooting process.

Which of the following are valid considerations in AWS X-Ray that the developer should follow? (Select TWO.)

A. Set the annotations object with any additional custom data that you want to store in the segment.
B. Set the namespace subsegment field to remote for AWS SDK calls and aws for other downstream calls.
C. Set the metadata object with key-value pairs that you want X-Ray to index for search.
D. Set the namespace subsegment field to aws for AWS SDK calls and remote for other downstream calls.
E. Set the metadata object with any additional custom data that you want to store in the segment.

---

**Question 25.** A company has an AWS Amplify application, relying on Amazon Cognito for user authentication. Multi-factor authentication (MFA) is disabled for their User Pool. There has been a recent data breach in a popular website. The company is worried that attackers might exploit compromised email addresses and passwords to sign into their applications. For this reason, they want to enforce MFA only on users with suspicious login attempts.

How can the company satisfy these requirements?

A. Create a subscription filter Lambda function that monitors for the CompromisedCredentialRisk metric from Advanced Security Metrics in CloudWatch Logs and triggers MFA when detected.
B. Recreate the User Pool and enable SMS text message MFA.
C. Enable Adaptive Authentication for the User Pool.
D. Enable the Time-based one-time password (TOTP) software token MFA for the User Pool.

---

**Question 26.** A developer is building an application that will be hosted in ECS and must be configured to run tasks and services using the Fargate launch type. The application will have four different tasks, each of which will access different AWS resources than the others.

Which of the following is the MOST efficient solution that can provide your application in ECS access to the required AWS resources?

A. Create 4 different Container Instance IAM Roles with the required permissions and attach them to each of the 4 ECS tasks.
B. Create an IAM Group with all the required permissions and attach them to each of the 4 ECS tasks.
C. Create 4 different IAM Roles with the required permissions and attach them to each of the 4 ECS tasks.
D. Create 4 different Service-Linked Roles with the required permissions and attach them to each of the 4 ECS tasks.

---

**Question 27.** A developer has a set of EC2 instances that runs the Amazon Kinesis Client Library to process a data stream in AWS. Based on the custom metrics, it shows that the instances are maxing out their CPU Utilization, and there are insufficient Kinesis shards to handle the rate of data flowing through the stream.

Which of the following is the BEST course of action that the developer should take to solve this issue and prevent this situation from re-occurring in the future?

A. Increase the number of instances up to the number of open shards.
B. Increase the instance size to a larger type.
C. Increase both the instance size and the number of open shards.
D. Increase the number of shards.

---

**Question 28.** A tech company has a real-time traffic monitoring system which uses Amazon Kinesis Data Stream to collect data and a group of EC2 instances that consume and process the data stream. Your development team is responsible for adjusting the number of shards in the data stream to adapt to changes in the rate of data flow.

Which of the following are correct regarding Kinesis resharding which your team should consider in managing the application? (Select TWO.)

A. You can increase the stream's capacity by splitting shards.
B. You have to merge the hot shards to increase the capacity of the stream.
C. The data records that are flowing to the parent shards will be lost when you reshard.
D. You can decrease the stream's capacity by merging shards.
E. You have to split the cold shards to decrease the capacity of the stream.

---

**Question 29.** A company has 5 different applications running on several On-Demand EC2 instances. The DevOps team is required to set up a graphical representation of the key performance metrics for each application. These system metrics must be available on a single shared screen for more effective and visible monitoring.

Which of the following should the DevOps team do to satisfy this requirement using Amazon CloudWatch?

A. Set up a custom CloudWatch Alarm with a unique metric name for each application.
B. Set up a custom CloudWatch dimension with a unique metric name for each application.
C. Set up a custom CloudWatch Event with a unique metric name for each application.
D. Set up a custom CloudWatch namespace with a unique metric name for each application.

---

**Question 30.** A developer is building a prototype microservices that are running as tasks in an Amazon ECS Cluster. His manager instructed him to define a task placement strategy which needs to be both cost and resource efficient. The task placement should minimize the number of instances in use which will keep the cost down since high availability is not much of a concern for this prototype.

What should the developer implement to meet the above requirements?

A. Distribute tasks evenly across all available EC2 instances using the spread task placement strategy.
B. Place tasks randomly using the random task placement strategy.
C. Distribute tasks among all registered EC2 instances based on the least available amount of CPU or memory using the binpack task placement strategy.
D. Distribute tasks evenly across Availability Zones, and then re-distribute the tasks among EC2 instances based on the least available amount of CPU/memory within each Availability Zone.

---

**Question 31.** A multinational e-commerce company hosts its product descriptions on an Amazon RDS database. All descriptions are originally written in English. Users can request on-demand translations via a Lambda function, which fetches the description and builds the Amazon Translate's TranslateText API for the task. There has been a surge in translation requests of popular products, which is increasing the RDS read capacity and increased response times.

How can a developer improve the Lambda function's response time cost-effectively without performing database optimizations?

A. Use AWS Step Functions with a Parallel state to concurrently run multiple instances of the Lambda function for translation.
B. Use the /tmp storage in the Lambda function to cache recently translated product descriptions.
C. Update the Lambda function to use asynchronous invocation. Push the translation requests to an Amazon SQS queue and then process in batches.
D. Store the results of the TranslateText API in an Amazon DynamoDB Accelerator (DAX) cluster.

---

**Question 32.** A serverless application, which is composed of multiple Lambda functions, has been deployed using AWS SAM. A developer was instructed to easily manage the deployments of the functions using CodeDeploy. When there is a new deployment, 10 percent of the incoming traffic should be shifted to the new version every 10 minutes until all traffic is shifted from the old version.

What should the developer do to properly deploy the functions that satisfies this requirement?

A. Deploy the functions using an Immutable deployment configuration.
B. Deploy the functions using an All-at-once deployment configuration.
C. Deploy the functions using a Linear deployment configuration.
D. Deploy the functions using a Canary deployment configuration.

---

**Question 33.** A developer is preparing the application specification (AppSpec) file in CodeDeploy, which will be used to deploy her Lambda functions to AWS. In the deployment, she needs to configure CodeDeploy to run a task before the traffic is shifted to the deployed Lambda function version.

Which deployment lifecycle event should she configure in this scenario?

A. BeforeAllowTraffic
B. Install
C. Start
D. BeforeInstall

---

**Question 34.** A social media application is using DynamoDB to manage and store the session data of its users. As the number of users grew, the number of items in the table exponentially increased as well. You have to reduce storage usage and also reduce the cost of storing irrelevant data without using provisioned throughput to rectify this issue.

Which of the following is the MOST cost-effective solution that you should implement?

A. Implement a Write-Through caching strategy in your application.
B. Use a Lambda function with CloudWatch Events to schedule a purge of stale items in the table on a daily basis.
C. Turn on Time To Live (TTL) in the table.
D. Implement a Lazy Loading caching strategy to your application.

---

**Question 35.** A serverless application is using API Gateway with a non-proxy Lambda Integration. A developer was tasked to expose a GET method on a new /getcourses resource to invoke the Lambda function, which will allow the consumers to fetch a list of online courses in JSON format. The consumers must include a query string parameter named courseType in their request to get the data.

What is the MOST efficient solution that the developer should do to accomplish this requirement?

A. Configure the method response of the resource.
B. Configure the integration response of the resource.
C. Configure the method request of the resource.
D. Configure the integration request of the resource.

---

**Question 36.** A company has a central data repository in Amazon S3 that needs to be accessed by developers belonging to different AWS accounts. The required IAM role has been created with the appropriate S3 permissions.

Given that the developers mostly interact with S3 via APIs, which API should the developers call to use the IAM role?

A. AssumeRole
B. GetSessionToken
C. AssumeRoleWithWebIdentity
D. AssumeRoleWithSAML

---

**Question 37.** You are planning to create a DynamoDB table for your employee profile website. This will be used by the Human Resources department to easily view details about each employee.

When choosing the partition key of the table, which of the following is the BEST attribute to use?

A. department_id since employees will fall in these departments.
B. employee_name because this will speed up searching of records.
C. employee_id because each employee ID is unique.
D. position_id because this will help sort the records per department.

---

**Question 38.** Your manager assigned you a task of implementing server-side encryption with customer-provided encryption keys (SSE-C) to your S3 bucket, which will allow you to set your own encryption keys. Amazon S3 will manage both the encryption and decryption process using your key when you access your objects, which will remove the burden of maintaining any code to perform data encryption and decryption.

To properly upload data to this bucket, which of the following headers must be included in your request?

A. x-amz-server-side-encryption, x-amz-server-side-encryption-customer-key and x-amz-server-side-encryption-customer-key-MD5 headers
B. x-amz-server-side-encryption-customer-algorithm, x-amz-server-side-encryption-customer-key and x-amz-server-side-encryption-customer-key-MD5 headers
C. x-amz-server-side-encryption and x-amz-server-side-encryption-aws-kms-key-id headers
D. x-amz-server-side-encryption-customer-key header only

---

**Question 39.** An application is hosted in Elastic Beanstalk, which is currently running in Java 7 runtime environment. A new version of the application is ready to be deployed, and the developer was tasked to upgrade the platform to Java 8 to accommodate the changes. All user traffic must be immediately directed to the new version. If problems arise, the developer should be able to quickly revert to the previous version.

Which of the following is the MOST appropriate action that the developer should do to upgrade the platform?

A. Perform a Traffic splitting deployment.
B. Perform a Blue/Green Deployment.
C. Manually upgrade the Java runtime environment of the EC2 instances in the Elastic Beanstalk environment.
D. Update the environment's platform version to Java 8.

---

**Question 40.** A multinational company uses Amazon EC2 Auto Scaling to maintain a fleet of EC2 instances behind an Application Load Balancer (ALB). The Amazon EC2 instances are configured with the Amazon CloudWatch agent to publish custom metrics. However, the newly launched EC2 instances within the Auto Scaling group fail to send the metrics to Amazon CloudWatch.

What changes are required to ensure the custom metrics are sent from all newly launched EC2 instances?

A. Attach the CloudWatchAgentServerPolicy to the IAM role specified in the EC2 Auto Scaling launch template to ensure proper permissions for the CloudWatch agent.
B. Attach the CloudWatchAgentAdminPolicy IAM policy to the IAM role specified in the EC2 Auto Scaling launch template to provide enhanced permissions.
C. Configure the IAM role for the EC2 instances with the CloudWatchAgentReadOnlyAccess policy to allow the CloudWatch agent to read default metrics and publish data.
D. Add a user data script in the EC2 Auto Scaling launch template to install and start the CloudWatch agent upon instance initialization.

---

**Question 41.** An application in your development account is running in an AWS Elastic Beanstalk environment which has an attached Amazon RDS database. It is also brings down the database which hinders you from performing seamless updates with Blue-green deployments. This poses a critical security risk if the company decides to deploy the application in production.

In this scenario, how can you decouple your database instance from your Elastic Beanstalk environment without losing any data?

A. Use a Canary deployment strategy to decouple the Amazon RDS instance from your Elastic Beanstalk environment. Create an RDS DB snapshot of the database and enable deletion protection. Create a new Elastic Beanstalk environment with the necessary information to connect to the Amazon RDS instance and delete the old environment.
B. Use the blue / green deployment strategy to decouple the Amazon RDS instance from your Elastic Beanstalk environment. Create an RDS DB snapshot of the database and enable deletion protection. Create a new Elastic Beanstalk environment with the necessary information to connect to the Amazon RDS instance. Before terminating the old Elastic Beanstalk environment, remove its security group first before proceeding.
C. Use the blue / green deployment strategy to decouple the Amazon RDS instance from your Elastic Beanstalk environment and enable deletion protection. Create a new Elastic Beanstalk environment with the necessary information to connect to the Amazon RDS instance. Before terminating the old Elastic Beanstalk environment, remove the RDS security group first before proceeding.
D. Use a Canary deployment strategy to decouple the Amazon RDS instance from your Elastic Beanstalk environment. Create an RDS DB snapshot of the database and enable deletion protection. Create a new Elastic Beanstalk environment with the necessary information to connect to the Amazon RDS instance and delete the old environment.

---

**Question 42.** A developer monitors multiple sensors inside a data center which detects various environmental conditions that may affect their running servers. In the current architecture, the data is initially processed by an AWS Lambda function and then stored in a remote data warehouse. To make the system more dynamic and scalable, the developer plans to use an Amazon SQS FIFO queue to store the data, which will be polled by the Lambda function. There is a known issue with the sensor devices of processing duplicate data intermittently.

What action can the developer take to reduce the chances of processing duplicate messages?

A. Use an Amazon SQS Standard queue instead of a FIFO queue to avoid any duplicate messages.
B. Configure the Amazon SQS queue to automatically drop a duplicate message whenever it arrives within the MessageVisibilityTimeout.
C. Add a MessageDeduplicationId parameter to the SendMessage API request.
D. Refactor the Lambda function to store the message's content and drop the incoming messages with similar content within a 5-minute period.

---

**Question 43.** A company has an AWS account with only 2 Lambda functions, which process data and store the results in an S3 bucket. An Application Load Balancer is used to distribute the incoming traffic to the two Lambda functions as registered targets. You noticed that in peak times, the first Lambda function works with optimal performance but the second one is throttling the incoming requests.

Which of the following is the MOST likely root cause of this issue?

A. The concurrency execution limit provided to the first function is less than the second function.
B. The first function is using the unreserved account concurrency while the second function has been set with a concurrency execution limit of 800.
C. The concurrency execution limit provided to the first function is significantly higher than the second function.
D. The first function is using the unreserved account concurrency while the second function has been set with a concurrency execution limit of 1000.

---

**Question 44.** An application has recently been migrated from an on-premises data center to a development Elastic Beanstalk environment. A developer will do iterative tests and therefore needs to deploy code changes and view them as quickly as possible.

Which of the following options take the LEAST amount of time to complete the deployment?

A. Rolling
B. Rolling with additional batch
C. All at once
D. Immutable

---

**Question 45.** A company is deploying the package of its Lambda function, which is compressed as a ZIP file, to AWS. However, they are getting an error in the deployment process because the package is too large. The manager instructed the developer to keep the deployment package small to make the development process much easier and more modularized. This should also help prevent errors that may occur when dependencies are installed and packaged with the function code.

Which of the following options is the MOST suitable solution that the developer should implement?

A. Zip the deployment package again to further compress the zip file.
B. Compress the deployment package as TAR file instead.
C. Upload the other dependencies of your function as a separate Lambda Layer instead.
D. Upload the deployment package to S3.

---

**Question 46.** A Docker application hosted on an ECS cluster has encountered intermittent unavailability issues and timeouts. The lead DevOps engineer instructed you to instrument the application to detect where high latencies are occurring and to determine the specific services and paths impacting application performance.

Which of the following steps should you take to accomplish this task properly? (Select TWO.)

A. Create a Docker image that runs the X-Ray daemon, upload it to a Docker image repository, and then deploy it to your Amazon ECS cluster.
B. Add the xray-daemon.config configuration file in your Docker image.
C. Configure the port mappings and network mode settings in your task definition file to allow traffic on UDP port 2000.
D. Configure the port mappings and network mode settings in the container agent to allow traffic on TCP port 2000.
E. Manually install the X-Ray daemon to the instances via a user data script.

---

**Question 47.** A company has different AWS accounts, namely Account A, Account B, and Account C, which are used for their Development, Test, and Production environments respectively. A developer needs access to perform an audit whenever a new version of the application has been deployed to the Test (Account B) and production (Account C) environments.

What is the MOST efficient way to provide the developer access to execute the specified task?

A. Create separate identities and passwords for the developer on both the Test and Production accounts.
B. Enable AWS multi-factor authentication (MFA) to the IAM User of the developer.
C. Set up AWS Organizations and attach a Service Control Policy to the developer to access the other accounts.
D. Grant the developer cross-account access to the resources of Accounts B and C.

---

**Question 48.** A development team is working on an AWS Serverless Application Model (SAM) application with its source code hosted on GitHub. A newly recruited developer clones the repository and observes that the SAM template contains references to AWS Lambda functions with CodeUri pointing to local file paths. The developer has added a new Lambda function and must redeploy the updated version to Production.

Which combination of steps must be taken to satisfy the requirement? (Select Two)

A. Execute sam build to resolve dependencies and construct deployment artifacts for all functions and layers in the SAM template.
B. Use the sam deploy command to deploy the application with a specified CloudFormation stack.
C. Run sam init to initialize a new SAM project.
D. Execute sam publish to make the application available in the AWS Serverless Application Repository.
E. Use the sam sync command to synchronize the local changes to the application in AWS.

---

**Question 49.** A company has developed a Lambda function that will send status updates to a third-party provider for analytics. You need to schedule this function to run every 30 minutes.

Which of the following is the MOST manageable and cost-effective way of setting up this task?

A. Enable scheduling on the AWS Console of your Lambda function. Define a schedule to run it at 30-minute intervals.
B. Integrate Amazon EventBridge (Amazon CloudWatch Events) with Lambda, which will automatically trigger the function every 30 minutes.
C. Launch an EC2 instance that has a cron job that triggers the Lambda function every 30 minutes.
D. Use the Task Scheduler of your Windows PC to trigger the Lambda function every 30 minutes.

---

**Question 50.** A developer is creating a real-time auction app for second-hand cars using Kinesis Data Streams to ingest bids. The auction rules are as follows:

A bid must be processed only once

An EC2 instance consumer must process bids in the same order they were received.

Which solution will meet the requirement?

A. Embed a unique ID in each bid record. Use Kinesis PutRecord API to write bids. Assign a timestamp-based value for the SequenceNumberForOrdering parameter.
B. Replace the stream with an SQS FIFO queue and use the SendMessage API to write bids. Provide a unique id in the MessageDeduplicationId parameter for each bid request.
C. Replace the stream with an SQS FIFO queue and use the SendMessageBatch API to write bids. Provide a unique id in the MessageDeduplicationId parameter for each bid request.
D. Embed a unique ID in each bid record. Use Kinesis PutRecords API to write bids. Assign a timestamp-based value for the PartitionKey parameter.

---

**Question 51.** In order to quickly troubleshoot their systems, your manager instructed you to record the calls that your application makes to all AWS services and resources. You developed a custom code that will send the segment documents directly to X-Ray by using the PutTraceSegments API.

What should you include in your segment document to meet the above requirement?

A. metadata
B. tracing header
C. annotations
D. subsegments

---

**Question 52.** You recently deployed an application to a newly created AWS account, which uses two identical Lambda functions to process ad-hoc requests. The first function processes incoming requests efficiently but the second one has a longer processing time even though both of the functions have exactly the same code. Based on your monitoring, the Throttles metric of the second function is greater than the first one in Amazon CloudWatch.

Which of the following are possible solutions that you can implement to fix this issue? (Select TWO.)

A. Set the concurrency execution limit of the second function to 0.
B. Configure the second function to use an unreserved account concurrency.
C. Set the concurrency execution limit of both functions to 450.
D. Set the concurrency execution limit of both functions to 500.
E. Decrease the concurrency execution limit of the first function.

---

**Question 53.** Your development team is currently developing a financial application in AWS. One of the requirements is to create and control the encryption keys used to encrypt your data using the envelope encryption strategy to comply with the strict IT security policy of the company.

Which of the following correctly describes the process of envelope encryption?

A. Encrypt plaintext data with a data key and then encrypt the data key with a top-level encrypted key.
B. Encrypt plaintext data with a KMS key and then encrypt the KMS key with a top-level plaintext data key.
C. Encrypt plaintext data with a KMS key and then encrypt the KMS key with a top-level encrypted data key.
D. Encrypt plaintext data with a data key and then encrypt the data key with a top-level plaintext key.

---

**Question 54.** A company is heavily using a range of AWS services to host their enterprise applications. Currently, their deployment process still has a lot of manual steps which is why they plan to automate their software delivery process using continuous integration and delivery (CI/CD) pipelines in AWS. They will use CodePipeline for automating their software release process and CodeDeploy for deploying applications to various compute platforms in AWS.

In this architecture, which of the following are valid considerations when using CodeDeploy? (Select TWO.)

A. The CodeDeploy agent communicates using HTTP over port 80.
B. CodeDeploy can deploy applications to EC2, AWS Lambda, and Amazon ECS only.
C. You have to install and use the CodeDeploy agent installed on your EC2 instances and ECS cluster.
D. AWS Lambda compute platform deployments cannot use an in-place deployment type.
E. CodeDeploy can deploy applications to both your EC2 instances as well as your on-premises servers.

---

**Question 55.** You are developing a serverless application in AWS composed of several Lambda functions and a DynamoDB database. The requirement is to process the requests asynchronously.

Which of the following is the MOST suitable way to accomplish this?

A. Use the Invoke API to call the Lambda function and set the invocation type request parameter to RequestResponse.
B. Use the InvokeAsync API to call the Lambda function and set the invocation type request parameter to Event.
C. Use the Invoke API to call the Lambda function and set the invocation type request parameter to Event.
D. Use the InvokeAsync API to call the Lambda function and set the invocation type request parameter to RequestResponse.

---

**Question 56.** Your team is developing a new feature on your application which is already hosted in Elastic Beanstalk. After several weeks, the new version of the application is ready to be deployed and you were instructed to handle the deployment.

What is the correct way to deploy the new version to Elastic Beanstalk via the CLI?

A. Package your application as a tar file and deploy it using the eb deploy command.
B. Package your application as a zip file and deploy it using the aws elasticbeanstalk update-application command.
C. Package your application as a zip file and deploy it using the eb deploy command.
D. Package your application as a tar file and deploy it using the aws elasticbeanstalk update-application command.

---

**Question 57.** A developer is building an image processing utility using an AWS Lambda function. The function processes images in parallel using multiple threads to optimize performance. The images are stored in an Amazon S3 bucket and retrieved for processing. However, the function is not performing as efficiently as expected, with the processing time taking longer than anticipated, even when handling relatively small images.

Which action should the developer modify to achieve better performance in the AWS Lambda function?

A. Utilize Amazon S3 Transfer Acceleration for image uploads.
B. Increase the timeout setting of the Lambda function.
C. Optimize memory allocation for the Lambda function.
D. Use AWS Step Functions to split tasks into smaller workflows.

---

**Question 58.** You have an application that reads an individual item from a DynamoDB table, modifies it locally, and submits the changes as a new entry to a separate table before proceeding onto the next item. The process is repeated for the next 100 entries, and it consumes a lot of time performing this entire process.

Which strategy can be applied to your application in order to shorten the time needed to process all the necessary entries with MINIMAL configuration?

A. Modify your application to use multithreading.
B. Deploy your application into a cluster of EC2 instances.
C. Use DynamoDB conditional writes.
D. Use DynamoDB's BatchGetItem and BatchWriteItem API operations.

---

**Question 59.** An ECS Cluster has a running X-Ray Daemon that enables developers to easily debug and troubleshoot their application. However, the trace data being sent to AWS X-Ray is still not as detailed as your manager wants it to be. There is a new requirement that requires the application to provide more granular timing information and more details about its downstream calls to various AWS resources.

What should you do to satisfy this requirement?

A. Use metadata
B. Use inferred segment
C. Use annotations
D. Use subsegments

---

**Question 60.** A Java web application built using AWS SDK for Java with a DynamoDB database is concurrently accessed by thousands of users during peak time. The application is highly write-intensive and there are a lot of incidents where it overwrites stale data from the DynamoDB table.

How can you ensure your database writes are protected from being overwritten by other write operations that are occurring at the same time without affecting the application performance?

A. Implement optimistic locking with version number.
B. Implement overly optimistic locking (OOL).
C. Implement pessimistic locking with read locking.
D. Implement pessimistic locking with write locking.

---

**Question 61.** A developer is using API Gateway Lambda Authorizer to provide authentication for every API request and control access to your API. The requirement is to implement an authentication strategy which is similar to OAuth or SAML.

Which of the following is the MOST suitable method that the developer should use in this scenario?

A. Token-based Authorization
B. AWS STS-based Authentication
C. Request Parameter-based Authorization
D. Cross-Account Lambda Authorizer

---

**Question 62.** A leading commercial bank has an online banking portal that is hosted in an Auto Scaling group of EC2 instances with an Application Load Balancer in front to distribute the incoming traffic. The application has been instrumented, and the X-Ray daemon has been installed in all instances to allow debugging and troubleshooting using AWS X-Ray.

In this architecture, from which source will AWS X-Ray fetch the client IP address?

A. From the source IP of the IP packet.
B. From the X-Forwarded-Host header of the request.
C. From the X-Forwarded-For header of the request.
D. From the ipAddress query parameter of the request if it exists.

---

**Question 63.** A write-heavy data analytics application is using DynamoDB database which has global secondary index. Whenever the application is performing heavy write activities on the table, the DynamoDB requests return a ProvisionedThroughputExceededException.

Which of the following is the MOST likely cause of this issue?

A. The provisioned throughput exceeds the current throughput limit for your account.
B. The provisioned write capacity for the global secondary index is greater than the write capacity of the base table.
C. The provisioned write capacity for the global secondary index is less than the write capacity of the base table.
D. The rate of requests exceeds the allowed throughput.

---

**Question 64.** Due to the popularity of serverless computing, your manager instructed you to share your technical expertise to the whole software development department of your company. You are planning to deploy a simple Node.js 'Hello World' Lambda function to AWS using CloudFormation.

Which of the following is the EASIEST way of deploying the function to AWS?

A. Upload the code in S3 as a ZIP file then specify the S3 path in the ZipFile parameter of the AWS::Lambda::Function resource in the CloudFormation template.
B. Include your function source inline in the ZipFile parameter of the AWS::Lambda::Function resource in the CloudFormation template.
C. Upload the code in S3 then specify the S3Key and S3Bucket parameters under the AWS::Lambda::Function resource in the CloudFormation template.
D. Include your function source inline in the Code parameter of the AWS::Lambda::Function resource in the CloudFormation template.
