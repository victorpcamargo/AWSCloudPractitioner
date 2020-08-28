# AWS Cloud Practitioner - Study Content

## AWS Support

### Plans
|Description|Basic|Developer|Enterprise|Business|
|-----------|-----------|-----------|-----------|-----------|
|Provide access to guidance, configuration and troubleshooting of AWS with interoperability  many common operating systems, platforms, and application stack components|||YES|YES|
|Access to Infrastructure Event Management for an additional fee||||YES|
|Provides access to 7 core checks from the AWS Trusted Advisor Best Practice Checks|YES|YES|||
|Provides architectural guidance contextual to your specific use-cases||||YES|
|Allows one contact to open unlimited cases||YES|||
|Allows unlimited contacts to open unlimited cases|||YES|YES|
|Concierge support team as well as a response time of around an hour in case the systems go down|||YES||
|AWS support plan provides access to a Technical Account Manager (TAM)|||YES||

- Enterprise - AWS Enterprise Support provides customers with concierge-like service where the main focus is helping the customer achieve their outcomes and find success in the cloud. With Enterprise Support, you get 24x7 technical support from high-quality engineers, tools and technology to automatically manage the health of your environment, consultative architectural guidance delivered in the context of your applications and use-cases, and a designated Technical Account Manager (TAM) to coordinate access to proactive/preventative programs and AWS subject matter experts. You get access to guidance, configuration, and troubleshooting of AWS interoperability with many common operating systems, platforms, and application stack components. Enterprise Support plan provides a response time of fewer than 15 minutes for business-critical systems and provides a response time of less than an hour for production systems related outage.

- Business - AWS recommends Business Support if you have production workloads on AWS and want 24x7 phone, email and chat access to technical support and architectural guidance in the context of your specific use-cases. You get full access to AWS Trusted Advisor Best Practice Checks. You get access to guidance, configuration, and troubleshooting of AWS interoperability with many common operating systems, platforms, and application stack components. Also, you get access to Infrastructure Event Management for an additional fee.

- Basic - The basic plan only provides access to the following:
  - Customer Service & Communities - 24x7 access to customer service, documentation, whitepapers, and support forums.
  - AWS Trusted Advisor - Access to the 7 core Trusted Advisor checks and guidance to provision your resources following best practices to increase performance and improve security.
  - AWS Personal Health Dashboard - A personalized view of the health of AWS services, and alerts when your resources are impacted.

- Developer - AWS recommends Developer Support plan if you are testing or doing early development on AWS and want the ability to get email-based technical support during business hours as well as general architectural guidance as you build and test. This plan also supports general guidance on how services can be used for various use cases, workloads, or applications. You do not get access to Infrastructure Event Management with this plan. This plan provides access to just the 7 core Trusted Advisor checks. AWS Developer Support plan allows one primary contact to open unlimited cases.

#### References:
#### https://aws.amazon.com/premiumsupport/plans/

--

### AWS Abuse Team
The AWS Abuse team can assist you when AWS resources are used to engage in abusive behavior.

Details of the various scenarios that the AWS Abuse team can address:
- SPAM:  You are receiving unwanted emails from an AWS-owned IP addredd, or AWS resources are used to spam websites or forums.
- Port scanning: Your logs show tat one or more AWS-owned IP addresses are sending packets to multiple ports on your server, and you believe this is an attempt to discover unsecured ports.
- Denial-of-service (Dos) attacks: Your logs show that one or more AWS-owned IP address are used to flood ports on your resources with packets, and you believe that this is an attempt to overwhelm or crash your server or the software running on your server.
- Intrusion attempts: Your logs show that one or more AWS-owned IP addresses are used to attempt to log in to your resources.
- Hosting objectionable or copyrighted content: You have evidence that AWS resources are used to host or distribute illegal content or distribute copyrighted content without the consent of the copyright holder.
- Distributing malware: You have evidence that AWS resources are used to distribute software that was knowingly created to compromise or cause harm to computers or machines on which it is installed.

#### References:
#### https://aws.amazon.com/premiumsupport/knowledge-center/report-aws-abuse/

---
## Network

A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by AWS PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon network.

There are two types of VPC endpoints: interface endpoints and gateway endpoints.

