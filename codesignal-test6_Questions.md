# CodeSignal Test 6 - Questions

---

**Question 1.** A company has launched a new serverless application using AWS Lambda. The app ran smoothly for a few weeks until it was featured on a popular website. As its popularity grew, so did the number of users receiving an error. Upon viewing the Lambda function's monitoring graph, the developer discovered a lot of throttled invocation requests.

What can the developer do to troubleshoot this issue? (Select THREE.)

A. Use a compiled language like Golang to improve the function's performance
B. Use exponential backoff in the application
C. Deploy the Lambda function in VPC
D. Increase Lambda function timeout
E. Request a service quota increase
F. Configure reserved concurrency

---

**Question 2.** A development team has a serverless architecture composed of multiple Lambda functions that invoke one another. As the number of Lambda functions increases, the team finds it increasingly difficult to manage the coordination and dependencies between them, leading to errors, duplication of code, and difficulty debugging and troubleshooting issues.

Which refactorization should the team implement?

A. Use AWS CodePipeline to define the source, build, and deployment stages for each Lambda function.
B. Use AWS AppConfig's feature flag to gradually release new code changes to each Lambda function.
C. Create an AWS AppSync GraphQL API endpoint and configure each Lambda function as a resolver.
D. Create an AWS Step Functions state machine and convert each Lambda function into individual Task states.

---

**Question 3.** A company is storing highly classified documents on its file server. These documents contain blueprints for electronic devices and are never to be made public due to a legal agreement. To comply with the strict policy, you must explore the capabilities of AWS KMS to improve data security.

Which of the following is the MOST suitable procedure for encrypting data?

A. Generate a data key using a KMS key. Then, encrypt data with the ciphertext version of the data key.
B. Use a symmetric key for encryption and decryption.
C. Generate a data key using a KMS key. Then, encrypt data with the plaintext data key.
D. Use a combination of symmetric and asymmetric encryption. Encrypt the data with a symmetric key and use the asymmetric private key to decrypt the data.

---

**Question 4.** A transcoding media service is being developed in AWS. Photos uploaded to Amazon S3 will trigger Step Functions to coordinate a series of processes that will perform image analysis tasks. The final output should contain the input plus the results of the final state to conform to the application's logic flow.

What should the developer do?

A. Declare a ResultPath field filter on the Amazon States Language specification.
B. Declare an InputPath field filter on the Amazon States Language specification.
C. Declare an OutputPath field filter on the Amazon States Language specification.
D. Declare a Parameters field filter on the Amazon States Language specification.

---

**Question 5.** A serverless application consists of multiple Lambda Functions and a DynamoDB table. The application must be deployed by calling the CloudFormation APIs using AWS CLI. The CloudFormation template and the files containing the code for all the Lambda functions are located on a local computer.

What should the Developer do to deploy the application?

A. Use the aws cloudformation update-stack command and deploy using aws cloudformation deploy.
B. Use the aws cloudformation deploy command.
C. Use the aws cloudformation validate-template command and deploy using aws cloudformation deploy.
D. Use the aws cloudformation package command and deploy using aws cloudformation deploy.

---

**Question 6.** A code that runs on a Lambda function performs a DynamoDB call from a DynamoDB table. The function runs three times every week. You noticed that the application kept receiving a ProvisionedThroughputExceededException error for 10 seconds most of the time.

How should you handle this error?

A. Enable DynamoDB Accelerator (DAX) to reduce response times from milliseconds to microseconds.
B. Create a Local Secondary Index (LSI) to the existing DynamoDB table to increase the provisioned throughput.
C. Reduce the frequency of requests using error retries and exponential backoff.
D. Refactor the code in the Lambda function to optimize its performance.

---

**Question 7.** An IAM user with programmatic access wants to get information about specific EC2 instances on the us-east-1 region. Due to strict policy, the user was compiled to use the describe-instances operation using AWS Command Line Interface (CLI). He wants to check whether he has the required permission to initiate the command without actually making the request.

Which of the following actions should be done to solve the problem?

A. Add the --dry-run parameter to the describe-instances command.
B. Add the --filters parameter to the describe-instances command.
C. Add the --max-items parameter to the describe-instances command.
D. Add the --generate-cli-skeleton parameter to the describe-instances command.

---

**Question 8.** A developer is looking for a way to decrease the latency in retrieving data from an Amazon RDS MySQL database. He wants to implement a caching solution that supports Multi-AZ replication with sub-millisecond response times.

What must the developer do that requires the LEAST amount of effort?

A. Set up an Elasticache for Redis cluster between the application and database. Configure it to run with replication to achieve high availability.
B. Set up an Elasticache for Memcached cluster between the application and database. Configure it to run with replication to achieve high availability.
C. Set up AWS Global Accelerator and integrate it with your application to improve overall performance.
D. Convert the database schema using the AWS Schema Conversion Tool and move the data to DynamoDB. Enable Amazon DynamoDB Accelerator (DAX).

---

**Question 9.** A full-stack developer has developed an application written in Node.js to host an upcoming mobile game tournament. The developer has decided to deploy the application using AWS Elastic Beanstalk because of its ease-of-use. Upon experimenting, he learned that he could configure the webserver environment with several resources.

Which of the following services can the developer configure with Elastic Beanstalk? (Select THREE.)

A. Application Load Balancer
B. Amazon Athena
C. Amazon EC2 Instance
D. AWS Lambda
E. Amazon CloudFront
F. Amazon CloudWatch

