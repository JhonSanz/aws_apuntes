A company is planning to migrate their On-premises Services to the Cloud. Which of the following would help them do a cost benefit analysis of moving to the AWS Cloud.

 D. AWS Consolidating billing
 B. AWS Config
 A. AWS TCO calculator 
 C. AWS Cost Explorer 
Answer – A
The AWS Documentation mentions the following
Use this calculator to compare the cost of running your applications in an on-premises or colocation environment to AWS. Describe your on-premises or colocation configuration to produce a detailed cost comparison with AWS.
For more information on the TCO Calculator, please refer to the below URL:
https://awstcocalculator.com/

2 / 65
Which of the following disaster recovery deployment mechanisms that has the highest downtime

 C. Multi Site 
 A. Pilot light
 B. Warm standby
 D. Backup and Restore 
Answer – D
The below snapshot from the AWS Documentation shows the spectrum of the Disaster recovery methods. If you go to the further end of the spectrum you have the least time for downtime for the users.


In most traditional environments, data is backed up to tape and sent off-site regularly. If you use this method, it can take a long time to restore your system in the event of a disruption or disaster.
https://d1.awsstatic.com/whitepapers/aws-disaster-recovery.pdf
For more information on Disaster recovery techniques, please refer to the below URL:
https://aws.amazon.com/blogs/aws/new-whitepaper-use-aws-for-disaster-recovery/

3 / 65
Which of the following service is most useful when a Disaster Recovery method is triggered in AWS.

 A. Amazon Route 53 
 C. Amazon SQS
 B. Amazon SNS
 D. Amazon Inspector 
Answer – A
Rouet53 is a domain name system service by AWS. When a Disaster does occur , it can be easy to switch to secondary sites using the Route53 service.
The AWS Documentation additionally mentions the following
Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service. It is designed to give developers and businesses an extremely reliable and cost effective way to route end users to Internet applications by translating names like www.example.com into the numeric IP addresses like 192.0.2.1 that computers use to connect to each other. Amazon Route 53 is fully compliant with IPv6 as well
For more information on AWS Route53, please refer to the below URL:
https://aws.amazon.com/route53/
Option B – Amazon SNS
This service is used for notification service and primarily used for mass delivery of messages, predominantly to mobile users. This service will not help us when moving to the DR site, but rather can be used to inform the required users with reference to the change in the server.
https://aws.amazon.com/sns/
https://aws.amazon.com/disaster-recovery/
Option C – Amazon SQS
This service is a distributed message queuing service and supports programmatic sending of messages via web service applications as a way to communicate over the Internet. Since the question refers to triggering of service that is needed for DR job this service is not the required service for this requirement.
https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html
Option D – Amazon Inspector
This is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS. It automatically assesses applications for exposure, vulnerabilities, and deviations from best practices. For our requirement this service is not the correct option, reason we need to use a service that will help us in pointing the correct DNS server when an DR operation is done, so that the existing and new users doesn’t get disrupted from the services they are accessing.
https://aws.amazon.com/inspector/

4 / 65
Which of the following can be used to increase the fault tolerance of an application.

 D. Deploying resources across multiple AWS Accounts
 B. Deploying resources across multiple VPC’s
 C. Deploying resources across multiple Availability Zones 
 A. Deploying resources across multiple edge locations
Answer – C
Each AZ is a set of one or more data centers. By deploying your AWS resources to multiple Availability zones , you are designing with failure with mind. So if one AZ were to go down , the other AZ’s would still be up and running and hence your application would be more fault tolerant.
For more information on AWS Regions and AZ’s, please refer to the below URL:
http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html

5 / 65
Why is Amazon DynamoDB service best-suited for implementation in mobile, Internet of Things (IoT) and gaming applications?

 B. DynamoDB has a flexible data model and single-digit millisecond latency 
 C. Whilst in operation, DynamoDB instances are spread across at least three geographically distinct centers, AWS Regions
 A. DynamoDB is a fully-managed database instance with no infrastructure overheads
 D. DynamoDB supports eventual and strongly consistent reads
Correct Answer – B
The use cases mentioned in the scenario have unstructured data in common, therefore, the most appropriate attribute of Amazon DynamoDB is its flexible data model and single-digit millisecond latency.
https://aws.amazon.com/blogs/database/how-to-determine-if-amazon-dynamodb-is-appropriate-for-your-needs-and-then-plan-your-migration/
Option A. is INCORRECT because being fully-managed and having no infrastructure overheads does not distinguish DynamoDB as the best-suited solution for the given use cases.
Option C. is INCORRECT because the aspect of fault-tolerance, disaster recovery and high availability is also present in Amazon Relational Databases (RDS), this feature does not distinguish the service in accordance with the described use cases.
Option D. is INCORRECT because this attribute of DynamoDB does not fully justify its exclusive choice over other instances when considered for implementation in the use cases mentioned in the question.

6 / 65
Which of the following can be used to spin up EC2 instances on the AWS Cloud ?

 A. EBS Volumes
 D. Amazon VMware
 B. EBS Snapshots 
 C. Amazon Machine Image 
Answer – C
The AWS Documentation mentions the following
An Amazon Machine Image (AMI) provides the information required to launch an instance, which is a virtual server in the cloud. You specify an AMI when you launch an instance, and you can launch as many instances from the AMI as you need. You can also launch instances from as many different AMIs as you need.
For more information on Amazon Machine Images, please refer to the following Link:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html

7 / 65
Which of the following is the responsibility of AWS according to the Shared Security Model? Choose 3 answers from the options given below

 A. Managing AWS Identity and Access Management (IAM)
 C. Monitoring physical device security 
 B. Securing edge locations 
 D. Implementing service organization Control (SOC) standards 
Answer – B,C and D
The responsibility of AWS includes the following
1) Securing edge locations
2) Monitoring physical device security
3) Implementing service organization Control (SOC) standards
For more information on AWS Shared Responsibility Model, please refer to the below URL:
https://aws.amazon.com/compliance/shared-responsibility-model/

8 / 65
Which of the following features of Amazon RDS allows for better availability of databases. Choose 2 answers from the options given below

 D. Multi-Region 
 A. VPC Peering
 C. Read Replica’s 
 B. Multi-AZ 
Answer – B and C
The AWS Documentation mentions the following
If you are looking to use replication to increase database availability while protecting your latest database updates against unplanned outages, consider running your DB instance as a Multi-AZ deployment.
You can use Multi-AZ deployments and Read Replicas in conjunction to enjoy the complementary benefits of each. You can simply specify that a given Multi-AZ deployment is the source DB instance for your Read Replica(s). That way you gain both the data durability and availability benefits of Multi-AZ deployments and the read scaling benefits of Read Replicas.
For more information on AWS RDS, please visit the FAQ Link:
https://aws.amazon.com/rds/faqs/

9 / 65
Which of the following components of the Cloudfront service can be used to distribute contents to users across the globe.

 D. Amazon Edge locations 
 A. Amazon VPC
 B. Amazon Regions 
 C. Amazon Availability Zones
Answer – D
The AWS documentation mentions the following
Amazon CloudFront is a web service that speeds up distribution of your static and dynamic web content, such as .html, .css, .js, and image files, to your users. CloudFront delivers your content through a worldwide network of data centers called edge locations.
For more information on Amazon Cloudfront, please refer to the below URL:
http://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html

10 / 65
Which of the following AWS services use serverless technology. Choose 2 answers from the options given below.

 A. DynamoDB 
 C. Simple Storage Service 
 B. EC2
 D. AWS Autoscaling
Answer – A and C
The Simple Storage service and DynamoDB are services where you don’t need to manage the underlying infrastructure.
For more information on AWS S3 and DynamoDB, please refer to the below URL:
https://aws.amazon.com/compliance/shared-responsibility-model/
https://aws.amazon.com/s3/
https://aws.amazon.com/dynamodb/

