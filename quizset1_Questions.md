# AWS Developer Associate - Quiz Set 1 (Questions 1–75)

---

**Question 1.** A company uses Amazon API Gateway to expose a set of APIs to customers. The APIs have caching enabled in API Gateway. Customers need a way to invalidate the cache for each API when they test the API. What should a developer do to give customers the ability to invalidate the API cache?

A. Ask the customers to use AWS credentials to call the InvalidateCache API operation.
B. Attach an InvalidateCache policy to the IAM execution role that the customers use to invoke the API. Ask the customers to send a request that contains the Cache-Control:max-age=0 HTTP header when they make an API call.
C. Ask the customers to use the AWS SDK API Gateway class to invoke the InvalidateCache API operation.
D. Attach an InvalidateCache policy to the IAM execution role that the customers use to invoke the API. Ask the customers to add the INVALIDATE_CACHE query string parameter when they make an API call.

---

**Question 2.** A developer is creating an AWS CloudFormation stack. The stack contains IAM resources with custom names. When the developer tries to deploy the stack, they receive an InsufficientCapabilities error. What should the developer do to resolve this issue?

A. Specify the CAPABILITY_AUTO_EXPAND capability in the CloudFormation stack.
B. Use an administrators role to deploy IAM resources with CloudFormation.
C. Specify the CAPABILITY_IAM capability in the CloudFormation stack.
D. Specify the CAPABILITY_NAMED_IAM capability in the CloudFormation stack.

---

**Question 3.** A developer is preparing to begin development of a new version of an application. The previous version of the application is deployed in a production environment. The developer needs to deploy fixes and updates to the current version during the development of the new version of the application. The code for the new version of the application is stored in AWS CodeCommit. Which solution will meet these requirements?

A. From the main branch, create a feature branch for production bug fixes. Create a second feature branch from the main branch for development of the new version.
B. Create a Git tag of the code that is currently deployed in production. Create a Git tag for the new version. Push the two tags to the CodeCommit repository.
C. From the main branch, create a branch of the code that is currently deployed in production. Apply an IAM policy that ensures no other users can push or merge to the branch.
D. Create a new CodeCommit repository for development of the new version of the application. Create a Git tag for the new version.

---

**Question 4.** A developer is building a serverless application that connects to an Amazon Aurora PostgreSQL database. The serverless application consists of hundreds of AWS Lambda functions. During every Lambda function scale out, a new database connection is made that increases database resource consumption. The developer needs to decrease the number of connections made to the database. The solution must not impact the scalability of the Lambda functions. Which solution will meet these requirements?

A. Configure provisioned concurrency for each Lambda function by setting the ProvisionedConcurrentExecutions parameter to 10.
B. Enable the connection manager in Amazon Aurora PostgreSQL. Change the connection string of each Lambda function to point to cluster cache management.
C. Use Amazon RDS Proxy to create a connection pool to manage the database connections. Change the connection string of each Lambda function to reference the proxy.
D. Configure reserved concurrency for each Lambda function by setting the ReservedConcurrentExecutions parameter to 10.

---

**Question 5.** A developer is setting up infrastructure by using AWS CloudFormation. If an error occurs when the resources described in the Cloud Formation template are provisioned, successfully provisioned resources must be preserved. The developer must provision and update the CloudFormation stack by using the AWS CLI. Which solution will meet these requirements?

A. Add an --enable-termination-protection command line option to the create-stack command and the update-stack command.
B. Add a --disable-rollback command line option to the create-stack command and the update-stack command.
C. Add a --parameters ParameterKey=PreserveResources,ParameterValue=True command line option to the create-stack command and the update-stack command.
D. Add a --tags Key=PreserveResources,Value=True command line option to the create-stack command and the update-stack command.

---

**Question 6.** A developer is working on an application that processes operating data from IoT devices. Each IoT device uploads a data file once every hour to an Amazon S3 bucket. The developer wants to immediately process each data file when the data file is uploaded to Amazon S3. The developer will use an AWS Lambda function to process the data files from Amazon S3. The Lambda function is configured with the S3 bucket information where the files are uploaded. The developer wants to configure the Lambda function to immediately invoke after each data file is uploaded. Which solution will meet these requirements?

A. Add an asynchronous invocation to the Lambda function. Select the S3 bucket as the source.
B. Add an Amazon EventBridge event to the Lambda function. Select the S3 bucket as the source.
C. Add a trigger to the Lambda function. Select the S3 bucket as the source.
D. Add a layer to the Lambda function. Select the S3 bucket as the source.

---

**Question 7.** A developer is building an application integrating an Amazon API Gateway with an AWS Lambda function. When calling the API, the developer receives the following error: Wed Nov 08 01:13:00 UTC 2017 : Method completed with status: 502 What should the developer do to resolve the error?

A. Change the HTTP endpoint of the API to an HTTPS endpoint.
B. Change the format of the payload sent to the API Gateway.
C. Change the format of the Lambda function response to the API call.
D. Change the authorization header in the API call to access the Lambda function.

---

**Question 8.** An IT department uses Amazon S3 to store sensitive images. After more than 1 year, the company rarely accesses the images, but the company wants a storage solution that maximizes resiliency. The IT department needs access to the images that have been moved to archival storage within 24 hours. Which solution will meet these requirements MOST cost-effectively?

A. Use S3 Standard-Infrequent Access (S3 Standard-IA) to store the images. Use S3 Glacier Deep Archive with standard retrieval to store and retrieve archived images.
B. Use S3 Standard-Infrequent Access (S3 Standard-IA) to store the images. Use S3 Glacier Deep Archive with bulk retrieval to store and retrieve archived images.
C. Use S3 Intelligent-Tiering to store the images. Use S3 Glacier Deep Archive with standard retrieval to store and retrieve archived images.
D. Use S3 One Zone-Infrequent Access (S3 One Zone-IA) to store the images. Use S3 Glacier Deep Archive with bulk retrieval to store and retrieve archived images.

---

**Question 9.** A company has an application that stores data in Amazon RDS instances. The application periodically experiences surges of high traffic that cause performance problems. During periods of peak traffic, a developer notices a reduction in query speed in all database queries. The team's technical lead determines that a multi-threaded and scalable caching solution should be used to offload the read traffic. The solution needs to improve performance. Which solution will meet these requirements with the LEAST complexity?

A. Use Amazon ElastiCache for Memcached to offload read requests from the main database.
B. Replicate the data to Amazon DynamoDB Set up a DynamoDB Accelerator (DAX) cluster.
C. Configure the Amazon RDS instances to use Multi-AZ deployment with one standby instance. Offload read requests from the main database to the standby instance.
D. Use Amazon ElastiCache for Redis to offload read requests from the main database.

---

**Question 10.** A company has a serverless application on AWS that uses a fleet of AWS Lambda functions that have aliases. The company regularly publishes new Lambda function versions by using an in-house deployment solution. The company wants to improve the release process and to use traffic shifting. A newly published function version should initially make available only to a fixed percentage of production users. Which solution will meet these requirements?

