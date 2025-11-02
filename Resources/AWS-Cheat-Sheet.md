# AWS Cloud Computing - Complete Cheat Sheet

## 🚀 Ultimate Reference Guide for Diploma Students

---

## Table of Contents

1. [Cloud Computing Fundamentals](#cloud-computing-fundamentals)
2. [AWS Services Quick Reference](#aws-services-quick-reference)
3. [Common AWS CLI Commands](#common-aws-cli-commands)
4. [Security Best Practices](#security-best-practices)
5. [Cost Optimization Tips](#cost-optimization-tips)
6. [Troubleshooting Guide](#troubleshooting-guide)
7. [Keyboard Shortcuts](#keyboard-shortcuts)
8. [Important URLs](#important-urls)

---

## Cloud Computing Fundamentals

### **5 Characteristics (Remember: OBRRE)**
1. **O**n-Demand Self-Service
2. **B**road Network Access
3. **R**esource Pooling
4. **R**apid Elasticity
5. **E**conomy (Measured Service)

### **Service Models (IPS)**

| Model | You Manage | AWS Manages | Example |
|-------|------------|-------------|---------|
| **IaaS** | OS, Apps | Hardware | EC2, S3 |
| **PaaS** | Apps Only | OS, Hardware | Elastic Beanstalk |
| **SaaS** | Nothing | Everything | AWS Chime |

### **Deployment Models (PPHC)**
- **P**ublic: AWS, Azure, GCP
- **P**rivate: Own data center
- **H**ybrid: Public + Private
- **C**ommunity: Shared group

---

## AWS Services Quick Reference

### **Compute**

| Service | Purpose | Use Case | Cost |
|---------|---------|----------|------|
| **EC2** | Virtual Servers | Web hosting | From ₹0.63/hr |
| **Lambda** | Serverless Functions | Event processing | Free 1M requests |
| **Lightsail** | Simple VPS | Starter projects | From ₹3.50/mo |
| **Elastic Beanstalk** | App Platform | Quick deployment | Only resource cost |

### **Storage**

| Service | Purpose | Use Case | Cost |
|---------|---------|----------|------|
| **S3** | Object Storage | Files, backups | ₹2.30/GB/mo |
| **EBS** | Block Storage | EC2 disk | ₹6/GB/mo |
| **EFS** | File System | Shared storage | ₹24/GB/mo |
| **Glacier** | Archive | Long-term backup | ₹0.36/GB/mo |

### **Database**

| Service | Purpose | Use Case | Cost |
|---------|---------|----------|------|
| **RDS** | Relational DB | MySQL, PostgreSQL | From ₹12/mo |
| **DynamoDB** | NoSQL | High-speed apps | Free 25GB |
| **ElastiCache** | In-memory | Caching | From ₹13/mo |
| **Aurora** | AWS MySQL/PostgreSQL | High performance | From ₹29/mo |

### **Networking**

| Service | Purpose | Use Case | Free Tier |
|---------|---------|----------|-----------|
| **VPC** | Virtual Network | Isolated network | Yes |
| **Route 53** | DNS Service | Domain management | 50 queries free |
| **CloudFront** | CDN | Fast content delivery | 1TB transfer |
| **ELB** | Load Balancer | Distribute traffic | 750 hrs |

### **Security & Identity**

| Service | Purpose | Free? |
|---------|---------|-------|
| **IAM** | Access Management | ✅ Yes |
| **Cognito** | User Authentication | 50K MAU free |
| **KMS** | Key Management | 20K requests free |
| **WAF** | Web Firewall | 1M requests free |

### **Management & Monitoring**

| Service | Purpose | Free Tier |
|---------|---------|-----------|
| **CloudWatch** | Monitoring | 10 metrics |
| **CloudTrail** | Audit Logs | 1 trail free |
| **Systems Manager** | Ops Management | Basic free |
| **Trusted Advisor** | Recommendations | Basic free |

---

## Common AWS CLI Commands

### **Installation**

```bash
# Windows (PowerShell)
msiexec.exe /i https://awscli.amazonaws.com/AWSCLIV2.msi

# Mac
brew install awscli

# Linux
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

### **Configuration**

```bash
# Configure AWS CLI
aws configure

# Set values
AWS Access Key ID: YOUR_KEY
AWS Secret Access Key: YOUR_SECRET
Default region: ap-south-1
Default output format: json

# List configurations
aws configure list

# Set specific profile
aws configure --profile student
```

### **S3 Commands**

```bash
# List all buckets
aws s3 ls

# Create bucket
aws s3 mb s3://my-bucket-name

# Upload file
aws s3 cp file.txt s3://my-bucket-name/

# Upload folder
aws s3 cp myfolder/ s3://my-bucket-name/myfolder/ --recursive

# Download file
aws s3 cp s3://my-bucket-name/file.txt ./

# List bucket contents
aws s3 ls s3://my-bucket-name/

# Delete file
aws s3 rm s3://my-bucket-name/file.txt

# Delete bucket
aws s3 rb s3://my-bucket-name --force

# Sync folder
aws s3 sync ./myfolder s3://my-bucket-name/myfolder/

# Make file public
aws s3api put-object-acl --bucket my-bucket-name --key file.txt --acl public-read
```

### **EC2 Commands**

```bash
# List instances
aws ec2 describe-instances

# Start instance
aws ec2 start-instances --instance-ids i-1234567890abcdef0

# Stop instance
aws ec2 stop-instances --instance-ids i-1234567890abcdef0

# Terminate instance
aws ec2 terminate-instances --instance-ids i-1234567890abcdef0

# List regions
aws ec2 describe-regions

# List availability zones
aws ec2 describe-availability-zones --region ap-south-1

# Create key pair
aws ec2 create-key-pair --key-name MyKeyPair --query 'KeyMaterial' --output text > MyKeyPair.pem

# List security groups
aws ec2 describe-security-groups

# Get instance status
aws ec2 describe-instance-status --instance-ids i-1234567890abcdef0
```

### **IAM Commands**

```bash
# List users
aws iam list-users

# Create user
aws iam create-user --user-name student-john

# List groups
aws iam list-groups

# Create group
aws iam create-group --group-name Developers

# Add user to group
aws iam add-user-to-group --user-name student-john --group-name Developers

# List policies
aws iam list-policies

# Attach policy to user
aws iam attach-user-policy --user-name student-john --policy-arn arn:aws:iam::aws:policy/AmazonS3ReadOnlyAccess

# Create access key
aws iam create-access-key --user-name student-john

# List access keys
aws iam list-access-keys --user-name student-john
```

### **RDS Commands**

```bash
# List DB instances
aws rds describe-db-instances

# Create DB instance
aws rds create-db-instance \
    --db-instance-identifier mydb \
    --db-instance-class db.t2.micro \
    --engine mysql \
    --master-username admin \
    --master-user-password password123 \
    --allocated-storage 20

# Stop DB instance
aws rds stop-db-instance --db-instance-identifier mydb

# Start DB instance
aws rds start-db-instance --db-instance-identifier mydb

# Delete DB instance
aws rds delete-db-instance --db-instance-identifier mydb --skip-final-snapshot
```

---

## Security Best Practices

### **AWS Account Security**

#### **Root Account:**
```
✅ DO:
- Enable MFA immediately
- Use strong password (16+ chars)
- Create IAM users for daily work
- Never share credentials
- Set up billing alerts

❌ DON'T:
- Use for daily tasks
- Create access keys
- Share with anyone
- Disable MFA
- Ignore security alerts
```

#### **IAM Best Practices:**

1. **Enable MFA for all users**
```bash
# Via Console
IAM → Users → Security credentials → Enable MFA
```

2. **Use groups, not individual permissions**
```
Good: Create "Developers" group → Add users
Bad: Attach policies to each user individually
```

3. **Principle of Least Privilege**
```
Give minimum permissions needed
Example: S3 read-only instead of full access
```

4. **Rotate access keys regularly**
```
Create new key → Update apps → Delete old key
Frequency: Every 90 days
```

5. **Use IAM roles for EC2**
```
Instead of: Storing keys on EC2
Use: Attach IAM role to EC2
```

### **Password Policy**

```
Minimum length: 12 characters
Require:
☑ Uppercase letters (A-Z)
☑ Lowercase letters (a-z)
☑ Numbers (0-9)
☑ Symbols (!@#$%^&*)
☑ Expiration: 90 days
☑ Prevent reuse: Last 5 passwords
```

### **Security Groups Rules**

```
✅ GOOD:
SSH (22):    Your IP only (123.45.67.89/32)
HTTP (80):   Anywhere (0.0.0.0/0)
HTTPS (443): Anywhere (0.0.0.0/0)
Custom:      Specific IP range

❌ BAD:
SSH (22):    Anywhere (0.0.0.0/0) ← Security risk!
RDP (3389):  Anywhere (0.0.0.0/0) ← Security risk!
```

### **S3 Bucket Security**

```bash
# Enable encryption
aws s3api put-bucket-encryption \
    --bucket my-bucket \
    --server-side-encryption-configuration \
    '{"Rules": [{"ApplyServerSideEncryptionByDefault": {"SSEAlgorithm": "AES256"}}]}'

# Block public access (recommended)
aws s3api put-public-access-block \
    --bucket my-bucket \
    --public-access-block-configuration \
    "BlockPublicAcls=true,IgnorePublicAcls=true,BlockPublicPolicy=true,RestrictPublicBuckets=true"

# Enable versioning
aws s3api put-bucket-versioning \
    --bucket my-bucket \
    --versioning-configuration Status=Enabled

# Enable logging
aws s3api put-bucket-logging \
    --bucket my-bucket \
    --bucket-logging-status file://logging.json
```

---

## Cost Optimization Tips

### **Free Tier Limits (Remember!)**

```
EC2:           750 hours/month (t2.micro)
S3:            5 GB storage + 20K GET + 2K PUT
RDS:           750 hours/month (db.t2.micro)
Lambda:        1 million requests + 400K GB-seconds
Data Transfer: 15 GB outbound
CloudFront:    50 GB transfer + 2M requests
```

### **Cost Saving Strategies**

#### **1. Right-Sizing**
```
DON'T use:   t2.large ($0.094/hr)
When:        t2.micro ($0.0116/hr) works

Savings:     $60/month per instance
```

#### **2. Stop Unused Resources**
```
EC2 Running 24/7:    $8.35/month
EC2 Running 8hr/day: $2.78/month

Savings: $5.57/month (67%)
```

#### **3. Delete Old Data**
```
S3 Storage:
- Delete unused files
- Move to Glacier (90% cheaper)
- Enable lifecycle policies

EBS Volumes:
- Delete unused volumes
- Take snapshots, delete volume
- Use gp3 instead of gp2 (20% cheaper)
```

#### **4. Use Reserved Instances (Production)**
```
On-Demand:      $0.0116/hour
1-Year Reserved: $0.0070/hour (40% savings)
3-Year Reserved: $0.0043/hour (63% savings)

Use only if: Running 24/7 for 1+ years
```

#### **5. Set Up Billing Alerts**
```bash
# CloudWatch Alarm
Alert when: Monthly charges > $5
Action: Send email notification

# Budget
Set: Monthly budget $10
Alert: At 80% ($8) and 100% ($10)
```

### **Cost Monitoring Commands**

```bash
# Get current month cost
aws ce get-cost-and-usage \
    --time-period Start=2025-01-01,End=2025-01-31 \
    --granularity MONTHLY \
    --metrics BlendedCost

# Get service-wise cost
aws ce get-cost-and-usage \
    --time-period Start=2025-01-01,End=2025-01-31 \
    --granularity MONTHLY \
    --metrics BlendedCost \
    --group-by Type=SERVICE
```

---

## Troubleshooting Guide

### **Common Issues & Solutions**

#### **1. Can't Connect to EC2**

**Error:** `Connection timed out` or `Permission denied`

**Solutions:**
```
Check 1: Instance is running?
→ AWS Console → EC2 → Instances → Status

Check 2: Security group allows SSH (port 22)?
→ Security Groups → Inbound rules → SSH from My IP

Check 3: Using correct key file?
→ Verify key file name matches
→ chmod 400 key.pem (Mac/Linux)

Check 4: Using correct username?
→ Amazon Linux: ec2-user
→ Ubuntu: ubuntu
→ CentOS: centos

Check 5: Correct public IP?
→ IP changes when you stop/start
→ Use Elastic IP for fixed address

Fix Command:
ssh -i mykey.pem ec2-user@PUBLIC-IP -v
(Add -v for verbose error messages)
```

#### **2. Website Not Accessible (EC2)**

**Error:** `This site can't be reached`

**Solutions:**
```
Check 1: Web server running?
sudo systemctl status httpd    # Amazon Linux
sudo systemctl status apache2  # Ubuntu

Start if stopped:
sudo systemctl start httpd
sudo systemctl start apache2

Check 2: Security group allows HTTP (port 80)?
→ Inbound rules → HTTP from Anywhere

Check 3: Firewall on EC2?
sudo iptables -L
sudo iptables -F  # Clear rules (temporary)

Check 4: Test locally first:
curl localhost  # Should show HTML

Check 5: Using HTTP not HTTPS:
http://PUBLIC-IP (not https://)
```

#### **3. S3 Access Denied**

**Error:** `AccessDenied` or `403 Forbidden`

**Solutions:**
```
Check 1: File is public?
→ S3 Console → Object → Permissions → Public

Check 2: Bucket policy allows public access?
→ Bucket → Permissions → Bucket policy

Sample Public Policy:
{
    "Version": "2012-10-17",
    "Statement": [{
        "Sid": "PublicReadGetObject",
        "Effect": "Allow",
        "Principal": "*",
        "Action": "s3:GetObject",
        "Resource": "arn:aws:s3:::BUCKET-NAME/*"
    }]
}

Check 3: Block public access disabled?
→ Bucket → Permissions → Block public access
→ Must be OFF for public files

Check 4: IAM permissions (if using CLI)?
→ User has s3:GetObject permission
```

#### **4. EC2 Key Permission Error (Windows)**

**Error:** `WARNING: UNPROTECTED PRIVATE KEY FILE!`

**Solution:**
```
Windows:
1. Right-click .pem file → Properties
2. Security tab → Advanced
3. Disable inheritance
4. Remove all users except yourself
5. Give yourself full control

Mac/Linux:
chmod 400 mykey.pem
```

#### **5. Free Tier Exceeded**

**Error:** Getting charged when shouldn't

**Solutions:**
```
Check 1: Using correct instance type?
→ Must be t2.micro (not t2.small)

Check 2: Running hours exceeded?
→ 750 hours = ~1 instance 24/7
→ 2 instances = only 375 hours each

Check 3: Data transfer exceeded?
→ Free tier: 15 GB out
→ Check CloudWatch metrics

Check 4: Multiple regions?
→ Free tier is PER REGION
→ Use only ap-south-1

Check 5: Old resources forgotten?
→ Check all regions for:
   - Running EC2
   - EBS volumes
   - Elastic IPs (not attached)
   - Load Balancers
   - RDS instances
```

#### **6. IAM User Can't Login**

**Error:** `Invalid username or password`

**Solutions:**
```
Check 1: Using correct URL?
→ https://ACCOUNT-ID.signin.aws.amazon.com/console
→ Not root login URL

Check 2: Username correct?
→ Usernames are case-sensitive

Check 3: Password correct?
→ First login? Must change password

Check 4: User has console access?
→ IAM → Users → Security credentials
→ Console access must be enabled

Check 5: Account active?
→ Check email for verification
```

---

## Keyboard Shortcuts

### **AWS Console**

```
Alt + S         : Open service search
Ctrl + K        : Command palette
Ctrl + Q        : Quick search
/               : Focus search bar
Esc             : Close modals
```

### **SSH Terminal**

```
Ctrl + C        : Cancel command
Ctrl + D        : Logout
Ctrl + L        : Clear screen
Ctrl + R        : Search command history
Ctrl + A        : Go to line start
Ctrl + E        : Go to line end
Ctrl + U        : Delete line before cursor
Ctrl + K        : Delete line after cursor
Tab             : Auto-complete
↑ ↓             : Navigate command history
```

### **Useful Linux Commands**

```bash
# System Info
whoami          # Current user
hostname        # Server name
uname -a        # System details
df -h           # Disk space
free -m         # Memory usage
top             # Running processes
htop            # Better process viewer

# Navigation
pwd             # Current directory
ls              # List files
ls -la          # List all with details
cd ~            # Go to home
cd ..           # Go up one level
cd /path        # Go to path

# File Operations
cat file.txt    # Show file contents
nano file.txt   # Edit file (simple)
vi file.txt     # Edit file (advanced)
cp file1 file2  # Copy file
mv file1 file2  # Move/rename file
rm file.txt     # Delete file
mkdir folder    # Create folder
rmdir folder    # Delete empty folder
rm -rf folder   # Delete folder (careful!)

# File Permissions
chmod 400 file  # Read only (for keys)
chmod 644 file  # Standard file
chmod 755 file  # Executable
chown user file # Change owner

# Services
sudo systemctl start httpd      # Start service
sudo systemctl stop httpd       # Stop service
sudo systemctl restart httpd    # Restart service
sudo systemctl status httpd     # Check status
sudo systemctl enable httpd     # Auto-start on boot

# Network
curl localhost                  # Test web server
wget URL                        # Download file
ping google.com                 # Test connectivity
netstat -tulpn                  # Show open ports
ifconfig                        # Network config
```

---

## Important URLs

### **AWS Console**
```
Main Console:     https://console.aws.amazon.com
IAM:              https://console.aws.amazon.com/iam
EC2:              https://console.aws.amazon.com/ec2
S3:               https://s3.console.aws.amazon.com
RDS:              https://console.aws.amazon.com/rds
Lambda:           https://console.aws.amazon.com/lambda
CloudWatch:       https://console.aws.amazon.com/cloudwatch
Billing:          https://console.aws.amazon.com/billing
```

### **Documentation**
```
AWS Docs:         https://docs.aws.amazon.com
EC2 Guide:        https://docs.aws.amazon.com/ec2
S3 Guide:         https://docs.aws.amazon.com/s3
IAM Guide:        https://docs.aws.amazon.com/iam
CLI Reference:    https://docs.aws.amazon.com/cli
```

### **Learning & Support**
```
Free Tier:        https://aws.amazon.com/free
Skill Builder:    https://skillbuilder.aws
Training:         https://aws.amazon.com/training
Educate:          https://aws.amazon.com/education/awseducate
Forums:           https://forums.aws.amazon.com
re:Post:          https://repost.aws
YouTube:          https://www.youtube.com/c/amazonwebservices
```

### **Pricing & Tools**
```
Pricing Calc:     https://calculator.aws
Cost Management:  https://console.aws.amazon.com/cost-management
Service Health:   https://status.aws.amazon.com
Architecture:     https://aws.amazon.com/architecture
Well-Architected: https://aws.amazon.com/architecture/well-architected
```

### **Certification**
```
Certification:    https://aws.amazon.com/certification
Practice Exams:   https://explore.skillbuilder.aws/learn/signin
Exam Guide:       https://aws.amazon.com/certification/certified-cloud-practitioner
```

---

## Quick Command Reference Card

**Print this page for quick access!**

```
# Connect to EC2
ssh -i key.pem ec2-user@IP

# Update EC2
sudo yum update -y

# Install Apache
sudo yum install httpd -y
sudo systemctl start httpd

# Upload to S3
aws s3 cp file.txt s3://bucket/

# List S3
aws s3 ls s3://bucket/

# Start EC2
aws ec2 start-instances --instance-ids i-xxxxx

# Stop EC2
aws ec2 stop-instances --instance-ids i-xxxxx

# Check service
sudo systemctl status httpd

# View logs
sudo tail -f /var/log/httpd/error_log

# Edit file
sudo nano /var/www/html/index.html

# Check disk
df -h

# Check memory
free -m

# Process list
top
```

---

## Emergency Contacts & Support

### **AWS Support Tiers:**
```
Basic (Free):         7/24 customer service, forums
Developer ($29/mo):   Business hours email support
Business ($100/mo):   24/7 phone, email, chat support
Enterprise (Custom):  Dedicated TAM, < 15 min response
```

### **For Students:**
```
AWS Educate:     https://aws.amazon.com/education/awseducate
Student Support: educate-support@amazon.com
Forums:          https://forums.aws.amazon.com
Community:       https://repost.aws
```

---

## Version Control

**Last Updated:** November 2025  
**Version:** 1.0  
**For:** Diploma Computer Engineering Students

---

## Feedback

Found errors or want to suggest improvements?
- Note them down
- Share with instructor
- Help improve this guide

---

**Keep this cheat sheet handy! 📌**  
**Practice makes perfect! 💪**  
**Good luck with your AWS journey! 🚀**

---

*AWS Cloud Computing Course*  
*Complete Cheat Sheet*  
*© 2025 - For Educational Use*