11 / 65
By default who from the below roles has complete administrative control over all resources in the respective AWS account?

 C. AWS Security Team
 B. AWS Account Owner 
 A. AWS Support Team
 D. AWS Technical Account Manager (TAM)
Answer – B
The entire of control of data within an AWS account is with the Account Owner.
For more information on AWS Account identifiers, please refer to the below URL:
https://docs.aws.amazon.com/general/latest/gr/root-vs-iam.html
https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_accounts_create.html

12 / 65
You are the architect of a custom application running inside your corporate data center. The application runs with some unresolved bugs that produce a lot of data inside custom log files generating time-consuming activities to the operation team who is responsible for analyzing them.
You want to move the application to AWS using EC2 instances, and at the same time, take the opportunity for improving logging and monitoring capabilities but without touching the application code.
What AWS service should you use to satisfy the requirement?

 B. AWS CloudTrail
 D. AWS Application Logs
 C. AWS CloudWatch Logs 
 A. AWS Kinesis Data Streams
Answer: C
Option A is INCORRECT because in order to feed a Data Streams from custom logs you have to change the application code. AWS documentations describes this with the following sentence: “To put data into the stream, you must specify the name of the stream, a partition key, and the data blob to be added to the stream.”
Option B is INCORRECT because is unrelated to the scenario and custom log files.
Option C is CORRECT because AWS CloudWatch Logs has the capability to reuse existing application logs increasing efficiency in operation with the ability to generate on them metrics, alerts and analytics with AWS CloudWatch Logs Insight.
As the application and custom log files are exactly as they were when the application was running on-prem you don’t need to change any piece of application code that make them ingestible by AWS CloudWatch Logs
AWS official documentation in the FAQ section highlights the reusing capability with the sentence “AWS CloudWatch Logs lets you monitor and troubleshoot your systems and applications using your existing system, application and custom log files… so, no code changes are required.”
You can also leverage CloudWatch Metrics, Alarms and Dashboards with Logs to get full operational visibility into your applications. This empowers you to understand your applications, make improvements, and find and fix problems quickly, so that you can continue to innovate rapidly.
Option D is INCORRECT because AWS Application Logs does not exist.
Diagram: none
References:
https://aws.amazon.com/cloudwatch/faqs/

13 / 65
Which of the below cannot be used to get data from Amazon Glacier?

 D. AWS S3 Lifecycle policies 
 A. AWS Glacier API
 C. AWS Glacier SDK
 B. AWS Console 
Answer – B
Note that the AWS Console cannot be used to upload data onto Glacier. The console can only be used to create a Glacier vault which can be used to upload the data.
For more information on uploading data onto Glacier, please refer to the following Link:
https://docs.aws.amazon.com/amazonglacier/latest/dev/uploading-an-archive.html
Option A – AWS Glacier API
– AWS Glacier is a storage service optimized for infrequently used data, or “cold data”. This option is used for programatically access Glacier and work with it. Due to this reason this option is not matched with the question.
https://docs.aws.amazon.com/amazonglacier/latest/dev/amazon-glacier-api.html
Option C – AWS Glacier SDK: SDK i.e., Software Development Kit is used to develop applications for Amazon S3 Glacier. They provide libraries that map to the underlying REST API and provide objects that you can use to easily construct requests and process responses. Due to this reason, it’s not the valid answer for the asked question.
https://docs.aws.amazon.com/amazonglacier/latest/dev/using-aws-sdk.html
Option D – AWS S3 Lifecycle Policies: It’s an XML file, which comprises a set of rules with predefined actions that you want Amazon S3 to perform on objects during their lifetime. Using this we can have access to Glacier and work with it, and due to this, it’s not the correct answer to our question.???????
https://aws.amazon.com/about-aws/whats-new/2016/03/introducing-new-amazon-s3-lifecycle-policies/???????

14 / 65
Your company is planning to move to the AWS Cloud. You need to give a presentation on the cost perspective when moving existing resources to the AWS Cloud. When it comes to Amazon EC2, which of the following is an advantage when it comes to the cost perspective.

 D. Ability to tag instances to reduce the overall cost
 A. Having the ability of automated backups of the EC2 instance, so that you don’t need to worry about the maintenance costs.
 C. The ability to only pay for what you use 
 B. The ability to choose low cost AMI’s to prepare the EC2 Instances
Answer – C
One of the advantages of EC2 Instances is the per second billing concept. This is given in the AWS documentation also
With per-second billing, you pay for only what you use. It takes cost of unused minutes and seconds in an hour off of the bill, so you can focus on improving your applications instead of maximizing usage to the hour. Especially, if you manage instances running for irregular periods of time, such as dev/testing, data processing, analytics, batch processing and gaming applications, can benefit.
For more information on EC2 Pricing, please refer to the below URL:
https://aws.amazon.com/ec2/pricing/

15 / 65
Why does it take between 24 to 48 hours for changes made to a hosted zone in Amazon Route53 to reflect globally?

 A. AWS Name Servers need between 24 to 48 hours to create record sets, update their respective values and process changes.
 D. If changes to the hosted zone are made in the same AWS Region as the DNS resolver, it can take between 6 to 12 hours.
 B. DNS resolvers around the world can only reflect the changes in their cache after the Time To Live (TTL) has expired, it is 24 hours by default. 
 C. AWS Name Servers around the world update their cache in tandem, it takes between 24 hours to 48 hours for the process to complete.
Correct Answer – B
Generally, DNS resolvers query for changes every 86400 seconds, which means DNS resolver cache is stagnant for up to 24 hours. This can be changed, but the widely accepted time is 24 hours.
https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/troubleshooting-new-dns-settings-not-in-effect.html#troubleshooting-new-dns-settings-not-in-effect-cached-resource-record-set
Option A. is INCORRECT because AWS Name servers save the changes made to hosted zones within 60 seconds.
https://aws.amazon.com/route53/faqs/
Option C. is INCORRECT because Amazon Route53 uses a global network of interconnected DNS servers which simultaneously take up changes to a hosted zone. The process does not occur in tandem.
Option D. is INCORRECT because Amazon Route53 is not Region-specific, therefore it is not possible to determine in which AWS Region changes are made.

16 / 65
A company is deploying a two-tier, highly available web application to AWS. The application needs a storage layer to store artifacts such as photos and videos. Which of the following services can be used as the underlying storage mechanism?

 A. Amazon EBS volume
 B. Amazon S3 
 D. Amazon RDS instance
 C. Amazon EC2 instance store
Answer – B
Amazon S3 is the default storage service that should be considered for companies. It provides durable storage for all static content.
For more information on AWS S3, please visit the Link:
https://aws.amazon.com/s3/

17 / 65
A company wants to have a database hosted on AWS. As much as possible they want to have control over the database itself. Which of the following would be an ideal option for this.

 D. Using the Amazon Aurora service
 C. Hosting the database on an EC2 Instance 
 A. Using the AWS DynamoDB service
 B. Using the AWS RDS service
Answer – C
If you want a self-managed database, that means you want complete control over the database engine and the underlying infrastructure. In such a case you need to host the database on an EC2 Instance
For more information on EC2 Instances, please refer to the below URL:
https://aws.amazon.com/ec2/

18 / 65
You are planning on deploying a video based application onto the AWS Cloud. These videos will be accessed by users across the world. Which of the below services can help stream the content in an efficient manner to the users across the globe?

 B. Amazon Cloudtrail
 D. Amazon S3
 A. Amazon SES
 C. Amazon CloudFront 
Answer – C
The AWS Documentation mentions the following
Amazon CloudFront is a web service that gives businesses and web application developers an easy and cost effective way to distribute content with low latency and high data transfer speeds. Like other AWS services, Amazon CloudFront is a self-service, pay-per-use offering, requiring no long term commitments or minimum fees. With CloudFront, your files are delivered to end-users using a global network of edge locations.
For more information on CloudFront, please visit the Link:
https://aws.amazon.com/cloudfront/