A. Configure routing on the alias of the new function by using a weighted alias.
B. Configure a canary deployment type for Lambda.
C. Configure routing on the new versions by using environment variables.
D. Configure a linear deployment type for Lambda.

---

**Question 11.** A developer is creating a new REST API by using Amazon API Gateway and AWS Lambda. The development team tests the API and validates responses for the known use cases before deploying the API to the production environment. The developer wants to make the REST API available for testing by using API Gateway locally. Which AWS Serverless Application Model Command Line Interface (AWS SAM CLI) subcommand will meet these requirements?

A. Sam local invoke
B. Sam local generate-event
C. Sam local start-lambda
D. Sam local start-api

---

**Question 12.** A developer has created an AWS Lambda function that makes queries to an Amazon Aurora MySQL DB instance. When the developer performs a test, the DB instance shows an error for too many connections. Which solution will meet these requirements with the LEAST operational effort?

A. Create a read replica for the DB instance. Query the replica DB instance instead of the primary DB instance.
B. Migrate the data to an Amazon DynamoDB database.
C. Configure the Amazon Aurora MySQL DB instance for Multi-AZ deployment.
D. Create a proxy in Amazon RDS Proxy. Query the proxy instead of the DB instance.

---

**Question 13.** A company needs to set up database credentials for all its AWS Cloud resources. The company's resources include Amazon RDS DB instances, Amazon DocumentDB clusters, and Amazon Aurora DB instances. The company's security policy mandates that database credentials be encrypted at rest and rotated at a regular interval. Which solution will meet these requirements MOST securely?

A. Set up IAM database authentication for token-based access. Generate user tokens to provide centralized access to RDS DB instances, Amazon DocumentDB clusters, and Aurora DB instances.
B. Create parameters for the database credentials in AWS Systems Manager Parameter Store. Set the Type parameter to SecureString. Set up automatic rotation on the parameters.
C. Store the database access credentials as an encrypted Amazon S3 object in an S3 bucket. Block all public access on the S3 bucket. Use S3 server-side encryption to set up automatic rotation on the encryption key.
D. Create an AWS Lambda function by using the SecretsManagerRotationTemplate template in the AWS Secrets Manager console. Create secrets for the database credentials in Secrets Manager. Set secrets rotation on a schedule.

---

**Question 14.** A company built a new application in the AWS Cloud. The company automated the bootstrapping of new resources with an Auto Scaling group by using AWS CloudFormation templates. The bootstrap scripts contain sensitive data. The company needs a solution that is integrated with CloudFormation to manage the sensitive data in the bootstrap scripts. Which solution will meet these requirements in the MOST secure way?

A. Put the sensitive data into a CloudFormation parameter. Encrypt the CloudFormation templates by using an AWS Key Management Service (AWS KMS) key.
B. Put the sensitive data into an Amazon S3 bucket. Update the CloudFormation templates to download the object from Amazon S3 during bootstrap.
C. Put the sensitive data into AWS Systems Manager Parameter Store as a secure string parameter. Update the CloudFormation templates to use dynamic references to specify template values.
D. Put the sensitive data into Amazon Elastic File System (Amazon EFS). Enforce EFS encryption after file system creation. Update the CloudFormation templates to retrieve data from Amazon EFS.

---

**Question 15.** A company wants to automate part of its deployment process. A developer needs to automate the process of checking for and deleting unused resources that supported previously deployed stacks but are no longer in use. The company has a central application that uses the AWS Cloud Development Kit (AWS CDK) to manage and update the parameter store and to invoke the Lambda functions. The developer's solution must integrate as seamlessly as possible within the current deployment process. Which solution will meet these requirements with the LEAST amount of configuration?

A. In the central AWS CDK application, write a handler function in the code that uses AWS SDK to check for and delete unused resources. Create an AWS Lambda function and invoke the Lambda function when the deployment stack runs.
B. In the central AWS CDK application, write a handler function in the code that uses AWS SDK to check for and delete unused resources. Use the cdk CustomResource construct to deploy the function code to an AWS Lambda function and to invoke the Lambda function when the deployment stack runs.
C. In the central AWS CDK, write a handler function in the code that uses AWS SDK to check for and delete unused resources. Create an AWS Lambda function and use the cdk CustomResource construct to import the Lambda function into the stack and to invoke the Lambda function when the deployment stack runs.
D. In the AWS Lambda console, write a handler function in the code that uses AWS SDK to check for and delete unused resources. Use the cdk CustomResource construct to import the Lambda function into the stack and to invoke the Lambda function when the deployment stack runs.

---

**Question 16.** A company has developed a new serverless application using AWS Lambda functions that will be deployed using the AWS Serverless Application Model (AWS SAM) CLI. Which step should the developer complete prior to deploying the application?

A. Compress the application to a .zip file and upload it into AWS Lambda.
B. Test the new AWS Lambda function by first tracing it in AWS X-Ray.
C. Bundle the serverless application using a SAM package.
D. Create the application environment using the eb create my-env command.

---

**Question 17.** A company is migrating its PostgreSQL database into the AWS Cloud. The company wants to use a database that will secure and regularly rotate database credentials. The company wants a solution that does not require additional programming overhead. Which solution will meet these requirements?

A. Use Amazon Aurora PostgreSQL for the database. Store the database credentials in AWS Systems Manager Parameter Store. Turn on rotation.
B. Use Amazon Aurora PostgreSQL for the database. Store the database credentials in AWS Secrets Manager. Turn on rotation.
C. Use Amazon DynamoDB for the database. Store the database credentials in AWS Systems Manager Parameter Store. Turn on rotation.
D. Use Amazon DynamoDB for the database. Store the database credentials in AWS Secrets Manager. Turn on rotation.

---

**Question 18.** A developer is testing an application that invokes an AWS Lambda function asynchronously. During the testing phase, the Lambda function fails to process after two retries. How can the developer troubleshoot the failure?

A. Configure AWS CloudTrail logging to investigate the invocation failures.
B. Configure Dead Letter Queues by sending events to Amazon SQS for investigation.
C. Configure Amazon Simple Workflow Service to process any direct unprocessed events.
D. Configure AWS Config to process any direct unprocessed events.

---

**Question 19.** A company needs to distribute firmware updates to its customers around the world. Which service will allow easy and secure control of the access to the downloads at the lowest cost?

A. Use Amazon CloudFront with signed URLs for Amazon S3.
B. Create a dedicated Amazon CloudFront Distribution for each customer.
C. Use Amazon CloudFront with AWS Lambda@Edge.
D. Use Amazon API Gateway and AWS Lambda to control access to an S3 bucket.

---

