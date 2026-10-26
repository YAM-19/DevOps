# Creating Virtual Machines and Infrastructure Automation

## 1. Creating Virtual Machines

Virtual machines can be created using cloud platforms such as AWS and Microsoft Azure.

- AWS provides virtual machines through EC2.
- Azure provides virtual machines through Azure Virtual Machines.

A VM provides CPU, RAM, storage, and an operating system without requiring users to purchase physical hardware.

## 2. Manual vs. Automated VM Creation

### Manual Creation
- VMs are created through the cloud console.
- Users configure the operating system, instance type, storage, and networking.
- Useful for learning and small tasks.
- Can be time-consuming and prone to human error.

### Automated Creation
- Infrastructure is created using scripts, code, or configuration files.
- Reduces repetitive manual work.
- Improves consistency and repeatability.
- Suitable for managing infrastructure at scale.

**Key Point:** DevOps engineers prioritize automation for repeatable infrastructure tasks.

## 3. Methods of Infrastructure Automation

### 3.1 AWS CLI

AWS CLI (Command Line Interface) allows users to manage AWS resources through terminal commands.

Uses:
- Managing EC2 instances.
- Listing S3 buckets.
- Automating cloud operations through scripts.

Example command structure:

```bash
aws ec2 run-instances \
  --image-id ami-xxxxxxxx \
  --instance-type t3.micro \
  --key-name my-key
```

Replace the example AMI ID and key name with valid values. Configure networking, security, and permissions as required.

### 3.2 API Calls and Boto3

- API (Application Programming Interface) allows applications to communicate with cloud services.
- Boto3 is the AWS SDK for Python.

Uses:
- Creating EC2 instances using Python.
- Starting and stopping instances.
- Automating AWS resource management.

### 3.3 AWS CloudFormation

AWS CloudFormation is an Infrastructure as Code (IaC) service that creates and manages AWS resources using templates.

- Uses YAML or JSON templates.
- Groups resources into stacks.
- Supports repeatable infrastructure deployment.

### 3.4 AWS CDK

AWS Cloud Development Kit (CDK) allows developers to define infrastructure using programming languages such as Python, TypeScript, and Java.

- Infrastructure is written as code.
- CDK generates AWS CloudFormation templates.
- Useful for developers who prefer programming languages.

### 3.5 Terraform

Terraform is an Infrastructure as Code tool developed by HashiCorp.

- Uses declarative configuration files written in HCL.
- Supports multiple cloud providers, including AWS and Azure.
- Helps manage infrastructure consistently.
- Useful for single-cloud, multi-cloud, and hybrid-cloud environments.

## 4. Comparison of Automation Tools

| Tool | Purpose |
|---|---|
| AWS CLI | Manage AWS using commands |
| Boto3 | Manage AWS using Python |
| CloudFormation | Define AWS infrastructure using templates |
| AWS CDK | Define AWS infrastructure using programming languages |
| Terraform | Manage infrastructure across providers |

## 5. Infrastructure as Code (IaC)

Infrastructure as Code is the practice of creating and managing infrastructure using code or configuration files instead of relying entirely on manual setup.

Benefits:
- Automation.
- Consistency.
- Repeatability.
- Version control.
- Reduced human error.
- Easier maintenance and scaling.

Example: Instead of manually creating five EC2 instances, a DevOps engineer can define the infrastructure in Terraform and provision it through code.

## 6. Steps to Create an AWS EC2 Instance

1. Log in to the AWS Management Console.
2. Open the EC2 service.
3. Click Launch instance.
4. Enter an instance name.
5. Select an Amazon Machine Image (AMI).
6. Choose an instance type.
7. Configure a key pair if SSH access is needed.
8. Configure networking and security group rules.
9. Review storage settings.
10. Launch the instance.
11. Verify that the instance is running.

Azure virtual machines can be created similarly through the Azure portal.

**Cost Reminder:** Check current pricing and Free Tier eligibility before launching resources. Stopping an instance may not stop charges for attached storage or other resources.

## 7. Key Takeaways

- AWS EC2 and Azure Virtual Machines provide cloud-based computing resources.
- Automation reduces repetitive manual work.
- AWS CLI, Boto3, CloudFormation, and CDK are AWS automation methods.
- Terraform supports infrastructure management across multiple cloud providers.
- IaC makes infrastructure repeatable, consistent, and easier to maintain.
