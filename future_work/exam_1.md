Which of the following are advantages of having infrastructure hosted on the AWS Cloud?
Choose 2 answers from the options given below.

 A. Having complete control over the physical infrastructure
 B. Having the pay as you go model 
 C. No Upfront costs 
 D. Having no need to worry about security
Answer – B and C
The Physical infrastructure is a responsibility of AWS and not with the customer. Hence it is not an advantage of moving to the AWS Cloud.
And AWS provides security mechanisms, but even the responsibility of security lies with the customer.

A web administrator maintains several public and private web-based resources for an organisation. Which service can they use to keep track of the expiry dates of SSL/TLS certificates as well as updating and renewal?

 A. AWS Data Lifecycle Manager
 B. AWS License Manager
 C. AWS Firewall Manager
 D. AWS Certificate Manager 
Correct Answer – D
The AWS Certificate Manager allows the web administrator to maintain one or several SSL/TLS certificates, both private and public certificates, including their update and renewal such that the administrator does not worry about imminent expiry of certificates.
https://aws.amazon.com/certificate-manager/
Option A. is INCORRECT because an AWS Lifecycle Manager serves the purpose of creating lifecycle policies for specified resources in order to automate operations.
https://docs.aws.amazon.com/dlm/?id=docs_gateway
Option B. is INCORRECT because AWS License Manager serves the purpose of differentiating, maintaining third-party software provisioning vendor licenses as well as decreases the risk of license expirations and the penalties.
https://docs.aws.amazon.com/license-manager/?id=docs_gateway
Option C. is INCORRECT because AWS Firewall Manager aids in the administration of Web Application Firewall (WAF), by presenting a centralised point of setting firewall rules across different web resources.
https://docs.aws.amazon.com/firewall-manager/?id=docs_gateway

An organisation has a persistently high amount of throughput, it requires connectivity with no jitter and very low latency between its on-premise infrastructure and its AWS cloud build to support live streaming and real-time services. What is the MOST appropriate solution to meet this requirement?

 A. AWS Data Streams
 B. AWS Kinesis
 C. Kinesis Data Firehose
 D. AWS Direct Connect 
Correct Answer – D
AWS Direct Connect is a cloud service solution that makes it easy to establish a dedicated network connection from the organisation’s premises to AWS. The service provides a dedicated network connection with one of the AWS Direct Connect locations making it possible to guaranteed high bandwidth and very low latency connectivity.
https://aws.amazon.com/directconnect/
Option A. is INCORRECT because the scenarios requires a connectivity option whilst Amazon Kinesis Data Streams (KDS), is a massively scalable and durable real-time data streaming service. It does not, however, guarantee the quality of connectivity between the organisations on-premise infrastructure and the AWS cloud build. The data KDS collects is available in milliseconds to enable real-time analytics use cases such as real-time dashboards, real-time anomaly detection, dynamic pricing, and more.
https://aws.amazon.com/kinesis/data-streams/
Option B. is INCORRECT because the organisation requires a connectivity solution and not an application service. Amazon Kinesis makes it easy to collect, process, and analyze real-time, streaming data in order to get timely insights and react quickly to new information.
https://aws.amazon.com/kinesis/
Option C. is INCORRECT because Amazon Kinesis Data Firehose is used to load streaming data into various destinations like data lakes, data stores and analytics tools. The service, however, does not guarantee link quality between the organisation’s on-premise infrastructure and that in the AWS cloud.
https://aws.amazon.com/kinesis/data-firehose/

When designing a highly available architecture, what is the difference between vertical scaling (scaling up) and horizontal scaling (scaling out)?

 A. Scaling up provides for high availability whilst scaling out brings fault-tolerance
 B. Scaling out is not cost-effective compared to scaling up
 C. Scaling up adds more resources to an instance, scaling out adds more instances 
 D. Autoscaling groups require scaling up whilst launch configurations use scaling out
Correct Answer – C
In high availability architectures, Autoscaling is used to give elasticity to the design where horizontal scaling (scaling out) uses Autoscaling groups to increase processing capacity in response to changes in preset threshold parameters. It could involve adding more EC2 instances of a web server. Vertical scaling (scaling up), which can create a single point of failure, involves adding more resources to a particular instance to meet demand.
https://docs.aws.amazon.com/autoscaling/plans/userguide/what-is-aws-auto-scaling.html
Option A. is INCORRECT because scaling up does not provide high availability, adding more resources to one instance is often not a best-practice in architecture design.
Option B. is INCORRECT because scaling out is actually cost-effective since it involves only adding more resources in response to demand and reducing resources (scaling down) when demand is low
Option D. is INCORRECT because all Autoscaling groups require a launch configuration as the basis of what resources would be provisioned or deprovisioned to meet predefined parameters.

In Cost Optimization, what is referred to as EC2 Right Sizing?

 A. It is a cost-effective solution to determine the appropriate Amazon EC2 resources such as memory, processor type and storage when provisioning an instance type.
 B. It is a cost-saving solution that analyses data over a period of time to determine and recommend the type of Amazon EC2 instances appropriate for your workload. 
 C. It is the scaling down or scaling up of Amazon EC2 instances and instance types to meet workload demand by maintaining only the threshold resources. 
 D. It is a cost-saving solution that outlines the recommendations of best practice in four aspects namely cost optimization, performance, fault-tolerance and service limits.
Correct Answer – B
Cost Optimization: EC2 Right Sizing utilizes managed services to execute right-sizing analysis to provide detailed recommendations for more cost-saving builds and implementations of Amazon EC2 instances.
https://aws.amazon.com/solutions/cost-optimization-ec2-right-sizing/
Option A. is INCORRECT because when provisioning a new Amazon EC2 instance, the user is presented with instance types to choose from, these have varying capacities depending on use case.
Option C. is INCORRECT because it describes the mechanism of Auto Scaling and not Amazon EC2 Right Sizing
Option D. is INCORRECT because it describes the function of AWS Trusted Advisor which outlines the recommendations of best practice in five not four aspects. Cost optimization, security, performance, fault-tolerance and service limits.

An administrator would like to efficiently automate the replication and deployment of a specific software configuration existent on one EC2 instance onto four hundred others. Which AWS service is BEST suited for this implementation?

 A. AWS OpsWorks 
 B. AWS Beanstalk
 C. AWS Launch Configuration
 D. AWS Auto-scaling 
Correct Answer – A
AWS OpsWorks provides a fully managed configuration automation and management service of Chef and Puppet. These platforms will allow for the use of code to automate the configuration of the EC2 instances, including replication as stated in the scenario. With Chef and Puppet, OpsWorks allows for the automation of how servers are configured, deployed, and managed across Amazon EC2 instances or on-premises compute environments.
Option B. is INCORRECT because AWS Elastic Beanstalk is a service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS. It will not be able to autonomously replicate a specific software service configuration onto a multitude of EC2 instances.
https://aws.amazon.com/elasticbeanstalk/
Option C. is INCORRECT because a Launch Configuration is primarily an instance configuration template that an Auto Scaling group uses to launch EC2 instances. It is the blueprint of the Auto Scaling group and determines the configuration output of each instance.
https://docs.aws.amazon.com/autoscaling/ec2/userguide/LaunchConfiguration.html
Option D. is INCORRECT because Auto-scaling is responsive to preset threshold levels in a deployment environment. It does not offer a fully managed functionality that allows for the mass replication of a specific configuration as the scenario outlines. CloudWatch parameters, it monitors applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.
https://aws.amazon.com/autoscaling/

Which of the following is the responsibility of the customer when ensuring that data on EBS volumes is kept safe

 A. Deleting the data when the device is destroyed
 B. Creating EBS snapshots 
 C. Attaching volumes to EC2 Instances
 D. Creating copies of EBS Volumes
Answer – B
Creating snapshots of EBS Volumes can help ensure that you have a backup of your EBS volume in place.
For more information on EBS Snapshots, please refer to the below URL:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSSnapshots.html

There is a requirement to store objects. The objects must be downloadable via a URL. Which storage option would you choose?

 A. Amazon S3 
 B. Amazon Glacier
 C. Amazon Storage Gateway
 D. Amazon EBS
Answer – A
Amazon S3 is the perfect storage option. It also provides the facility of assigning a URL to each object which can be used to download the object.
For more information on AWS S3, please visit the Link:
https://aws.amazon.com/s3/
B is incorrect. Glacier is for archival and long-term storage.
This question is to check the user understanding of AWS S3 service terminology and use cases. If you see the question, they mentioned “Object” and those should be downloadable via a URL. It’s not possible with EBS

