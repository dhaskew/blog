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