An interface endpoint is an elastic network interface with a private IP address from the IP address range of your subnet that serves as an entry point for traffic destined to a supported service. Interface endpoints are powered by AWS PrivateLink, a technology that enables you to privately access services by using private IP addresses.

A gateway endpoint is a gateway that you specify as a target for a route in your route table for traffic destined to a supported AWS service. The following AWS services are supported:
- Amazon S3
- DynamoDB

#### References:
#### https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html

---
## Storage

- EFS - Amazon EFS is a file storage service for use with Amazon EC2. Amazon EFS provides a file system interface, file system access semantics, and concurrently-accessible storage for up to thousands of Amazon EC2 instances. Amazon EFS uses the Network File System protocol. Amazon EFS provides a simple, scalable, fully managed elastic NFS file system for use with AWS Cloud services and on-premises resources. It is built to scale on-demand to petabytes without disrupting applications, growing and shrinking automatically as you add and remove files, eliminating the need to provision and manage capacity to accommodate growth. The service is designed to be highly scalable, highly available, and highly durable. Amazon EFS file systems store data and metadata across multiple Availability Zones in an AWS Region. EFS file system can be mounted on instances across multiple Availability Zones.

- EBS - Amazon Elastic Block Store (EBS) is an easy to use, high-performance block storage service designed for use with Amazon Elastic Compute Cloud (EC2) for both throughput and transaction-intensive workloads at any scale. EBS volumes cannot be accessed simultaneously by multiple EC2 instances. Designed for mission-critical systems, EBS volumes are replicated within an Availability Zone (AZ) and can easily scale to petabytes of data. EBS volume can be attached to a single instance in the same Availability Zone.

- Instance Store - An instance store provides temporary block-level storage for your instance. This storage is located on disks that are physically attached to the host computer. Instance Store volumes cannot be accessed simultaneously by multiple EC2 instances. This is a good option when you need storage with very low latency, but you don't need the data to persist when the instance terminates or you can take advantage of fault-tolerant architectures. Instances store is ideal for temporary storage of information that changes frequently, such as buffers, caches, scratch data, and other temporary content, or for data that is replicated across a fleet of instances, such as a load-balanced pool of web servers.

- S3 - Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. S3 is object storage and it does not support file append operations.

#### References:
#### https://aws.amazon.com/efs/

---
## AWS EC2

- Use Mode

||Dedicated Host|Dedicated Instance|
|-----------|-----------|-----------|
|Billing|Per-host billing|Per-instance billing|
|Visibility of sockets, cores, and host ID|Provides visibility of the number of sockets and physical cores|No visibility|
|Host and instance affinity|Allows you to consistently deploy your instances to the same physical server over time|Not supported|
|Targeted instance placement|Provides additional visibility and control over how instances are placed on a physical server|Not supported|
|Automatic instance recovery|Supported|Supported|
|Bring Your Own License (BYOL)|Supported|Not Supported|

  - Amazon EC2 Dedicated Hosts
    - Amazon EC2 Dedicated Hosts allow you to use your eligible software licenses from vendors such as Microsoft and Oracle on Amazon EC2. An Amazon EC2 Dedicated Host is a physical server fully dedicated for your use, so you can help address corporate compliance requirements.
  - Dedicated instance
    - Dedicated Instances are Amazon EC2 instances that run in a virtual private cloud (VPC) on hardware that's dedicated to a single customer. Dedicated Instances that belong to different AWS accounts are physically isolated at the hardware level. However, Dedicated Instances may share hardware with other instances from the same AWS account that are not Dedicated Instances. You cannot use Dedicated Instances for using server-bound software licenses.
  - Reserved Instance
    - Reserved Instances provide you with significant savings (up to 75%) on your Amazon EC2 costs compared to On-Demand Instance pricing. Reserved Instances are not physical instances, but rather a billing discount applied to the use of On-Demand Instances in your account. You can purchase a Reserved Instance for a one-year or three-year commitment, with the three-year commitment offering a bigger discount. You cannot use Reserved Instances for using server-bound software licenses.
  - On-Demand Instance
    - An On-Demand Instance is an instance that you use on-demand. You have full control over its lifecycle — you decide when to launch, stop, hibernate, start, reboot, or terminate it. There is no long-term commitment required when you purchase On-Demand Instances. There is no upfront payment and you pay only for the seconds that your On-Demand Instances are running. The price per second for running an On-Demand Instance is fixed. On-demand instances cannot be interrupted. You cannot use On-demand Instances for using server-bound software licenses.