An administrator noticed a consistent spike in processor and memory activity on the organisation’s web servers that host a large web application, this was after installing Secure Socket Layer/Transport Layer Security (SSL/TLS) for security. This increased activity degraded the web application’s responsiveness. What is the best-practice solution to resolve the situation?

 A. Migrate the web application onto m4.4xlarge EC2 instances with robust compute, processing and networking capability.
 B. Offload the SSL/TLS from running locally to AWS CloudHSM. 
 C. Create an auto-scaling group that scales out as traffic to the web application cluster increases.
 D. Create a custom AWS CloudWatch metric to monitor the instance resources, by writing a script in the AWS Command Line Interface (AWS CLI). 
Correct Answer – B
AWS CloudHSM service can take up SSL/TLS processing for the web servers. Layer Security (TLS) are used to confirm the identity of web servers and establish secure HTTPS connections over the Internet. Using CloudHSM for this processing reduces the burden on the organisation’s web servers and provides extra security by storing the web server’s private key in CloudHSM.
https://aws.amazon.com/cloudhsm/
Option A. is INCORRECT because opting for EC2 instances with larger resource capacities is not best-practice. During periods of low activity, these resources will be idle therefore not cost-effective. Cloud infrastructure and resources should scale-in and out on-demand, thereby aligning service costs to actual usage.
https://aws.amazon.com/ec2/instance-types/
Option C. is INCORRECT because the cause of the degraded web application is not due to increased traffic, therefore the auto-scaling group will not solve the situation since it will respond to the web application traffic metric to the web servers.
https://aws.amazon.com/autoscaling/
Option D. is INCORRECT because creating a custom AWS CloudWatch metric to monitor the instance’s resources will not help reduce the high workload on the web servers in any way. It will, however, give visual output to the administrator to observe usage patterns. From the scenario, this is already in place.
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/mon-scripts.html

Which AWS service provides infrastructure security optimization recommendations?

 A. AWS Application Programming Interface(API)
 B. Reserved Instances
 C. AWS Trusted Advisor 
 D. Amazon Elastic Compute Cloud (Amazon EC2) SpotFleet
Answer – C
The AWS documentation mentions the following
An online resource to help you reduce cost, increase performance, and improve security by optimizing your AWS environment, Trusted Advisor provides real time guidance to help you provision your resources following AWS best practices
For more information on the AWS Trusted Advisor, please refer to the below URL:
https://aws.amazon.com/premiumsupport/trustedadvisor/
Choices A, B, and D are incorrect. They are not related to infrastructure security optimization.

A company needs to know which user was responsible for terminating several critical Amazon Elastic Compute Cloud (EC2) Instances. Where can the customer find this information?

 A. AWS Trusted Advisor
 B. Amazon EC2 instance usage report
 C. Amazon CloudWatch 
 D. AWS CloudTrail logs 
Answer – D
Using CloudTrail , one can monitor all the API activity conducted on all AWS services.
The AWS Documentation additionally mentions the following
AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command line tools, and other AWS services. This event history simplifies security analysis, resource change tracking, and troubleshooting.
For more information on AWS Cloudtrail, please refer to the below URL:
https://aws.amazon.com/cloudtrail/
Answers A, B and C are incorrect. CloudWatch is the most appropriate place to monitor activity in AWS.

Select which use case scenario best suits the implementation of an Amazon RDS database instance over a NoSQL/non-relational database.

 A. Where datasets are constantly evolving and cannot be confined to a static data schema
 B. Where vertical scaling of the database’s resources is not permissible and is seldom necessary.
 C. In an organisation whose datasets are dynamic and document-based
 D. In an organisation where only a finite number of processes query the database in predictable and well-structured Schemas.. 
Correct Answer – D
Amazon Relational databases service (RDS) is best suited in scenarios where the dataset and forms are consistent such that their data schema is persistently valid. It is best to deploy in an environment where the load can be anticipated and is somewhat finite. Amazon RDS engines include Amazon Aurora, MariaDB, PostgreSQL
https://aws.amazon.com/rds/
Option A. is INCORRECT because Amazon RDS engines are inappropriate in a scenario where datasets are constantly evolving and the data schema is flexible. NoSQL/non-relational databases fit this use case.
Option B. is INCORRECT because Amazon Relational Database service engines will scale up with the increase in load and is often necessary as the traffic patterns to the database increases.
Option C. is INCORRECT because in a scenario where the datasets are dynamic and document-based, the use of JSON and not SQL is appropriate, therefor non-relationals/NoSQL database engines such as Amazon DynamoDB.
https://aws.amazon.com/nosql/

Which of the following is an accurate statement regarding AWS resource tags?

 A. All AWS resource tags have a semantic interpretation
 B. Within a resource tag, every defined key must have a value string 
 C. By default, resource tags are assigned as null, null
 D. Resource tags can be edited or removed at any time 
 E. Placement group does not support tags
Correct Answer – D, E
Resource tags are critical when architecting in the cloud for labeling assets to make it possible to easily administer and manage them. Useful when running queries about billing, auditing, and asset lookups for quantities. They are a user-defined key-value pair with variable characters.
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html

Option A. is INCORRECT because resource tags do not have a semantic meaning they are plain-text characters whose utility can be derived by the user who defines them.
Option B. is INCORRECT because a user can define a key and not specify the character string for its value, leaving it empty but cannot set the value to null
Option C. is INCORRECT because resource tags are not assigned by default, the user has to explicitly define them.

Option E: Placement groups do support tags

There is an external audit being carried out on your company. The IT auditor needs to have a log of all access to the AWS resources in the company’s account. Which of the below services can assist in providing these details?

 A. AWS Cloudwatch
 B. AWS CloudTrail 
 C. AWS EC2
 D. AWS SNS
Answer – B
Using CloudTrail , one can monitor all the API activity conducted on all AWS services.
The AWS Documentation additionally mentions the following
AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command line tools, and other AWS services. This event history simplifies security analysis, resource change tracking, and troubleshooting.
For more information on AWS Cloudtrail, please refer to the below URL:
https://aws.amazon.com/cloudtrail/

A Disaster Recovery Strategy on AWS should be based on launching resources in a separate :

 A. Subnet
 B. AWS Region 
 C. Security Group
 D. Amazon Virtual Private Cloud (Amazon VPC)
Answer – B
The AWS Documentation mentions the following
Businesses are using the AWS cloud to enable faster disaster recovery of their critical IT systems without incurring the infrastructure expense of a second physical site. The AWS cloud supports many popular disaster recovery (DR) architectures from “pilot light” environments that may be suitable for small customer workload data center failures to “hot standby” environments that enable rapid failover at scale. With data centers in Regions all around the world, AWS provides a set of cloud-based disaster recovery services that enable rapid recovery of your IT infrastructure and data.
For more information on enabling AWS Disaster Recovery, please refer to the below URL:
https://aws.amazon.com/disaster-recovery/
A, C and D are incorrect. A subnet, security group and VPC will not add the additional redundancy required for Disaster Recovery.

A cloud solutions architect needs to execute urgent mission-critical tasks on the AWS Management console, but has left their Windows-based machine at home. What secure option can be used to administer these tasks on the cloud infrastructure given that only non-graphical user interface (non-GUI), Linux-based machines are readily available?

 A. Share the AWS Management console credentials with the person at home over the phone, so they can execute on the cloud solutions architect behalf
 B. Use third-party remote desktop software to access the Windows-based machine at home from the non-GUI workstations and administer the necessary tasks
 C. Use Secure Shell (SSH) to securely connect to the Windows-based machine from one of the non-GUI Linux-based machines then log onto the AWS Management console 
 D. Install and run AWS CLI on one of the non-GUI Linux-based machines, in a shell environment such as bash, the cloud solutions architect can access ALL services just as they could from a Windows-based machine. 
Correct Answer – D
AWS Command Line Interface (AWS CLI) is an open source tool that enables access and interaction with AWS services using commands in the command-line shell. With minimal configuration the cloud solutions architect would start using the functionality equivalent to that provided by the browser-based AWS Management Console from the command prompt in a terminal program such as bash.
https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html
Option A. is INCORRECT because sharing AWS Management console credentials is bad-practice and poses a high security risk.
https://aws.amazon.com/iam/details/managing-user-credentials/
Option B. is INCORRECT accessing the AWS Management console via third-party remote desktop software is insecure since the remote machine can be compromised.
Option C. is INCORRECT because it is rather cumbersome in comparison, though secure the option is oblivious of the direct access method of AWS CLI

Which of the following statements about scalability is most accurate? Choose 2 answers from the options given below

 A. A scalable system diverts traffic based on demand 
 B. A scalable system diverts traffic to instances with the least load 
 C. A scalable system diverts traffic across multiple regions
 D. A scalable system diverts traffic to instances with higher capacity 