---

**Question 10.** A developer is writing a custom script that will run in an Amazon EC2 instance. The script needs to access the local IP address from the instance to manage a connection to an application outside the AWS Cloud. The developer found out that the details about an instance can be viewed by visiting a certain Uniform Resource Identifier (URI).

Which of the following is the correct URI?

A. http://169.254.169.254/latest/meta-data/
B. http://254.169.254.169/latest/meta-data/
C. http://169.254.169.254/latest/user-data/
D. http://254.169.169.254/latest/user-data/

---

**Question 11.** A company wants to centrally organize login credentials for its internal application. The application prompts users to change passwords every 35 days. Expired login credentials must be removed automatically, and an email notification should be sent to the users when their passwords are about to expire. A developer must create a solution with the least amount of development effort.

Which solution meets the requirements?

A. Store the credentials as Standard Parameters in AWS Systems Manager (SSM) Parameter Store and configure Expiration and ExpirationNotification policies. Create an Amazon EventBridge rule that sends Amazon SNS email notifications.
B. Use AWS Secret Managers to store user credentials and turn on automatic rotation.
C. Store the credentials as Advanced Parameters in AWS Systems Manager (SSM) Parameter Store and configure Expiration and ExpirationNotification policies. Create an Amazon EventBridge rule that sends Amazon SNS email notifications.
D. Use AWS Secrets Manager to store user credentials. Create a Lambda function that runs periodically to send Amazon SNS email notifications for passwords nearing expiration.

---

**Question 12.** A developer manages a web application hosted on a fleet of Amazon EC2 instances behind a public Application Load Balancer (ALB). Each instance is equipped with an HTTP server that logs incoming requests. Upon reviewing the logs, the developer realizes that they are only capturing the IP address of the ALB instead of the client's public IP address.

What modification should the developer make to ensure the log files include the client's public IP address?

A. Update the HTTP server's logging configuration to log the X-Forwarded-For header information.
B. Deploy the Amazon CloudWatch Logs agent on each instance, customizing it to capture and log the client's IP address.
C. Implement the AWS X-Ray daemon on all instances, adjusting its settings to record the client's IP address in the logs.
D. Configure the HTTP server to include the Host header in its logging configuration.

---

**Question 13.** A software development team uses AWS CodePipeline to facilitate continuous integration and delivery (CI/CD) for a Node.js application. The team requires a centralized way of distributing internal npm packages used by the application. It's crucial that the pipeline automatically starts to build whenever a new version of the package is released.

Which solution aligns with these requirements?

A. Create an Amazon ECR private repository and store the npm packages in it. Use Amazon SNS notifications to initiate CodePipeline pipeline builds.
B. Establish an AWS CodeArtifact repository to store the npm packages. Configure an Amazon EventBridge rule to detect changes in the repository and trigger CodePipeline pipeline builds.
C. Store the npm packages in an Amazon S3 bucket. Use Amazon SNS to trigger a CodePipeline pipeline build when a new package version is uploaded to the bucket.
D. Set up an Amazon ECR private repository to host the npm package. Utilize an AWS Lambda function to initiate a CodePipeline pipeline build whenever a new package version is published to the repository.

---

**Question 14.** A company processes data from IoT (Internet of Things) devices using an AWS Lambda function. To ensure that the Lambda function performs within the expected performance criteria, the business must closely monitor it to comply with its necessary service level agreement (SLA). The company wants to measure the application's throughput by tracking the total number of messages the Lambda function processes within a specified timeframe.

Which action should a developer take to meet the requirements?

A. Enable AWS Step Functions to orchestrate the message processing workflow of the Lambda function and monitor the execution times to infer throughput.
B. Utilize the Lambda function's ConcurrentExecutions metric in Amazon CloudWatch to assess throughput.
C. Update the application to log throughput metrics to Amazon CloudWatch Logs and configure Amazon EventBridge to periodically trigger a secondary Lambda function to calculate throughput.
D. Update the application to send custom Amazon CloudWatch metrics for each message processed by the Lambda function, and use these metrics for throughput calculation.

---

**Question 15.** A developer must ensure that any new log data published to an existing Amazon CloudWatch Logs group is encrypted. The log group has been actively receiving data for the past few weeks. The log data should be encrypted using an AWS Key Management Service (AWS KMS) key.

Which approach requires the least administrative effort to meet the requirements?

A. Manually encrypt log data before submission using client-side scripts that utilize KMS.
B. Associate an existing AWS KMS key with the log group by executing the aws logs associate-kms-key command with the key's Amazon Resource Name.
C. Implement custom encryption using AWS CloudHSM to encrypt logs before sending logs to CloudWatch.
D. Create a new log group with encryption settings using the AWS CLI aws logs create-log-group command, specifying the KMS key ARN.

---

**Question 16.** An engineering team is developing a cloud-based solution for their user registration system for an online service, utilizing AWS for their infrastructure. During the registration process, user form submissions are placed in a queue using Amazon Simple Queue Service (Amazon SQS). An AWS Lambda function is triggered to create new user accounts. However, the team has noticed that the Lambda function occasionally fails or times out, which results in incomplete user registrations. The team is looking for an efficient way to diagnose and fix these processing failures.

What should the engineering team implement to address these operational needs?