#### References:
#### https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html

---
## Containerization

- Amazon Elastic Container Registry (ECR)
  - Amazon Elastic Container Registry (ECR) can be used to store, manage, and deploy Docker container images. Amazon ECR eliminates the need to operate your container repositories. You can then pull your docker images from ECR and run those on Amazon Elastic Container Service (ECS).
- Amazon Elastic Container Service (ECS)
  - Amazon Elastic Container Service (Amazon ECS) is a highly scalable, fast, container management service that makes it easy to run, stop, and manage Docker containers on a cluster. You cannot use ECS to store and deploy docker container images.

#### References:
#### https://aws.amazon.com/ecr/
#### https://aws.amazon.com/ecs/

---
## Security

- AWS WAF is a web application firewall that lets you monitor the HTTP and HTTPS requests that are forwarded to an Amazon API Gateway API, Amazon CloudFront or an Application Load Balancer. HTTP and HTTPS requests are part of the Application layer, which is layer 7. AWS WAF charges based on the number of web access control lists (web ACLs) that you create, the number of rules that you add per web ACL, and the number of web requests that you receive (it is not a free service).

- AWS Shield offers protection to the layer 3 and 4. layer 3 is the Network layer and this layer decides which physical path data will take when it moves on the network. Layer 4 is the Transport layer and this layer data transmission occurs using TCP or UDP protocols

- AWS Shield Standard is activated for all AWS customers, by default. For higher levels of protection against attacks, you can subscribe to AWS Shield Advanced. While AWS Shield Standard helps protect all AWS customers, you get better protection if you are using Amazon CloudFront and Amazon Route 53. All AWS customers benefit from the automatic protections of AWS Shield Standard, at no additional charge.

- AWS Shield Advanced provides expanded DDoS attack protection for web applications running on the following resources: Amazon Elastic Compute Cloud, Elastic Load Balancing (ELB), Amazon CloudFront, Amazon Route 53, AWS Global Accelerator. With Shield Advanced, you also have exclusive access to advanced, real-time metrics and reports for extensive visibility into attacks on your AWS resources. With the assistance of the DRT (DDoS response team), AWS Shield Advanced includes intelligent DDoS attack detection and mitigation for not only for network layer (layer 3) and transport layer (layer 4) attacks but also for application layer (layer 7) attacks. AWS Shield Advanced is a paid service that provides additional protections for internet-facing applications.

#### References:
#### https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html
#### https://docs.aws.amazon.com/waf/latest/developerguide/ddos-overview.html
#### https://docs.aws.amazon.com/waf/latest/developerguide/shield-chapter.html

--
### AWS Secrets Manager
- AWS Secrets Manager helps you protect secrets needed to access your applications, services, and IT resources. The service enables you to easily rotate, manage, and retrieve database credentials, API keys, and other secrets throughout their lifecycle. Users and applications retrieve secrets with a call to Secrets Manager APIs, eliminating the need to hardcode sensitive information in plain text. It cannot be used to discover and protect your sensitive data in AWS. With Secrets Manager, you pay based on the number of secrets stored and API calls made.

---
## AWS Artifact
- AWS Artifact is your go-to, central resource for compliance-related information that matters to your organization. It provides on-demand access to AWS’ security and compliance reports and select online agreements. Reports available in AWS Artifact include our Service Organization Control (SOC) reports, Payment Card Industry (PCI) reports, and certifications from accreditation bodies across geographies and compliance verticals that validate the implementation and operating effectiveness of AWS security controls. Different types of agreements are available in AWS Artifact Agreements to address the needs of customers subject to specific regulations. For example, the Business Associate Addendum (BAA) is available for customers that need to comply with the Health Insurance Portability and Accountability Act (HIPAA). It is not a service, it's a no-cost, self-service portal for on-demand access to AWS’ compliance reports.

#### References:
#### https://aws.amazon.com/artifact/

---
## Cloud Computing

- Agility - In the world of cloud computing, "Agility" refers to the ability to rapidly develop, test and launch software applications that drive business growth Another way to explain "Agility" - AWS provides a massive global cloud infrastructure that allows you to quickly innovate, experiment and iterate. Instead of waiting weeks or months for hardware, you can instantly deploy new applications. This ability is called Agility.