Answer – A and B
Scalability would scale-out ( increase the number of instances ) or scale in ( decrease the number of instances )
Also when one of the instances is with the least load it will divert the traffic to the least loaded instance, so that it takes more load
Both of the above are taken care of by ‘autoscaling’ We just need to enable autoscaling for our instances and traffic would automatically diverted based on demand or load
For more information on AWS Autoscaling service, please refer to the below URL:
https://aws.amazon.com/autoscaling/
https://aws.amazon.com/elasticloadbalancing/

Choose the disaster recovery deployment mechanism that has the lowest downtime.

 A. Pilot light
 B. Warm standby 
 C. Backup Restore 
 D. Devops
Answer – B
The below snapshot from the AWS Documentation shows the spectrum of the Disaster recovery methods. If you go to the further end of the spectrum you have the least time for downtime for the users.


For more information on Disaster recovery techniques, please refer to the below URL:
https://aws.amazon.com/blogs/aws/new-whitepaper-use-aws-for-disaster-recovery/

A business analyst would like to move away from creating complex database queries and static spreadsheets when generating regular reports for high-level management. They would like to dynamically publish insightful, graphically appealing reports with interactive dashboards. Which service can they use to accomplish this?

 A. Amazon QuickSight 
 B. Business intelligence on Amazon Redshift
 C. Amazon CloudWatch dashboards 
 D. Amazon Athena integrated with Amazon Glue
Correct Answer – A
Amazon QuickSight is the most appropriate service to utilise in the scenario, it is a fully-managed service that allows for insightful business intelligence reporting, with creative methods of data delivery including graphical and interactive dashboards. QuickSight includes machine learning which allows users to discover inconspicuous trends and patterns on their datasets.
https://aws.amazon.com/quicksight/
Option B. is INCORRECT because Amazon Redshift service is a data warehouse and will not meet the requirements of interactive dashboards and dynamic means of delivering reports.
Option C. is INCORRECT because Amazon CloudWatch dashboards will not accomplish the requirements of the scenario, they are used to monitor AWS system resources and infrastructure services, though they are customizable and present information in a graphical manner.
Option D. is INCORRECT because Amazon Athena is query service that allows for easy data analysis in Amazon S3 by using standard SQL. This services will not meet the requirements of the scenario.

Which TWO statements best describe the AWS Personal Health Dashboard.

 A. A concise representation of the general status of AWS services
 B. User-specific view on the availability and performance of AWS services underlying their AWS resources. 
 C. A service that prompts the user with alerts and notifications on AWS scheduled activities, pending issues, and planned changes. 
 D. A minute-by-minute update of system outages and service errors on the AWS global infrastructure
 E. A rolling log of all service interruptions across the AWS network, records of incidencies persistent for a year 
Correct Answer – B, C
The Personal Health Dashboard is a tool that shows the status of AWS services that are running user-specific resources. It is a graphical representation that sends alerts, notifications of any personal pending issues, planned changes and scheduled activities.
https://aws.amazon.com/premiumsupport/technology/personal-health-dashboard/
Option A. is INCORRECT because it describes a general overview of the Service Health Dashboard
Option D. is INCORRECT because it describes the Service Health Dashboard
Option E. is INCORRECT because it describes the Status History of the Service Health Dashboard

On a social media website, creative content goes viral for a few days and then rapidly declines in popularity and views thereafter. Which storage class and configuration option would you choose for a cost-effective storage?

 A. Amazon S3 Standard with object versioning
 B. Amazon S3 Intelligent-Tiering 
 C. Amazon Elastic File Store (EFS)
 D. Amazon S3 Standard with lifecycle policies 
Correct Answer – D
Transition actions—Define when objects transition to another storage class.For example, you might choose to transition objects to the STANDARD_IA storage class 30 days after you created them, or archive objects to the GLACIER storage class one year after creating them.
https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html
Option A. is incorrect because when the media file is no longer popular after a few weeks, storing it in Amazon S3 Standard with object versioning will not be cost-effective. Object versioning has little relevance in the scenario.
Option B. is incorrect because Amazon S3 Intelligent-Tiering will transition the file between two storage classes only, frequent and infrequent access. When the media file is no longer popular, even infrequent access will not be cost-effective.
Option C. is incorrect because Amazon Elastic File Store (EFS) is most appropriate as a shared file storage volume. It will not be a cost-effective method to store the media file.

Which statements accurately distinguish AWS Cloud9 from AWS Lambda. (Select TWO).

 A. With AWS Cloud9, developers can share in real-time a development environment with just a few clicks and pair program together. This is not possible with AWS Lambda 
 B. AWS Lambda can be used to create functions that run in AWS Cloud9 IDE 
 C. AWS Lambda functions are dependent on the Amazon API Gateway whilst AWS Cloud9 IDE can write, run, and debug any code
 D. AWS Cloud9 provides an online platform to write, run, and debug code from the browser, whilst AWS Lambda functions can be installed locally 
 E. Without locally installing an integrated development environment, AWS Cloud9 will not run. 
Correct Answer – A, B
AWS Cloud9 IDE has a real-time collaborative function that allows developers to share environments amongst teams and live code. It is accurate that functions written in AWS Lambda environment can be run and debugged in the AWS Cloud9 IDE.
https://docs.aws.amazon.com/cloud9/latest/user-guide/lambda-functions.html
Option C. is INCORRECT because functions written in AWS Lambda can still be invoked or triggered by a service without going through an API gateway
Option D. is INCORRECT because AWS Lambda is a serverless environment service that does not require any resources to be installed locally on a server or desktop
Option E. is INCORRECT because AWS Cloud9 is an integrated development environment that runs off Amazon infrastructure in the cloud and is fully functional without the need to run any resources locally on any server or desktop.

During a live sports event in a remote location, local photographers are required to promptly upload images into an Amazon S3 bucket for processing by the editorial team. How can this process be optimized?

 A. Using Cross Region replication
 B. Using S3 Transfer Acceleration 
 C. Using S3 Standard as the object storage class
 D. Using an FTP server with a web interface
Correct Answer – B
Using S3 Transfer Acceleration will allow the photographers to upload the images to a distinct URL, allowing them to upload images to the nearest Edge Location, then the file will be transferred in a fast, secure via the Amazon backbone network to the S3 bucket.
https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html
Option A. is incorrect because Cross Region replication is not relevant in this scenario as there is no immediate need to copy (replicate) S3 bucket contents.
Option C. is incorrect because using S3 Standard as the object storage class will not optimize the process of uploading images as outlined in the scenario.
Option D. is incorrect because using an FTP server will not optimize the process of uploading the files to the S3 bucket.

In a multi-node deployment architecture of Amazon Redshift data warehouse, what is the role of a leader node?

 A. To access compressed data from the underlying columns
 B. To receive queries and manage client connections 
 C. Primarily act as an in-memory buffer area to improve operational efficiency 
 D. To store data and perform computations and queries
Correct Answer – B
There are two conventional architectures in which to deploy the Amazon Redshift data warehouse, as a single node which handles both client session and computations. The second as a multi node deployment. The latter consists of a leader node which receives queries and manages client connections to the database warehouse, whilst one or more compute nodes will store data and perform computations.
https://docs.aws.amazon.com/redshift/latest/dg/c_high_level_system_architecture.html
Option A is INCORRECT because the leader node does not fetch data from underlying tables, it is the function of the compute nodes
Option C is INCORRECT because an in-memory buffer area is a caching service which is not the function of the leader node.
Option D is INCORRECT because writing to file and performing computations and queries is the function of the compute nodes

A startup company for social media apps would like to grant freelance developers temporary access to its Lambda functions setup on AWS. These developers would be signing-in via Facebook authentication. Which service is most appropriate to use in securely granting access?

 A. Create user credentials using Identity Access Management, IAM
 B. Use Amazon Cognito for web-identity federation 
 C. Create temporary access roles using IAM
 D. Use a third-party Web ID, federated access provider
Correct Answer – B
Amazon Cognito web identity federation service acts as a broker that allows successfully authenticated users access to AWS resources. After successful authentication on platforms such as Facebook, LinkedIn or Google – users are awarded temporary authentication code from Amazon Cognito thereby gaining temporary access.
https://aws.amazon.com/cognito/
Option A. is INCORRECT because the access required is temporary and from a social media sign-in not directly onto the AWS environment. Identity Access Management (IAM) user will be granted access directly using AWS specified credentials.
Option C. in INCORRECT because the IAM user credentials will not authenticate on Facebook, they are confined to logging onto the AWS environment in this instance.
Option D. is INCORRECT because there is no need to take on third-party Web ID, federated access providers since Amazon has the Cognito service to perform that function.

Which of the following services can be used as a web application firewall in AWS.

 A. AWS EC2
 B. AWS WAF 
 C. AWS Firewall 
 D. AWS Protection
