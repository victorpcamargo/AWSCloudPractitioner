# Stephane Maarek | Ultimate AWS Certified Cloud Practitioner - 2020
## https://itau.udemy.com/course/aws-certified-cloud-practitioner-new/learn/lecture/19891628#overview

---

# Cloud Computing

## The Deployment Models of the Cloud

- **Private Cloud**
    - Cloud services used by a single organization, not exposed to the public
    - Complete control
    - Security for sensitive applications
    - Meet specific business need
- **Public Cloud**
    - Cloud resources owned and operated by a thirdparty cloud service provider delivered over the Internet
    - Six Advantages of Cloud Computing
- **Hybrid Cloud**
    - Keep some servers on premises and extend some capabilities to the Cloud
    - Control over sensitive assets in your private infrastructure
    - Flexibility and costeffectiveness of the public cloud

## Six Advantages of Cloud Computing

- **Trade capital expense (CAPEX) for operational expense (OPEX)**
    - Pay On-Demand: don't own hardware
    - Reduced Total Cost of Ownership (TCO) & Operational Expense (OPEX)
- **Benefit from massice economies of scale**
    - Prices are reduced as AWS is more efficient due to large scale
- **Stop guessing capacity**
    - Scale based on actual measured usage
- **Increase speed and agility**
- **Stop spending money running and maintaining data centers**
- **Go global in minutes** 
    - Leverage the AWS global infrastructure

## Problem Solved by The Cloud

- **Flexibility**: Change resource types when needed
- **Cost-effectiveness**: Pay-as-you-go, for what you use
- **Scalability**: Accommodate larger loads by making hardware stronger or adding additional nodes
- **Elasticity**: Ability to scale out and scale-in when needed
- **High-availability and fault-tolerance**: build across data centers
- **Agility**: rapidly develop, test and launch software applications

## Types of Cloud Computing

- **Infrastructure as a Service (IaaS)**
    - Provide building blocks for cloud IT
    - Provides networking, computers, data storage space
    - Highest level of flexibility
    - Easy parallel with traditional on-premises IT
- **Platform as a Service (PaaS)**
    - Removes the need for your organization to manage the underlying infrastructure
    - Focus on the deployment and management of your applications
- **Software as a Service (SaaS)**
    - Completed product that is run and managed by the service provider

---

# AWS Cloud Overview

## AWS Global Infrastructure

- **AWS Regions**
    - A region is a cluster of data centers
    - Most AWS services are region-scoped
    - Each region has many AZ (Min 2, Max 6 - Usually 3)
- **AWS Availability Zones**
    - Each AZ is one or more discrete data centers with redundant power, networking, and connectivity
    - They're separate from each other, so that they're isolated from disasters
    - They're connected with high bandwidth, ultra-low latency networking
- **AWS Data Centers**
- **AWS Edge Locations / Points of Presence**
    - Content is delivered to end users with lower latency

## Tour of the AWS Console

- AWS has **Global Services**:
    - **Identity and Access Management (IAM)**
    - **Route 53 (DNS Service)**
    - **CloudFront (Content Delivery Networking)**
    - **WAF (Web Application Firewall)**
- **Most AWS services are Region-scoped**:
    - **Amazon EC2 (IaaS)**
    - **Elastic Beanstalk (PaaS)**
    - **Lambda (Function as a Service - FaaS)**
    - **Rekognition (SaaS)**

## Shared Responsability Model diagram

- **Customer** = Responsability for the security **IN** the Cloud
- **AWS** = Responsability fot the security **OF** the Cloud