19 / 65
Which of the following features of AWS RDS allows you to reduce the load on the database while reading data?

 C. Using snapshots
 D. Using Multi-AZ feature
 A. Cross region replication
 B. Creating Read Replicas 
Answer – B
The AWS Documentation mentions the following
You can reduce the load on your source DB Instance by routing read queries from your applications to the read replica. Read replicas allow you to elastically scale out beyond the capacity constraints of a single DB instance for read-heavy database workloads.
For more information on Read Replicas, please refer to the below URL:
https://aws.amazon.com/rds/details/read-replicas/

20 / 65
Which of the following scenarios is most appropriate to implement Amazon ElastiCache in order to improve on performance?

 C. Where there are frequent reads of dynamic content on a web application
 D. Where there are infrequent random reads to static content on a web application
 B. Where there are frequent reads of static content on a web application 
 A. Where there are frequent writes to a database instance
Correct Answer – B
In the scenario outlined in Option B, implementing and configuring Amazon ElastiCache will improve the performance by storing frequently accessed content in-memory. The storage type is a managed, high-speed, volatile and not disk-based, making information retrieval faster than disk-based stored content.
https://aws.amazon.com/caching/
Option A. is INCORRECT because caching frequent writes to a database instance will not be the most appropriate method to improve on its performance. Deploying the most appropriate storage type would be suffice.
Option C. is INCORRECT because caching dynamic content will still result in retrieval of content from disk. This would not improve on the performance. Caching is most effective when the same information or content is frequently accessed.
Option D. is INCORRECT because this scenario can be improved by opting for appropriate storage option. Random and infrequently accessed content will expire regularly whilst cached therefore, this will not improve the performance in the scenario.

21 / 65
Your company is planning to host a large ecommerce application on the AWS Cloud. One of their major concerns is Internet attacks such as DDos attacks. Which of the following services can help mitigate this concern. Choose 2 answers from the options given below

 C. AWS EC2
 D. AWS Config 
 A. Cloudfront 
 B. AWS Shield 
Answer – A and B
The AWS Documentation mentions the following on DDoS attacks
AWS Services for DDoS Attack Mitigation
AWS offers globally distributed, high network bandwidth and resilient services that, when used in conjunction with application-specific strategies, are key to mitigating DDoS attacks. For more information on how to leverage each of these services and details on how their various features help protect against DDoS attacks, see the whitepaper AWS Best Practices for DDoS Resiliency.
AWS Shield
AWS Shield is a managed DDoS protection service that is available in two tiers: Standard and Advanced. AWS Shield Standard applies always-on detection and inline mitigation techniques, such as deterministic packet filtering and priority-based traffic shaping, to minimize application downtime and latency. AWS Shield Standard is included automatically and transparently to your Elastic Load Balancing load balancers, Amazon CloudFront distributions, and Amazon Route 53 resources at no additional cost. When you use these services that include AWS Shield Standard, you receive comprehensive availability protection against all known infrastructure layer attacks. Customers who have the technical expertise to manage their own monitoring and mitigation of application layer attacks can use AWS Shield together with AWS WAF rules to create a comprehensive DDoS attack mitigation strategy.
AWS Shield Advanced provides enhanced DDoS attack detection and monitoring for application-layer traffic to your Elastic Load Balancing load balancers, CloudFront distributions, Amazon Route 53 hosted zones and resources attached to an Elastic IP address, such Amazon EC2 instances. AWS Shield Advanced uses additional techniques to provide granular detection of DDoS attacks, such as resource-specific traffic monitoring to detect HTTP floods or DNS query floods. AWS Shield Advanced includes 24×7 access to the AWS DDoS Response Team (DRT), support experts who apply manual mitigations for more complex and sophisticated DDoS attacks, directly create or update AWS WAF rules, and can recommend improvements to your AWS architectures. AWS WAF is included at no additional cost for resources that you protect with AWS Shield Advanced.
AWS Shield Advanced includes access to near real-time metrics and reports, for extensive visibility into infrastructure layer and application layer DDoS attacks. You can combine AWS Shield Advanced metrics with additional, fine-tuned AWS WAF metrics for a more comprehensive CloudWatch monitoring and alarming strategy. Customers subscribed to AWS Shield Advanced can also apply for a credit for charges that result from scaling during a DDoS attack on protected Amazon EC2, Amazon CloudFront, Elastic Load Balancing, or Amazon Route 53 resources. See the AWS Shield Developer Guide for a detailed comparison of the two AWS Shield offerings.
AWS WAF
AWS WAF is a web application firewall that helps protect web applications from common web exploits that could affect application availability, compromise security, or consume excessive resources. You can use AWS WAF to define customizable web security rules that control which traffic accesses your web applications. If you use AWS Shield Advanced, you can use AWS WAF at no extra cost for those protected resources and can engage the DRT to create WAF rules.
AWS WAF rules use conditions to target specific requests and trigger an action, allowing you to identify and block common DDoS request patterns and effectively mitigate a DDoS attack. These include size constraint conditions to block a web request based on the length of its query string or request body, and geographic match conditions to implement geo restriction (also known as geoblocking) on requests that originate from specific countries. For a complete list of conditions, see the AWS WAF Developer Guide. With AWS WAF, you can also create rate-based rules that automatically block requests from a single IP address if they exceed a customer-defined rate limit. One benefit of rate-based rules is that you can block requests from an IP address while it exceeds the threshold, and then automatically allow requests from that same client once they drop to an acceptable rate. This helps ensure that regular viewers are not held in a persistent block list. You can also combine the rate limit with conditions to trigger different actions for distinct scenarios.
Amazon Route 53
One of the most common targets of DDoS attacks is the Domain Name System (DNS). Amazon Route 53 is a highly available and scalable DNS service designed to route end users to infrastructure running inside or outside of AWS. Route 53 makes it possible to manage traffic globally through a variety of routing types, and provides out-of-the-box shuffle sharding and Anycast routing capabilities to protect domain names from DNS-based DDoS attacks.
Amazon CloudFront
Amazon CloudFront distributes traffic across multiple edge locations and filters requests to ensure that only valid HTTP(S) requests will be forwarded to backend hosts. CloudFront also supports geoblocking, which you can use to prevent requests from particular geographic locations from being served.
Elastic Load Balancing
Elastic Load Balancing automatically distributes incoming application traffic across multiple targets, such as Amazon Elastic Compute Cloud (Amazon EC2) instances, containers, and IP addresses, and multiple Availability Zones, which minimizes the risk of overloading a single resource. Elastic Load Balancing, like CloudFront, only supports valid TCP requests, so DDoS attacks such as UDP and SYN floods are not able to reach EC2 instances. It also offers a single point of management and can serve as a line of defense between the internet and your backend, private EC2 instances. Elastic Load Balancing includes the Application Load Balancer, which is best suited for load balancing of HTTP and HTTPS traffic and also directly supports AWS WAF.
VPCs and Security Groups
Amazon Virtual Private Cloud (Amazon VPC) allows customers to configure subnet routes, public IP addresses, security groups, and network access control lists in order to minimize application attack surfaces. You can configure load balancers and EC2 instance security groups to allow traffic that originates from specific IP addresses only, such as that from CloudFront or AWS WAF, protecting backend application components from a direct attack.
For more information on DDos attack prevention, please refer to the below URL:
https://aws.amazon.com/answers/networking/aws-ddos-attack-mitigation/

22 / 65
Your design team is planning to design an application that will be hosted on the AWS Cloud. One of their main non-functional requirements is given below
Reduce inter-dependencies so failures do not impact other components
Which of the following concepts does this requirement relate to?

 B. Decoupling 
 A. Integration
 C. Aggregation
 D. Segregation
Answer – B
The entire concept of decoupling components is to ensure that the different components of an applications can be managed and maintained separately. If all components are tightly coupled then when one component goes down , the entire application would do down. Hence it is always a better design practice to decouple application components.
For more information on a decoupled architecture, please refer to the below URL:
http://whatis.techtarget.com/definition/decoupled-architecture