Answer – B
The AWS Documentation mentions the following
AWS WAF is a web application firewall that lets you monitor the HTTP and HTTPS requests that are forwarded to Amazon CloudFront or an Application Load Balancer. AWS WAF also lets you control access to your content.
For more information on AWS WAF, please refer to the below URL:
https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html

A developer would like to automate the installation, updating of a set of applications on a series of EC2 instances and on-premise servers. Which is the most appropriate service to use to achieve this requirement?

 A. AWS CodeBuild
 B. AWS CodeCommit
 C. AWS CodeDeploy 
 D. AWS CloudFormation 
Correct Answer – C
AWS CodeDeploy is a deployment service that allows developers to automate the installation of applications to hosts, Amazon EC2 instances, Amazon ECS instances, serverless Lambda functions or even on-premises servers. AWS CodeDeploy can enable the update of those applications.
https://docs.aws.amazon.com/codedeploy/latest/userguide/welcome.html
Option A. is INCORRECT because AWS CodeBuild is a fully managed service that primarily compiles source code and runs unit tests with the output being artifacts that will be ready for deployment.
https://docs.aws.amazon.com/codebuild/latest/userguide/welcome.html
Option B. is INCORRECT because AWS CodeCommit service primarily serves the function of controlling software build versions as well as a private storage for software development assets such as binary files, source code and related documentation.
https://docs.aws.amazon.com/codecommit/latest/userguide/welcome.html
Option D. is INCORRECT because AWS CloudFormation will not be able to run deployments of applications onto on-premises infrastructure. Furthermore, AWS CloudFormation automates the deployment of AWS resources but not applications and code onto hosts.

In Amazon S3, what is the difference between lifecycle policies and intelligent tiering?

 A. Lifecycle policies are not dependant on access patterns as is the case with intelligent tiering, instead they are pre-configured with a transition rule. 
 B. Intelligent tiering is an object storage class which is not dependant on access patterns, it uses a pre-configured transition rule. 
 C. When transitioning objects into different storage classes, intelligent tiering is automatic whilst lifecycle policies have to be manually triggered.
 D. Lifecycle policies cannot be configured to permanently delete objects from an S3 bucket whilst intelligent tiering can do so if versioning is turned on.
Correct Answer – A
Within Amazon S3, lifecycle policies are used to automatically transition objects through different storage classes in accordance to a preconfigured rule. This rule will typically move the object regardless of how frequently it is accessed.
https://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html
Option B. is incorrect because intelligent tiering uses access patterns when determining transitioning action.
https://aws.amazon.com/s3/storage-classes/
Option C. is incorrect because lifecycle policies are automatically triggered when the ‘days after creation’ period lapses.
Option D. is incorrect because lifecycle policies can indeed be configured to permanently delete objects. Intelligent tiering cannot be configured to permanently delete objects even if versioning is turned on for the objects.

What is the best-suited file storage option for use when an administrator is looking to deploy shared file access, linux-based workloads which will require up to petabytes of data stores?

 A. Amazon EFS 
 B. Amazon S3
 C. AWS Snowball
 D. Amazon EBS 
Correct Answer – A
Amazon Elastic File Storage (EFS) is the best-suited file storage option for the described scenario as it is designed for shared file access as well as scaling to petabyte data store.
https://aws.amazon.com/efs/when-to-choose-efs/
Option B. is incorrect because Amazon S3 is an object data store which is not suitable for deploying linux-based workloads as the scenario outlines.
Option C. is incorrect because AWS Snowball is a data transport solution and data migration which is not suitable for deploying shared file access builds.
https://aws.amazon.com/snowball/
Option D. is incorrect because Amazon Elastic Block store is block storage service for access by an EC2 instance but without the capability of a share file access. Applications that utilize persistent or dedicated block storage for a single instance can use Amazon EBS storage.
https://aws.amazon.com/efs/when-to-choose-efs/

A group of developers for a startup company store their source code and binary files on a shared open-source repository platform which is publicly accessible over the internet. They have embarked on a new project in which their client requires high confidentiality and security on all development assets. What AWS service can the developers use to meet the requirement?

 A. AWS CodeCommit 
 B. AWS CodeDeploy
 C. AWS Lambda
 D. AWS CodeStar
Correct Answer – A
AWS CodeCommit is a managed source control service that can be used as a data store to store source code, binaries, scripts, HTML pages and images which are accessible over the internet. CodeCommit encrypts files in transit and at rest which fulfills the additional client requirement (high confidentiality & security) mentioned in the question. Also, CodeCommit works well with Git tools, and other existing CI/CD tools.
https://aws.amazon.com/codecommit/
Option B. is INCORRECT because AWS CodeDeploy is a deployment service that automates application deployments to Amazon EC2 instances, on-premises instances, serverless Lambda functions, or Amazon ECS services.
https://docs.aws.amazon.com/codedeploy/latest/userguide/welcome.html
Option C. is INCORRECT because AWS Lambda will allow the developers in the scenario to run code without provisioning or managing servers. The company would pay only for the compute time consumed – there would be no charge when your code is not running.
https://aws.amazon.com/lambda/
Option D. is INCORRECT because AWS CodeStar provides a unified user interface, enabling you to easily manage your software development activities in one place. With AWS CodeStar, you can set up your entire continuous delivery toolchain in minutes, allowing you to start releasing code faster. AWS CodeStar makes it easy for your whole team to work together securely, allowing you to easily manage access and add owners, contributors, and viewers to your projects.
https://aws.amazon.com/codestar/

A start-up organisation would like to instantaneously deploy a complex web and mobile application development environment, complete with the necessary resources and peripheral assets. How can this be achieved efficiently?

 A. By putting together the necessary components from AWS services, starting with EC2 instances.
 B. Creating AWS Lambda functions that will be triggered by single-button click to call the appropriate API of the respective resources and peripheral assets needed.
 C. Using AWS Quick Starts to identify and provision the appropriate AWS CloudFormation templates 
 D. Making use of the AWS Serverless Application Repository to identify and deploy the resources needed for a web and mobile application development environment.
Correct Answer – C
AWS CloudFormation can be used in conjunction with AWS Quick Starts templates, which are a repository of AWS CloudFormation templates designed by expert architects. These can include third-party resources and peripheral assets tailor-made for a single-button push deployment of specific environments.
https://aws.amazon.com/quickstart/?quickstart-all.sort-by=item.additionalFields.updateDate&quickstart-all.sort-order=desc
Option A. is INCORRECT because it is cumbersome and not efficient to put together the AWS services and resources necessary to deploy a complex web and mobile application development environment.
Option B. is INCORRECT because it is tedious and not efficient to create AWS Lambda function for each of the required components.
Option D. is INCORRECT because AWS Serverless Application Repository is primarily used by developers and enterprises to search, look-up, publish and deploy serverless applications on the cloud.
https://docs.aws.amazon.com/serverlessrepo/latest/devguide/what-is-serverlessrepo.html

Which use case would warrant the cost-effective implementation of Amazon EC2 Reserved Instances with Spot Instances in the same build?

 A. A build that has sudden unpredictable workload spikes but for a short time horizon
 B. One in which there is a predictable resource demand over a long time horizon
 C. One that has a predictable workload over a long time horizon with prolonged and unpredictable spikes. 
 D. One that has a constantly predictable workload with brief unpredictable spikes 
Correct Answer – D
In use cases that are characterised by a constantly predictable workload with brief unpredictable spikes, Amazon EC2 Reserved Instances would be the most cost-effective to meet the constantly predictable workload. Whilst Spot Instances in an auto scaling group would be suffice to meet the demands of the build.
https://aws.amazon.com/solutions/case-studies/mercadolibre-ec2/
Option A. is INCORRECT because this use case would be cost-effectively serviced by Amazon EC2 Reserved Instances with on-demand instances in an auto scaling group to meet the resource demands of the spike.
Option B. is INCORRECT because this use case would be cost-effectively serviced by Amazon EC2 Reserved Instances alone.
Option C. is INCORRECT because this use case would be cost-effectively serviced by Amazon EC2 Reserved Instances with on-demand instances in an auto scaling group to meet the resource demands of the spike.

A building access security system is generating inaccurate logs because users often share access tags when entering the building. How can this be solved effectively?

 A. Encourage users not to share tags by introducing violation penalties
 B. Use Amazon Rekognition 
 C. Implement Amazon SageMaker
 D. Implement Amazon Transcribe