- Elasticity - This refers to the ability to acquire resources as you need and release when they are no longer needed is termed as Elasticity of the Cloud.

- Reliability - This refers to the ability of a system to recover from infrastructure or service disruptions, by dynamically acquiring computing resources to meet demand, and mitigate disruptions.

- Scalability - Scalability is the measurement of a system's ability to grow to accommodate an increase in demand, or shrink down to a diminishing demand.

### Six Advantages of Cloud Computing:
- Trade capital expense for variable expense
  - Instead of having to invest heavily in data centers and servers before you know how you're going to use them, you can pay only when you consume computing resources, and pay only for how much you consume.
- Benefit from massive economies of scale
  - By using cloud computing, you can achieve a lower variable cost than you can get on your own. Because usage from hundreds of thousands of customers is aggregated in the cloud, providers such as AWS can achieve higher economies of scale, which translates into lower pay as-you-go prices.
- Stop guessing capacity
  - Eliminate guessing on your infrastructure capacity needs. When you make a capacity decision prior to the blind and application, you often end up either sitting on expensive I don't researchers are dealing with limited capacity. With cloud computing, these problems go away. You can access as much or as little capacity as you need, And scale up and down as required with only a few minutes notice.
- Increase speed and agility
  - In a cloud computing, environment new IT services are only a click away, which means that you reduce the time to make those resources available to your developers from weeks to just minutes. This results in a dramatic increase in agility for the organization, Since the cost and time it takes to experiment and develop it is significantly lower.
- Go global in minutes and deploy applications in multiple regions around the world with just a few clicks
  - Focus on projects that differentiate your business, not the infrastruture. Cloud computing lets you focus on your own customers,Rather than on the heavy lifting of racking, stacking, and powering servers.
- Go global in minutes
  - Easily deploy your application in multiple regions around the world with just a few clicks.This means you can provide lower latency and a better experience for your customers at minimal cost.

#### References:
#### https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html
#### https://wa.aws.amazon.com/wat.concepts.wa-concepts.en.html
#### https://docs.aws.amazon.com/whitepapers/latest/aws-overview/six-advantages-of-cloud-computing.html
---
## AWS Well-Architected Framework

There are three best practice areas for Reliability in the cloud - Foundations, Change Management, Failure Management. Being aware of how change affects a system (change manage- ment) allows you to plan proactively, and monitoring allows you to quickly identify trends that could lead to capacity issues or SLA breaches.

- AWS Config - AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources. Config continuously monitors and records your AWS resource configurations and allows you to automate the evaluation of recorded configurations against desired configurations. Think resource-specific history, audit, and compliance; think Config.
  - With AWS Config, you can do the following:
    - Evaluate your AWS resource configurations for desired settings.
    - Get a snapshot of the current configurations of the supported resources that are associated with your AWS account.
    - Retrieve configurations of one or more resources that exist in your account.
    - Retrieve historical configurations of one or more resources.
    - Receive a notification whenever a resource is created, modified, or deleted.
    - View relationships between resources. For example, you might want to find all resources that use a particular security group.

- AWS CloudTrail - AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command-line tools, and other AWS services.

- Amazon CloudWatch - Amazon CloudWatch is a monitoring and observability service built for DevOps engineers, developers, site reliability engineers (SREs), and IT managers. CloudWatch provides data and actionable insights to monitor applications, respond to system-wide performance changes, optimize resource utilization, and get a unified view of operational health.

- AWS Trusted Advisor - AWS Trusted Advisor is an online tool that provides you real-time guidance to help you provision your resources following AWS best practices on cost optimization, security, fault tolerance, service limits, and performance improvement.

- Amazon Inspector - Amazon Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS. Amazon Inspector automatically assesses applications for exposure, vulnerabilities, and deviations from best practices.

- Amazon GuardDuty - Amazon GuardDuty is a threat detection service that monitors malicious activity and unauthorized behavior to protect your AWS account. GuardDuty analyzes billions of events across your AWS accounts from AWS CloudTrail (AWS user and API activity in your accounts), Amazon VPC Flow Logs (network traffic data), and DNS Logs (name query patterns). This service is for AWS account level access, not for instance-level management like an EC2. GuardDuty cannot be used to check OS vulnerabilities.