**Question 20.** A company has an ecommerce application. To track product reviews, the company's development team uses an Amazon DynamoDB table. Every record includes the following:
- A Review ID, a 16-digit universally unique identifier (UUID)
- A Product ID and User ID, 16-digit UUIDs that reference other tables
- A Product Rating on a scale of 1-5
- An optional comment from the user
The table partition key is the Review ID. The most performed query against the table is to find the 10 reviews with the highest rating for a given product. Which index will provide the FASTEST response for this query?

A. A global secondary index (GSI) with Product ID as the partition key and Product Rating as the sort key
B. A global secondary index (GSI) with Product ID as the partition key and Review ID as the sort key
C. A local secondary index (LSI) with Product ID as the partition key and Product Rating as the sort key
D. A local secondary index (LSI) with Review ID as the partition key and Product ID as the sort key

---

**Question 21.** A developer is storing sensitive data generated by an application in Amazon S3. The developer wants to encrypt the data at rest. A company policy requires an audit trail of when the AWS Key Management Service (AWS KMS) key was used and by whom. Which encryption option will meet these requirements?

A. Server-side encryption with Amazon S3 managed keys (SSE-S3)
B. Server-side encryption with AWS KMS managed keys (SSE-KMS)
C. Server-side encryption with customer-provided keys (SSE-C)
D. Server-side encryption with self-managed keys

---

**Question 22.** A development team maintains a web application by using a single AWS RDS template. The template defines web servers and an Amazon RDS database. The team uses the CloudFormation template to deploy the CloudFormation stack to different environments. During a recent application deployment, a developer caused the primary development database to be dropped and recreated. The result of this incident was a loss of data. The team needs to avoid accidental database deletion in the future. Which solutions will meet these requirements? (Choose two.)

A. Add a CloudFormation DeletionPolicy attribute with the Retain value to the database resource.
B. Update the CloudFormation stack policy to prevent updates to the database.
C. Modify the database to use a Multi-AZ deployment.
D. Create a CloudFormation stack set for the web application and database deployments.
E. Add a CloudFormation DeletionPolicy attribute with the Retain value to the stack.

---

**Question 23.** A developer needs to deploy an application running on AWS Fargate using Amazon ECS. The application has environment variables that must be passed to a container for the application to initialize. How should the environment variables be passed to the container?

A. Define an array that includes the environment variables under the environment parameter within the service definition.
B. Define an array that includes the environment variables under the environment parameter within the task definition.
C. Define an array that includes the environment variables under the entryPoint parameter within the task definition.
D. Define an array that includes the environment variables under the entryPoint parameter within the service definition.

---

**Question 24.** A developer has been asked to create an AWS Lambda function that is invoked any time updates are made to items in an Amazon DynamoDB table. The function has been created, and appropriate permissions have been added to the Lambda execution role. Amazon DynamoDB streams have been enabled for the table, but the function is still not being invoked. Which option would enable DynamoDB table updates to invoke the Lambda function?

A. Change the StreamViewType parameter value to NEW_AND_OLD_IMAGES for the DynamoDB table.
B. Configure event source mapping for the Lambda function.
C. Map an Amazon Simple Notification Service (Amazon SNS) topic to the DynamoDB streams.
D. Increase the maximum runtime (timeout) setting of the Lambda function.

---

**Question 25.** A developer is building a web application that uses Amazon API Gateway to expose an AWS Lambda function to process requests from clients. During testing, the Developer notices that the API Gateway times out even though the Lambda function finishes under the set time limit. Which of the following API Gateway metrics in Amazon CloudWatch can help the Developer troubleshoot the issue? (Choose two.)

A. CacheHitCount
B. IntegrationLatency
C. CacheMissCount
D. Latency
E. Count

---

**Question 26.** A developer is creating an Amazon DynamoDB table. The entire table must be encrypted at rest. Which solution will meet this requirement MOST cost-effectively?

A. Create the DynamoDB table by using default encryption settings.
B. Encrypt the data by using the DynamoDB Encryption Client.
C. During creation of the DynamoDB table, configure encryption at rest with an AWS Key Management Service (AWS KMS) AWS managed key.
D. During creation of the DynamoDB table, configure encryption at rest with an AWS Key Management Service (AWS KMS) customer managed key.

---

**Question 27.** A company developed an API application on AWS by using Amazon CloudFront, Amazon API Gateway, and AWS Lambda. The API has a minimum of four requests every second. A developer notices that many API users run the same query by using the POST method. The developer wants to cache the POST requests to optimize the API resources. Which solution will meet these requirements?

A. Configure the CloudFront cache. Update the application to return cached content based upon the default request headers.
B. Override the cache method in the selected stage of API Gateway. Select the POST method.
C. Save the latest request response in Lambda /tmp directory. Update the Lambda function to check the /tmp directory.
D. Save the latest request in AWS Systems Manager Parameter Store. Modify the Lambda function to take the latest request response from Parameter Store.

---

**Question 28.** An application writes items to an Amazon DynamoDB table. As the application scales to thousands of instances, calls to the DynamoDB API generate occasional ThrottlingException errors. The application is coded in a language incompatible with the AWS SDK. How should the error be handled?

A. Add exponential backoff to the application logic
B. Use Amazon SQS as an API message bus
C. Pass API calls through Amazon API Gateway
D. Send the items to DynamoDB through Amazon Kinesis Data Firehose

---

**Question 29.** A company has an application that runs as a series of AWS Lambda functions. Each Lambda function receives data from an Amazon Simple Notification Service (Amazon SNS) topic and writes the data to an Amazon Aurora DB instance. To comply with an information security policy, the company must ensure that the Lambda functions all use a single securely encrypted database connection string to access Aurora. Which solution will meet these requirements?

A. Use IAM database authentication for Aurora to enable secure database connections for all the Lambda functions.
B. Store the credentials and read the credentials from an encrypted Amazon RDS DB instance.
C. Store the credentials in AWS Systems Manager Parameter Store as a secure string parameter.
D. Use Lambda environment variables with a shared AWS Key Management Service (AWS KMS) key for encryption.

---

**Question 30.** A company needs to distribute firmware updates to its customers around the world. Which service will allow easy and secure control of the access to the downloads at the lowest cost?

A. Use Amazon CloudFront with signed URLs for Amazon S3
B. Create a dedicated Amazon CloudFront Distribution for each customer
C. Use Amazon CloudFront with AWS Lambda@Edge
D. Use Amazon API Gateway and AWS Lambda to control access to an S3 bucket

---

**Question 31.** A company caches session information for a web application in an Amazon DynamoDB table. The company wants an automated way to delete old items from the table. What is the simplest way to do this?

A. Write a script that deletes old records; schedule the script as a cron job on an Amazon EC2 instance.
B. Add an attribute with the expiration time; enable the Time To Live feature based on that attribute.
C. Each day, create a new table to hold session data; delete the previous day's table.
D. Add an attribute with the expiration time; name the attribute ItemExpiration.

---