A. Set up an Amazon DynamoDB table to capture failed user registration attempts. Modify the Lambda function to route messages that cannot be processed to this table for further examination.
B. Extend the maximum timeout for the Lambda function's execution to 20 minutes. Verify on AWS CloudTrail's event logs to identify and examine errors related to user registrations.
C. Implement a dead-letter queue (DLQ) associated with the SQS queue. Configure the Lambda function to divert messages that fail to process correctly to this DLQ for subsequent analysis and action.
D. Lengthen the message visibility timeout setting of the SQS queue. Utilize Amazon CloudWatch Logs to pinpoint and troubleshoot errors during user registration processing.

---

**Question 17.** A web developer must deploy new features to a web application that can be turned on or off based on certain conditions. These new functionalities should not be accessible until fully developed and tested. The company wants to seamlessly control the visibility and access of these new features without reloading them until officially released.

Which of the following solutions would fulfill these criteria?

A. Develop a feature flag feature using AWS Lambda functions. Store the feature flag values in AWS Systems Manager Parameter Store. Use the Lambda function to fetch and check the feature flag status to manage the availability of new functionalities.
B. Employ AWS Amplify DataStore to maintain pre-release feature data. Use AWS Amplify DataStore cloud synchronization capabilities to modify feature visibility.
C. Utilize Amazon DynamoDB to store information about upcoming features. Leverage Amazon DynamoDB Streams to switch features' status from hidden to visible upon updates.
D. Utilize AWS AppConfig to set the feature flag by creating a feature flag configuration profile. Enable and disable the feature flags according to development progress.

---

**Question 18.** A startup wants an application that triggers processes in response to customer orders and inventory updates using AWS Lambda and Amazon EventBridge. The application requires a Lambda function to send the specific events to an Amazon EventBridge event bus. The developer has written the event bus triggered action on EventBridge. Upon deployment, the developer notices AccessDeniedException errors in the event logs, which is the reason why the function is not functioning as intended.

Which solution will help the developer in resolving the issue?

A. Adjust the AWS Lambda function's execution role to grant it permissions for the PutEvents action on EventBridge.
B. Implement a resource-based policy on the Lambda function that grants necessary permissions to perform the PutEvents action on EventBridge.
C. Establish a Virtual Private Cloud (VPC) peering connection to facilitate communication between AWS Lambda and EventBridge.
D. Update the developer's IAM role by including permission to explicitly allow the PutEvents operation on EventBridge.

---

**Question 19.** An enterprise deployed a new serverless application on AWS designed for real-time data processing. This application uses AWS Lambda functions to fetch data from Amazon S3, process it, and then store the results in a DynamoDB database. After deployment, users began experiencing intermittent slow responses. The development team suspects the issue might be related to the interaction between the Lambda function and Amazon S3, as this is where the latching occurs.

Which approach should a developer take to identify the root cause of the latency issue while following operational excellence principles?

A. Implement additional log statements within the Lambda function to record execution times with precise timestamps surrounding each call to external services. Then, redeploy the enhanced Lambda function. After sufficient operational data has been gathered, analyze the Amazon CloudWatch logs for the function to identify potential culprits for the delayed responses.
B. Analyze the detailed metrics and logs available in Amazon CloudWatch for the Lambda function. Focus on execution duration and error rates. Apply anomaly detection models to identify unusual patterns or spikes in latency.
C. Enhance the Lambda function with AWS X-Ray SDK integration, including the setup for HTTP/HTTPS requests and SDK client handlers. Redeploy the function with the modifications. Activate X-Ray tracing and, upon collecting sufficient operational data, utilize the X-Ray service maps to analyze average response timings and pinpoint probable sources of latency.
D. Explore the AWS CloudWatch Synthetics to generate canary that mimics user interactions with the portal. Ensure AWS X-Ray tracing is enabled for this canary to gain insights into the service interactions and performance metrics. After gathering enough data, review the outcomes on the CloudWatch Synthetics dashboard to locate the latency issues.

---

**Question 20.** An engineer is developing a cloud-native application on AWS designed to handle a large volume of data. Within this application, a state machine in AWS Step Functions calls upon multiple AWS Lambda functions for processing. Occasionally, one of these Lambda functions encounters a timeout error when processing requests, particularly during spikes in data volume, leading to service errors. The engineer must set up the system so that any invocation of the Lambda function that fails due to time limits is automatically picked up and retried again.

Which approach would ensure the system meets this requirement?

A. Establish a designated Fail state within the AWS Step Functions state machine architecture. Determine a retry limit for handling execution failures.
B. Integrate a Retry field into the AWS Step Functions state machine's configuration. Specify the maximum attempts for retries and the target timeout error type as the retry trigger.
C. Set the TimeoutSeconds value within the AWS Step Functions state machine setup. Assign a limit for retry attempts in response to operation timeouts.
D. Modify the AWS Step Functions state machine to forward the function call to an Amazon SNS topic and link the topic to the Lambda function. Set a retry limit for the Lambda to handle timeout error scenarios.

---

**Question 21.** A technology firm manages an internal portal that contains proprietary information. The firm intends to make this portal available to the general public. However, access must be restricted solely to employees authenticated through the firm's OpenID Connect (OIDC) compatible identity provider. This authentication mechanism must be implemented without modifying the existing application code.

Which action will accomplish this requirement?

