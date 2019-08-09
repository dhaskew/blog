---
layout: post
title:  "AWS"
date:   2019-04-15 18:46:57 -0400
categories: aws
---

* Links
  * https://d1.awsstatic.com/training-and-certification/docs-dev-associate/AWS_Certified_Developer_Associate_Updated_June_2018_Exam_Guide_v1.3.pdf
  * https://aws.amazon.com/certification/recertification/
  * https://d0.awsstatic.com/whitepapers/Security/AWS_Security_Best_Practices.pdf
  * https://aws.amazon.com/cli/

* Things to do
  * Two factor authenticatinon enabled? Enable it.
  * Are you still using AWS resources as your root account? Create a less priviledged account with manage permissions.
  * Modify the default VPC - experiment
  * Create a new VPC
    * understand subnets and availability zones
  * Create an EC2 instance
    * Connect to it via ssh and/or rdp
  * Create an Elastic IP / Externap IP address
    * and assign it to an EC2 instance
  * Create a Load Balancer?
  * Create an Auto Scaling Group?
    * load creation tools to test scaling group policies
      * jmeter
      * apache benchmark
  * Create a CloudFormation template and use it to create/update/delete a resource stack
  * Use Elastic BeanStalk to automate installation of a web service
  * CloudFront setup for blog?
    * create a distribution
    * when to invalidate?
  * SNS - implement an alert to your email/sms
  * Create a lambda function
    * integrate with blog?
    * contact form that sends an email (via SES)?

* API Gateway
  * can sit in front of restful API

* Cloud Front
  * used to cache data
  * can sit in-front of S3 Buckets
  * "edging" your content
  * a "distribution"
    * ttl
    * different behaviors based on path
    * 

* Elasticache
  * redis, memcached style service
  * uses "clusters" of nodes
  * Redis is super popular

* CORS = Cross Origin Resource Store

* AMI = Amazon Machine Image
  * can be created from the AWS dashboard as a clone of an existing image

* CloudFormation
  * service to provision resources using templates
    * templates are json documents
    * no limit on number of resources created
  * stack
    * a collection resources created by a template
    * can be created, updated, deleted (including its resources)
  * security groups can be managed as well

* CloudFormer
  * Creates a CloudFormation template based on existing infrastructure 

* EC2 = Elastic Cloud Compute
  * instance prices vary by type (windows >$ linux)
  * Security Groups
    * used to control access to EC2 instances

* EBS = Elastic Block Strorage
  * for use with EC2
  * you can disconnect your storage for the EC2 instance to use with other instances?

* S3 = Simple Storage Service
  * max file size = 5T
  * Bucket = collection of files
  * pricing
    * amount of data stored
    * amount of data transfered
    * number of requests



* RDS = Relational Database Service
  * managed databases in the cloud
  * security groups help with security
  * pricing
    * type of database
    * region
    * ec2 instance type
  * creating an RDS instance also sets up an EC2 instance at the same time
  * can create read replica's
  * daily backups are standard
  * multiple database engine choices
    * oracle
    * mysql
    * postgres
    * ....

* Route53 = DNS
  * route via weighted routing
  * geolocation routing
  * failover routing
  * pricing
    * hosted zone
    * number of queries 
    * number of dns entries
  * health check services
    * setup rules and alerts to make sure your services are up.


* Elastic Beanstalk
  * runs your code on EC2 instances
  * helps deployment to EC2
  * helps with monitoring and logging
  * you define "Applications"
  * "Applications" are versioned and stored in s3
  * "Applications" are deployed to an environment - prod/cert/test
  * Logs/Monitoring dashboard
  * its basicially free
    * you pay for EC2 instances / load balancers / S3
  * Uses CloudFormation in the background


* DynamoDB
  * NoSQL database service
  * document or key/value mode
  * pay for how much you store and how often you query
    * provisioned thoughput capacity
    * amount of data stored

* RedShift
  * data wharehousing solution
  * ETL tools
  * clusters/nodes
  * encryption available
  * pricing varieds by node type
    * dense compute vs dense storage nodes
  
* VPC = Virtual Private Cloud
  * control access to resources
  * security groups + routing rules controls
    * routing tables
      * what goes where
    * network ACLs
      * who gets in
  * public vs private subnets for security
  * FREE

