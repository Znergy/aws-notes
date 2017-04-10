# AWS General Notes

## **EBS volume**
* a cloud based hard drive
* When creating an EC2 instance, we provision EBS volumes to store things we want to persist past the point when the specific server or EC2 instance is terminated. 
* Without a EBS volume any data stored on that EC2 instance would be lost when the EC2 instance was terminated 
* You can also create a snapshot of an EBS volume and then recreate a volume out of it later. 

## **S3**
* used for **limitless cloud storage** (google drive or dropbox)
* S3 can also be setup to work as a hosting service for your entire website (meaning you upload html/css/js/php files into your S3 bucket and run from there) 
* This works well for a static website

## **EC2** 
* Can be used to host your web applications and web servers

## **RDS**
* Can be used to host your database

## **Availability Zones**
* like physical data centers

## **NoSQLDatabases**
* NoSQL stands for ‘Not Only SQL’, meaning that an application can use both relational type of commands and a mix of no sql commands. Both are supported.
* **SimpleDB**
  * excellent for smaller amounts of data 
  * I/O speed can be bad 
  * 10GB limit per table 
  * use in combination with S3
* **DynamoDB** (this took over from SimpleDB) (Current NoSQL AWS database) 
  * hosted on SSD (freaking fast) 
  * I/O is much better on DynamoDB versus SimpleDB 
  * no size or request limits 
  * pay for performance 
    
## **CloudWatch**
* CloudWatch is a scalable monitoring service that allows you to monitor various AWS services all through the same place in the AWS Console.
* You can also monitor things using the SDK API 
* You can also monitor custom metrics from your own application 
* CPU utilization 
* Network throughput 
* Error rates, and many more 
* You can set a CPU limit on your servers and when a server is above 75% for more than 10 minutes an alarm will sound and you can set responses that should take place when the alarm is tripped. Using the simple notification service, see below 
  
## **Elastic Load Balancing**
* ELB is a scalable, and fault tolerant load balancing for multiple EC2 instances.
* Works with Auto Scaling and CloudWatch 
* Load balance requests over a set of EC2 instances 
* Can monitor the health of EC2 instances and shutdown non performant instances 
* Can trigger scale-up or scale-down events 
### **Auto Scaling**
* Auto Scaling helps scale your application as needed
* Works with CloudWatch and ELB (Elastic Load Balancing - balancing EC2 instances as needed) 
* Auto scaling working with CloudWatch would allow you to scale up or down based off an CloudWatch alarm triggering (code says CPU over 75% for 10 minutes, add EC2 instance) 
### **Automatically provision**
* You can EC2 instances when load increases
* Using Auto Scaling you will always know that you will have enough capacity for either scenario (low cpu, terminate EC2 instance - high cpu, start EC2 instance) 
### Shutdown instances when load decreases
### **Pre-emptive scaling**
* Example, you can use Auto Scaling to provision an extra ten EC2 instances during a single 24-hr period while doing a promotion. After 24-hrs, it drops back to two EC2 instances. 
### **Monitor health of EC2 instances**

## **Sources**
* [Free Udemy Course](https://www.udemy.com/aws-step-functions/learn/v4/content)