A. Set up an internet-facing Application Load Balancer. Create a listener rule for the load balancer for HTTPS on port 443. Configure the rule's default action to authenticate users using the OIDC IdP configuration.
B. Set up an internet-facing Application Load Balancer. Create a listener rule for the load balancer for HTTPS on port 80. Add a default authenticating operation that returns the OIDC IdP configuration.
C. Set up an internet-facing Network Load Balancer. Create a listener rule for the load balancer for HTTPS on port 443. Configure the rule's default action to authenticate users using the OIDC IdP configuration.
D. Set up an internet-facing Application Load Balancer. Create a listener rule for the load balancer for HTTPS on port 443. Configure the rule's default action to invoke an AWS Lambda function for OIDC authentication.

---

**Question 22.** A software engineer utilizes AWS IAM Identity Center (AWS Single Sign-On) to communicate with the AWS CLI and SDK on their on-premises server. The engineer initially enabled SSO access correctly and was able to make API calls to multiple AWS services without any issues. Strangely, the engineer has suddenly begun to receive Access Denied messages when trying to make the same API calls. The engineer has confirmed that there have been no modifications to any configuration files, scripts, or data on their local machine. Furthermore, the developer ensured that their network connection and VPN access were operational.

Which is the MOST probable reason for the engineer's access issue?

A. The permission set assigned by the IAM Identity Center lacks the required permissions to perform the API call.
B. The credentials issued by the IAM Identity Center federated role are no longer valid.
C. The AWS CLI executable file of the engineer has had its access permissions modified.
D. The engineer's VPN connection is incorrectly configured.

---

**Question 23.** A company is developing a serverless website that consists of images, videos, HTML pages and JavaScript files. There is also a requirement to serve the files with lowest possible latency to its global users.

Which combination of services should be used in this scenario? (Select TWO.)

A. Amazon EC2
B. Amazon S3
C. Amazon Glacier
D. Amazon Elastic File System
E. Amazon CloudFront

---

**Question 24.** A developer is creating a script using AWS CLI to retrieve a list of objects in an S3 bucket. However, the script is timing out if the bucket has tens of thousands of objects.

Which solution would most likely rectify the issue?

A. Enable CORS
B. Apply the pagination parameters in the AWS CLI command
C. Enable Amazon S3 Transfer Acceleration
D. Increase the AWS CLI timeout value

---

**Question 25.** A company decided to re-use the same Lambda function for multiple stages of their API, but the function should read data from a different Amazon DynamoDB table depending on which stage is being called. In order to accomplish this, they instructed the developer to pass configuration settings to a Lambda function through mapping templates in API Gateway.

Which of the following is the MOST suitable solution that the developer should use to meet this requirement?

A. Create environment variables in the Lambda function.
B. Set up traffic shifting with Lambda Aliases.
C. Set up an API Gateway Private Integration to the Lambda function.
D. Use Stage Variables.

---

**Question 26.** In order to quickly troubleshoot their systems, your manager instructed you to record the calls that your application makes to all AWS services and resources. You developed a custom code that will send the segment documents directly to X-Ray by using the PutTraceSegments API.

What should you include in your segment document to meet the above requirement?

A. metadata
B. subsegments
C. tracing header
D. annotations

---

**Question 27.** The read and write operations to an Amazon DynamoDB table are throttled, causing errors in a stateful application that maintains user sessions. Despite checking Amazon CloudWatch metrics, the consumed capacity units have not exceeded the provisioned capacity. The development team has noticed that a "hot partition" is being accessed more frequently than others by downstream services.

What should be done to resolve this issue with MINIMAL cost? (Select TWO.)

A. Increase the amount of read or write capacity for your table.
B. Implement error retries and exponential backoff.
C. Use DynamoDB Accelerator (DAX).
D. Implement read sharding to distribute workloads evenly.
E. Refactor your application to distribute your read and write operations as evenly as possible across your table.

---

**Question 28.** A company has assigned a developer to automate its department's patch management, data synchronization, and other recurring tasks. The developer needs a service to coordinate multiple AWS services into serverless workflows.

Which of the following is the MOST cost-effective service the developer should implement in this scenario?

A. AWS Batch
B. AWS Lambda
C. AWS Elastic Beanstalk
D. AWS Step Functions

---

**Question 29.** A developer is designing the cloud architecture of an internal application which will be used by about a hundred employees. She needs to ensure that the architecture is elastic enough to adequately match the supply of resources to the demand while maintaining its cost-effectiveness.

Which of the following services can provide the MOST elasticity to the architecture? (Select TWO.)

A. AWS WAF
B. Amazon EC2 Spot Fleet
C. Amazon DynamoDB
D. Amazon RDS
E. Amazon CloudFront

---

**Question 30.** A company has a website hosted in a multicontainer Docker environment in Elastic Beanstalk. There is a requirement to integrate the website with API Gateway where it simply passes client-submitted method requests to the backend. It is important that the client connects to the API Gateway after the API method is set up, except for known issues such as unsupported characters.

Which of the following integration types is the MOST suitable one to use to meet this requirement?

A. AWS_PROXY
B. HTTP_PROXY
C. HTTP
D. AWS

---

**Question 31.** A company operates an e-commerce website on Amazon Elastic Container Service (ECS) behind an Application Load Balancer (ALB). They've set their ALB as an origin for Amazon CloudFront. Users interact with the website via a custom domain (online storefront) set up in Route 53 and within a public hosted zone in Amazon Route 53. The company wants to display region-specific pricing, for example users from the UK should navigate to https://tutorialsdojo.com/uk/, while users from the US should navigate to https://tutorialsdojo.com/us/.