Correct Answer – B
Amazon Rekognition enables the uptake of imagery and video for analysis in applications. By uploading imagery or video footage to the Rekognition API, the service engine would then identify and distinguish facial features, text, objects and activities. This service will meet the requirements of the scenario as an access control solution.
https://docs.aws.amazon.com/rekognition/latest/dg/what-is.html
Option A. is INCORRECT because though the method could deter users from sharing tags, it could still happen. It is not an effective way of managing user access.
Option C. is INCORRECT because AWS SageMaker is a fully managed machine learning service. Developers build and train machine learning models, then deploy them into a live hosted environments. This services will not meet the requirements of the scenario.
Option D. is INCORRECT because AWS Transcribe uses machine learning technologies to convert audio files, spoken words, into plain text. The service will not resolve the scenario.

Which tool can you use to forecast your AWS spending?

 A. AWS Organizations
 B. Amazon Dev Pay
 C. AWS Trusted Advisor
 D. AWS Cost Explorer 
Answer – D
The AWS Documentation mentions the following
Cost Explorer is a free tool that you can use to view your costs. You can view data up to the last 13 months, forecast how much you are likely to spend for the next three months, and get recommendations for what Reserved Instances to purchase. You can use Cost Explorer to see patterns in how much you spend on AWS resources over time, identify areas that need further inquiry, and see trends that you can use to understand your costs. You also can specify time ranges for the data, and view time data by day or by month.
For more information on the AWS Cost Explorer, please refer to the below URL:
http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-explorer-what-is.html
A, B and C are incorrect. These services do not relate to billing and cost.

A radio station compiles a list of the most popular songs each year and will seldom refer to the information thereafter. Listeners can get access to this information up to 24 hours after request. Which is the most cost-effective object storage for this information?

 A. Amazon S3 Glacier 
 B. Amazon S3 One Zone – Infrequently Accessed
 C. Amazon S3 Glacier Deep Archive 
 D. Amazon S3 Standard – Infrequently Accessed
Correct Answer – C
Amazon S3 Glacier Deep Archive is the most cost-effective object storage to implement because the information will be rarely accessed and when it is accessed, its retrieval period will not be instant.
https://aws.amazon.com/s3/faqs/#Amazon_S3_Glacier_Deep_Archive
Option A. is incorrect because the information is relevant once, when it is created and might not be referred to again, Amazon S3 Glacier is appropriate to a certain degree but not the most cost-effective option.
Option B. is incorrect because Amazon S3 One Zone – Infrequently Accessed is suitable for information that warrants a short retrieval time. In the scenario, a short retrieval time is not critical.
Option D. is incorrect because Amazon S3 Standard – Infrequently Accessed is not a cost-effective option since the list of songs will only be relevant once and then rarely accessed thereafter.

Which of the following is a factor when calculating Total Cost of Ownership (TCO) for the AWS Cloud?

 A. The number of servers migrated to AWS 
 B. The number of users migrated to AWS
 C. The number of passwords migrated to AWS
 D. The number of keys migrated to AWS
Answer – A
Running servers will incur costs. The number of running servers is one factor of Server Costs; a key component of AWS’s Total Cost of Ownership (TCO).
For more information on AWS TCO, please refer to the below URL:
https://aws.amazon.com/blogs/aws/the-new-aws-tco-calculator/
B, C and D are incorrect. These are not factors in AWS’s Total Cost of Ownership.

There is a requirement to host a database server for a minimum period of one year. Which of the following would result in the least cost?

 A. Spot Instances 
 B. On-Demand
 C. No Upfront costs Reserved
 D. Partial Upfront costs Reserved 
Answer – D
If the database is going to be used for a minimum of one year at least , then it is better to get Reserved Instances. You can save on costs , and if you use a partial upfront options , you can get a better discount
For more information on AWS Reserved Instances, please visit the Link:
https://aws.amazon.com/ec2/pricing/reserved-instances/
A is incorrect. Spot instances can be terminated with fluctuations in market prices. Unless the question specifies a use case where high availability is not a requirement, this cannot be assumed.
B is incorrect. On-Demand is not the most cost efficient solution.
C is incorrect. No upfront payment is required , however its costlier option than Partial/All upfront payment.
For more information on Reserved Instances Payment option, please check below AWS Docs:
https://docs.aws.amazon.com/aws-technical-content/latest/cost-optimization-reservation-models/reserved-instance-payment-options.html
Note:
Reserved Instances do not renew automatically; when they expire, you can continue using the EC2 instance without interruption, but you are charged On-Demand rates. In the above example, when the Reserved Instances that cover the T2 and C4 instances expire, you go back to paying the On-Demand rates until you terminate the instances or purchase new Reserved Instances that match the instance attributes.
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-reserved-instances.html

Amazon Elastic Compute Cloud (Amazon EC2) Spot instances would be most appropriate for which of the following scenarios:

 A. Workloads that are only run in the morning and stopped at night
 B. Workloads where the availability of the Amazon EC2 instances can be flexible 
 C. Workloads that need to run for long periods of time without interruption
 D. Workloads that are critical and need Amazon EC2 instances with termination protection
Answer – B
The AWS documentation mentions the following
Spot Instances are a cost-effective choice if you can be flexible about when your applications run and if your applications can be interrupted. For example, Spot Instances are well-suited for data analysis, batch jobs, background processing, and optional tasks
For more information on AWS Spot Instances, please refer to the below URL:
http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html
A, C and D are incorrect. Since spot instances can be terminated by Amazon depending on market prices, it cannot be guaranteed to run during specific period of need, computing with time constraints or highly critical computing.

During an organisation’s information systems audit, the administrator is requested to provide a dossier of security and compliance reports as well as online service agreements that exist between the organisation and AWS. Which service can they utilize to acquire this information?

 A. AWS Artifact 
 B. AWS Resource Center
 C. AWS Service Catalog
 D. AWS Directory Service
Correct Answer – A
AWS Artifact is a comprehensive resource center for access to AWS’ auditor issued reports as well as security and compliance documentation from several renowned independent standards organisations.
https://aws.amazon.com/artifact/
Option B. is INCORRECT because the AWS Resource Center a repository of tutorials, whitepapers, digital trainings and project Use cases that aid in learning the core concepts of Amazon Web Services.
https://aws.amazon.com/getting-started/
Option C. is INCORRECT because AWS Service Catalog allows organisations to create and save their own IT service catalogs for use, they have to be approved by AWS. IT service catalogs can be multi-tiered application architectures.
https://docs.aws.amazon.com/servicecatalog/latest/adminguide/introduction.html
Option D. is INCORRECT because AWS Directory Service is an AWS tool that provides multiple ways to use Amazon Cloud Directory and Microsoft Active Directory with other AWS services.
https://docs.aws.amazon.com/directoryservice/latest/admin-guide/what_is.html

What can be termed as a user-defined label that has a key-value pair of variable character length. It is assigned to AWS resources as metadata for administration and management purposes?

 A. Resource Tag 
 B. Resource Group
 C. Resource Flag
 D. Tag key
Correct Answer – A
AWS Resource tags are critical component when architecting in the cloud, they create an identifying mechanism for the user to group, classify and order all their provisioned resources appropriately.
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html
Option B. is INCORRECT because AWS Resource groups enable the ordering of AWS resources into logical groupings. Resources can be ordered by application, environment or software component.
Option C. is INCORRECT because flags are used in AWS CloudFormation, the option is inaccurate.
Option D. is INCORRECT because a tag key is only part of what makes up a resource tag, each resource tag will have a key and value string.

The Trusted Advisor service provides insight regarding which five categories of an AWS account?

 A. Security, fault tolerance, high availability, connectivity and Service Limits
 B. Security, access control, high availability, performance and Service Limits
 C. Performance, cost optimization, security, fault tolerance and Service Limits 
 D. Performance, cost optimization, access control, connectivity and Service Limits
Answer – C
Below is the screenshot of what services the Trusted Advisor Dashboard offers.


For more information on the AWS Trusted Advisor, please visit the Link:
https://aws.amazon.com/premiumsupport/trustedadvisor/

What best describes the “Principle of Least Privilege”? Choose the correct answer from the options given below:

 A. All users should have the same baseline permissions granted to them to use basic AWS services.
 B. Users should be granted permission to access only resources they need to do their assigned job. 
 C. Users should submit all access requests in written form so that there is a paper trail of who needs access to different AWS resources.
 D. Users should always have a little more access granted to them then they need, just in case they end up needed it in the future.
Answer – B
The principle means giving a user account only those privileges which are essential to perform its intended function. For example, a user account for the sole purpose of creating backups does not need to install software: hence, it has rights only to run backup and backup-related applications.
For more information on principle of least privilege, please refer to the following Link:
https://en.wikipedia.org/wiki/Principle_of_least_privilege
A, C and D are incorrect. These actions would not adhere to the Principle of Least Privilege.