23 / 65
An administrator is looking to run their cloud infrastructure along best practice guidelines by leveraging on Amazon Inspector and AWS Trusted Advisor services.
Which of the following statements correctly describe how this can be done? (Select TWO)

 A. Running Amazon Inspector service to probe and protect cloud infrastructure from threats regularly
 E. Amazon Inspector will highlight pending tasks to be resolved in only performance and cost optimization best practices whilst AWS Trusted Advisor will alert the administrator of security vulnerabilities. 
 D. AWS Trusted Advisor will highlight pending tasks to be resolved in only performance and cost optimization best practices whilst Amazon Inspector will alert the administrator of security vulnerabilities.
 C. Regularly running Amazon Inspector service on EC2 instances to get a concise list of security vulnerabilities and exposures to attack. 
 B. Adhering to recommendations given in the main pillars of AWS Trusted Advisor, which are cost optimization, security, performance, fault-tolerance and service limits 
Correct Answer – B, C
Amazon Inspector will assess AWS provisioned infrastructure for compliance and security vulnerabilities. AWS Trusted Advisor will provide real-time guidelines in best practice implementation and maintenance of AWS resources.
https://aws.amazon.com/premiumsupport/technology/trusted-advisor/
https://docs.aws.amazon.com/inspector/latest/userguide/inspector_introduction.html
Option A. is INCORRECT because Amazon Inspector service does not protect against any security threats to a user’s resources on the cloud.
Option D. is INCORRECT because AWS Trusted Advisor will highlight recommendations of best practice in five aspects namely cost optimization, security, performance, fault-tolerance and service limits.
Option E. is INCORRECT because Amazon Inspector will alert the administrator of security vulnerabilities and not AWS Trusted Advisor.

24 / 65
Your company is planning to use the AWS Cloud. But there is a management decision that resources need to split department wise. And the decision is tending towards managing multiple AWS accounts. Which of the following would help in effective management and also provide an efficient costing model.

 A. AWS Organizations 
 D. AWS Cost Explorer
 C. AWS Trusted Advisor
 B. Amazon Dev Pay
Answer – A
The AWS Documentation mentions the following
AWS Organizations offers policy-based management for multiple AWS accounts. With Organizations, you can create groups of accounts and then apply policies to those groups. Organizations enables you to centrally manage policies across multiple accounts, without requiring custom scripts and manual processes.
For more information on the AWS Organizations, please refer to the below URL:
https://aws.amazon.com/organizations/

25 / 65
You are requested to expose your serverless application implemented with AWS Lambda to HTTP clients.( using HTTP Proxy )
Which of the following AWS services can you use to accomplish the task? (Select TWO)

 A. AWS Elastic Load Balancing (ELB) 
 C. AWS API Gateway 
 B. AWS Route53 
 E. AWS Elastic Beanstalk
 D. AWS Lightsail
Answer: A and C
Option A is CORRECT because AWS documentation mentions it “Application Load Balancers now support invoking Lambda functions to serve HTTP(S) requests. This enables users to access serverless applications from any HTTP client, including web browsers.
Option B is INCORRECT because Route53 is a Domain Name System and not an HTTP proxy.
Option C is CORRECT because API Gateway + Lambda is a common pattern for exposing serverless functions via HTTP/HTTPS. AWS documentation mentions it “Creating, deploying, and managing a REST application programming interface (API) to expose backend HTTP endpoints, AWS Lambda functions, or other AWS services”
Option D is INCORRECT because AWS Lightsail has a completely different goal. It is a service to speed up provisioning of AWS resources.
Option E is INCORRECT because AWS Elastic Beanstalk has a completely different goal. It is a service that makes easier for developers to quickly deploy and manage applications in the AWS Cloud. Developers simply upload their application, and Elastic Beanstalk automatically handles the deployment details of capacity provisioning, load balancing, auto-scaling, and application health monitoring.
Diagram: none
References:
ELB:
https://aws.amazon.com/elasticloadbalancing/faqs/?nc=sn&loc=6
API Gateway:
https://aws.amazon.com/api-gateway/faqs/

26 / 65
Which of the following services allows you to analyze EC2 Instances against pre-defined security templates to check for vulnerabilities

 C. AWS WAF
 B. AWS Inspector 
 A. AWS Trusted Advisor
 D. AWS Shield
Answer – B
The AWS Documentation mentions the following
Amazon Inspector enables you to analyze the behavior of your AWS resources and helps you to identify potential security issues. Using Amazon Inspector, you can define a collection of AWS resources that you want to include in an assessment target. You can then create an assessment template and launch a security assessment run of this target.
For more information on AWS Inspector, please refer to the below URL:
https://docs.aws.amazon.com/inspector/latest/userguide/inspector_introduction.html

27 / 65
Which of the following options is true regarding the vulnerability and security assessment on AWS resources ?

 C. Vulnerability and security assessments can be conducted on specified AWS resources. 
 D. It is not permissible to run vulnerability and penetration tests on AWS resources without the prior consent and approval of AWS.
 A. AWS is responsible for security of the cloud, vulnerability and penetration testing is not permissible and unnecessary on AWS resources and infrastructure.
 B. An organisation can contract a third-party organisation to run vulnerability and security assessments on any of their AWS resources.
Correct Answer – C
AWS permits users to conduct vulnerability and penetration testing certain specified AWS services. This allows organisations to comply with any industry regulations that stipulate that vulnerability and penetration testing be conducted on services and infrastructure.
https://aws.amazon.com/security/penetration-testing/
Option A. is incorrect because vulnerability and penetration testing and security assessments are permissible, even as AWS maintains robust security measures on infrastructure.
Option B. is incorrect because vulnerability and penetration testing, security assessments can only be run on a specified list of AWS resources. There are AWS resources which these tests are not allowed.
Option D. is incorrect because vulnerability and penetration tests can be conducted on specific AWS service resources without the consent of AWS.
https://aws.amazon.com/security/penetration-testing/

28 / 65
An organization runs several EC2 instances inside a VPC using three subnets, one for Development, one for Test and one for Production. The Security team has some concerns about the VPC configuration and requires to restrict the communication across the EC2 instances using Security Groups.
Which of the following options is true for Security Groups?

 B. You can change a Security Group associated to an instance if the instance state is stopped but not if the instance state is running.
 C. You can change a Security Group only if there are no instances associated to it.
 A. You can change a Security Group associated to an instance if the instance state is stopped or running. 
 E. None of the above 
 D. The only Security Group you can change is the Default Security Group.
Answer: A
Option A is CORRECT because the AWS documentation mentions it in the section called “Changing an Instance’s Security Group” using the following sentence: “After you launch an instance into a VPC, you can change the security groups that are associated with the instance. You can change the security groups for an instance when the instance is in the running or stopped state.”
Option B, C, D and E are INCORRECT as a consequence of A.
Diagram: none
References:
https://docs.aws.amazon.com/en_pv/vpc/latest/userguide/VPC_SecurityGroups.html

29 / 65
Your company is moving a large application to AWS using a set of EC2 instances. A key requirement is reusing existing server-bound software licensing. Which of the following options is the best for satisfying the requirement?

 C. EC2 Dedicated Hosts 
 B. EC2 Reserved Instances
 D. EC2 Spot Instances
 A. EC2 Dedicated Instances 
Answer: C
Option A is INCORRECT because despite instances run on a single-tenant hardware AWS does not give visibility to sockets and cores required for reusing server bound licenses. AWS highlights this in the comparison table at the following link:
https://aws.amazon.com/ec2/dedicated-hosts/
Option B is INCORRECT because Reserved Instances are only a purchasing option and there’s no way to control the hardware where these instances are running on.
Option C is CORRECT because instances run on a dedicated hardware where AWS gives visibility of physical characteristics. AWS documentation mentions this with the following sentence: “…Dedicated Host gives you additional visibility and control over how instances are placed on a physical server, and you can consistently deploy your instances to the same physical server over time. As a result, Dedicated Hosts enable you to use your existing server-bound software licenses and address corporate compliance and regulatory requirements.”
Option D is INCORRECT because Spot Instances are only a purchasing option.
Diagram: none
References:
AWS documentation that explains the possibility of reusing server bound license
https://aws.amazon.com/ec2/dedicated-hosts/

