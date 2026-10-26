# AWS EC2, CLI and Automation

## 1. Connecting to EC2 Instances

Amazon EC2 provides virtual servers in the AWS Cloud. DevOps engineers connect to EC2 instances to configure servers, install software, deploy applications, and troubleshoot issues.

### Methods of Connecting to EC2

**AWS Console**
- Log in to the AWS Management Console.
- Open EC2 and select the instance.
- Click Connect.
- Choose an available connection method and follow the instructions.

**SSH (Secure Shell)**

SSH allows secure remote access to Linux servers.

Requirements:
- EC2 public IP address or reachable hostname.
- Private key file (.pem).
- Correct username for the AMI.
- Security group allowing SSH traffic, typically on port 22.

Example for Ubuntu:

```bash
ssh -i "my-key.pem" ubuntu@<EC2-PUBLIC-IP>
```

Example for Amazon Linux:

```bash
ssh -i "my-key.pem" ec2-user@<EC2-PUBLIC-IP>
```

### SSH Key Permissions

On Linux or macOS:

```bash
chmod 600 my-key.pem
```

On Windows, configure file permissions to restrict access to the private key.

**Security:** Never share private keys or upload them to GitHub.

## 2. AWS CLI

AWS CLI (Command Line Interface) allows users to manage AWS resources using terminal commands.

### Verify Installation

```bash
aws --version
```

### Configure Credentials

```bash
aws configure
```

Enter the requested credentials, default region, and output format. Use secure credential practices and never commit access keys to a Git repository.

### Useful AWS CLI Commands

Check the configured AWS identity:

```bash
aws sts get-caller-identity
```

List S3 buckets:

```bash
aws s3 ls
```

List EC2 instances:

```bash
aws ec2 describe-instances
```

These commands require valid credentials and appropriate IAM permissions.

## 3. AWS CloudFormation

AWS CloudFormation is an Infrastructure as Code (IaC) service that creates and manages AWS resources using YAML or JSON templates.

### Key Concepts
- Template: Defines AWS resources and their configuration.
- Stack: A collection of resources managed together by CloudFormation.
- IaC: Infrastructure is defined and managed through code.

### Basic Workflow
1. Prepare or obtain a CloudFormation template.
2. Review the template and permissions.
3. Open CloudFormation in the AWS Console.
4. Choose Create stack.
5. Upload the template or provide its supported location.
6. Configure parameters and permissions.
7. Review resources and potential costs.
8. Create the stack and monitor its status.

Always inspect templates before deployment because they may create chargeable resources or grant excessive permissions.

## 4. AWS Boto3

Boto3 is the AWS SDK for Python. It allows Python programs to interact with AWS services.

Uses:
- Creating and managing EC2 instances.
- Listing S3 buckets and objects.
- Starting and stopping resources.
- Automating repetitive cloud operations.

### Install Boto3

```bash
python -m pip install boto3
```

### Example: List S3 Buckets

```python
import boto3

s3 = boto3.client("s3")
response = s3.list_buckets()

for bucket in response["Buckets"]:
    print(bucket["Name"])
```

This program prints the names of S3 buckets accessible to the configured AWS identity. Boto3 uses the AWS credential provider chain, so configure credentials securely before running scripts.

## 5. AWS Management Tools

| Tool | Purpose |
|---|---|
| AWS Console | Manage resources through a graphical interface |
| SSH | Connect securely to remote Linux servers |
| AWS CLI | Manage AWS resources using terminal commands |
| CloudFormation | Create infrastructure using YAML or JSON templates |
| Boto3 | Automate AWS services using Python |

## 6. Practical Tasks

- [ ] Verify AWS CLI installation using `aws --version`.
- [ ] Configure credentials securely.
- [ ] Verify identity using `aws sts get-caller-identity`.
- [ ] List accessible S3 buckets using `aws s3 ls`.
- [ ] Inspect EC2 instances using the CLI.
- [ ] Practise SSH connections to a Linux EC2 instance.
- [ ] Review a CloudFormation template.
- [ ] Install Boto3 and practise listing S3 buckets using Python.

## 7. Key Takeaways

- SSH enables secure remote server access.
- SSH private keys must be protected.
- AWS CLI manages resources through terminal commands.
- CloudFormation creates infrastructure from templates.
- Boto3 automates AWS services using Python.
- These tools help DevOps engineers reduce manual work and manage infrastructure efficiently.

**Security and Cost Reminder:** Never upload .pem files, AWS access keys, secret keys, or other credentials to GitHub. Check AWS pricing before creating resources. Stopping an instance may not stop charges for attached storage or other resources.