An administrator would like to automate the creation of new AWS accounts for the research and development department of the organisation where new workloads need to be spun-up promptly and categorized into groups. How can this be achieved efficiently?

 A. Use of AWS CloudFormation would be sufficient 
 B. Use of AWS Organisations 
 C. Using the AWS API to programmatically create each account via command line interface
 D. AWS Identity Access Management (IAM)
Correct Answer – B
AWS Organizations allows the user to automate the creation of new AWS accounts when they need to quickly launch new workloads. The administrator can add these new accounts to user-defined groups in an organization for easy categorization. For example, you can create separate groups to categorize development and production accounts, and then apply a Service Control Policy (SCP) to the production group allowing only access to AWS services required by production workloads.
https://aws.amazon.com/organizations/
Option A. is INCORRECT because AWS CloudFormation does not aide in the automated AWS account creation. AWS CloudFormation provides a common language for the administrator to describe and provision all the infrastructure resources in their cloud environment. CloudFormation allows the administrator to use a simple text file to model and provision, in an automated and secure manner, all the resources needed for applications across all regions and accounts. This file serves as a single source of truth for your cloud environment.
https://aws.amazon.com/cloudformation/
Option C. is INCORRECT because using AWS API to programmatically create each account via command-line interface is feasible but not efficient.
The AWS Command Line Interface (CLI) is a unified tool to manage your AWS services. With just one tool to download and configure, you can control multiple AWS services from the command line and automate them through scripts.
https://aws.amazon.com/cli/
Option D. is INCORRECT because using AWS Identity Access Management (IAM) to fulfill the task is inefficient and tedious. AWS Identity and Access Management (IAM) enables you to manage access to AWS services and resources securely. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources. IAM is a feature of your AWS account offered at no additional charge. You will be charged only for use of other AWS services by your users.
https://aws.amazon.com/iam/

According to the AWS, what is the benefit of Elasticity?

 A. Minimize storage requirements by reducing logging and auditing activities 
 B. Create systems that scale to the required capacity based on changes in demand 
 C. Enable AWS to automatically select the most cost-effective services.
 D. Accelerate the design process because recovery from failure is automated, reducing the need for testing
Answer – B
The concept of Elasticity is the means of an application having the ability to scale up and scale down based on demand. An example of such a service is the Autoscaling service
For more information on AWS Autoscaling service, please refer to the below URL:
https://aws.amazon.com/autoscaling/
A, C and D are incorrect. Elasticity will not have positive effects on storage, cost or design agility.

One of a blogger’s articles has gone viral which has resulted in a lot of traffic to their blog. This excessive amount of traffic has in turn caused poor browsing experience for some readers. How can normal service to the blog be restored?

 A. Set up a Web Application Firewall (WAF) that will allow legitimate traffic and deny maliciously generated traffic.
 B. Set up Read replicas on the backend RDS instance where the article resides. 
 C. Upgrade the backend RDS instance to a non-relational database.
 D. Configure Multi-AZ to enhance the performance of the backend RDS instances running the blog. 
Correct Answer – B
Read replicas will enhance the database performance and durability by allowing for automated distribution of load amongst several database instances with the exact copy of the parent database. In this scenario the web server will read the target article from several RDS instances in the read replica cluster, thereby getting good response times, consequently improving browsing experience.
https://aws.amazon.com/rds/details/read-replicas/
Option A. is INCORRECT because the increase in traffic is not due to malicious synthetic traffic, therefore setting up a Web Application Firewall (WAF) would not meet the requirements of the scenario.
Option C. is INCORRECT because upgrading the RDS instance to non-relation instance will still result in a high amount of read requests from the web server, therefore will not meet the needs of the scenario.
Option D. is INCORRECT because Multi-AZ will not enhance the performance and durability of the RDS instance in the scenario. It would ensure that the RDS instance remains reachable even when the AWS Availability Zone it was initially provisioned in is down or unreachable
https://aws.amazon.com/rds/details/multi-az/

As per the AWS Acceptable Use Policy, penetration testing of EC2 instances:

 A. May be performed by AWS, and will be performed by AWS upon customer request.
 B. May be performed by AWS, and is periodically performed by AWS.
 C. Are expressly prohibited under all circumstances.
 D. Can be performed by the customer, provided they work with the list of services mentioned by AWS. 
 E. May be performed by the customer on their owninstances, only if performed from EC2 instances. 
Answer – D.
You no need to take prior authorization from AWS before doing a penetration test on EC2 Instances.
Please refer to the below URL: for more details.
https://aws.amazon.com/security/penetration-testing/
A, B and C are incorrect. AWS says as below:
############
Permitted Services – You’re welcome to conduct security assessments against AWS resources that you own if they make use of the services listed below. We’re constantly updating this list; click here to leave us feedback, or request for inclusion of additional services:
o Amazon EC2 instances, NAT Gateways, and Elastic Load Balancers
o Amazon RDS
o Amazon CloudFront
o Amazon Aurora
o Amazon API Gateways
o AWS Lambda and Lambda Edge functions
o Amazon Lightsail resources
o Amazon Elastic Beanstalk environments
###########

A new department has recently joined the organization and the administrator needs to compose access permissions for the group of users. Given that they have varying roles and access needs, what is the best-practice approach when granting access?

 A. After gathering information on their access needs, the administrator should allow every user to access the most common resources and privileges on the system.
 B. The administrator should grant all users the same permissions and then grant more upon request.
 C. The administrator should grant all users the least privilege and add more privileges to only to those who need it. 
 D. Users should have no access and be granted temporary access on the occasions that they need to execute a task.
Correct Answer – C
The best-practice for AWS Identity Access Management (IAM) is to grant the least amount of permissions on the system, enough to only execute the required tasks of the user’s role. Additional permissions can be granted per user in accordance to the tasks they wish to perform on the system.
https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#grant-least-privilege
Option A. is incorrect because granting users access to the most common resources presents security vulnerabilities, especially from those who have access to resources they do not need.
Option B. is incorrect because granting users the same privileges on the system means other users might get access to resources they do not need to carry out their job functions. This presents a security risk.
Option D. is incorrect because the users are part of the organisation, it will be cumbersome for the administrator to constantly create temporal access passes for internal staff.

An organisation utilizes a software suite, that consists of a multitude of underlying microservices hosted on the cloud. The application is frequently giving runtime errors. Which service will help in the troubleshooting process?

 A. AWS CloudTrail
 B. AWS CloudWatch 
 C. AWS X-Ray 
 D. Amazon Elasticsearch Service
Correct Answer – C
AWS X-Ray helps developers analyze and debug production, distributed applications, such as those built using a microservices architecture. With X-Ray, developers can understand how the application and its underlying services are performing to identify and troubleshoot the root cause of performance issues and errors. X-Ray provides an end-to-end view of requests as they travel through an application, and shows a map of an application’s underlying components.
https://aws.amazon.com/xray/
Option A. is INCORRECT because AWS CloudTrail primarily records user or API activity, ‘who has done what’. It logs, continuously monitors, and retains account activity related to actions across AWS infrastructure. CloudTrail provides event history in the AWS account activity but NOT that of the interaction of software microservices within a suite.
https://aws.amazon.com/cloudtrail/
Option B. is INCORRECT because AWS CloudWatch does the primary function of monitoring and NOT debugging. It collates data and actionable insights to monitor applications, responds to system-wide performance changes, optimize resource utilization, and get a unified view of operational health. The service, however, does neither debugs nor logs errors that occur amongst software microservices within a suite.
https://aws.amazon.com/cloudwatch/
Option D. is INCORRECT because Amazon Elasticsearch is a fully managed service that enables the secure ingest of data from any source so that it can be searched, analyzed, and visualized it in real time. It does not allow for debugging or error detection.
https://aws.amazon.com/elasticsearch-service/

The main benefit of decoupling an application is to:

 A. Create a tightly integrated application
 B. Reduce inter-dependencies so failures do not impact other components 
 C. Enable data synchronization across the web application layer.
 D. Have the ability to execute automated bootstrapping actions.
Answer – B
The entire concept of decoupling components is to ensure that the different components of an applications can be managed and maintained separately. If all components are tightly coupled then when one component goes down , the entire application would do down. Hence it is always a better design practice to decouple application components.
For more information on a decoupled architecture, please refer to the below URL:
http://whatis.techtarget.com/definition/decoupled-architecture
A is incorrect. Decoupling would be the inverse of creating tight integration.
C and D are incorrect. Decoupling has no impact on these choices.

Which AWS services can be used to store files? Choose 2 answers from the options given below:

 A. Amazon CloudWatch
 B. Amazon Simple Storage Service (Amazon S3) 
 C. Amazon Elastic Block Store (Amazon EBS) 
 D. AWS Config
 E. Amazon Athena