**Question 32.** A developer is using AWS Elastic Beanstalk to create a deployment for a web application that supports ecommerce. According to a company requirement, Amazon EC2 instances that host one version of the application must be retired when the deployment of a new version is complete. Which deployment methods can the developer use to meet this requirement? (Choose two.)

A. All-al-once deployment
B. In-place deployment
C. Rolling deployment without an additional batch
D. Blue/green deployment
E. Immutable deployment

---

**Question 33.** A developer is building a web and mobile application for two types of users: regular users and guest users. Regular users are required to log in, but guest users do not log in. Users should see only their own data, regardless of whether they authenticate. Users need AWS credentials before they can access AWS resources. What is the MOST secure solution that the developer can implement to allow access for guest users?

A. Use Amazon Cognito credentials provider to issue temporary credentials that are linked to an unauthenticated role that has access to the required resources.
B. Set up an IAM user that has permissions to the required resources. Hardcode the IAM credentials in the web and mobile application.
C. Generate temporary keys that are stored in AWS Key Management Service (AWS KMS). Use the temporary keys to access the required resources.
D. Generate temporary credentials. Store the temporary credentials in AWS Secrets Manager. Use the temporary credentials to access the required resources.

---

**Question 34.** An application that is deployed to Amazon EC2 is using Amazon DynamoDB. The application calls the DynamoDB REST API. Periodically, the application receives a ProvisionedThroughputExceededException error when the application writes to a DynamoDB table. Which solutions will mitigate this error MOST cost-effectively? (Choose two.)

A. Modify the application code to perform exponential backoff when the error is received.
B. Modify the application to use the AWS SDKs for DynamoDB.
C. Increase the read and write throughput of the DynamoDB table.
D. Create a DynamoDB Accelerator (DAX) cluster for the DynamoDB table.
E. Create a second DynamoDB table. Distribute the reads and writes between the two tables.

---

**Question 35.** A developer is modifying an existing AWS Lambda function. While checking the code, the developer notices hardcoded parameter values for an Amazon RDS for SQL Server user name, database, host, and port. There are also hardcoded parameter values for an Amazon S3 bucket and an Amazon Simple Notification Service (Amazon SNS) topic. The developer wants to store the credentials in an encrypted format in a centralized location so that the developer can also to turn on rotation for the credentials. The developer also wants to update the parameter values without modifying code in other applications and to update the parameter values without modifying code. Which solution will meet these requirements?

A. Create an RDS database secret in AWS Secrets Manager. Set the user name, database, host, and port. Turn on secret rotation. Create SecureString parameters in AWS Systems Manager Parameter Store for the DynamoDB table, S3 bucket, and SNS topic. Turn on rotation.
B. Create an RDS database secret in AWS Secrets Manager. Set the user name, database, host, and port. Turn on secret rotation. Create SecureString parameters in AWS Systems Manager Parameter Store for the DynamoDB table, S3 bucket, and SNS topic.
C. Create RDS database parameters in AWS Systems Manager Parameter Store for the user name, database, host, and port. Turn on rotation. Create a Lambda function and use the cdk CustomResource construct. Schedule the credentials rotation. Schedule the function with an Amazon CloudWatch event every minute.
D. Create RDS database parameters in AWS Systems Manager Parameter Store for the user name, database, host, and port. Store the DynamoDB table, S3 bucket, and SNS topic in Amazon S3. Create a Lambda function and use the cdk CustomResource construct. Schedule the credentials rotation. Invoke the Lambda function on a schedule.

---

**Question 36.** A mobile app stores blog posts in an Amazon DynamoDB table. Millions of posts are added every day, and each post represents a single item in the table. The mobile app requires only recent posts. Any post that is older than 48 hours can be removed. What is the MOST cost-effective way to delete posts that are older than 48 hours?

A. For each item, add a new attribute of type String that has a timestamp that is set to the blog post creation time. Create a global secondary index (GSI) with the new attribute as the sort key. Create an AWS Lambda function to scan the GSI and remove posts that are older than 48 hours by using the BatchWriteItem API operation. Place the script in a container image. Schedule an Amazon Elastic Container Service (Amazon ECS) task that invokes the container to run every 5 minutes.
B. For each item, add a new attribute of type String that has a timestamp that is set to the blog post creation time. Create a global secondary index (GSI) with the new attribute as the partition key and remove posts that are older than 48 hours by using the BatchWriteItem API operation. Place the script in a container image. Schedule an Amazon Elastic Container Service (Amazon ECS) task that invokes the container to run every 5 minutes.
C. For each item, add a new attribute of type Date that has a timestamp that is set to 48 hours after the blog post creation time. Create a global secondary index (GSI) with the new attribute as a sort key. Create an AWS Lambda function to scan the table and remove posts that are older than 48 hours by using the BatchWriteItem API operation. Schedule the function with an Amazon CloudWatch event every minute.
D. For each item, add a new attribute of type Number that has a timestamp that is set to 48 hours after the blog post creation time. Configure the DynamoDB table with a TTL that references the new attribute.

---

**Question 37.** A developer has an application that is composed of many different AWS Lambda functions. The Lambda functions all use some of the same dependencies. To avoid security issues, the developer is constantly updating the dependencies of all of the Lambda functions. The result is duplicated effort for each function. How can the developer keep the dependencies of the Lambda functions up to date with the LEAST additional complexity?

A. Define a maintenance window for the Lambda functions to ensure that the functions get updated copies of the dependencies.
B. Upgrade the Lambda functions to the most current runtime version.
C. Define a Lambda layer that contains all of the shared dependencies.
D. Use an AWS CodeCommit repository to host the dependencies in a centralized location.

---

**Question 38.** A developer at a company recently created a serverless application to process and show data from files. The application's user interface (UI) allows users to select and start processing the files. The UI displays a message when the result is available to view. The application uses AWS Step Functions with AWS API Gateway and AWS Lambda functions to process the files. The company's IT team reports that the request to process a file is often returning timeout errors. The application must be updated so that the UI can display a message while the files are being processed. The backend process that is invoked by the API needs to send an email message when the report processing is complete. What should the developer do to meet these requirements?

A. Change the API Gateway route to add an X-Amz-Invocation-Type header with a static value of 'Event' in the integration request. Deploy the API Gateway stage to apply the changes.
B. Change the configuration of the Lambda function that implements the request to process a file. Configure the maximum concurrency of the Lambda function to process the file. Deploy the API Gateway stage to apply the changes.
C. Change the API Gateway timeout value to match the Lambda function timeout value. Deploy the API Gateway stage to apply the changes.
D. Change the API Gateway route to add an X-Amz-Target header with a static value of 'Async' in the integration request. Deploy the API Gateway stage to apply the changes.

---

**Question 39.** A developer accesses AWS CodeCommit over SSH. The SSH keys configured to access AWS CodeCommit are tied to a user with the following permissions: "codecommit:CreateBranch" "codecommit:Put**" The developer needs to create/delete branches. Which specific IAM permissions need to be added, based on the principle of least privilege?

