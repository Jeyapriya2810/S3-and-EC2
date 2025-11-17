# EX - 2 Cloud Storage Creation (S3) And Launching An EC2 Instance In AWS

## Aim

- Sign up and configure an AWS account.
- Create and manage IAM roles and users.
- Launch and connect to an EC2 instance.
- Install and configure AWS CLI on Windows.
- Understand AWS Free Tier usage.
- Explore AWS documentation and core services (EC2, S3, IAM, etc.).

## Algorithm

1. Sign up for an AWS account using the AWS Console.
2. Set up IAM users and assign required permissions.
3. Log in to AWS Management Console and explore key services.
4. Launch a new EC2 instance with proper configurations.
5. Create and download a key pair (.pem).
6. Configure a security group with necessary inbound rules.
7. Connect to the EC2 instance using PowerShell or PuTTY (on Windows).
8. Install AWS CLI for Windows and run `aws configure` to set up credentials.

## Procedure

### 1. AWS Account Setup

- Go to [AWS Console](https://aws.amazon.com/console/) and create an account.
- Navigate to IAM and create users and roles with required permissions.
- Log in to AWS Management Console.
- Explore key services such as EC2, S3, IAM, RDS, and VPC.
- Review Free Tier usage to avoid exceeding limits.

![image](https://github.com/user-attachments/assets/d82ac702-5641-47c2-a70d-9f42e9125c82)


### 2. Create & Manage EC2 Instance (Windows)

- Open EC2 Dashboard and click **Launch Instance**.
- Select an Amazon Machine Image (Ubuntu or Amazon Linux).
- Choose `t2.micro` as the instance type for Free Tier.
- Configure VPC, subnet, and enable auto-assign public IP.
- Set root volume size (default 8GB).
- Configure security group to allow:
  - **SSH (port 22)**
  - **HTTP (port 80)** if needed
- Create and download a `.pem` key pair.
- Click **Launch** and wait for the instance to initialize.

![image](https://github.com/user-attachments/assets/9031762b-0166-4ec8-9234-dbe7e60f1ee1)


#### Connecting to EC2 from Windows:

- **Using PowerShell** (with OpenSSH):
  ```powershell
  ssh -i path\to\your-key.pem ec2-user@your-instance-public-ip
  
### Using PuTTY:

- Convert `.pem` to `.ppk` using **PuTTYgen**.
- Use **PuTTY** to SSH into your instance using the public IP address and `.ppk` key.

---

### 3. AWS CLI Installation on Windows

- Download the Windows installer from the [AWS CLI official page](https://aws.amazon.com/cli/).
- Run the installer and complete the setup.
- Open **Command Prompt** and configure AWS CLI:

### Outcome:

![image](https://github.com/user-attachments/assets/1b4997e6-8d4e-4592-9e80-1f551018e981)

![image](https://github.com/user-attachments/assets/b9000051-c8e4-46e1-91cd-b99a2ea794db)

### Result:
Successfully set up AWS environment on Windows, launched EC2 instance, and configured AWS CLI.