Answer – B and C
The AWS documentation mentions the following
Amazon S3 is object storage built to store and retrieve any amount of data from anywhere – web sites and mobile apps, corporate applications, and data from IoT sensors or devices. It is designed to deliver 99.999999999% durability, and stores data for millions of applications used by market leaders in every industry.
For more information on the Simple Storage Service, please refer to the below URL:
https://aws.amazon.com/s3/
Amazon Elastic Block Store (Amazon EBS) provides persistent block storage volumes for use with Amazon EC2 instances in the AWS Cloud. Each Amazon EBS volume is automatically replicated within its Availability Zone to protect you from component failure, offering high availability and durability.
For more information on Amazon EBS, please refer to the below URL:
https://aws.amazon.com/ebs/
Answer A is incorrect. Amazon CloudWatch is used for performance monitoring.
Answer D is incorrect. AWS Config is used to audit and monitor configuration changes.
Answer E is incorrect. Amazon Athena is a serverless query service used to analyze BigData stored in S3.

Which of the following solutions can improve the performance of a web server that receives high levels of traffic, running an online banking portal? (Select TWO).

 A. Web server to be configured with a private IP address and hosted behind a NAT gateway
 B. Web server to be configured with a public IP address and hosted behind a WAF
 C. For an added layer of security, host the web server on a Content Distribution Network (CDN)
 D. Use of SSL acceleration 
 E. Relieve computational overhead on the web server by offloading HTTPS session processes to hardware security modules in an AWS CloudHSM cluster. 
Correct Answer – D, E
During the SSL/TLS session transactions between the browsers and web server, there is a heightened demand for computational capacity thus offloading these processes to AWS CloudHSM cluster would greatly improve the performance of the web server. This is referred to as SSL acceleration.
https://docs.aws.amazon.com/cloudhsm/latest/userguide/ssl-offload.html
Option A. is INCORRECT because configuring the server to a private IP address behind a NAT gateway will not improve the performance of the web server, though it will add a security layer.
Option B. is INCORRECT because configuring the server with a public IP address will not add any performance enhancement to the web server.
Option C. is INCORRECT because hosting the server on a CDN will not add a layer of security.
https://aws.amazon.com/cloudfront/

“S3 Intelligent-Tiering” object storage class delivers automatic cost savings by moving data between which of the two access tiers?

 A. Standard access and Frequent access
 B. Frequent access and Infrequent access 
 C. Standard access and Infrequent access
 D. Standard access and One Zone-Infrequent access
Correct Answer – B
S3 Intelligent-Tiering stores objects in two access tiers: one tier that is optimized for frequent access and another lower-cost tier that is optimized for infrequent access. The transitioning is based on the access patterns of the objects.
https://aws.amazon.com/about-aws/whats-new/2018/11/s3-intelligent-tiering/
Option A. is incorrect because Amazon S3 intelligent tiering storage class does not transition objects into the Standard storage class
Option C. is incorrect because the Standard storage class though similar to Frequent access, is not the same.
Option D. is incorrect because Amazon S3 intelligent tiering storage class does not transition objects into the Standard and One Zone-Infrequent access classes.

Which AWS service gives the user the ability to group AWS resources across different AWS Regions by application and then collectively view their operational data for monitoring purposes?

 A. Systems Manager 
 B. Management Console
 C. Resource Groups
 D. Resource Access Manager (AWS RAM) 
Correct Answer – A
AWS Systems Manager allows users to gain control of their AWS resources by unifying services into a user interface. One in which they can be able to view, automate and monitor operational tasks.
https://aws.amazon.com/systems-manager/
https://docs.aws.amazon.com/systems-manager/latest/userguide/what-is-systems-manager.html
Option B. is incorrect because the Manage Console is a web-based graphical user interface that users interact with when administering AWS services and resources.
https://docs.aws.amazon.com/awsconsolehelpdocs/latest/gsg/getting-started.html?id=docs_gateway#learn-whats-new
Option C. is incorrect because Resource Groups are a collection of AWS resources within a single AWS Region. In the scenario, the AWS resources are in different AWS Regions.
https://docs.aws.amazon.com/ARG/latest/userguide/welcome.html
Option D. is incorrect because Resource Access Manager (AWS RAM) allows users to share resources with other AWS accounts or via AWS Organizations. AWS RAM can be used to collate a set of AWS resources across multiple AWS accounts in order to share capacity.
https://docs.aws.amazon.com/ram/latest/userguide/what-is.html

Which of the following is the concept of the Elastic load balancer?

 A. To distribute traffic to multiple EC2 Instances 
 B. To scale up EC2 Instances
 C. To distribute traffic to AWS resources across multiple regions
 D. To increase the size of the EC2 Instance based on demand
Answer – A
The AWS Documentation mentions the following
A load balancer distributes incoming application traffic across multiple EC2 instances in multiple Availability Zones. This increases the fault tolerance of your applications. Elastic Load Balancing detects unhealthy instances and routes traffic only to healthy instances.
For more information on the Elastic Load Balancer service, please refer to the below URL:
https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/introduction.html

An administrator would like to prepare a report that will be presented to the auditing team. The report is meant to depict that the organisations’ cloud infrastructure has followed the widely accepted industry standards of deployment, maintenance and monitoring. Which tool can they use to assist them?

 A. AWS CloudTrail 
 B. AWS Trusted Advisor
 C. AWS Organisations
 D. AWS Total Cost of Ownership
Correct Answer – A
AWS CloudTrail is a service that primarily tracks governance, compliance, operational auditing, and risk auditing of your AWS account. CloudTrail logs continuously monitors, and retains account activity related to actions across all AWS infrastructure. CloudTrail provides event history of AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command line tools, and other AWS services. This event history simplifies security analysis, resource change tracking, and troubleshooting.
https://aws.amazon.com/cloudtrail/
Option B. is INCORRECT because AWS Trusted Advisor offers best practice checks and recommendations across five categories: cost optimization; security; fault tolerance; performance; and service limits. In the scenario, the administrator can be able to run a report on all of the organisation’s infrastructure and present the information to the auditors accordingly.
https://aws.amazon.com/premiumsupport/technology/trusted-advisor/
Option C. INCORRECT because AWS Organizations helps you centrally govern your environment as you grow and scale your workloads on AWS. Whether you are a growing startup or a large enterprise, Organizations helps you to centrally manage billing; control access, compliance, and security; and share resources across your AWS accounts. Using AWS Organizations, you can automate account creation, create groups of accounts to reflect your business needs, and apply policies for these groups for governance. You can also simplify billing by setting up a single payment method for all of your AWS accounts.
https://aws.amazon.com/organizations/
Option D. INCORRECT because AWS Total Cost of Ownership (TCO) helps in the assessment of cost of infrastructure versus using cloud services. The resources helps by reducing the need to invest in large capital expenditures and providing a pay-as-you-go model that empowers you to invest in the capacity you need and use only when the business requires it. TCO calculators allow for the estimation of the cost savings when using AWS and provide a detailed set of reports that can be used in executive presentations.
https://aws.amazon.com/tco-calculator/

What is the value of having AWS Cloud services accessible through an Application Programming Interface (API)?

 A. It allows developers to work with AWS resources programmatically 
 B. AWS resources will always be cost-optimized
 C. All application testing can be managed by AWS.
 D. Customer–owned, on–premises infrastructure becomes programmable.
Answer – A
It allows developers to easily work with the various AWS resources programmatically
For more information on the various programming tools available for AWS, please refer to the below URL:
https://aws.amazon.com/tools/
Option B is incorrect. The AWS API does not reduce cost.
Option C is incorrect. API allows the customer’s developers to work with resources, not AWS.
Options D is incorrect. The AWS API only allows the customer to manage AWS resources, not on-premise.

A file-sharing service uses Amazon S3 to store files uploaded by users. Files are accessed with random frequency, popular ones are downloaded every day whilst others not so often and some rarely. What is the most cost-effective Amazon S3 object storage class to implement?

 A. Amazon S3 Standard 
 B. Amazon S3 Glacier
 C. Amazon S3 One Zone-Infrequently Accessed
 D. Amazon S3 Intelligent-Tiering 