How can a developer incorporate this feature in the least amount of operational overhead?

A. Configure the Route 53 record to use the geolocation routing policy.
B. Use AWS Web Application Firewall (WAF) geo-matching rule to identify the user-country and attach it to the ALB. Configure ALB listener rules with path conditions to route traffic based on the identified country.
C. Forward the CloudFront-Viewer-Address header to the web server running on the ECS cluster. Implement a custom logic that matches the header's value against a GeoIP database to determine user location. Based on the resolved location, redirect users to the appropriate region-specific URL.
D. Implement a CloudFront function that returns the appropriate URL based on the CloudFront-Viewer-Country. Configure the distribution to trigger the function on Viewer request events.

---

**Question 32.** A developer has recently completed a new version of a serverless application that is ready to be deployed using AWS SAM. There is a requirement that the traffic should shift from the previous Lambda function to the new version in the shortest time possible, but you still don't want to shift traffic all at once.

Which deployment configuration strategy is the MOST suitable one to use in this scenario?

A. CodeDeployDefault.LambdaCanary10Percent5Minutes
B. CodeDeployDefault.LambdaLinear10PercentEvery2Minutes
C. CodeDeployDefault.LambdaAllAtOnce
D. CodeDeployDefault.LambdaLinear10PercentEvery1Minute

---

**Question 33.** You are working as an IT Consultant for a top investment bank in Europe which uses several serverless applications in their AWS account. They just launched a new API Gateway service with a Lambda proxy integration and you were instructed to test out the new functionalities. You got a connection refused error whenever you use this invoke URL: http://finance&accounts.execute-api.us-east-1.amazonaws.com/tutorialslabs/ of the API Gateway.

Which of the following is the MOST likely cause of this issue?

A. You are not using HTTP/2 in invoking the API.
B. You are not using WebSocket in invoking the API.
C. You are not using HTTPS in invoking the API.
D. You are not using FTP in invoking the API.

---

**Question 34.** A media company seeks to protect its copyrighted images from unauthorized distribution. They want images uploaded to their Amazon S3 bucket to be automatically watermarked. A developer has already prepared the Lambda function for this image processing job.

Which option must the developer configure to automatically invoke the function at each upload?

A. Set up an Amazon S3 Event Notification to trigger the Lambda function when an ObjectCreated/Put event is detected in the bucket.
B. Enable S3 Storage Lens to monitor the bucket and configure the Lambda function to be invoked whenever the metrics indicate a new object creation.
C. Use S3 Object Lambda to process images on retrieval and apply watermarks dynamically before the images are served to users.
D. Configure an S3 Lifecycle policy to transition images to the INTELLIGENT_TIERING storage class. Use S3 Inventory to generate a report of images that weren't watermarked and set up the Lambda function to process the report.

---

**Question 35.** A company has an application that is using CloudFront to serve their static contents to their users around the globe. They are receiving a number of bad reviews from their customers lately because it takes a lot of time to log into their website. Sometimes, their users are also getting HTTP 504 errors which is why the developer was instructed to fix this problem immediately.

Which of the following combination of options should the developer use together to set up a cost-effective solution for this scenario? (Select TWO.)

A. Customize the content that the CloudFront web distribution delivers to your users using Lambda@Edge, which allows your Lambda functions to execute the authentication process in AWS locations closer to the users.
B. Configure an origin failover by creating an origin group with two origins. Specify one as the primary origin and the other as the second origin which CloudFront automatically switches to when the primary origin returns specific HTTP status code failure responses.
C. Add a Cache-Control max-age directive to your objects in CloudFront and specify the longest practical value for max-age to increase the cache hit ratio of your CloudFront distribution.
D. Launch your application to multiple AWS regions to serve your global users. Use a Route 53 record with latency routing policy to route incoming traffic to the region with the best latency to the user.
E. Launch your application to multiple and geographically disperse VPCs on various AWS regions then create a transit VPC to easily connect all resources. Use several AWS Lambda functions in the region using the AWS Serverless Application Model (SAM) to improve the overall application performance.

---

**Question 36.** A startup has recently launched their new mobile game and is gaining a lot of new users everyday. The founders plan to add a new feature which will enable cross-device syncing of user profile data across mobile devices to improve the user experience.

Which of the following services should they use to meet this requirement?

A. AWS Amplify
B. Cognito User Pools
C. Cognito Identity Pools
D. Cognito Sync

---

**Question 37.** You are using an AWS Lambda function to process records in an Amazon Kinesis Data Streams stream which has 100 active shards. The Lambda function takes an average of 10 seconds to process the data and the stream is receiving 50 new items per second.

Which of the following statements are TRUE regarding this scenario?

A. There will be at most 100 Lambda function invocations running concurrently.
B. The Lambda function will throttle the incoming requests due to the excessive number of Kinesis shards.
C. The Lambda function has 500 concurrent executions.
D. The Kinesis shards must be merged to increase the data capacity of the stream as well as the concurrency execution of the Lambda function.

---

**Question 38.** A developer is working on an application which stores data to an Amazon DynamoDB table with the DynamoDB Streams feature enabled. He set up an event source mapping with an AWS Lambda function to monitor any table changes then store the new value to an S3 bucket and maintain the new value in the DynamoDB table. When a record is updated, it should only send a copy of the item's previous value in the DynamoDB table.

