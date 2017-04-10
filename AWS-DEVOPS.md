# DevOps Notes

## **Java and AWS**

### **Command line clients**
* Used for scripted solutions, like provision resources and other service management tasks 

### **AWS Java SDKs**
* Amazon has a lot of SDKs available for various languages including java 
* Java SDK includes the API client as a jar file and some code examples for common tasks 

### Make use of **AWS services at runtime**.
* You will often bundle the jar from the SDK into your application. 
* You do this so the Java SDK is part of your application's ‘classpath’ 
* If you’re smart and like to use Apache Maven to build your software then the AWS jar is available in the central repository so it’s easy to include in your builds 

### **AWS API** serves two main purposes for Java applications
* First use case, is to manage and provision other AWS services from within your application 
  * Example, you can request additional servers to be provisioned, a database to be provisioned, a user to be created all from within your application! 
* Second use case, is to interact with already provisioned AWS resources. Like, reading files from S3 or reading and writing to the simple q service. 

### **Eclipse Integration**
* There is an AWS Eclipse plugin which will allow you to access and manage some AWS resources/services right from within Eclipse environment 
  * In addition, the plug-in provides you project types that will allow you to quickly create new Eclipse projects that can interact with AWS resources 

### **Maven Integration**
* Also, although there is no ‘official’ Maven integrations published by AWS there are many community projects making Maven integrations for AWS projects easier 

## **AWS at Development Time**

### **Self-Serve Hardware**
* Similar to VMWare 

### **Guarantee everyone’s environment is the same**
* Avoid the expense of redundant hardware 

### **Work with more than one development setup**
* You can test on multiple configurations without having to purchase the hardware itself 

### **No more sacred demo environments**
* Companies no longer have to make sure no one touches the demo environment because a big client is coming 
* With Self-Serve hardware you can use whatever you need for however long you need then just toss it away 

### **Continuous integration opportunities**
* If you work on a smart team, you will be using some type of continuous integration server like ‘Jenkins’ 

## **AWS at Testing Time**

### **Self serve hardware for testers**

### **Guarantee test environments are identical**

### **Make it easy to start each test run with a clean baseline**

### **Avoid redundant resources allocated to the test team**

### **Can run performance tests without hurting others**

### **Make QA environment available globally**

## **Sources** 
### [AWS For Java Developers](https://www.youtube.com/watch?v=ItDBrtCxpcA)