A. "codecommit:CreateBranch"
B. "codecommit:Put**"
C. "codecommit:IAMUpdate**"
D. "codecommit:**"

---

**Question 40.** A developer is working on an AWS Lambda function that accesses Amazon DynamoDB. The Lambda function must retrieve an item and update some of its attributes, or create the item if it does not exist. The Lambda function has access to the primary key. Which IAM permissions should the developer request for the Lambda function to achieve this functionality?

A. dynamodb:DeleteItem, dynamodb:GetItem, dynamodb:PutItem
B. dynamodb:UpdateItem, dynamodb:GetItem, dynamodb:DescribeTable
C. dynamodb:GetRecords, dynamodb:PutItem, dynamodb:UpdateTable
D. dynamodb:UpdateItem, dynamodb:GetItem, dynamodb:PutItem

---

**Question 41.** A Developer created configuration specifications for an AWS Elastic Beanstalk application in a file named healthcheckurl.yaml in the .ebextensions/directory of their application source bundle. The file contains the following:

option_settings:
  - namespace: aws:elasticbeanstalk:application
    option_name: Application Healthcheck URL
    value: /health-check

After the application launches, the health check is not being run on the correct path, even though it is valid. What can be done to correct this configuration file?

A. Convert the file to JSON format.
B. Rename the file to a .config extension.
C. Change the configuration section from options_settings to resources.
D. Change the namespace of the option settings to a custom namespace.

---

**Question 42.** A developer is building a serverless application that is based on AWS Lambda. The developer initializes the AWS software development kit (SDK) outside of the Lambda handler function. What is the PRIMARY benefit of this action?

A. Improves legibility and stylistic convention
B. Takes advantage of runtime environment reuse
C. Provides better error handling
D. Creates a new SDK instance for each invocation

---

**Question 43.** A developer at a company needs to create a small application that makes the same API call once each day at a designated time. The company does not have infrastructure in the AWS Cloud yet, but the company wants to implement this functionality on AWS. Which solution meets these requirements in the MOST operationally efficient manner?

A. Use a Kubernetes cron job that runs on Amazon Elastic Kubernetes Service (Amazon EKS).
B. Use an Amazon Linux crontab scheduled job that runs on Amazon EC2.
C. Use an AWS Lambda function that is invoked by an Amazon EventBridge scheduled event.
D. Use an AWS Batch job that is submitted to an AWS Batch job queue.

---

**Question 44.** A developer has code that is stored in an Amazon S3 bucket. The code must be deployed as an AWS Lambda function across multiple accounts in the same AWS Region as the S3 bucket. An AWS CloudFormation template that runs for each account will deploy the Lambda function. What is the MOST secure way to allow CloudFormation to access the Lambda code in the S3 bucket?

A. Grant the CloudFormation service role the S3 ListBucket and GetObject permissions. Add a bucket policy to Amazon S3 with the principal of "AWS": [account numbers].
B. Grant the CloudFormation service role the S3 GetObject permission. Add a bucket policy to Amazon S3 with the principal of "AWS": "**".
C. Use a service-based link to grant the Lambda function the S3 ListBucket and GetObject permissions by explicitly adding the S3 bucket's account number in the resource.
D. Use a service-based link to grant the Lambda function the S3 GetObject permission. Add a resource of "**" to allow access to the S3 bucket.

---

**Question 45.** An application that runs on AWS Lambda requires access to specific highly confidential objects in an Amazon S3 bucket. In accordance with the principle of least privilege, a company grants access to the S3 bucket by using only temporary credentials. How can a developer configure access to the S3 bucket in the MOST secure way?

A. Hardcode the credentials that are required to access the S3 objects in the application code. Use the credentials to access the required S3 objects.
B. Create a secret access key and access key ID with permission to access the S3 bucket. Store the key and key ID in AWS Secrets Manager. Configure the application to retrieve the Secrets Manager secret and use the credentials to access the S3 objects.
C. Create a Lambda function execution role. Attach a policy to the role that grants access to specific objects in the S3 bucket.
D. Create a secret access key and access key ID with permission to access the S3 bucket. Store the key and key ID as environment variables in Lambda. Use the environment variables to access the required S3 objects.

---

**Question 46.** When using the AWS Encryption SDK, how does the developer keep track of the data encryption keys used to encrypt data?

A. The developer must manually keep track of the data encryption keys used for each data object.
B. The SDK encrypts the data encryption key and stores it (encrypted) as part of the returned ciphertext.
C. The SDK stores the data encryption keys automatically in Amazon S3.
D. The data encryption key is stored in the Userdata for the EC2 instance.

---

**Question 47.** A developer is troubleshooting an application that uses Amazon DynamoDB in the us-west-2 Region. The application is deployed to an Amazon EC2 instance. The application requires read-only permissions to a table that is named Cars. The EC2 instance has an attached IAM role that contains the following IAM policy:

When the application tries to read from the Cars table, an Access Denied error is returned. How can the developer resolve this error?

A. Modify the IAM policy resource to "arn:aws:dynamodb:us-west-2:account-id:table/**".
B. Modify the IAM policy to include the dynamodb:* action.
C. Create a trust policy that specifies the EC2 service principal. Associate the role with the policy.
D. Create a trust relationship between the role and dynamodb.amazonaws.com.

---

**Question 48.** A developer has observed an increase in bugs in the AWS Lambda functions that a development team has deployed. The developer wants to implement automated testing of Lambda functions in an environment that closely simulates the Lambda environment. The developer also needs to implement automated testing of Lambda functions. The developer also needs to integrate the tests into the team's continuous integration and continuous delivery (CI/CD) pipeline before the AWS Cloud Development Kit (AWS CDK) deployment. Which solution will meet these requirements?

A. Create sample events based on the Lambda documentation. Create automated test scripts that use the sam local invoke command to invoke the Lambda functions. Check the response. Document the test scripts for the other developers on the team. Update the CI/CD command to run the unit testing framework.
B. Install a unit testing framework in the Lambda execution environment to replace the Lambda execution environment by using a unit testing framework. Create sample events for the other Lambda functions. Document how to run the unit testing framework. Update the CI/CD command to run the unit testing framework.
C. Use the AWS Serverless Application Model (AWS SAM) CLI. Use the sam local invoke command to generate sample events for the automated tests. Create automated test scripts that use the sam local invoke command to invoke the Lambda functions. Check the response. Update the CI/CD/pipeline to run the Docker container.
D. Create sample events based on the Lambda documentation. Create a Docker container from the Node.js base image to simulate the Lambda execution environment. Document the test scripts for the other developers on the team. Update the CI/CD pipeline to run the Docker container.

---

**Question 49.** A developer wants to deploy a new version of an AWS Elastic Beanstalk application. During deployment, the application must maintain full capacity and avoid service interruption. Additionally, the developer must minimize the cost of additional resources that support the deployment. Which deployment method should the developer use to meet these requirements?