#### References:
#### https://d1.awsstatic.com/whitepapers/architecture/AWS_Well-Architected_Framework.pdf
#### https://aws.amazon.com/config/
#### https://aws.amazon.com/cloudtrail/
--
### Pillars Mandated in AWS Well-Architect Framework

The AWS Well-Architected Framework helps you understand the pros and cons of decisions you make while building systems on AWS. By using the Framework you will learn architectural best practices for designing and operating reliable, secure, efficient, and cost-effective systems in the cloud. It provides a way for you to consistently measure your architectures against best practices and identify areas for improvement.

- The AWS Well-Architected Framework is based on five pillars — Operational Excellence, Security, Reliability, Performance Efficiency, and Cost Optimization.
  - "Security" - The ability to protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies.
  - "Performance Efficiency" - The ability to use computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve.
  - "Reliability" - Foundations are part of the Reliability pillar of the AWS Well-Architected Framework. AWS states that before architecting any system, foundational requirements that influence reliability should be in place. The services that are part of foundations are: AWS IAM, Amazon VPC, AWS Trusted Advisor, AWS Service Quotas (earlier known as AWS Service Limits).



---
## Migration from on-premises to AWS Cloud

- Leverage AWS Professional Services and set up AWS Landing Zone to accelerate the infrastructure migration
  - The AWS Professional Services organization is a global team of experts that can help you realize your desired business outcomes when using the AWS Cloud. AWS Professional Services consultants can supplement your team with specialized skills and experience that can help you achieve quick results.
  - AWS Landing Zone is a solution that helps customers more quickly set up a secure, multi-account AWS environment based on AWS best practices. This solution can help save time by automating the set-up of an environment for running secure and scalable workloads while implementing an initial security baseline through the creation of core accounts and resources.
  - Therefore, leveraging AWS Professional Services along with AWS Landing Zone can accelerate the infrastructure migration for the startup.

- Utilize AWS Partner Network (APN) to build a custom solution for this infrastructure migration
  - The AWS Partner Network (APN) is the global partner program for technology and consulting businesses that leverage Amazon Web Services to build solutions and services for customers. The startup can work with experts from APN to build a custom solution for this infrastructure migration.

- Raise a support ticket with AWS Support for further assistance
  - AWS Support cannot help with complex infrastructure migration of this nature.

- Use AWS Trusted Advisor to automate the infrastructure migration
  - Trusted Advisor cannot automate the infrastructure migration.

#### References:
#### https://aws.amazon.com/partners/
#### https://aws.amazon.com/professional-services/
#### https://aws.amazon.com/solutions/implementations/aws-landing-zone/

---
## Serverless stack on AWS Cloud

AWS provides a set of fully managed services that you can use to build and run serverless applications. Serverless applications don’t require provisioning, maintaining, and administering servers for backend components such as compute, databases, storage, stream processing, message queueing, and more. You also no longer need to worry about ensuring application fault tolerance and availability.

### The AWS serverless platform
- Compute
  - AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume - there is no charge when your code is not running. 
  - Lambda@Edge allows you to run Lambda functions at AWS Edge locations in response to Amazon CloudFront events.
  - AWS Fargate is a purpose-built serverless compute engine for containers. Fargate scales and manages the infrastructure required to run your containers.
- Storage
  - Amazon Simple Storage Service (Amazon S3) provides developers and IT teams with secure, durable, highly-scalable object storage. Amazon S3 is easy to use, with a simple web service interface to store and retrieve any amount of data from anywhere on the web.
  - Amazon Elastic File System (Amazon EFS) provides simple, scalable, elastic file storage. It is built to elastically scale on demand, growing and shrinking automatically as you add and remove files.
- Data stores
  - Amazon DynamoDB is a fast and flexible NoSQL database service for all applications that need consistent, single-digit millisecond latency at any scale.
  - Amazon Aurora Serverless is an on-demand, auto-scaling configuration for Amazon Aurora (MySQL-compatible edition), where the database will automatically start up, shut down, and scale capacity up or down based on your application's needs.
  - Amazon RDS Proxy is a highly available database proxy that manages thousands of concurrent connections to relational databases, allowing you to build highly scalable, secure serverless applications that connect to relational databases.