Which StreamViewType is the MOST suitable one to use in the DynamoDB configuration to fulfill this scenario?

A. OLD_IMAGE
B. NEW_IMAGE
C. NEW_AND_OLD_IMAGES
D. KEYS_ONLY

---

**Question 39.** A company is re-architecting its legacy application to use AWS Lambda and DynamoDB. The table is provisioned to have 10 read capacity units, and each item has a size of 4 KB.

How many eventual and strong consistent read requests can the table handle per second?

A. 10 strongly consistent reads and 10 eventually consistent reads per second
B. 10 strongly consistent reads and 20 eventually consistent reads per second
C. 20 strongly consistent reads and 10 eventually consistent reads per second
D. 5 strongly consistent reads and 20 eventually consistent reads per second

---

**Question 40.** A company has a development team that's heavily relying on AWS CodeBuild, and CodeDeploy. The management would like to further automate its CI/CD process. They requested a system that monitors the status of each code change, from the moment it's committed through to its deployment.

Which of the following AWS services will help you achieve this?

A. AWS CodePipeline
B. Amazon CodeGuru
C. AWS Elastic Beanstalk
D. AWS Fault Injection Simulator

---

**Question 41.** A web application is uploading large files, which are over 4 GB in size, to an Amazon S3 bucket called data.tutorialsdojo.com every 30 minutes.

To minimize the time required for each upload, which of the following actions should be taken?

A. Use the BatchWriteItem API.
B. Enable Transfer Acceleration in the bucket.
C. Use the PutItem API.
D. Use the Multipart upload API.

---

**Question 42.** A developer is building a Docker application using Amazon ECS. The application requires containers to maintain long-lived connections and access specific ports on the host container instance to send or receive traffic using port mapping.

Which component of ECS should the developer configure to properly implement this task?

A. Service scheduler
B. Container Agent
C. Task definition
D. Container instance

---

**Question 43.** A developer is planning to add a global secondary index in a DynamoDB table. This will allow the application to query a specific index that can span all of the data in the base table, across all partitions.

Which of the following should the developer consider when using this type of index? (Select TWO.)

A. Queries or scans on this index consume capacity units from the index, not from the base table.
B. For each partition key value, the total size of all indexed items must be 10 GB or less.
C. Queries or scans on this index consume read capacity units from the base table.
D. Queries on this index support eventual consistency only.
E. When you query this index, you can choose either eventual consistency or strong consistency.

---

**Question 44.** You are developing a high-traffic online stocks trading application, which will be hosted in an ECS Cluster and will be accessed by thousands of investors for intraday stocks trading. Each task of the cluster should be evenly placed across multiple Availability Zones to avoid any service disruption.

Which of the following is the MOST suitable placementStrategy configuration that you should use in your task definition?

A. `{"placementStrategy": [{"field": "attribute:ecs.availability-zone", "type": "spread"}]}`
B. `{"placementStrategy": [{"field": "memory", "type": "binpack"}]}`
C. `{"placementStrategy": [{"type": "random"}]}`
D. `{"placementStrategy": [{"field": "instanceId", "type": "spread"}]}`

---

**Question 45.** A serverless application is using API Gateway with a non-proxy Lambda integration. A developer was tasked to expose a GET method on a new /getcourses resource to invoke the Lambda function, which will allow the consumers to fetch a list of online courses in JSON format. A developer included a parameter named courseType in their request to get the data.

What is the MOST efficient solution that the developer should do to accomplish this requirement?

A. Configure the method request of the resource.
B. Configure the integration response of the resource.
C. Configure the method response of the resource.
D. Configure the integration request of the resource.

---

**Question 46.** You are developing an online game where the app preferences and game state of the player must be synchronized across devices. It should also allow multiple users to synchronize and collaborate shared data in real time.

Which of the following is the MOST appropriate solution that you should implement in this scenario?

A. Integrate AWS AppSync to your mobile app.
B. Integrate Amazon Cognito Sync to your mobile app.
C. Integrate Amazon Pinpoint to your mobile app.
D. Integrate AWS Amplify to your mobile app.

---

**Question 47.** A company is using OpenAPI, which is also known as Swagger, for the API specifications of their REST web services that are hosted on their premises data center. They want to migrate their system to AWS using Lambda and API Gateway. In line with this, you are instructed to create a new API with all resources and methods from their Swagger definition.

Which of the following is the EASIEST way to accomplish this task?

A. Create models and templates for request and response mappings based on the company's API definitions.
B. Import their Swagger or OpenAPI definitions to API Gateway using the AWS Console.
C. Use CodeDeploy to migrate and deploy the company's web services to API Gateway.
D. Use AWS SAM to migrate and deploy the company's web services to API Gateway.

---

**Question 48.** A tech company has a real-time traffic monitoring system which uses Amazon Kinesis Data Stream to collect data and a group of EC2 instances that consume and process the data. Your development team is responsible for adjusting the number of shards in the data stream, to adapt to changes in the rate of data flow.

Which of the following are correct regarding Kinesis resharding? (Select TWO.)

A. You can decrease the stream's capacity by merging shards.
B. You have to merge the hot shards to increase the capacity of the stream.
C. You have to split the cold shards to decrease the capacity of the stream.
D. The data records that are flowing to the parent shards will be lost when you reshard.
E. You can increase the stream's capacity by splitting shards.

---