A. All at once
B. Rolling with additional batch
C. Blue/green
D. Immutable

---

**Question 50.** A developer must analyze performance issues with production-distributed applications written as AWS Lambda functions. These distributed Lambda applications invoke other components that make up the applications. How should the developer identify and troubleshoot the root cause of the performance issues in production?

A. Add logging statements to the Lambda functions, then use Amazon CloudWatch to view the logs.
B. Use AWS CloudTrail and then examine the logs.
C. Use AWS X-Ray, then examine the segments and errors.
D. Run Amazon Inspector agents and then analyze performance.

---

**Question 51.** A Development team has pushed out 10 applications running on several Amazon EC2 instances. The Operations team is asking for a graphical representation of one key performance metric for each application. These metrics should be available on one screen for easy monitoring. Which steps should the Developer take to accomplish this using Amazon CloudWatch?

A. Create a custom namespace with a unique metric name for each application.
B. Create a custom dimension with a unique metric name for each application.
C. Create a custom event with a unique metric name for each application.
D. Create a custom alarm with a unique metric name for each application.

---

**Question 52.** A developer is creating a serverless website with content that includes HTML files, images, videos, and JavaScript (client-side scripts). Which combination of services should the Developer use to create the website?

A. Amazon S3 and Amazon CloudFront
B. Amazon EC2 and Amazon ElastiCache
C. Amazon ECS and Redis
D. AWS Lambda and Amazon API Gateway

---

**Question 53.** An application runs on multiple EC2 instances behind an ELB. Where is the session data best written so that it can be served reliably across multiple requests?

A. Write data to Amazon ElastiCache.
B. Write data to Amazon Elastic Block Store.
C. Write data to Amazon EC2 Instance Store.
D. Write data to the root filesystem.

---

**Question 54.** A company uses Amazon DynamoDB for managing and tracking orders. The DynamoDB table is partitioned based on the order date. The company receives a huge increase in orders during a sales event, causing DynamoDB writes to throttle, and the consumed throughput is far below the provisioned throughput. According to AWS best practices, how can this issue be resolved with MINIMAL costs?

A. Create a new DynamoDB table for every order date.
B. Increase the read and write capacity units of the DynamoDB table.
C. Add a random number suffix to the partition key values.
D. Add a global secondary index to the DynamoDB table.

---

**Question 55.** A developer is writing a serverless application that requires an AWS Lambda function to be invoked every 10 minutes. What is an automated and serverless way to invoke the function?

A. Deploy an Amazon EC2 instance based on Linux, and edit its /etc/crontab file by adding a command to periodically invoke the Lambda function.
B. Configure an environment variable named PERIOD for the Lambda function. Set the value to 600.
C. Create an Amazon EventBridge rule that runs on a regular schedule to invoke the Lambda function.
D. Create an Amazon Simple Notification Service (Amazon SNS) topic that has a subscription to the Lambda function with a 600-second timer.

---

**Question 56.** A developer maintains applications that store several secrets in AWS Secrets Manager. The applications use secrets that have changed over time. The developer needs to identify required secrets that are still in use. The developer does not want to cause any application downtime. What should the developer do to meet these requirements?

A. Configure an AWS CloudTrail log file delivery to an Amazon S3 bucket. Create an Amazon CloudWatch alarm for the GetSecretValue Secrets Manager API operation requests.
B. Create a secretsmanager-secret-unused AWS Config managed rule. Create an Amazon EventBridge rule to initiate notifications when the AWS Config managed rule is met.
C. Deactivate the applications secrets and monitor the applications error logs temporarily.
D. Configure AWS X-Ray for the applications. Create a sampling rule to match the GetSecretValue Secrets Manager API operation requests.

---

**Question 57.** A company uses a custom root certificate authority certificate chain (Root CA Cert) that is 10 KB in size to generate SSL certificates for its on-premises HTTPS endpoints. One of the company's cloud-based applications has hundreds of AWS Lambda functions that pull data from these endpoints. A developer updated the trust store of the Root CA Cert as a text file in the Lambda deployment bundle. After 3 years of development, the Root CA Cert is no longer valid and must be updated. The developer needs a solution that updates all Lambda functions that use the Root CA Cert. The solution must also work for all development, testing, and production environments. Each environment is managed in a separate AWS account. Which combination of steps should the developer take to meet these requirements MOST cost-effectively? (Choose two.)

A. Store the Root CA Cert as a secret in AWS Secrets Manager. Create a resource-based policy. Add IAM users to allow access to the policy.
B. Store the Root CA Cert as a SecureString parameter in AWS Systems Manager Parameter Store. Create a resource-based policy. Add IAM users to allow access to the policy.
C. Store the Root CA Cert in an Amazon S3 bucket. Create a resource-based policy to allow access to the bucket.
D. Refactor the Lambda code to load the Root CA Cert from the Root CA Cert's location. Modify the runtime trust store inside the Lambda function handler.
E. Refactor the Lambda code to load the Root CA Cert from the Root CA Cert's location. Modify the runtime trust store outside the Lambda function handler.

---

**Question 58.** A company has multiple Amazon VPC endpoints in the same VPC. A developer needs to configure an Amazon S3 bucket policy so users can access an S3 bucket only by using these VPC endpoints. Which solution will meet these requirements?

A. Create multiple S3 bucket polices by using each VPC endpoint ID that have the aws:SourceVpce value in the StringNotEquals condition.
B. Create a single S3 bucket policy that has the aws:SourceVpce value and in the StringEquals condition to use vpc-*.
C. Create a single S3 bucket policy that has the aws:SourceVpce value and in the StringNotEquals condition to use vpc-*.
D. Create a single S3 bucket policy that has multiple aws:sourceVpce value in the StringEquals condition. Repeat for all the VPC endpoint IDs.

---

**Question 59.** A team of developers is using an AWS CodePipeline pipeline as a continuous integration and continuous delivery (CI/CD) mechanism for a web application. A developer has written unit tests to programmatically test the functionality of the application code. The unit tests produce a test report that shows the results of each individual test. The developer now wants to integrate the tests automatically during the CI/CD process. Which solution will meet this requirement with the LEAST operational effort?

A. Write a Git pre-commit hook that runs the tests before every commit. Ensure that each developer who is working on the project has the hook installed locally. Review the test report and resolve any issues before pushing changes to AWS CodeCommit.
B. Add a new stage to the pipeline. Use AWS CodeBuild as the provider. Add the new stage after the stage that deploys code revisions to the test environment. Write a buildspec that fails the CodeBuild build if any test does not pass. View the test results in CodeBuild. Resolve any issues.
C. Add a new stage to the pipeline. Use AWS CodeBuild as the provider. Add the new stage after the stage that deploys code revisions to the test environment. Write a buildspec that fails the CodeBuild build if any test does not pass. Integrate the report with the CodeBuild console. View the test results in CodeBuild. Resolve any issues.
D. Add a new stage to the pipeline. Use Jenkins as the provider. Configure CodePipeline to use Jenkins to run the unit tests. Write a Jenkinsfile that fails the pipeline if any test does not pass. View the test results in Jenkins. Resolve any issues.