* Cloudwatch
  * monitoring service
  * alerts / alarms
  * billing alarms
  * pricing varies by alarms / dashboards / etc

* CloudFront
  * CDN, Cloud delivery network
  * "Distributions"
  * pricing varies by region / data transfer

* SNS = Simple Notification Service
  * simple notificatin service
  * "topics"

* IAM = Identity and Access Management
  * access management service
  * two factor authentication?
  * define policies
    * who can launch ec2 instances
    * who can create s3 buckets
  * policy statements
    * action - operation user wants to perform
    * effect - allow / deny
    * resource - resource the user wants to perform the action on
  * Users and Groups
    * group polices - custom and existing templates from AWS

https://console.aws.amazon.com

What is the status of Amazon's services? : https://status.aws.amazon.com/

https://github.com/aws


===== TEST NOTES =====

* Elastic Beanstalk
  * Configuration Files (.ebextensions) – Settings for any options that are not applied directly to the environment, and also not specified in a saved configuration, are loaded from configuration files in the .ebextensions folder at the root of the application source bundle.
  * Tomcat / Passenger / Puma 
* API Gateway
  * import a rest api
    * openapi 2 and 3
    * swagger?
* Code Commit
  * event notifications configured in console
  * uses cloudwatch event rules under the hood
* SNS
  * payloads can be different per device type
  * json keypairs
* EC2
  * instance metadata
    * retrieve via curl or other get request to http://169.254.169.254/latest/meta-data/
  * user data 
    * limited to 16k
    * base64 encoded
* Lambda
  * 1000 concurrent connections
  * 75GB function and layer storage
  * timeout - 900 seconds / 15 mins
  * 128 MB to 3008 MB in 64MB chunks
  * 1024 threads
  * https://docs.aws.amazon.com/lambda/latest/dg/limits.html
* S3
  * multipart upload recommended at 100MB
* DynamoDB
  * read request unit = 4k = represents:
    * 1 strongly consistent read
    * 2 eventually consistent reads 
  * write request unit = 1k
    * 1 normal write
    * transactional write require 2 units per 1k
* Cognito
  * A user pool is a user directory in Amazon Cognito. With a user pool, your users can sign in to your web or mobile app through Amazon Cognito. Your users can also sign in through social identity providers like Facebook or Amazon, and through SAML identity providers. Whether your users sign in directly or through a third party, all members of the user pool have a directory profile that you can access through an SDK. 
  * After successfully authenticating a user, Amazon Cognito issues JSON web tokens (JWT) that you can use to secure and authorize access to your own APIs, or exchange for AWS credentials. 
  * The two main components of Amazon Cognito are user pools and identity pools. Identity pools provide AWS credentials to grant your users access to other AWS services. To enable users in your user pool to access AWS resources, you can configure an identity pool to exchange user pool tokens for AWS credentials
* SQS
  * polling model message queues
  * FIFO queue vs Standard (loose FIFO)
  * FIFO is deliver once
    * 1 consumer per message group
    * 3000 / second with batching
    * 300 / second solo
  * Standard is deliver at least once
  * By grouping messages into batches, you can reduce your Amazon SQS costs
  * each message can have 10 metadata attributes
  * long polling vs short polling
    * long polling
      * cheaper
      * not good in multithreaded consumers
      * 20 max timeout  recommended
  * PurgeQueue action to clear queue
  * message retention is 1 min to 14 days, default is 4 days
  * MessageRetentionPeriod attribute
  * message size from 1k to 256k
  * max message count is 120K for standard and 20k for FIFO
  * message queue names limited to 80 chars
  * 30 second default Visibility Timout
    * max is 12 hours
* S3
  * normal max upload is 5GB, 5TB in parts
  * Transfer Acceleration takes advantage of Amazon CloudFront’s globally distributed edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimized network path. 
  * S3 Transfer Acceleration optimizes the TCP protocol and adds additional intelligence between the client and the S3 bucket, making S3 Transfer Acceleration a better choice if a higher throughput is desired. If you have objects that are smaller than 1GB or if the data set is less than 1GB in size, you should consider using Amazon CloudFront's PUT/POST commands for optimal performance.
  * multipart upload
    * max size 5TB
    * max number of parts 10000
    * part size 5mb to 5gb
    *  