**Question 49.** A global financial company has hundreds of users from all over the world who regularly upload terabytes of transactional data to a centralized Amazon S3 bucket. Users from different parts of the globe are experiencing delays in uploading data, which in turn affects throughput and ensure consistently fast data transfer to the S3 bucket regardless of the user's location.

Which should be used to satisfy the above requirement?

A. AWS Transfer for SFTP
B. AWS Direct Connect
C. S3 Transfer Acceleration
D. Amazon CloudFront

---

**Question 50.** You recently deployed an application to a newly created AWS account, which uses two identical Lambda functions to process all-hoc requests. The first function processes incoming requests efficiently but the second one has a longer processing time even though both of the functions have the same configuration. In your monitoring, the Throttles metric of the second function is greater than the first one in Amazon CloudWatch.

Which of the following are feasible solutions that you can implement to fix this issue? (Select TWO.)

A. Set the concurrency execution limit of both functions to 450.
B. Decrease the concurrency execution limit of the first function.
C. Set the concurrency execution limit of the second function to 0.
D. Set the concurrency execution limit of both functions to 500.
E. Configure the second function to use an unreserved account concurrency.

---

**Question 51.** A company is transitioning their systems to AWS due to the limitations of their on-premises data center. As part of this project, a developer was assigned to build a brand new serverless architecture in AWS, which will be composed of AWS Lambda, API Gateway, and DynamoDB. The developer needs a framework that will allow him to share configuration such as memory and timeouts between resources and deploy all related resources together as a single versioned entity.

Which of the following is the MOST appropriate service that the developer should use in this scenario?

A. AWS Systems Manager
B. Serverless Application Framework
C. AWS SAM
D. AWS CloudFormation

---

**Question 52.** A company has 5 different applications running on several On-Demand EC2 instances. The DevOps team is required to set up a graphical representation of the key performance metrics for each application. These system metrics must be available on a single shared screen for more effective and timely monitoring.

Which of the following should the DevOps team do to satisfy this requirement using Amazon CloudWatch?

A. Set up a custom CloudWatch alarm with a unique metric name for each application.
B. Set up a custom CloudWatch dimension with a unique metric name for each application.
C. Set up a custom CloudWatch namespace with a unique metric name for each application.
D. Set up a custom CloudWatch Event with a unique metric name for each application.

---

**Question 53.** In the next financial year, a company has decided to develop a completely new version of its legacy application that will utilize Node.js and GraphQL. The new architecture aims to offer an end-to-end view of requests as they traverse the application and display a map of the underlying components. To achieve this, the application will be hosted in an Auto Scaling group of Linux EC2 instances behind an Application Load Balancer. The application must be instrumented to send trace data to the AWS X-Ray.

Which of the following options is the MOST suitable way to satisfy this requirement?

A. Enable AWS X-Ray tracing on the ASG's launch template.
B. Enable AWS Web Application Firewall (WAF) on the ALB to monitor web requests.
C. Refactor your application to send segment documents directly to X-Ray by using the PutTraceSegments API.
D. Use a user data script to install the X-Ray daemon.

---

**Question 54.** A financial company has a cryptocurrency application that has been hosted in Elastic Beanstalk for a couple of months. Recently, the application's performance has been degrading, so you decided to check the CPU and memory utilization of the underlying EC2 instances in CloudWatch. However, you are only seeing the CPU utilization of the instances but not the memory utilization.

Which of the following is the MOST likely cause of this issue?

A. The detailed monitoring is not enabled in CloudWatch.
B. The .ebextensions/cwp-daemon.config file in Elastic Beanstalk is missing.
C. CloudWatch does not track memory utilization by default.
D. X-Ray Daemon is not installed on the EC2 instances.

---

**Question 55.** A new IT policy requires you to trace all calls that your Node.js application sends to external HTTP web APIs as well as SQL database queries. You have to instrument your application, which is hosted in Elastic Beanstalk. In order to properly trace the calls via the X-Ray console, you have to instrument your application.

What should you do to comply with the given requirement?

A. Create a Docker image that runs the X-Ray daemon.
B. Enable active tracing in the Elastic Beanstalk by including the healthcheckurl.config configuration file in the .ebextensions directory of your source code.
C. Use a user data script to run the daemon automatically.
D. Enable the X-Ray daemon by including the xray-daemon.config configuration file in the .ebextensions directory of your source code.

---

**Question 56.** An API gateway with a Lambda proxy integration takes a long time to complete its processing. There were also occurrences where some requests timed out. You want to monitor the responsiveness of your API calls as well as the underlying Lambda function.

Which of the following CloudWatch metrics should you use to troubleshoot this issue? (Select TWO.)

A. CacheHitCount
B. CacheMissCount
C. Count
D. IntegrationLatency
E. Latency

---

**Question 57.** A developer uses AWS X-Ray to create a trace on an instrumented web application to identify any performance bottlenecks. The segment documents being sent by the application contain annotations that the developer wants to utilize in order to identify and filter out certain documents being sent to the X-Ray service.

Which of the following should the developer do in order to satisfy this requirement with minimal configuration? (Select TWO.)

A. Use filter expressions via the X-Ray console.
B. Fetch the data using the BatchGetTraces API.
C. Fetch the trace IDs and annotations using the GetTraceSummaries API.
D. Send trace results to an S3 bucket then query the trace output using Amazon Athena.
E. Configure Sampling Rules in the AWS X-Ray Console.

---