- API Proxy
  - Amazon API Gateway is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale. It offers a comprehensive platform for API management. API Gateway allows you to process hundreds of thousands of concurrent API calls and handles traffic management, authorization and access control, monitoring, and API version management.
- Application integration
  - Amazon SNS is a fully managed pub/sub messaging service that makes it easy to decouple and scale microservices, distributed systems, and serverless applications.
  - Amazon SQS is a fully managed message queuing service that makes it easy to decouple and scale microservices, distributed systems, and serverless applications.
  - AWS AppSync simplifies application development by letting you create a flexible GraphQL API to securely access, manipulate, and combine data from one or more data sources. 
  - Amazon EventBridge is a serverless event bus service that makes it easy to access application data from a variety of sources and send it into your AWS environment.
- Orchestration
  - AWS Step Functions makes it easy to coordinate the components of distributed applications and microservices using visual workflows. Building applications from individual components that each perform a discrete function lets you scale and change applications quickly. Step Functions is a reliable way to coordinate components and step through the functions of your application.
- Analytics
  - Amazon Kinesis is a platform for streaming data on AWS, offering powerful services to make it easy to load and analyze streaming data, and also providing the ability for you to build custom streaming data applications for specialized needs.
  - Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. Athena is serverless, so there is no infrastructure to manage, and you pay only for the queries that you run.
- Developer tooling
  - AWS provides tools and services that aid developers in the serverless application development process. AWS and its partner ecosystem offer tools for continuous integration and delivery, testing, deployments, monitoring and diagnostics, SDKs, frameworks, and integrated development environment (IDE) plugins.

### References
#### https://aws.amazon.com/serverless/
#### https://aws.amazon.com/athena/

---
## Data Analitycs

- Amazon Macie
  - Amazon Macie is a fully managed data security and data privacy service that uses machine learning and pattern matching to discover and protect your sensitive data in AWS. Macie automatically provides an inventory of Amazon S3 buckets including a list of unencrypted buckets, publicly accessible buckets, and buckets shared with AWS accounts outside those you have defined in AWS Organizations. Then, Macie applies machine learning and pattern matching techniques to the buckets you select to identify and alert you to sensitive data, such as personally identifiable information (PII).
- AWS Glue
  - AWS Glue is a fully managed extract, transform, and load (ETL) service that makes it easy for customers to prepare and load their data for analytics. AWS Glue job is meant to be used for batch ETL data processing. It cannot be used to discover and protect your sensitive data in AWS.
- Amazon Polly
  - Amazon Polly is a service that turns text into lifelike speech, allowing you to create applications that talk, and build entirely new categories of speech-enabled products. Polly's Text-to-Speech (TTS) service uses advanced deep learning technologies to synthesize natural sounding human speech. It cannot be used to discover and protect your sensitive data in AWS.
- Amazon Transcribe
  - You can use Amazon Transcribe to add speech-to-text capability to your applications. Amazon Transcribe uses a deep learning process called automatic speech recognition (ASR) to convert speech to text quickly and accurately. Amazon Transcribe can be used to transcribe customer service calls, to automate closed captioning and subtitling, and to generate metadata for media assets.
- Amazon Translate
  - Amazon Translate is used for language translation. Amazon Translate uses neural machine translation via deep learning models to deliver more accurate and more natural-sounding translation than traditional statistical and rule-based translation algorithms.

#### References:
#### https://aws.amazon.com/macie/
#### https://aws.amazon.com/polly/
#### https://aws.amazon.com/transcribe/

---
## AWS Monitoring

### Cost Optimization

- AWS Budgets
  - AWS Budgets gives you the ability to set custom budgets that alert you when your costs or usage exceed (or are forecasted to exceed) your budgeted amount.
  - You can also use AWS Budgets to set reservation utilization or coverage targets and receive alerts when your utilization drops below the threshold you define. Reservation alerts are supported for Amazon EC2, Amazon RDS, Amazon Redshift, Amazon ElastiCache, and Amazon Elasticsearch reservations.
- AWS Simple Monthly Calculator
  - The Simple Monthly Calculator provides an estimate of usage charges for AWS services based on certain information you provide. It helps customers and prospects estimate their monthly AWS bill more efficiently. You cannot use this service to receive alerts when the reservation utilization falls below the defined threshold.

--
### Cost-Effective