30 / 65
Which of the below mentioned services is equivalent to hosting virtual servers on an on-premises location?

 D. AWS Regions
 B. AWS Server
 A. AWS IAM
 C. AWS EC2 
Answer – C
The AWS Documentation mentions the following
Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers.
For more information on AWS EC2, please refer to the following Link:
https://aws.amazon.com/ec2/

31 / 65
Which of the following statements are FALSE when it comes to elasticity. Choose 2 answers from the options given below

 C. Diverting traffic across multiple regions 
 B. Diverting traffic to instances with the least load
 D. Diverting traffic to instances with higher capacity 
 A. Diverting traffic to instances based on the demand 
Answer – C and D
The concept of Elasticity is the means of an application having the ability to scale up and scale down based on demand. An example of such a service is the Autoscaling service
For more information on AWS Autoscaling service, please refer to the below URL:
https://aws.amazon.com/autoscaling/

32 / 65
Which of the following Amazon Web Services can be referred to as a serverless service? (Select three).

 D. Amazon DynamoDB 
 B. Elastic Load Balancing
 C. Amazon SNS 
 A. AWS Lambda 
The correct answers are A,C and D.
The serverless concept refers to the ability to leverage compute processing functions without the infrastructure overhead. AWS Lambda is a serverless online code scripting platform within AWS that allows the user to write, edit and run code functions in various languages including JSON. These functions can be triggered to call or invoke other AWS applications in the user’s build. AWS Cloud9 is a serverless online integrated development environment (IDE) used to author, edit, run debug code of various languages.
https://aws.amazon.com/serverless/
Option B is incorrect because Elastic Load Balancing can be described as a fully-managed service but not serverless.
Option D is correct. With DynamoDB, there are no servers to provision, patch, or manage and no software to install, maintain, or operate.

33 / 65
An ELB instance is configured with the default HealthCheck and Response Timeout intervals as 30 seconds and 5 seconds respectively. How long will it take for an instance within a target group to be labelled as OutOfService, if it goes down a second after the latest HealthCheck?

 C. 35 seconds
 D. 4 seconds
 B. 30 seconds
 A. 34 seconds 
Correct Answer – A
Since the health check runs every 30 seconds and the instance goes down one second into the cycle, it means 29 seconds will lapse before a new health check is run. Additionally, it will take 5 more seconds of the ELB instance probing the instance that is down, upon getting no response, it would then fail the health check. Therefore, 29 + 5 seconds = 34 seconds.
https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/elb-healthchecks.html
Option B. is INCORRECT because when a health check starts, the ELB gives the instance 5 seconds to respond during the probe.
Option C. is INCORRECT because the instance within the target group goes down 1 second after the latest health check cycle.
Option D. is INCORRECT because the health check runs after every 30 seconds window. So during this window, the ELB will not be probing the target group.

34 / 65
You have a set of EC2 Instances hosted on the AWS Cloud. The EC2 Instances are hosting a web application. Which of the following acts as a firewall to your VPC and the instances in it? Choose 2 answers from the options given below

 D. Usage of the Internet gateway
 B. Usage of AWS Config
 C. Usage of Network Access Control Lists 
 A. Usage of Security Groups 
