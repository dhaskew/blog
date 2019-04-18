---
layout: post
title:  "AWS"
date:   2019-04-15 18:46:57 -0400
categories: aws
---

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
    * # of queries 
    * # of dns entries
  * health check services
    * setup rules and alerts to make sure your services are up.





What is the status of Amazon's services? : https://status.aws.amazon.com/