- Amazon EC2 Reserved Instances
  - You can use Amazon EC2 Reserved Instances to reserve capacity and receive a discount on your instance usage compared to running On-Demand instances. The discounted usage price is reserved for the duration of your contract, allowing you to predict compute costs over the term of the Reserved Instance.

- So the percentage savings for each option is as follows:
  - "No upfront payment option with the standard 1-year term" - 36%
  - "All upfront payment option with the standard 1-year term" - 40%
  - "No upfront payment option with the standard 3-years term" - 56%
  - "Patial upfront payment option with the standard 3-years term" - 59%

***Exam Alert:*
For the exam, there is no need to memorize these savings numbers. All you need to remember is that a 3 years term would always be more cost-effective than a 1-year term. Then within a term, "all upfront" is better than "partial upfront" which in turn is better than "no upfront" from a cost savings perspective.**

#### References:
#### https://d0.awsstatic.com/whitepapers/aws_pricing_overview.pdf

--
### Data Transfer

- There are three fundamental drivers of cost with AWS: compute, storage, and outbound data transfer. In most cases, there is no charge for inbound data transfer or data transfer between other AWS services within the same region. Outbound data transfer is aggregated across services and then charged at the outbound data transfer rate.
- Per AWS pricing, data transfer between AWS services within the same region is not charged, so there would be no data transfer charge for moving 500 GB of data from an EC2 instance to an S3 bucket in the same region.

--
### Logging

- AWS CloudTrail
  - AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account. With CloudTrail, you can log, continuously monitor, and retain account activity related to actions across your AWS infrastructure. CloudTrail provides event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command-line tools, and other AWS services. You cannot use this service to receive alerts when the reservation utilization falls below the defined threshold.

--
### Compliance

- AWS Trusted Advisor
  - AWS Trusted Advisor is an online tool that provides real-time guidance to help provision your resources following AWS best practices. Whether establishing new workflows, developing applications, or as part of ongoing improvement, recommendations provided by Trusted Advisor regularly help keep your solutions provisioned optimally. AWS Trusted Advisor analyzes your AWS environment and provides best practice recommendations in five categories: Cost Optimization, Performance, Security, Fault Tolerance, Service Limits. You cannot use this service to receive alerts when the reservation utilization falls below the defined threshold.

#### References:
#### https://aws.amazon.com/aws-cost-management/aws-budgets/
#### https://aws.amazon.com/premiumsupport/technology/trusted-advisor/best-practice-checklist/

---
## AWS Global Infrastructure

AWS has the concept of a Region, which is a physical location around the world where AWS clusters data centers. Each AWS Region consists of multiple (two or more), isolated, and physically separate AZ's within a geographic area. Each AZ has independent power, cooling, and physical security and is connected via redundant, ultra-low-latency networks.

An Availability Zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity in an AWS Region. All AZ’s in an AWS Region are interconnected with high-bandwidth, low-latency networking, over fully redundant, dedicated metro fiber providing high-throughput, low-latency networking between AZ’s.

#### References:
#### https://aws.amazon.com/about-aws/global-infrastructure/regions_az/

---
## AWS Shared Responsibility Model

Security and Compliance is a shared responsibility between AWS and the customer. This shared model can help relieve the customer’s operational burden as AWS operates, manages and controls the components from the host operating system and virtualization layer down to the physical security of the facilities in which the service operates.

Controls that apply to both the infrastructure layer and customer layers, but in completely separate contexts or perspectives are called shared controls. In a shared control, AWS provides the requirements for the infrastructure and the customer must provide their own control implementation within their use of AWS services. Configuration Management forms a part of shared controls - AWS maintains the configuration of its infrastructure devices, but a customer is responsible for configuring their own guest operating systems, databases, and applications.

- Customer
  - Responsability for security IN the Cloud.
    - Customer Data
    - Platform, Applications, Identify & Access Management
    - Operating System, Networking & Firewall Configuration
    - Client-side data encryption & data integrity authentication
    - Server-side encryption (Filesystem and/or data)
    - Network traffic protection (Encryption, Integrity, Identity)
- AWS
  - Responsability for security OF the Cloud.
    - Software
      - Compute
      - Storage
      - Database
      - Networking
    - Hardware/AWS Global Infrastructure
      - Regions
      - Avaiability Zones
      - Edge Location

#### References:
#### https://aws.amazon.com/compliance/shared-responsibility-model/