Answer – A and C
The AWS Documentation mentions the following
A security group acts as a virtual firewall for your instance to control inbound and outbound traffic
A network access control list (ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets.
For more information on Security Groups, please refer to the following Link:
https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_SecurityGroups.html
For more information on Network Access Control Lists, please refer to the following Link:
https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_ACLs.html

35 / 65
A research team conducting its work in remote locations of the world, without internet access, wishes to leverage Amazon services for their storage. The team collects petabytes of information at a time. Which service will best meet to transfer the petabytes of information?

 C. Amazon S3 Glacier 
 A. Amazon S3
 D. AWS Snowball 
 B. Amazon Elastic Block Store (EBS)
Correct Answer – D
The AWS Snowball service uses physical storage devices to transfer large amounts of data between Amazon Simple Storage Service (Amazon S3) and your onsite data storage location at faster-than-internet speeds. By working with AWS Snowball, you can save time and money. Snowball provides powerful interfaces that you can use to create jobs, track data, and track the status of your jobs through to completion.
Snowball devices are physically rugged devices that are protected by the AWS Key Management Service (AWS KMS). They secure and protect your data in transit.
https://docs.aws.amazon.com/snowball/latest/ug/whatissnowball.html
Option A. is incorrect because Amazon S3 is object storage most suitable when there is internet connectivity, in this scenario there is none.
Option B. is incorrect because Amazon EBS provide block level storage volumes suitable for operating systems, database instances and applications. In order for the research team to store data to detached EBS volumes (not attached to EC2 instances), they would need internet connectivity. In the scenario, remote location does not have connectivity.
Option C. is incorrect because is object storage optimized for infrequent access nor usage, it would require the researchers in the scenario to be online in order to upload the data. The solution ought to be accessible offline.

36 / 65
Which of the following terms refers to a geographic location in AWS?

 D. Edge location
 C. Region 
 A. Availability Zone 
 B. Data center
Answer – C
Regions correspond to different geographic locations in AWS.
For more information on Regions and Availability Zones in AWS, please refer to the below URL:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html

37 / 65
Whilst running an application on an EC2 instance behind an Elastic Load Balancer, an administrator receives a 504 error on their browser. What does this mean?

 B. The application running on the EC2 instance is serving the 504 error page because it has exceeded its response timeout 
 C. The URL for the application has expired
 A. The ELB instance has stopped running
 D. The application is unresponsive so the ELB instance serves the 504 error page 
Correct Answer – D
The 504 error is served by the Elastic Load Balancer to indicated that the application is unresponsive, the idle time-out period has lapsed.
https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/ts-elb-error-message.html#ts-elb-errorcodes-http504
Option A. is INCORRECT because the error that is served when the ELB instance has stopped running is 503.
Option B. is INCORRECT because when the application behind the ELB is unresponsive, the error page is served by the ELB instance itself and not the application.
Option C. is INCORRECT because in the scenario there is no mention of signed URLs. The error that is served in such a scenario is “Request has expired” error.

38 / 65
A live online game uses DynamoDB instances in the backend to store real-time scores of the participants as they compete against each other from various parts of the world. Which data consistency option it the most appropriate to implement?

 A. Strongly consistent 
 D. Optimistic consistency
 C. Strong Eventual consistency
 B. Eventually consistent
Correct Answer – A
Since the gamers are participating live over the internet from geographically distinct locations, the data consistency will need to be that of immediately readable within a second of them being written. Therefore strongly consistent.
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.ReadConsistency.html
Option B. is INCORRECT because the scenarios outlines that the participants of the game are live, it will not suffice if any of them get updates on scores in less than real-time.
Option C. is INCORRECT because strong eventual consistency is not applicable in DynamoDB.
Option D. is INCORRECT because only two data consistency models are available with the DynamoDB service, optimistic consistency is not supported

39 / 65
You have a devops team in your current organization structure. They are keen to know if there is any service available in AWS which can be used to manage infrastructure as code. Which of the following can be met with such a requirement

 C. Using AWS Inspector
 D. Using AWS Trusted Advisor
 B. Using AWS Config
 A. Using AWS Cloudformation 
Answer – A
The AWS documentation mentions the following
AWS CloudFormation is a service that helps you model and set up your Amazon Web Services resources so that you can spend less time managing those resources and more time focusing on your applications that run in AWS. You create a template that describes all the AWS resources that you want (like Amazon EC2 instances or Amazon RDS DB instances), and AWS CloudFormation takes care of provisioning and configuring those resources for you. You don’t need to individually create and configure AWS resources and figure out what’s dependent on what; AWS CloudFormation handles all of that
For more information on AWS Cloudformation, please refer to the below URL:
https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html

40 / 65
Which of the following storage options provides the option of Lifecycle policies that can be used to move objects to archive storage.

 C. Amazon Storage Gateway
 A. Amazon S3 
 B. Amazon Glacier
 D. Amazon EBS 
Answer – A
The AWS Documentation mentions the following
Lifecycle configuration enables you to specify the lifecycle management of objects in a bucket. The configuration is a set of one or more rules, where each rule defines an action for Amazon S3 to apply to a group of objects. These actions can be classified as follows:
· Transition actions – In which you define when objects transition to another storage class. For example, you may choose to transition objects to the STANDARD_IA (IA, for infrequent access) storage class 30 days after creation, or archive objects to the GLACIER storage class one year after creation.
· Expiration actions – In which you specify when the objects expire. Then Amazon S3 deletes the expired objects on your behalf.
For more information on AWS Object Lifecycle management, please visit the Link:
https://aws.amazon.com/s3/

41 / 65
Your company is planning on moving to the AWS Cloud. Once the movement to the Cloud is complete, they want to ensure that the right security settings are put in place. Which of the below tools can assist from a Security compliance. Choose 2 answers from the options given below.

 C. AWS Support
 D. AWS Kinesis
 A. AWS Inspector 
 B. AWS Trusted Advisor 
Answer – A and B
The AWS documentation mentions the following
An online resource to help you reduce cost, increase performance, and improve security by optimizing your AWS environment, Trusted Advisor provides real time guidance to help you provision your resources following AWS best practices
The AWS Inspector can inspect EC2 Instances against common threats.
For more information on the AWS Trusted Advisor, please refer to the below URL:
https://aws.amazon.com/premiumsupport/trustedadvisor/
https://docs.aws.amazon.com/inspector/latest/userguide/inspector_introduction.html

42 / 65
Which of the following are features of an edge location. Choose 3 answers from the options given below

 B. Cache common responses 
 A. Distribute content to users 
 C. Distribute load across multiple resources 
 D. Used in conjunction with the Cloudfront service 
Answer – A,B and D
The AWS Documentation mentions the following
Amazon CloudFront employs a global network of edge locations and regional edge caches that cache copies of your content close to your viewers. Amazon CloudFront ensures that end-user requests are served by the closest edge location. As a result, viewer requests travel a short distance, improving performance for your viewers. For files not cached at the edge locations and the regional edge caches, Amazon CloudFront keeps persistent connections with your origin servers so that those files can be fetched from the origin servers as quickly as possible.
For more information on Cloudfront and Edge locations, please refer to the following Link:
https://aws.amazon.com/cloudfront/details/

43 / 65
Select TWO statements that describe the main roles of AWS Web Application Firewall (WAF) and AWS Shield?

 D. AWS Web Application Firewall (WAF) and AWS Shield are fully-managed services 
 A. AWS Shield Standard is inherently available within the AWS WAF service at no extra cost 
 E. AWS WAF is a web application firewall that includes AWS Shield – a service that prevents distributed denial of service (DDoS) attacks 
 B. AWS WAF is inherently available within the AWS Shield Standard service at an additional charge
 C. AWS Web Application Firewall (WAF) will provide expanded protection against SYN floods, DNS query floods and UDP reflection attacks at no additional cost 
Correct Answer – A, E
AWS Web Application Firewall (WAF) is a web-based application that allows for monitoring of ingress and egress traffic on provisioned web services. These could be in an AWS CloudFront distribution, behind an AWS Load Balancer or standalone instance. AWS WAF includes AWS Shield (AWS Shield Standard that comes at no additional cost and AWS Shield Advanced, on subscription) that protects against SYN floods, DNS query floods and UDP reflection attacks amongst others.
https://docs.aws.amazon.com/waf/latest/developerguide/ddos-overview.html
Option B. is INCORRECT because AWS Shield Standard service currently comes with no additional charge and the service is inherently available within AWS WAF and not vice versa.
Option C. is INCORRECT because AWS WAF includes AWS Shield Standard that comes at no additional cost and AWS Shield Advanced, available on subscription
Option D. is INCORRECT because AWS Web Application Firewall (WAF) and AWS Shield are not fully-managed services

44 / 65
Currently your organization has an operational team that takes care of ID management in their on-premise data center. They now also need to manage users and groups created in AWS. Which of the following AWS tools would they need to use for performing this management function.

 D. AWS Identity and Access Management (IAM) 
 B. AWS Cloud Trail
 A. AWS Config
 C. AWS Key Management Service (AWS KMS)
Answer – D
The AWS documentation mentions the following
AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources.
For more information on AWS IAM, please refer to the below URL:
http://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html
Option A – AWS Config
This service is used to assess, audit, and evaluate the configurations of your AWS resources. It continuously monitors and records your AWS resource configurations and allows you to automate the evaluation of recorded configurations against desired configurations.
With this description, it’s clearly understood that this service is not for managing users and groups as mentioned, but rather used for working on configuration of your AWS services. Hence this option is not the correct option for the question asked.
https://docs.aws.amazon.com/config/latest/developerguide/WhatIsConfig.html
Option B – AWS CloudTrail
This service is used for enabling governance, compliance, operational auditing, and risk auditing of your AWS account. Since this service is basically meant for “auditing”, and not for managing of users in the cloud, and hence not the correct option for our requirement.
https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html
Option C – AWS Key Management Service (AWS KMS)
This service is used for creating and managing of keys and control the use of encryption across a wide range of AWS services and in your applications. The basic usage of this to protect the data at various stages like in-transit, rest, etc., and not for handling users and groups in AWS. Hence this option is not the correct answer for the question asked.
https://docs.aws.amazon.com/kms/latest/developerguide/overview.html

45 / 65
A company currently has an application which consist of a .Net layer which connects to a MySQL database. They now want to move this application onto AWS. They want to make use of all AWS features such as high availability and automated backups. Which of the following would be an ideal database in AWS to migrate to for this requirement.

 B. DynamoDB
 D. An EC2 instance with Aurora installed.
 A. Aurora 
 C. An EC2 instance with MySQL installed.
Answer – A
The AWS Documentation mentions the following
Amazon Aurora (Aurora) is a fully managed, MySQL- and PostgreSQL-compatible, relational database engine. It combines the speed and reliability of high-end commercial databases with the simplicity and cost-effectiveness of open-source databases. It delivers up to five times the throughput of MySQL and up to three times the throughput of PostgreSQL without requiring changes to most of your existing applications.
For more information on Amazon Aurora, please refer to the below URL:
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Aurora.Overview.html

46 / 65
Which of the following can be attached to EC2 Instances to store data?

 A. Amazon Glacier
 D. Amazon SQS
 C. Amazon EBS Snapshots
 B. Amazon EBS Volumes 
Answer – B
The AWS Documentation mentions the following on EBS Volumes
An Amazon EBS volume is a durable, block-level storage device that you can attach to a single EC2 instance. You can use EBS volumes as primary storage for data that requires frequent updates, such as the system drive for an instance or storage for a database application
For more information on EBS Volumes, please refer to the below URL:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumes.html

47 / 65
When designing a system, you use the principle of “design for failure and nothing will fail”. Which of the following services/features of AWS can assist in supporting this design principle. Choose 3 answers from the options given below

 D. Pay as you go
 C. Elastic Load Balancer 
 A. Availability Zones 
 B. Regions 
Answer – A,B and C
Each AZ is a set of one or more data centers. By deploying your AWS resources to multiple Availability zones , you are designing with failure with mind. So if one AZ were to go down , the other AZ’s would still be up and running and hence your application would be more fault tolerant.
For disaster recovery scenarios , one can move or make resources run in other regions
And finally one can use the Elastic Load Balancer to distribute load to multiple backend instances within a particular region.
For more information on AWS Regions and AZ’s, please refer to the below URL:
http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html

48 / 65
Using Content Delivery Network (CDN) an administrator would like to serve varying types of content based on the viewer’s browser cookies. Which is the most appropriate serverless technique that can be used to achieve this?

 C. AWS CodeStar 
 A. AWS CodeCommit
 B. AWS Lambda@Edge 
 D. AWS Cloud9
Correct Answer – B
AWS Lambda@Edge is a serverless service that makes it possible to run event-triggered functions on Edge Locations within the AWS Content Delivery Network. Using AWS CloudFront, an administrator can introduce decision-making and compute processing closer to the viewer’s location, thereby improving on their browsing experience.
https://aws.amazon.com/lambda/edge/
Option A. is INCORRECT because AWS CodeCommit is inappropriate in addressing the scenario, it is a service that allows for the management of software development versions as well as software development assets such. These include binary files, documents and source code.
Option C. is INCORRECT because AWS CodeStar is a service used to manage software development projects. It is not the appropriate Option for the scenario. CodeStar project makes it possible to develop, build and deploy applications
Option D. is INCORRECT because it is not the best solution though it can be used in the scenario to write, run and deploy code. It is an integrated development environment (IDE) that can accommodate various runtimes. Since the Lambda@Edge is best suited to meet the requirements of the scenario, this makes this Option incorrect.

49 / 65
You have an EC2 Instance in development that interacts with the Simple Storage Service. The EC2 Instance is going to be promoted to the production environment. Which of the following features should be used for secure communication between the EC2 Instance and the Simple Storage Service.

 D. IAM policies 
 B. IAM Roles 
 C. IAM Groups
 A. IAM Users
Answer – B
The AWS Documentation mentions the following
An IAM role is similar to a user, in that it is an AWS identity with permission policies that determine what the identity can and cannot do in AWS. However, instead of being uniquely associated with one person, a role is intended to be assumable by anyone who needs it. Also, a role does not have standard long-term credentials (password or access keys) associated with it. Instead, if a user assumes a role, temporary security credentials are created dynamically and provided to the user.
For more information on IAM Roles, please refer to the below URL:
https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html

50 / 65
Your company handles a crucial ecommerce application. This applications needs to have an uptime of at least 99.5%. There is a decision to move the application to the AWS Cloud. Which of the following deployment strategies can help build a robust architecture for such an application.

 C. Deploying the application across Edge locations
 D. Deploying the application across multiple subnets
 A. Deploying the application across multiple VPC’s
 B. Deploying the application across multiple Regions 
Answer – B
The AWS Documentation mentions the following
Businesses are using the AWS cloud to enable faster disaster recovery of their critical IT systems without incurring the infrastructure expense of a second physical site. The AWS cloud supports many popular disaster recovery (DR) architectures from “pilot light” environments that may be suitable for small customer workload data center failures to “hot standby” environments that enable rapid failover at scale. With data centers in Regions all around the world, AWS provides a set of cloud-based disaster recovery services that enable rapid recovery of your IT infrastructure and data.
For more information on enabling AWS Disaster Recovery, please refer to the below URL:
https://aws.amazon.com/disaster-recovery/

51 / 65
Your company wants to move an existing Oracle database to the AWS Cloud. Which of the following services can help facilitate this move.

 B. AWS VM Migration Service
 A. AWS Database Migration Service 
 D. AWS Trusted Advisor
 C. AWS Inspector
Answer – A
The AWS Documentation mentions the following
AWS Database Migration Service helps you migrate databases to AWS quickly and securely. The source database remains fully operational during the migration, minimizing downtime to applications that rely on the database. The AWS Database Migration Service can migrate your data to and from most widely used commercial and open-source databases.
For more information on AWS Database migration, please refer to the below URL:
https://aws.amazon.com/dms/

52 / 65
Which statement is accurate about AWS Budgets and Cost Explorer?

 B. Both AWS Budgets and AWS Cost Explorer can be used to predict usage and to give recommended cost-optimization measures.
 C. AWS Cost Explorer will lists the costs incurred over a period of time with a further breakdown by region and linked account.
 A. AWS Budgets uses the cost visualizations provided by AWS Cost Explorer to show the status of preset budgets and to provide forecasts of estimated costs. 
 D. Due to the sensitivity of billing and cost management information, with the AWS Cost Explorer and AWS Budgets services, it is not possible to view the information for multiple accounts. 
Correct Answer – A
Under the Billing and Cost Management service in the AWS management service, it is possible to use the AWS Budgets and Cost Explorer to show the status of preset budgets and to provide forecasts of estimated costs.
https://aws.amazon.com/aws-cost-management/aws-cost-explorer/
Option B. is incorrect because AWS Budgets does not provide cost-optimization recommendations.
Option C. is incorrect because this is the function of the AWS Bills module under Billing and Cost Management.
Option D. is incorrect because it is possible to view billing information for multiple AWS accounts as long as the administrator has lawful jurisdiction over them.

53 / 65
Your company is planning to pay for an AWS Support plan. They have the following requirements as far as the support plan goes
24×7 access to Cloud Support Engineers via email, chat & phone
Response time of less than 1 hour for any business critical system faults
Which of the following plans will suffice to keep in mind the above requirement?

 B. Developer
 C. Business
 A. Basic
 D. Enterprise 
Answer – D
As per the AWS document, there is no critical support available for Basic, Developer and Business plans.
If you see the second point, it says “critical faults”. Critical faults can be handled only by the “Sr. Cloud Support Engineers”. Even if it is less than 1 hour or 15 mins.
Enterprise plan has critical support within 15 minutes. The question mentions less than 1 hour for critical faults. Normally it will be less than 15 minutes. Hence the correct answer is Enterprise.
The Enterprise support plan has support time less than 15 minutes for Business-critical system down.
For more information on the support plans, please refer to the following Link:
https://aws.amazon.com/premiumsupport/compare-plans/



54 / 65
There is a requirement to collect important metrics from AWS RDS and EC2 Instances. Which AWS service would be helpful to fulfill this requirement?

 D. Amazon Config
 C. Amazon CloudWatch 
 A. Amazon CloudFront
 B. Amazon CloudSearch
Correct Answer – C
The AWS documentation mentions the following:
Amazon CloudWatch is a monitoring service for AWS cloud resources and the applications you run on AWS. You can use Amazon CloudWatch to collect and track metrics, collect and monitor log files, set alarms, and automatically react to changes in your AWS resources
For more information on AWS Cloudwatch, please refer to the URL below:
https://aws.amazon.com/cloudwatch/

55 / 65
Which of the following does AWS perform on its behalf for EBS volumes to make it less prone to failure?

 B. Replication of the volume in the same Availability Zone 
 D. Replication of the volume across Edge locations
 C. Replication of the volume across Regions 
 A. Replication of the volume across Availability Zones
Answer – B
When you create an EBS volume in an Availability Zone, it is automatically replicated within that zone to prevent data loss due to failure of any single hardware component
For more information on EBS Volumes, please refer to the below URL:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumes.html

56 / 65
If there is a requirement to host EC2 Instances in the AWS Cloud wherein the utilization is guaranteed to be consistent for a long period of time, which of the following would you utilize to ensure costs are minimized?

 D. Regular instances
 C. Spot instances
 B. On-demand instances
 A. Reserved instances 
Answer – A
When you have instances that will be used continuously and throughout the year, the best option is to buy reserved instances. By buying reserved instances, you are actually allocated an instance for the entire year or the duration you specify with a reduced cost.
For more information on Reserved Instances, please visit the Link:
https://aws.amazon.com/ec2/pricing/reserved-instances/

57 / 65
Your company is planning to host resources in the AWS Cloud. They want to use services which can be used to decouple resources hosted on the cloud. Which of the following services can help fulfil this requirement

 B. AWS EBS Snapshots
 A. AWS EBS Volumes
 C. AWS Glacier
 D. AWS SQS 
Answer – D
The AWS Documentation mentions the following on the Simple Queue Service
Amazon Simple Queue Service (Amazon SQS) offers a reliable, highly-scalable hosted queue for storing messages as they travel between applications or microservices. It moves data between distributed application components and helps you decouple these components
For more information on AWS SQS, please refer to the below URL:
https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/Welcome.html
Note:
Decoupling is where the different components/layers that make up the system interact with each other using well-defined interfaces rather than depending tightly on eah other. With this architecture, the components/layers can be developed independently without having to wait for their dependencies to complete. This leads to pipelined development, resulting in more streamlined and faster development. This also improves testability of the components.
Please find the links that explains more about decoupling with SQS and examples.
https://aws.amazon.com/blogs/compute/building-loosely-coupled-scalable-c-applications-with-amazon-sqs-and-amazon-sns/
https://www.youtube.com/watch?v=UesxWuZMZqI
https://aws.amazon.com/getting-started/tutorials/send-fanout-event-notifications/

58 / 65
Which AWS Cloud service helps in quick deployment of resources which can make use of different programming languages such as .Net and Java?

 B. AWS Elastic Compute Cloud (Amazon EC2)
 C. AWS VPC
 D. AWS SQS
 A. AWS Elastic Beanstalk 
Answer – A
The AWS Documentation mentions the following
AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS.
For more information on enabling AWS Elastic beanstalk, please refer to the below URL:
https://aws.amazon.com/elasticbeanstalk/?p=tile

59 / 65
Your company has just started using the resources on the AWS Cloud. They want to get an idea on the costs being incurred so far for the resources being used. How can this be achieved.

 D. By seeing the AWS Cloud Trail logs.
 C. By using the AWS Trusted Advisor dashboard. This dashboard will give you all the costs.
 A. By going to the Amazon EC2 dashboard. Here you can see the costs of the running EC2 resources.
 B. By using the AWS Cost Explorer. Here you can see the running and forecast costs. 
The correct answer is Option B.
The AWS documentation mentions the following on AWS Cost Reports
Cost Explorer is a free tool that you can use to view your costs. You can view data up to the last 13 months, forecast how much you are likely to spend for the next three months, and get recommendations for what Reserved Instances to purchase
For more information on AWS Cost Reports, please refer to the below URL:
http://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-explorer-what-is.html

60 / 65
Which of the following can be used as an additional layer of security to using a user name and password when logging into the AWS Console.

 A. Multi-Factor Authentication (MFA) 
 D. Secondary user name
 C. Root access privileges
 B. Secondary password
Answer – A
The AWS Documentation mentions the following
AWS Multi-Factor Authentication (MFA) is a simple best practice that adds an extra layer of protection on top of your user name and password.
For more information on the AWS MFA, please refer to the below URL:
https://aws.amazon.com/iam/details/mfa/

61 / 65
Your company is planning to offload some of the batch processing workloads on to AWS. These jobs can be interrupted and resumed at any time. Which of the following instance types would be the most cost effective to use for this purpose.

 C. Full Upfront Reserved
 D. Partial Upfront Reserved
 B. Spot 
 A. On-Demand
Answer – B
The AWS documentation mentions the following
Spot Instances are a cost-effective choice if you can be flexible about when your applications run and if your applications can be interrupted. For example, Spot Instances are well-suited for data analysis, batch jobs, background processing, and optional tasks
For more information on AWS Spot Instances, please refer to the below URL:
http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html

62 / 65
Which of the following security requirements are managed by AWS? Select 3 answers from the options given below.

 E. Hardware patching 
 B. User permissions
 C. Physical security 
 D. Disk disposal 
 A. Password Policies
Answer – C, D and E
As per the Shared Responsibility model , the Patching of the underlying hardware and physical security of AWS resources is the responsibility of AWS.
For more information on AWS Shared Responsibility Model, please refer to the below URL:
https://aws.amazon.com/compliance/shared-responsibility-model/
Disk disposal:
Storage Device Decommissioning When a storage device has reached the end of its useful life, AWS procedures include a decommissioning process that is designed to prevent customer data from being exposed to unauthorized individuals. AWS uses the techniques detailed in DoD 5220.22-M (“National Industrial Security Program Operating Manual “) or NIST 800-88 (“Guidelines for Media Sanitization”) to destroy data as part of the decommissioning process. All decommissioned magnetic storage devices are degaussed and physically destroyed in accordance with industry-standard practices.
For more information on Disk disposal, please refer to the below URL:
https://d0.awsstatic.com/whitepapers/aws-security-whitepaper.pdf

63 / 65
After making changes to a record set in a Route53 hosted zone and saving accordingly, an administrator immediately attempts to test for the new settings. All the attempts are unsuccessful. What is the most plausible reason for this?

 A. In Amazon Route53, changes in the hosted zones cannot reflect until the set Time to live (TTL) duration has lapsed. 
 D. Whilst logged onto the hosted zone, the administrator did not commit the changes to the respective Amazon Route53 nameservers.
 B. It is likely that the administrator cleared the browser and DNS cache before testing.
 C. Changes to hosted zones propagate and reflect instantly but the administrator’s browser has cached content.
Correct Answer – A
In Amazon Route53 any alterations made to record sets in hosted zones will take the duration of the set Time to live (TTL) before they can reflect. However, flushing of the local DNS and browser cache will prompt a new query to the Route53 hosted zone thereby giving the new changes.
https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/resource-record-sets-values-basic.html#rrsets-values-basic-ttl
Option B. is INCORRECT because clearing the browser and DNS cache is actually the solution when attempting to view recently made changes to a hosted zone. So this cannot be the reason why the administrator got unsuccessful results.
Option C. is INCORRECT because changes to hosted zones in Amazon Route53 do not reflect instantly, only after the Time to live (TTL) duration has lapsed will the changes be realized.
Option D. is INCORRECT because the question states that the administrator saved the changes accordingly.

64 / 65
An administrator would like to check if the Amazon CloudFront identity they created is making access API calls to an S3 bucket where a static website is hosted. Where can this information be obtained?

 C. In the webserver, tail for identity access logs from the Amazon CloudFront identity
 B. Check AWS CloudWatch logs on the S3 bucket. 
 A. Configuring Amazon Athena to run queries on the Amazon CloudFront distribution
 D. In AWS CloudTrail Event history, look up access calls and filter for the Amazon CloudFront identity. 
Correct Answer – D
By viewing Event history in Amazon CloudTrail, the administrator can be able to access operational, access and activity logs for the past 90 days, to the S3 bucket that hosts the static website.
https://docs.aws.amazon.com/awscloudtrail/latest/userguide/view-cloudtrail-events-console.html
Option A. is INCORRECT because Amazon Athena will need a specific data repository from which a database and table can be created in order to run queries from. Data repositories can be a folder in an S3 bucket where logs are written to.
Option B. is INCORRECT because AWS CloudWatch does not log access API calls from one resource to another. AWS CloudTrail can do this.
Option C. is INCORRECT because it is not possible to access the underlying webserver, be it for Amazon CloudFront or S3, when an S3 bucket is configured for static web hosting. It is fully-managed by AWS.

65 / 65
Which of the following networking component can be used to host EC2 resources in the AWS Cloud?

 C. AWS Elastic Load Balancer
 B. AWS VPC 
 A. AWS Trusted Advisor
 D. AWS Autoscaling
Answer – B
The AWS Documentation mentions the following on Amazon VPC
Amazon Virtual Private Cloud (Amazon VPC) enables you to launch AWS resources into a virtual network that you’ve defined. This virtual network closely resembles a traditional network that you’d operate in your own data center, with the benefits of using the scalable infrastructure of AWS.
For more information on AWS VPC, please refer to the below URL:
https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Introduction.html