---

**Question 60.** A developer is planning to migrate on-premises company data to Amazon S3. The data must be encrypted, and the encryption keys must support automatic annual rotation. The company must use AWS Key Management Service (AWS KMS) to encrypt the data. Which type of keys should the developer use to meet these requirements?

A. Amazon S3 managed keys
B. Symmetric customer managed keys with key material that is generated by AWS
C. Asymmetric customer managed keys with key material that is generated by AWS
D. Symmetric customer managed keys with imported key material

---

**Question 61.** An organization is using Amazon CloudFront to ensure that its users experience low-latency access to its web application. The organization has identified a need to encrypt all traffic between users and CloudFront, and all traffic between CloudFront and the web application. How can these requirements be met? (Choose two.)

A. Use AWS KMS to encrypt traffic between CloudFront and the web application.
B. Set the Origin Protocol Policy to "HTTPS Only".
C. Set the Origin's HTTP Port to 443.
D. Set the Viewer Protocol Policy to "HTTPS Only" or "Redirect HTTP to HTTPS".
E. Enable the CloudFront option Restrict Viewer Access.

---

**Question 62.** A developer is trying to get data from an Amazon DynamoDB table called demoman-table. The developer configured the AWS CLI to use a specific IAM user's credentials. The developer ran the following command: aws dynamodb get-item --table-name demoman-table --key '{"id": {"N":"1993"}}' The command returned errors and no rows were returned. What is the MOST likely cause of these issues?

A. The command is incorrect; it should be rewritten to use put-item with a string argument.
B. The developer needs to log a ticket with AWS Support to enable access to the demoman-table.
C. Amazon DynamoDB cannot be accessed from the AWS CLI and needs to be called via the REST API.
D. The IAM user needs an associated policy with read access to demoman-table.

---

**Question 63.** A developer is building an application that gives users the ability to view bank accounts from multiple sources in a single dashboard. The developer has automated the process to retrieve API credentials for these sources. The process invokes an AWS Lambda function that is associated with an AWS CloudFormation custom resource. The developer wants a solution that will store the API credentials with minimal operational overhead. Which solution will meet these requirements in the MOST secure way?

A. Use the AWS SDK ssm:PutParameter operation in the Lambda function from the existing custom resource to store the credentials as a SecureString parameter. Set the CloudFormation resource value to reference the new credentials. Set the parameter type to SecureString.
B. Use the AWS SDK ssm:PutParameter operation in the Lambda function from the existing custom resource to store the credentials as a parameter. Set the CloudFormation resource value to reference the new credentials. Set the parameter type to SecureString. Set the NoEcho attribute to true.
C. Add an AWS Systems Manager Parameter Store resource to the CloudFormation template. Set the CloudFormation resource value to reference the new credentials. Set the parameter type to SecureString.
D. Use the AWS SDK ssm:PutParameter operation in the Lambda function from the existing custom resource to store the credentials as a parameter. Set the CloudFormation resource value to reference the new credentials. Set the parameter type to SecureString. Set the NoEcho attribute to true.

---

**Question 64.** A developer is building an application that uses AWS API Gateway APIs, AWS Lambda functions, and AWS DynamoDB tables. The developer uses the AWS Serverless Application Model (AWS SAM) to build and run serverless applications on AWS. Each time the developer pushes changes for only to the Lambda functions, all the artifacts in the application are rebuilt. The developer wants to implement AWS SAM Accelerate by running a command to only redeploy the Lambda functions that have changed. Which command will meet these requirements?

A. sam deploy --force-upload
B. sam deploy --no-execute-changeset
C. sam package
D. sam sync --watch

---

**Question 65.** A developer is creating an AWS Lambda function that searches for items from an Amazon DynamoDB table that contains customer contact information. The DynamoDB table items have the customer's email_address as the partition key and additional properties such as customer_type, name and job_title. The Lambda function runs whenever a user types a new character into the customer_type text input. The developer wants the search to return partial matches of all the email_address property of a particular customer_type. The developer does not want to recreate the DynamoDB table. Which solution will meet these requirements?

A. Add a global secondary index (GSI) to the DynamoDB table with customer_type as the partition key and email_address as the sort key. Perform a query on the GSI by using the begins_with key condition expression with the email_address property.
B. Add a global secondary index (GSI) to the DynamoDB table with email_address as the partition key and customer_type as the sort key. Perform a query on the GSI by using the begins_with key condition expression with the email_address property.
C. Add a local secondary index (LSI) to the DynamoDB table with customer_type as the partition key and email_address as the sort key. Perform a query on the LSI by using the begins_with key condition expression with the email_address property.
D. Add a local secondary index (LSI) to the DynamoDB table with job_title as the partition key and email_address as the sort key. Perform a query on the LSI by using the begins_with key condition expression with the email_address property.

---

**Question 66.** A company has an Amazon S3 bucket containing premier content that it intends to make available to only paid subscribers of its website. The S3 bucket currently has default permissions of all objects being private to prevent inadvertent exposure of the premier content to non-paying website visitors. How can the company limit the ability to download a file in the S3 bucket to paid subscribers only?

A. Apply a bucket policy that allows anonymous users to download the content from the S3 bucket.
B. Generate a pre-signed object URL for the premier content file when a paid subscriber requests a download.
C. Add a bucket policy that requires multi-factor authentication for requests to access the S3 bucket objects.
D. Enable server-side encryption on the S3 bucket for data protection against the non-paying website visitors.

---

**Question 67.** A company's website runs on an Amazon EC2 instance and uses Auto Scaling to scale the environment during peak times. Website users across the world are experiencing high latency due to static content on the EC2 instance, even during non-peak hours. Which combination of steps will resolve the latency issue? (Choose two.)

A. Double the Auto Scaling group's maximum number of servers.
B. Host the application code on AWS Lambda.
C. Scale vertically by resizing the EC2 instances.
D. Create an Amazon CloudFront distribution to cache the static content.
E. Store the application's static content in Amazon S3.

---

**Question 68.** An online food company provides an Amazon API Gateway HTTP API to receive orders for partners. The API is backed with an AWS Lambda function. The Lambda function stores the orders in an Amazon DynamoDB table. The company expects to onboard additional partners. Some of the partners require additional Lambda functions to register to the data stream. The company has already created an Amazon S3 bucket. The company needs to ensure that all orders and updates are stored in the S3 bucket for future analysis. How can the developer ensure that all orders and updates are stored in the S3 bucket with the LEAST development effort?

