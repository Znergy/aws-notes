# Questions I’ve run into while learning AWS

## What is **EC2**?

## What is **Elastic Load Balancing**?

## What is **S3**?

## What is **Auto Scaling**?

## What is **CloudWatch**?

## What is **SimpleDB**?

## What is **DynamoDB**?

## What is **NoSQL**?

## What is a **Relational DB**?

## What is **N-tier architecture**?

## What is **lambda**?

## What is **Route 53**?

## What is **API Gateway**?

## What is **Amazon Linux**?

## What does the **yum command** do?

## How do you connect to an **EC2 instance**?

## How do **make a S3 bucket**?

## How do you **remove a S3 bucket**?

## How do you **transfer files between S3 buckets**?

## How do you **copy a file from S3 to EC2**?

## What is **IAM**?

## What is a **role**?

## What is an **availability zone**?

## What is a **security group**?

## What is a **tag** used for?

## Why should we use **tags**?

## What is a **policy**?

## How do you get **sudo access** in **AWS CLI**?

## How do you **install gradle** in an **EC2** instance?

## What is **EBS** (Elastic Beanstalk)?

## What is an **EBS volume**?

## What is an **EBS Snapshot**?

## Why would you want to make an **EBS snapshot**?

## What is **Apache Tomcat**?

## What is **JavaSE**?

## What is a **.war** file? 

## What is a **.jar** file?

## How do you **create** a **.war** file?

## How do you create .jar file?

## What **IDE** can help with the process?

## How can you static **host a website using S3**?

## What is **Multi-AZ N-Tier Architecture**?

## How is it different from **single N-Tier Architecture**?

## What are the **benefits of Multi-AZ N-Tier Architecture** over a single N-Tier Architecture?

## What is **RDS**?

## How do you setup a **RDS postgreSQL server**?

## How do you **terminal into** your **RDS postgreSQL server**?

## How do you connect the **postgreSQL server to your Java application**?

## What is **Apache Maven**?

## How do you build a Java app that is **Apache Maven** focused?

## What is the **easiest way to launch** a **Java Application** to AWS?

## What service is the **easiest** (e.g. Maven, Gradle, Tomcat)?

## What is **gradle**, what is it used for?

## What does **provisioning** mean?

## What does **mounting** mean?

## What is the **AWS API**?

## How do you interact with the **AWS API**?

## What is the **Java SDK**?

## What is the ‘**simple q**’ service?

## What is **Eclipse**?

## What is the **AWS Eclipse plug-in**?

## What is **Cloud Formation**?

## How is **Cloud Formation used**?

## What are the **benefits** of **Cloud Formation**?

## What is **VMWare**?

## Why do people use **VMWare**?

## What is **continuous integration**?

## What is a **continuous integration server**?

## What is **Jenkins**?

## Why do people use **Jenkins**?

## What is **Maven**?

## What are **workflows**?

## What are **State Machines**?
* A **State Machine** is the flow from state change to state change (e.g. Start -> HelloWorld (app) -> End). The state changes from ‘Start’ to ‘HelloWorld’.
* A **State Machine** is a group of states.
* Each state could be either Task, Wait, Pass, Succeed, Fail, Choice, Parallel (img: https://s3-us-west-2.amazonaws.com/ryanjones-aws-images/step-functions.png)
 * **Task**: activity running on EC2 Node
 * **Wait**: just to wait
 * **Pass**: could be used for logging or any kind of thing that doesn’t affect the execution of the workflow (state machine group of states)
 * **Succeed**: to enforce success of a specific activity
 * **Fail**: throw an exception in a specific business scenario
 * **Choice**: key strength of step function. You can add condition, add multiple branches, move the execution in one of these branches
 * **Parallel**: is just a parallel execution of tasks
* A **State Machine** is defined in JSON format and integrates with Lambda functions or custom activities running in EC2

## What is **Workflow Execution**?
* Execution is an instance of the process or workflow (state machine)
* Workflow execution could be started by..
 * Starting state-machine execution from console
 * Starting state-machine execution from CLI
 * Invoking Step Functions using HTTPS endpoint service APIs
 * Invoking Step Functions from AWS SDKs as part of the application

## What are **micro-services**?

## What is an **Order Processing Workflow**? 
* Image: https://s3-us-west-2.amazonaws.com/ryanjones-aws-images/order_processing_workflow.png
* An order processing workflow is the visual way your app will function at each state change. See image above.
  * The format coming back is in a JSON format (e.g. Input { “pid”: 1, “quantity”: 5 }
    * Logic: If (quantity < 5) { inventoryExists = true; } else { inventoryExists = false; }  (in this lambda function we will check inventory, and set inventory flag to true if condition is met)
* The ‘pid’ is passed as output from each step to be input to next step (inventory (yes) -> processOrder -> updateInventory -> ChargeCustomer -> ShipOrder -> SendNotification)
* The input being passed to the first step is then passed as output to the next step.. That’s cool right!?

## What is **Order Processing Integration**?
* This is where the state machine and the business process intertwine..
* For instance, when we get to charging the customer. A process is invoked, this triggers a Lambda function)
* User clicks [BUY] -> API Gateway process order -> Lambda handles both the processing of order and batch processing -> lastly, the state changes to ShipOrder

## What are **AWS Step Functions**?
* Step Functions are used to create state machines (workflows)
* You can create fully serverless with Step Functions on Amazon cloud
* Orchestrate micro-services into workflow or multi-step applications
* Capable of processing sequential, branching, and parallel steps
* State machine is defined in JSON format and integrates with Lambda functions or custom activities running in EC2

## What is **JSON**?

## What is **AJAX**?
