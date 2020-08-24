# AWS Cloud Practitioner - Study Content

## AWS Support

### Plans
|Description|Basic|Developer|Enterprise|Corporate|Business|
|-----------|-----------|-----------|-----------|-----------|-----------|
|Provide access to guidance, configuration and troubleshooting of AWS with interoperability  many common operating systems, platforms, and application stack components|||YES||YES|
|

- Enterprise - AWS Enterprise Support provides customers with concierge-like service where the main focus is helping the customer achieve their outcomes and find success in the cloud. With Enterprise Support, you get 24x7 technical support from high-quality engineers, tools and technology to automatically manage the health of your environment, consultative architectural guidance delivered in the context of your applications and use-cases, and a designated Technical Account Manager (TAM) to coordinate access to proactive/preventative programs and AWS subject matter experts. You get access to guidance, configuration, and troubleshooting of AWS interoperability with many common operating systems, platforms, and application stack components.

- Business - AWS recommends Business Support if you have production workloads on AWS and want 24x7 phone, email and chat access to technical support and architectural guidance in the context of your specific use-cases. You get full access to AWS Trusted Advisor Best Practice Checks. You get access to guidance, configuration, and troubleshooting of AWS interoperability with many common operating systems, platforms, and application stack components.

- Basic - The basic plan only provides access to the following:
  - Customer Service & Communities - 24x7 access to customer service, documentation, whitepapers, and support forums. AWS Trusted Advisor- Access to the 7 core Trusted Advisor checks and guidance to provision your resources following best practices to increase performance and improve security. AWS Personal Health Dashboard - A personalized view of the health of AWS services, and alerts when your resources are impacted.

- Developer - AWS recommends Developer Support plan if you are testing or doing early development on AWS and want the ability to get email-based technical support during business hours. This plan also supports general guidance on how services can be used for various use cases, workloads, or applications. You do not get access to Infrastructure Event Management with this plan.

### References:
### https://aws.amazon.com/premiumsupport/plans/

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

### References:
### https://aws.amazon.com/premiumsupport/knowledge-center/report-aws-abuse/

---
## Network

A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by AWS PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon network.

There are two types of VPC endpoints: interface endpoints and gateway endpoints.

An interface endpoint is an elastic network interface with a private IP address from the IP address range of your subnet that serves as an entry point for traffic destined to a supported service. Interface endpoints are powered by AWS PrivateLink, a technology that enables you to privately access services by using private IP addresses.

A gateway endpoint is a gateway that you specify as a target for a route in your route table for traffic destined to a supported AWS service. The following AWS services are supported:
- Amazon S3
- DynamoDB

### References:
### https://docs.aws.amazon.com/vpc/latest/userguide/vpc-endpoints.html

---
## Storage

- EFS - Amazon EFS is a file storage service for use with Amazon EC2. Amazon EFS provides a file system interface, file system access semantics, and concurrently-accessible storage for up to thousands of Amazon EC2 instances. Amazon EFS uses the Network File System protocol.

- EBS - Amazon Elastic Block Store (EBS) is an easy to use, high-performance block storage service designed for use with Amazon Elastic Compute Cloud (EC2) for both throughput and transaction-intensive workloads at any scale. EBS volumes cannot be accessed simultaneously by multiple EC2 instances.

- Instance Store - An instance store provides temporary block-level storage for your instance. This storage is located on disks that are physically attached to the host computer. Instance Store volumes cannot be accessed simultaneously by multiple EC2 instances.

- S3 - Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. S3 is object storage and it does not support file append operations.

### References:
### https://aws.amazon.com/efs/

---
## Security

- AWS WAF is a web application firewall that lets you monitor the HTTP and HTTPS requests that are forwarded to an Amazon API Gateway API, Amazon CloudFront or an Application Load Balancer. HTTP and HTTPS requests are part of the Application layer, which is layer 7.

- AWS Shield offers protection to the layer 3 and 4. layer 3 is the Network layer and this layer decides which physical path data will take when it moves on the network. Layer 4 is the Transport layer and this layer data transmission occurs using TCP or UDP protocols

### References:
### https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html

---