![Shared Responsability Model diagram](https://d1.awsstatic.com/security-center/Shared_Responsibility_Model_V2.59d1eccec334b366627e9295b304202faf7b899b.jpg)

### Shared Responsability Model for IAM

- AWS
    - Infrastructure (global network security)
    - Configuration and vulnerability analysis
    - Compliance validation
- Customer
    - Users, Groups, Roles, Policies management and monitoring
    - Enable MFA on all accounts
    - Rotate all your keys often
    - Use IAM tools to apply appropriate permissions
    - Analyze access patterns & review permissions

### Shared Responsability Model for EC2

- AWS
    - Infrastructure (global network security)
    - Isolation on physical hosts
    - Replacing faulty hardware
    - Compliance validation
- Customer
    - Security Groups rules
    - Operating-system patches and updates
    - Software and utilities installed on the EC2 instance
    - IAM Roles assigned to EC2 & IAM user access management
    - Data security on your instance

---

# IAM - Identity and Access Management

## Users and Groups

- IAM is a **Global service**
- **Root account** created by default, *shouldn't be used or shared*
- **Users are people within your organization**, and can be grouped
- **Groups only contain users**, not other groups
- **Users don't have to belong to a group, and user can belong to multiple groups**

## Permissions

- **Users and Groups can be assigned JSON documents called policies**
- These policies define the permissions of the users
- **In AWS you apply the least privilege principle**: don't give more permissions than a user needs

## IAM Roles for Services

- Some AWS service will need to perform actions on your behalf
- To do so, we will assign permissions to AWS services with IAM Roles
- **Common roles**:
    - **EC2 Instance Roles**
    - **Lambda Function Roles**
    - **Roles for CloudFormation**

## IAM Security Tools

- **IAM Credentials Report** (account-level)
    - a report that lists all your account's users and the status of their various credentials
- **IAM Access Advisor** (user-level)
    - Access advisor show the service permissions granted to a user and when those services were last accessed
    - You can use this information to revise your policies

## IAM Guidelines & Best Practices

- Don’t use the root account except for AWS account setup
- One physical user = One AWS user
- **Assign users to groups and assign permissions to groups**
- Create a strong password policy
- **Use and enforce the use of Multi Factor Authentication (MFA)**
- **Create and use Roles for giving permissions to AWS services**
- **Use Access Keys for Programmatic Access (CLI / SDK)**
- **Audit permissions of your account with the IAM Credentials Report**
- Never share IAM users & Access Keys

## IAM Section - Summary

||
|---|
|Users: mapped to a physical user, has a password for AWS Console|
|Groups: contains users only|
|Policies: JSON document that outlines permissions for users or groups|
|Roles: for EC2 instances or AWS services|
|Security: MFA + Password Policy|
|Access Keys: access AWS using the CLI or SDK|
|Audit: IAM Credential Reports & IAM Access Advisor|

---

# AWS CLI

## AWS Access

- To access AWS, you have three options:
    - **AWS Management Console** (protected by password + MFA)
    - **AWS Command Line Interface (CLI)**: Protected by access keys
    - **AWS Software Developer Kit (SDK)** - for code: protected by access keys
- Access Keys are generated through the AWS Console
- Users manage their own access keys
- Access Keys are secret, just like a password. Don't share them
- **Access Key ID ~= username**
- **Secret Access Key ~= password**

---

# EC2 - Elastic Compute Cloud

## Concepts

- EC2 is one of the most popular of AWS’ offering
- EC2 = Elastic Compute Cloud = Infrastructure as a Service (IaaS)
- It mainly consists in the capability of :
    - Renting virtual machines (EC2)
    - Storing data on virtual drives (EBS)
    - Distributing load across machines (ELB)
    - Scaling the services using an auto-scaling group (ASG)

## Introduction to Security Groups

- Security Groups are the fundamental of network security in AWS
- **They control how traffic is allowed into or out of our EC2 Instances**
- **Security groups only contain allow rules**
- Security groups rules **can reference by IP or by security group**

### Security Groups Deeper Dive

- Security groups are **acting as a “firewall” on EC2 instances**
- They regulate:
    - **Access to Ports**
    - **Authorised IP ranges** – IPv4 and IPv6
    - **Control of inbound network** (from other to the instance)
    - **Control of outbound network** (from the instance to other

## EC2 Instance Connect

- Connect to your EC2 instance within your browser
- No need to use your key file that was downloaded
- The “magic” is that a temporary key is uploaded onto EC2 by AWS
- Works only out-of-the-box with Amazon Linux 2
- Need to make sure the port 22 is still opened!

## EC2 Instances Purchasing Options
- **On-Demand Instances**: short workload, predictable pricing
    - Pay for what you use:
        - **Linux - billing per second, after the first minute**
        - **All other operating systems (ex: Windows) - billing per hour**
    - Has the highest cost but **no upfront payment**
    - No long-term commitment
    - **Recommended for short-term and un-interrupted workloads**, where you can't predict how the application will behave
- **Reserved**: (**MINIMUM 1 year**)
    - **Reserved Instances**: long workloads
        - **Up to 72% discount compared to On-demand**
        - **Reservation period**: 1 year = + discount | **3 years = +++ discount**
        - **Purchasing options**: no upfront | partial upfront = + | **All upfront = ++ discount**
        - Reserve a **specific instance type**
        - **Recommended for steady-state usage applications (think database)**
    - **Convertible Reserved Instances**: long workloads with flexible instances
        - **Can change the EC2 instance type**
        - **Up to 45% discount**
    - **Scheduled Reserved Instances**: example – every Thursday between 3 and 6 pm
        - Launch within time window you reserve
        - **When you require a fraction of day / week / month**
        - Commitment for 1 year only
- **Spot Instances**: short workloads, cheap, can lose instances (less reliable)
    - Can get a discount of up to **90% compared to On-demand**
    - **Instances that you can “lose” at any point of time** if your max price is less than the current spot price
    - The **MOST cost-efficient** instances in AWS
    - **Useful for workloads that are resilient to failure**
        - Batch jobs
        - Data analysis
        - Image processing
        - Any distributed workloads
        - Workloads with a flexible start and end time
    - **Not suitable for critical jobs or databases**
- **Dedicated Hosts**: book an entire physical server, control instance placement
    - An Amazon EC2 Dedicated Host is a **physical server with EC2 instance capacity fully dedicated to your use**. Dedicated Hosts can **help you address compliance requirements** and **reduce costs** by allowing you to **use your existing server-bound software licenses**.
    - Allocated for your account for a **3-year period reservation**
    - **More expensive**
    - Useful for software that have complicated licensing model (**BYOL – Bring Your Own License**)
    - Or for **companies that have strong regulatory or compliance needs**
- **Dedicated Instances**: no other customers will share your hardware
    - Instances running on **hardware that’s dedicated to you**
    - **May share hardware with other instances in same account**
    - No control over instance placement (**can move hardware after Stop / Start**)

## EC2 Section – Summary

    - EC2 Instance: AMI (OS) + Instance Size (CPU + RAM) + Storage + security groups + EC2 User Data
    - Security Groups: Firewall attached to the EC2 instance
    - **EC2 User Data: Script launched at the first start of an instance**
    - SSH: start a terminal into our EC2 Instances (port 22)
    - **EC2 Instance Role: link to IAM roles**
    - Purchasing Options: **On-Demand, Spot, Reserved (Standard + Convertible + Scheduled), Dedicated Host, Dedicated Instance**