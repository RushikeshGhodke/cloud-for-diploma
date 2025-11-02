# Session 2: AWS Core Services

## Hands-on AWS Console & Services (90 minutes)

---

## 📋 Session Overview

**Duration:** 90 minutes  
**Prerequisites:** Session 1 completed  
**Objective:** Learn and practice AWS core services  
**Mode:** Theory + Live Demonstrations

---

## 🎯 Learning Outcomes

By the end of this session, students will be able to:
- ✅ Create and navigate AWS account
- ✅ Create and manage S3 buckets
- ✅ Launch and connect to EC2 instances
- ✅ Configure IAM users and permissions
- ✅ Set up security groups
- ✅ Understand AWS Free Tier

---

## 📚 Table of Contents

1. [AWS Account & Console](#1-aws-account--console)
2. [Amazon S3 - Simple Storage Service](#2-amazon-s3---simple-storage-service)
3. [Amazon EC2 - Elastic Compute Cloud](#3-amazon-ec2---elastic-compute-cloud)
4. [AWS IAM - Identity & Access Management](#4-aws-iam---identity--access-management)
5. [Other Important Services](#5-other-important-services)
6. [Session Summary](#session-2-summary)
7. [Practice Exercises](#practice-exercises)

---

**[Due to length, Session 2 content is split into multiple files]**

## Quick Navigation:

- **[AWS Account Setup](./02-AWS-Console-Guide.md)** - Creating account, Free Tier, Console navigation
- **[Amazon S3 Hands-On](./03-S3-Hands-On.md)** - Complete S3 tutorial with examples
- **[Amazon EC2 Hands-On](./04-EC2-Hands-On.md)** - EC2 launch, connect, management
- **[AWS IAM Hands-On](./05-IAM-Hands-On.md)** - Users, groups, policies, roles
- **[Practice Exercises](./06-Practice-Exercises.md)** - Hands-on exercises

---

## Session 2 Structure

### **Part 1: AWS Account & Console (15 minutes)**
- Creating AWS account step-by-step
- Understanding Free Tier limits
- Setting up billing alerts
- Navigating AWS Console
- Understanding regions and availability zones

### **Part 2: Amazon S3 (20 minutes)**
- What is S3?
- Creating buckets
- Uploading files
- Making files public
- Hosting static websites
- S3 pricing and best practices

### **Part 3: Amazon EC2 (30 minutes)**
- What is EC2?
- Instance types
- Launching EC2 instance
- Connecting via SSH
- Installing web server
- Managing instance states
- Security groups

### **Part 4: AWS IAM (20 minutes)**
- What is IAM?
- Creating users
- Creating groups
- Attaching policies
- Creating custom policies
- IAM roles for services
- Best practices

### **Part 5: Other Services (5 minutes)**
- Lambda overview
- RDS overview
- DynamoDB overview
- CloudWatch overview
- Elastic Beanstalk overview

---

## 🎯 Hands-On Labs

### **Lab 1: Create Your First S3 Bucket**
**Time:** 5 minutes  
**Objective:** Store and access files in cloud

**Steps:**
1. Navigate to S3
2. Create bucket with unique name
3. Upload a file
4. Make file public
5. Access via URL

---

### **Lab 2: Launch Your First EC2 Instance**
**Time:** 10 minutes  
**Objective:** Create a virtual server

**Steps:**
1. Navigate to EC2
2. Launch t2.micro instance
3. Create key pair
4. Configure security group
5. Connect via SSH
6. Run basic commands

---

### **Lab 3: Create IAM User**
**Time:** 5 minutes  
**Objective:** Set up secure access

**Steps:**
1. Navigate to IAM
2. Create user with console access
3. Add to group or attach policy
4. Save credentials
5. Test login

---

### **Lab 4: Host Static Website on S3**
**Time:** 10 minutes  
**Objective:** Deploy a live website

**Steps:**
1. Create S3 bucket
2. Upload HTML/CSS files
3. Enable static website hosting
4. Configure bucket policy
5. Access website via URL

---

### **Lab 5: Install Web Server on EC2**
**Time:** 10 minutes  
**Objective:** Run Apache web server

**Steps:**
1. Connect to EC2
2. Update system
3. Install Apache
4. Create custom HTML page
5. Access via public IP

---

## ⚠️ Important Reminders

### **Before Starting:**
- [ ] Have credit/debit card ready
- [ ] Valid email address
- [ ] Stable internet connection
- [ ] Laptop/computer ready
- [ ] Note-taking materials

### **During Labs:**
- [ ] Always check region (Mumbai preferred)
- [ ] Use t2.micro for Free Tier
- [ ] Save all credentials securely
- [ ] Note down resource IDs
- [ ] Stop/delete resources when done

### **After Session:**
- [ ] Review billing dashboard
- [ ] Stop all running EC2 instances
- [ ] Delete unnecessary S3 objects
- [ ] Complete practice exercises
- [ ] Prepare for Session 3

---

## 💰 Cost Management

### **Free Tier Services (12 Months):**
```
EC2:           750 hours/month (t2.micro)
S3:            5 GB storage
RDS:           750 hours/month
Data Transfer: 15 GB outbound
```

### **Always Free Services:**
```
Lambda:        1 million requests/month
DynamoDB:      25 GB storage
CloudWatch:    10 metrics
```

### **Estimated Costs for This Session:**
```
If using Free Tier:        ₹0 (FREE)
If exceeding limits:       ₹50-100 max
```

### **Cost Saving Tips:**
- ✅ Always use t2.micro for EC2
- ✅ Stop EC2 when not using
- ✅ Delete old S3 files
- ✅ Set billing alerts
- ✅ Monitor usage regularly

---

## 🛠️ Required Tools

### **For All Students:**
1. **Web Browser** - Chrome/Firefox (latest)
2. **AWS Account** - Created during session
3. **Text Editor** - Notepad/VS Code

### **For EC2 Connection:**

**Windows Users:**
- Option 1: PuTTY (download from putty.org)
- Option 2: Windows Terminal (built-in)
- Option 3: EC2 Instance Connect (browser-based) ⭐ Easiest

**Mac/Linux Users:**
- Terminal (built-in)
- SSH (pre-installed)

---

## 📝 Session 2 Checklist

### **AWS Account:**
- [ ] Account created successfully
- [ ] Credit card verified (₹2 charge)
- [ ] Billing alerts configured
- [ ] Console login working
- [ ] Region set to Mumbai (ap-south-1)

### **Amazon S3:**
- [ ] First bucket created
- [ ] File uploaded to S3
- [ ] File made public
- [ ] Static website hosted
- [ ] Understand S3 pricing

### **Amazon EC2:**
- [ ] EC2 instance launched
- [ ] Key pair downloaded safely
- [ ] Connected via SSH
- [ ] Security group configured
- [ ] Web server installed
- [ ] Instance stopped/terminated

### **AWS IAM:**
- [ ] IAM user created
- [ ] IAM group created
- [ ] Policy attached
- [ ] Custom policy created
- [ ] IAM role created
- [ ] Best practices understood

---

## 🎯 Learning Objectives Checklist

After this session, I can:

- [ ] Explain what each service does
- [ ] Create resources independently
- [ ] Navigate AWS Console confidently
- [ ] Manage costs effectively
- [ ] Troubleshoot common issues
- [ ] Follow security best practices
- [ ] Connect services together
- [ ] Deploy simple applications

---

## 🚀 Next Steps

**After completing Session 2:**

1. **Practice Labs** (30 minutes)
   - Repeat all demos yourself
   - Try variations
   - Document your steps

2. **Complete Exercises** (60 minutes)
   - Work through practice problems
   - Build sample projects
   - Test your understanding

3. **Prepare for Session 3** (Projects)
   - Review Session 1 & 2 notes
   - Have project ideas ready
   - Set up development environment

---

## 📚 Quick Reference Links

**AWS Console:**
- Main Console: https://console.aws.amazon.com
- S3 Console: https://s3.console.aws.amazon.com
- EC2 Console: https://console.aws.amazon.com/ec2
- IAM Console: https://console.aws.amazon.com/iam

**Documentation:**
- [S3 User Guide](https://docs.aws.amazon.com/s3/)
- [EC2 User Guide](https://docs.aws.amazon.com/ec2/)
- [IAM User Guide](https://docs.aws.amazon.com/iam/)

**Support:**
- [AWS Free Tier](https://aws.amazon.com/free/)
- [AWS Forums](https://forums.aws.amazon.com/)
- [AWS re:Post](https://repost.aws/)

---

## 🎓 Session 3 Preview

**Next Session: Hands-on Projects (120 minutes)**

**Projects We'll Build:**

1. **Portfolio Website** (S3 + CloudFront)
   - HTML/CSS/JavaScript
   - Custom domain (optional)
   - SSL certificate

2. **Dynamic Web App** (EC2 + Node.js)
   - REST API
   - Database integration
   - File upload feature

3. **Full-Stack Application** (EC2 + S3 + RDS)
   - Frontend on S3
   - Backend on EC2
   - Database on RDS

4. **Real-Time Chat App** (EC2 + WebSocket)
   - Socket.io integration
   - User authentication
   - Message persistence

5. **Image Processing App** (Lambda + S3)
   - Automatic image resize
   - Thumbnail generation
   - Serverless architecture

**Get excited! 🎉**

---

## 💡 Tips for Success

### **During Session:**
- ✅ Follow along with instructor
- ✅ Take screenshots of important steps
- ✅ Note down all resource IDs
- ✅ Ask questions immediately
- ✅ Help your classmates

### **After Session:**
- ✅ Review all notes same day
- ✅ Practice all demos again
- ✅ Complete homework exercises
- ✅ Clean up AWS resources
- ✅ Monitor billing dashboard

### **Best Practices:**
- ✅ Always use meaningful names
- ✅ Add tags to all resources
- ✅ Document your configurations
- ✅ Keep credentials secure
- ✅ Stop/delete when not using

---

## ❓ Common Questions

**Q1: Do I really need a credit card?**  
**A:** Yes, for identity verification. AWS charges ₹2 for verification (refunded).

**Q2: Will I be charged automatically?**  
**A:** No, only if you exceed Free Tier limits. Set billing alerts!

**Q3: What if I exceed Free Tier?**  
**A:** You'll be charged only for excess usage. Monitor regularly.

**Q4: Can I use debit card?**  
**A:** Yes, if international transactions are enabled.

**Q5: How long does account activation take?**  
**A:** Usually instant, maximum 24 hours.

**Q6: Can I delete my account later?**  
**A:** Yes, anytime from account settings.

**Q7: What if I forget to stop EC2?**  
**A:** You'll be charged. Always set billing alerts!

**Q8: Can I switch regions later?**  
**A:** Yes, but resources are region-specific.

**Q9: Is Free Tier really free?**  
**A:** Yes, within limits. Monitor usage carefully.

**Q10: What happens after 12 months?**  
**A:** Standard pricing applies. Plan accordingly.

---

## 📊 Progress Tracker

Track your Session 2 progress:

```
Module 1: AWS Account     [░░░░░] 0%
Module 2: Amazon S3       [░░░░░] 0%
Module 3: Amazon EC2      [░░░░░] 0%
Module 4: AWS IAM         [░░░░░] 0%
Module 5: Other Services  [░░░░░] 0%
Lab Exercises             [░░░░░] 0%

Overall Session 2:        [░░░░░] 0%
```

Update as you complete each module!

---

## 🎉 Congratulations!

You're about to start hands-on AWS learning!

**Remember:**
- 💪 Practice makes perfect
- 🤔 It's okay to make mistakes
- 🙋 Ask questions
- 🤝 Help others
- 🎯 Stay within Free Tier

**Let's get started! 🚀**

---

**Continue to Detailed Modules:**
- → [02-AWS-Console-Guide.md](./02-AWS-Console-Guide.md)
- → [03-S3-Hands-On.md](./03-S3-Hands-On.md)
- → [04-EC2-Hands-On.md](./04-EC2-Hands-On.md)
- → [05-IAM-Hands-On.md](./05-IAM-Hands-On.md)
- → [06-Practice-Exercises.md](./06-Practice-Exercises.md)

---

*End of Session 2 Overview*

*Total Duration: 90 minutes*  
*Prerequisite: Session 1*  
*Next: Session 3 - Hands-on Projects*

---

*Last Updated: November 2025*  
*Version: 1.0*  
*For: Diploma Computer Engineering Students*