**Question 58.** A developer has instrumented an application using the X-Ray SDK to collect all the data about the requests that an application server handles. There is a new requirement to develop a custom debug tool which will enable them to view the full traces of their application without using the X-Ray Console.

What should the developer do to accomplish this task?

A. Use the GetGroup API to get the list of trace IDs of the application and then retrieve the list of traces using BatchGetTraces API.
B. Use the GetServiceGraph API to get the list of trace IDs of the application and then retrieve the list of traces using GetTraceSummaries API.
C. Use the GetTraceSummaries API to get the list of trace IDs of the application and then retrieve the list of traces using BatchGetTraces API.
D. Use the BatchGetTraces API to get the list of trace IDs of the application and then retrieve the list of traces using GetTraceSummaries API.

---

**Question 59.** A Docker application hosted on an ECS cluster has encountered intermittent unavailability issues and latencies. The lead DevOps engineer instructed you to instrument the application to detect where high latencies are and to determine the specific services and paths impacting application performance.

Which of the following steps should you take to accomplish this task properly? (Select TWO.)

A. Add the xray-daemon.config configuration file in your Docker image.
B. Manually install the X-Ray daemon to the instances via a user data script.
C. Configure the port mappings and network mode settings in the container agent to allow traffic on TCP port 2000.
D. Create a Docker image that runs the X-Ray daemon, upload it to a Docker image repository, and then deploy it to your Amazon ECS cluster.
E. Configure the port mappings and network mode settings in your task-definition file to allow traffic on UDP port 2000.

---

**Question 60.** A company has an application hosted in an ECS Cluster that heavily uses an RDS database. A developer needs to closely monitor how the different processes on a DB instance use the CPU, such as the percentage of the CPU bandwidth or the total memory consumed by each process to ensure application performance.

Which of the following is the MOST suitable solution that the developer should implement?

A. Use Enhanced Monitoring in RDS.
B. Track the CPU% and MEMb% metrics that are readily available in the Amazon RDS console.
C. Develop a shell script that collects and publishes custom metrics to CloudWatch which tracks the real-time CPU Utilization of the RDS instance.
D. Use CloudWatch to track the CPU Utilization of your database.

---

**Question 61.** A serverless application, which uses a Lambda function integrated with API Gateway, provides data to a front-end application written in React/JS. The users are complaining that they are getting HTTP 504 errors intermittently when they use the application in CloudWatch logs of the Lambda function.

Which of the following is the MOST likely cause of this issue?

A. The API Gateway automatically enabled throttling in peak times which caused the HTTP 504 errors.
B. The underlying Lambda function has been running for more than 29 seconds causing the API Gateway request to time out.
C. There is an authorization failure occurring between API Gateway and the Lambda function.
D. The memory allocated for the Lambda function is insufficient.

---

**Question 62.** An application, which already uses X-Ray, generates thousands of trace data every hour. The developer wants to use a filter expression that will limit the results based on custom attributes or keys that he specifies.

How should the developer refactor the application in order to filter the results in the X-Ray console?

A. Create a new sampling rule based on the custom attributes.
B. Add the custom attributes as metadata in your segment document.
C. Include the custom attributes as new segment fields in the segment document.
D. Add the custom attributes as annotations in your segment document.

---

**Question 63.** An online stock trading platform is hosted in an Auto Scaling group of EC2 instances with an Application Load Balancer in front to distribute the incoming traffic. The developer must monitor the IP traffic going to and from network interfaces in your VPC to comply with financial regulatory requirements.

Which of the following options should the developer do to meet the requirement?

A. Create a flow log in your VPC.
B. Install and run the AWS X-Ray daemon to your EC2 instances using an instance metadata script.
C. Use AWS Inspector to capture information about the IP traffic going to and from the network interfaces of your EC2 instances.
D. Use CloudTrail logs to track all API calls and capture information about the IP traffic going to and from your VPC.

---

**Question 64.** A developer is utilizing AWS X-Ray to generate a visual representation of the requests flowing through their enterprise web application. Since the application interacts with multiple services, all requests must be traced in X-Ray, including any downstream calls made to AWS resources.

Which of the following actions should the developer implement for this scenario?

A. Pass multiple trace segments as a parameter of PutTraceSegments API.
B. Install AWS X-Ray on the different services that communicate with the application including the AWS resources that the application calls.
C. Use X-Ray SDK to generate segment documents with subsegments and send them to the X-Ray daemon, which will buffer them and upload to the X-Ray API in batches.
D. Use AWS X-Ray SDK to upload a trace segment by executing PutTraceSegments API.

---

**Question 65.** A company is developing an online system that lets patients schedule appointments with their preferred doctors at medical centers all over the country. The company uses Amazon DynamoDB as its primary database. The Amazon DynamoDB Streams feature is enabled on the booking data. A Lambda function integrated with Amazon EventBridge (Amazon CloudWatch Events) is used to process the data stream every 26 hours and can store the results to the S3 bucket. There are a lot of updated items in DynamoDB that are not sent to the S3 bucket, and there are no errors in the logs.

Which of the following is the MOST appropriate solution for this issue?

A. Set the value of StreamViewType parameter in DynamoDB Streams to NEW_IMAGE.
B. Increase the interval of running your function to 48 hours.
C. Set the value of StreamViewType parameter in DynamoDB Streams to NEW_AND_OLD_IMAGES.
D. Decrease the interval of running your function to 24 hours.