Correct Answer – D
S3 Intelligent-Tiering is a new Amazon S3 storage class designed for customers who want to optimize storage costs automatically when data access patterns change, without performance impact or operational overhead. S3 Intelligent-Tiering is the first cloud object storage class that delivers automatic cost savings by moving data between two access tiers — frequent access and infrequent access — when access patterns change, and is ideal for data with unknown or changing access patterns.
S3 Intelligent-Tiering stores objects in two access tiers: one tier that is optimized for frequent access and another lower-cost tier that is optimized for infrequent access. For a small monthly monitoring and automation fee per object, S3 Intelligent-Tiering monitors access patterns and moves objects that have not been accessed for 30 consecutive days to the infrequent access tier. There are no retrieval fees in S3 Intelligent-Tiering. If an object in the infrequent access tier is accessed later, it is automatically moved back to the frequent access tier. No additional tiering fees apply when objects are moved between access tiers within the S3 Intelligent-Tiering storage class. S3 Intelligent-Tiering is designed for 99.9% availability and 99.999999999% durability, and offers the same low latency and high throughput performance of S3 Standard.
https://aws.amazon.com/about-aws/whats-new/2018/11/s3-intelligent-tiering/
Option A. is incorrect because Amazon S3 Standard would be an inefficient class for storing those objects that will be accessed rarely.
Option B. is incorrect because storing objects that are frequently accessed in Amazon S3 Glacier would present operational bottlenecks since these objects would not be available instantly.
https://aws.amazon.com/s3/storage-classes/
Option C. is incorrect because storing those objects that are rarely accessed and those that would be accessed frequently in Amazon S3 One Zone-Infrequently Accessed would be inefficient.

You plan to deploy an application on AWS. This application needs to be PCI Compliant. Which of the below steps are needed to ensure compliance? Choose 3 answers from the below:

 A. Choose AWS services which are PCI Compliant 
 B. Ensure the right steps are taken during application development for PCI Compliance 
 C. Ensure the AWS Services are made PCI Compliant 
 D. Do an audit after the deployment of the application for PCI Compliance 
Answer – A, B and D

The below snapshot from the AWS Documentation mentions that some of the AWS services are already PCI compliant. This list should be checked when designing the application.



 

 

For more information on PCI Compliance and AWS, please refer to the following Link:
https://aws.amazon.com/compliance/pci-dss-level-1-faqs/
Apart from Option A & B, the application needs to be audited for PCI compliance.

C is incorrect. Some AWS services are PCI compliant but additional steps relating to Development may be required by the Customer to be fully PCI compliant.
Which AWS service automates infrastructure provisioning and administrative tasks for an analytical data warehouse?

 A. Amazon Redshift 
 B. Amazon DynamoDB
 C. Amazon ElastiCache
 D. Amazon Aurora 
Answer – A
The AWS documentation mentions the following
Amazon Redshift is a fully managed, petabyte-scale data warehouse service in the cloud. You can start with just a few hundred gigabytes of data and scale to a petabyte or more. This enables you to use your data to acquire new insights for your business and customers.
For more information on AWS Redshift, please refer to the below URL:
http://docs.aws.amazon.com/redshift/latest/mgmt/welcome.html
Choices B, C and D are incorrect. Amazon Redshift is the only data warehousing service out of the choices below.

A professional educational institution maintains a dedicated web server and database cluster that hosts an exam results portal for modules undertaken by its students. The resource is idle for most of the learning cycle and becomes excessively busy when exam results are released. How can this architecture be improved to be cost-efficient?

 A. Configure AWS elastic load-balancing between the webserver and database cluster
 B. Configure RDS multi-availability zone for performance optimisation
 C. Configure serverless architecture leveraging AWS Lambda functions 
 D. Migrate the web servers onto Amazon EC2 Spot Instances
Correct Answer – C
Leveraging AWS Lambda functions will remove the need to run a dedicated web server for the organisation. During periods of high requests to the database cluster, AWS lambda backend infrastructure will automatically scale out resources to adequately meet the demand. AWS Lambda provides a platform to run code without provisioning or managing any servers. The organisation pays only for the compute time they consume – there is no charge when your code is not running.
https://aws.amazon.com/lambda/
Option A. INCORRECT because the premise of the scenario is about cost-efficiency more than load and server responsiveness. Load-balancing would manage the traffic amongst the database clusters but would not relieve the organisation of maintaining a dedicated web server which only works occasionally.
https://aws.amazon.com/elasticloadbalancing/
Option B. INCORRECT because RDS multi-availability zone does not optimise the setup, rather it allows for disaster recovery, enhanced availability and durability. The scenarios requires a solution that reduces the cost of maintaining the organization’s infrastructure and run it efficiently.
https://aws.amazon.com/rds/details/multi-az/
Option D. INCORRECT because migrating to Amazon EC2 Spot Instances will negatively affect the operation of the portal during periods of high traffic. Instances could be terminated mid-transaction which would have adverse effects on the overall user experience. This would not be a cost-effective solution. Spot Instances let you take advantage of unused EC2 capacity in the AWS cloud. Spot Instances are available at up to a 90% discount compared to On-Demand prices. Spot Instances can reclaim the capacity back with two-minutes of notice.
https://aws.amazon.com/ec2/spot/

Which of the following is a benefit of running an application across two Availability Zones?

 A. Performance is improved over running in a single Availability Zone.
 B. It is more secure than running in a single Availability Zone.
 C. It significantly reduces the total cost of ownership versus running in a single Availability Zone.
 D. It increases the availability of an application compared to running in a single Availability Zone. 
The correct answer is Option D.
Each AZ is a set of one or more data centers. By deploying your AWS resources to multiple Availability zones , you are designing with failure in mind. So if one AZ were to go down , the other AZ’s would still be up and running and hence your application would be more fault tolerant.
For more information on AWS Regions and AZ’s, please refer to the below URL:
http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html
A, B and C are incorrect. Spreading an application across availability zones increases redundancy. It does not have a positive impact on performance, security or cost.

What is the AWS feature that enables fast, easy, and secure transfers of files over long distances between your client and your Amazon S3 bucket?

 A. File Transfer
 B. HTTP Transfer
 C. Amazon S3 Transfer Acceleration 
 D. S3 Acceleration 
Answer – C
The AWS Documentation mentions the following
Amazon S3 Transfer Acceleration enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. Transfer Acceleration takes advantage of Amazon CloudFront’s globally distributed edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimized network path.
For more information on S3 transfer acceleration, please visit the Link:
http://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html
Option A, B and D are incorrect. These features deal with transferring data but not between clients and an S3 bucket.

A department in an organisation has a stipulated monthly expenditure limit on their AWS account and is anxious about exceeding it. How best can they allay this concern?

 A. Regularly review their Billing and Cost management dashboard during the course of the month in the management console.
 B. Under Billing Preferences > Cost Management Preferences, they should tick the Receive Free Tier Usage Alerts checkbox.
 C. In AWS CloudWatch they ought to create an alarm that triggers each time the services bill surpasses the limit.
 D. In AWS Budgets, creating an email alert based on the budget parameters would suffice. 
Correct Answer – D
AWS Budgets provides a useful feature of setting custom budgets that prompt the user when their costs or usage are forecasted to exceed. The forecast aspect gives a buffer period in advance when alerting the user. Budgets can be tracked at the monthly, quarterly, or yearly level, and have customizable start and end dates. Alerts can be sent via email and/or Amazon Simple Notification Service (SNS) topic.
https://aws.amazon.com/aws-cost-management/aws-budgets/
Option A is INCORRECT because the regular review will not stop nor alert the department if their service bill were to exceed their stipulated budget.
https://docs.aws.amazon.com/account-billing/index.html
Option B is INCORRECT because selecting the Receive Free Tier Usage Alerts checkbox would notify the department each time their service bills goes out of the free-tier range only and not when it approaches the limit.
https://aws.amazon.com/about-aws/whats-new/2017/12/aws-free-tier-usage-alerts-automatically-notify-you-when-you-are-forecasted-to-exceed-your-aws-service-usage-limits/
Option C is INCORRECT because configuring an alarm in AWS CloudWatch that triggers after exceeding the bill will not meet the requirements of staying within the desired budget. The alarm triggers when the account billing exceeds the threshold specified. It triggers only when actual billing exceeds the threshold. It does not use projections based on the usage so far in the month.
https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/monitor_estimated_charges_with_cloudwatch.html

Which of the following is the concept of Autoscaling

 A. To scale out resources based on demand 
 B. To distribute traffic to multiple EC2 Instances
 C. To distribute traffic to AWS resources across multiple regions
 D. To increase the size of the EC2 Instance based on demand
Answer – A
The AWS Documentation mentions the following
AWS Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost. Using AWS Auto Scaling, it’s easy to setup application scaling for multiple resources across multiple services in minutes.
For more information on the Auto Scaling service, please refer to the below URL:
https://aws.amazon.com/autoscaling/

Your company has a set of EC2 Instances hosted in AWS. There is a requirement to create snapshots from the EBS volumes attached to these EC2 Instances in another geographical location. As per this requirement , where would you create the snapshots

 A. In another Availability Zone
 B. In another data center
 C. In another Region 
 D. In another Edge location
Answer – C
Regions correspond to different geographic locations in AWS.
For more information on Regions and Availability Zones in AWS, please refer to the below URL:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html