A. Create a new Lambda function and a new API Gateway HTTP endpoint. Configure the new Lambda function to publish updates to the data stream. Configure the Lambda function to write to the S3 bucket.
B. Use Amazon DynamoDB Streams on the DynamoDB table. Create a new Lambda function. Associate the stream's Amazon Resource Name (ARN) with the Lambda function. Configure the Lambda function to write to the S3 bucket as records come through the topic.
C. Enable DynamoDB Streams on the DynamoDB table. Create a new Lambda function. Associate the stream's Amazon Resource Name (ARN) with the Lambda function. Configure the Lambda function to write to the S3 bucket.
D. Modify the Lambda function to publish to a new Amazon Simple Notification Service (Amazon SNS) topic as the Lambda function receives orders. Subscribe a new Lambda function to the topic. Configure the new Lambda function to write to the S3 bucket as records come through the topic.

---

**Question 69.** A developer wants to add request validation to a production environment Amazon API Gateway API. The developer needs to test the changes before the API is deployed to the production environment. For the developer will send test requests to the API before it is deployed to the production environment. Which solution will meet these requirements with the LEAST operational overhead?

A. Export the existing API to an OpenAPI file. Create a new API. Import the OpenAPI file. Modify the new API to add request validation. Perform the tests. Modify the existing API to add request validation. Deploy the existing API to production.
B. Modify the existing API to add request validation. Deploy the updated API to a new API Gateway stage. Perform the tests. Deploy the existing API to the API Gateway production stage.
C. Create a new API. Add the necessary resources and methods, including new request validation. Perform the tests. Modify the existing API to add request validation. Deploy the existing API to production.
D. Clone the existing API. Modify the new API to add request validation. Perform the tests. Modify the existing API to add request validation. Deploy the existing API to production.

---

**Question 70.** A company has an application that uses AWS CodePipeline to automate its continuous integration and continuous delivery (CI/CD) workflow. The application uses AWS CodeCommit for version control. A developer who was working on one of the tasks did not pull the most recent changes from the main branch. A week later, the developer noticed merge conflicts. How can the developer resolve the merge conflicts in the developer's branch with the LEAST development effort?

A. Clone the repository. Create a new branch. Update the branch with the changes.
B. Create a new branch. Apply the changes from the previous branch.
C. Use the Commit Visualizer view to compare the commits when a feature was added. Fix the merge conflicts.
D. Stop the pull from the main branch to the feature branch. Rebase the feature branch from the main branch.

---

**Question 71.** A developer is creating an application for a company. The application needs to read the file doc.txt that is placed in the root folder of an Amazon S3 bucket that is named DOC-EXAMPLE-BUCKET. The company's security team requires the principle of least privilege to be applied to the application's IAM policy. Which IAM policy statement will meet these security requirements?

A.
```json
{
  "Action": [
    "s3:GetObject"
  ],
  "Effect": "Allow",
  "Resource": "arn:aws:s3:::DOC-EXAMPLE-BUCKET/doc.txt"
}
```

B.
```json
{
  "Action": [
    "s3:*"
  ],
  "Effect": "Allow",
  "Resource": "arn:aws:s3:::DOC-EXAMPLE-BUCKET/*"
}
```

C.
```json
{
  "Action": [
    "s3:*"
  ],
  "Effect": "Allow",
  "Resource": "arn:aws:s3:::DOC-EXAMPLE-BUCKET/"
}
```

D.
```json
{
  "Action": [
    "s3:GetObject"
  ],
  "Effect": "Allow",
  "Resource": "arn:aws:s3:::DOC-EXAMPLE-BUCKET/*"
}
```

---

**Question 72.** Users are reporting errors in an application. The application consists of several microservices that are deployed on Amazon Elastic Container Service (Amazon ECS) with AWS Fargate. Which combination of steps should a developer take to fix the errors? (Choose two.)

A. Deploy AWS X-Ray as a sidecar container to the Fargate cluster. Update the task role policy to allow access to the X-Ray API.
B. Deploy AWS X-Ray as a daemonset to the Fargate cluster. Update the service role policy to allow access to the X-Ray API.
C. Instrument the application by using the AWS X-Ray SDK. Update the application to use the PutXrayTrace API.
D. Instrument the application by using the AWS X-Ray SDK. Update the application to communicate with the X-Ray daemon.
E. Instrument the ECS task to send the stdout and stderr output to Amazon CloudWatch Logs. Update the task policy to allow the cloudwatch:PutLogs action.

---

**Question 73.** A company is developing a serverless multi-tier application on AWS. The company will build the serverless logic tier by using Amazon API Gateway and AWS Lambda. While the company develops the logic tier, a developer who works on the frontend of the application must develop integration tests. The tests must cover both positive and negative scenarios based on HTTP status codes. Which solution will meet these requirements with the LEAST effort?

A. Set up a mock integration for API methods in API Gateway. In the integration request from Method Execution, add simple mapping templates to return HTTP status codes.
B. Create two mock integration resources for API Gateway. In the API Gateway, return a success HTTP status code for one resource and an error HTTP status code for the other resource. Add messages that correspond to the HTTP status codes.
C. Create Lambda functions to perform tests. Build an API resource and return either success or error based on the HTTP status code for the other resource. Build an API Gateway Lambda integration. Select appropriate Lambda functions that correspond to the HTTP status codes.
D. Create a Lambda function to give a simple JSON return either success or error-based HTTP status codes. Build a mock integration in API Gateway. Select the Lambda function that corresponds to the HTTP status codes.

---

**Question 74.** A developer is setting up a deployment pipeline. The pipeline includes an AWS CodeBuild build stage that requires access to a database to run integration tests. The developer is using a buildspec.yml file to configure the database connection. Company policy requires automatic rotation of all database credentials. Which solution will handle the database credentials MOST securely?

A. Retrieve the credentials from variables that are hardcoded in the buildspec.yml file. Configure an AWS Lambda function with the new credentials every 30 days.
B. Retrieve the credentials from an environment variable that is linked to a SecureString parameter in AWS Systems Manager Parameter Store. Configure Parameter Store for automatic rotation.
C. Retrieve the credentials from an environment variable that is linked to an AWS Secrets Manager secret. Configure Secrets Manager to rotate the credentials.
D. Retrieve the credentials from an environment variable that contains the connection string in plaintext. Configure an Amazon EventBridge event to rotate the credentials.

---

**Question 75.** A company created four AWS Lambda functions that connect to a relational database server that runs on an Amazon RDS instance. A security team requires the company to automatically change the database password every 30 days. Which solution will meet these requirements MOST securely?

A. Store the database credentials in the environment variables of the Lambda function. Deploy the Lambda function with the new credentials every 30 days.
B. Store the database credentials in AWS Secrets Manager. Configure a 30-day rotation schedule for the credentials.
C. Store the database credentials in AWS Systems Manager Parameter Store secure strings. Configure a 30-day schedule for the secure strings.
D. Store the database credentials in an Amazon S3 bucket that uses server-side encryption with customer-provided encryption keys (SSE-C). Configure a 30-day key rotation schedule for the customer key.

---
