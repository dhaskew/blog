---
layout: post
title:  "AWS"
date:   2019-04-15 18:46:57 -0400
categories: aws
---

* Two factor authenticatinon enabled? Enable it.
* Are you still using AWS resources as your root account? Create a less priviledged account with manage permissions.


* EC2 = Elastic Cloud Compute
  * instance prices vary by type (windows >$ linux)
  * Security Groups
    * used to control access to EC2 instances

* EBS = Elastic Block Strorage
  * for use with EC2

* S3 = Simple Storage Service
  * max file size = 5T
  * Bucket = collection of files
  * pricing
    * amount of data stored
    * amount of data transfered
    * number of requests

* Cloud Front
  * used to cache data
  * can sit in-front of S3 Buckets
  * "edging" your content

* RDS = Relational Database Service
  * managed databases in the cloud
  * security groups help with security
  * pricing
    * type of database
    * region
    * ec2 instance type

* Route53 = DNS
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

