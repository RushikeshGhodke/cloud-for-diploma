# Practice Exercises - Session 1 & 2

## 🎯 Hands-On Practice for Diploma Students

---

## Table of Contents

1. [Session 1 Theory Exercises](#session-1-theory-exercises)
2. [Session 2 Practical Exercises](#session-2-practical-exercises)
3. [Mini Projects](#mini-projects)
4. [Challenge Exercises](#challenge-exercises)
5. [Solutions & Hints](#solutions--hints)

---

## Session 1 Theory Exercises

### **Exercise 1: Concept Mapping**

**Task:** Create a mind map connecting these concepts:
- Cloud Computing
- IaaS, PaaS, SaaS
- Public, Private, Hybrid
- AWS, EC2, S3

**Deliverable:** Hand-drawn or digital mind map

---

### **Exercise 2: Real-World Scenarios**

Match the correct deployment model:

1. **Scenario A:** A hospital needs to store patient medical records with strict privacy laws.
   - Answer: ________________

2. **Scenario B:** A startup wants to quickly launch a mobile app without buying servers.
   - Answer: ________________

3. **Scenario C:** An e-commerce company wants secure customer data but scalable website.
   - Answer: ________________

4. **Scenario D:** Universities in India want to share educational resources.
   - Answer: ________________

---

### **Exercise 3: Service Model Decision**

For each use case, choose IaaS, PaaS, or SaaS:

| Use Case | Model | Reason |
|----------|-------|--------|
| Host a website with full OS control | _____ | _____ |
| Use Gmail for business email | _____ | _____ |
| Deploy Node.js app quickly | _____ | _____ |
| Run data analytics on custom OS | _____ | _____ |
| Use Netflix for entertainment | _____ | _____ |

---

### **Exercise 4: Cost Calculation**

**Scenario:** A small business needs:
- 1 server running 24/7
- 50 GB storage
- 100 GB data transfer/month

**Calculate:**

**Traditional IT (Buy Server):**
- Server cost: ₹5,00,000
- Electricity: ₹2,000/month
- AC: ₹3,000/month
- IT admin: ₹25,000/month
- **Year 1 Total:** ________________

**AWS Cloud:**
- EC2 t2.micro: FREE (Free Tier)
- S3 50GB: ₹115/month
- Data transfer: ₹728/month
- **Year 1 Total:** ________________

**Savings:** ________________

---

### **Exercise 5: AWS Services Identification**

Match AWS service to its purpose:

| AWS Service | Purpose |
|-------------|---------|
| EC2 | A. Object storage |
| S3 | B. Virtual servers |
| RDS | C. NoSQL database |
| Lambda | D. Access management |
| IAM | E. Relational database |
| DynamoDB | F. Serverless functions |

**Answers:**
- EC2: _____
- S3: _____
- RDS: _____
- Lambda: _____
- IAM: _____
- DynamoDB: _____

---

## Session 2 Practical Exercises

### **Exercise 6: S3 Static Website**

**Difficulty:** ⭐ Easy  
**Time:** 15 minutes  
**Objective:** Host a personal portfolio website on S3

**Steps:**

1. **Create HTML file (index.html):**
```html
<!DOCTYPE html>
<html>
<head>
    <title>My Portfolio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 800px;
            margin: 50px auto;
            padding: 20px;
            background: #f0f0f0;
        }
        .container {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        h1 { color: #FF9900; }
        .section { margin: 20px 0; }
    </style>
</head>
<body>
    <div class="container">
        <h1>Welcome to My Portfolio</h1>
        <div class="section">
            <h2>About Me</h2>
            <p>I'm a Diploma Computer Engineering student learning AWS Cloud Computing.</p>
        </div>
        <div class="section">
            <h2>Skills</h2>
            <ul>
                <li>AWS Cloud Computing</li>
                <li>HTML/CSS</li>
                <li>JavaScript</li>
            </ul>
        </div>
        <div class="section">
            <h2>Projects</h2>
            <p>This website is hosted on Amazon S3! 🚀</p>
        </div>
        <div class="section">
            <h2>Contact</h2>
            <p>Email: your-email@example.com</p>
        </div>
    </div>
</body>
</html>
```

2. **Tasks:**
   - [ ] Create S3 bucket: `yourname-portfolio-2025`
   - [ ] Upload index.html
   - [ ] Enable static website hosting
   - [ ] Make bucket public
   - [ ] Test website URL
   - [ ] Share URL with instructor

**Submission:**
- Bucket name: ________________
- Website URL: ________________
- Screenshot of live website

---

### **Exercise 7: EC2 Web Server**

**Difficulty:** ⭐⭐ Medium  
**Time:** 20 minutes  
**Objective:** Launch EC2 and install Apache web server

**Steps:**

1. **Launch EC2 Instance:**
   - [ ] Instance type: t2.micro
   - [ ] AMI: Amazon Linux 2023
   - [ ] Key pair: Create new (save securely!)
   - [ ] Security group: Allow SSH (your IP) and HTTP (anywhere)

2. **Connect to EC2:**
   - [ ] Use EC2 Instance Connect or SSH
   - [ ] Verify connection

3. **Install Apache:**
```bash
# Update system
sudo yum update -y

# Install Apache
sudo yum install httpd -y

# Start Apache
sudo systemctl start httpd

# Enable on boot
sudo systemctl enable httpd

# Check status
sudo systemctl status httpd
```

4. **Create Custom Page:**
```bash
# Create your HTML file
sudo nano /var/www/html/index.html
```

```html
<!DOCTYPE html>
<html>
<head>
    <title>My EC2 Server</title>
</head>
<body>
    <h1>🎉 Success!</h1>
    <p>This page is served from AWS EC2!</p>
    <p>Instance ID: <strong>[Your Instance ID]</strong></p>
    <p>Region: Mumbai (ap-south-1)</p>
    <p>Created by: [Your Name]</p>
</body>
</html>
```

5. **Test:**
   - [ ] Access: http://YOUR-EC2-PUBLIC-IP
   - [ ] Verify page loads
   - [ ] Take screenshot

**Submission:**
- Instance ID: ________________
- Public IP: ________________
- Screenshot of webpage
- What challenges did you face?

---

### **Exercise 8: IAM User Management**

**Difficulty:** ⭐⭐ Medium  
**Time:** 15 minutes  
**Objective:** Create IAM users with different permissions

**Tasks:**

1. **Create Groups:**
   - [ ] Group 1: `Administrators`
      - Attach: AdministratorAccess
   - [ ] Group 2: `Developers`
      - Attach: AmazonS3FullAccess, AmazonEC2ReadOnlyAccess
   - [ ] Group 3: `ReadOnly`
      - Attach: ReadOnlyAccess

2. **Create Users:**
   - [ ] User 1: `admin-yourname` → Add to Administrators
   - [ ] User 2: `dev-yourname` → Add to Developers
   - [ ] User 3: `readonly-yourname` → Add to ReadOnly

3. **Create Custom Policy:**

**Name:** `S3-Specific-Bucket-Access`

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:ListBucket",
                "s3:GetObject"
            ],
            "Resource": [
                "arn:aws:s3:::YOUR-BUCKET-NAME",
                "arn:aws:s3:::YOUR-BUCKET-NAME/*"
            ]
        }
    ]
}
```

4. **Test:**
   - [ ] Login as each user
   - [ ] Verify permissions work correctly
   - [ ] Try accessing resources
   - [ ] Document results

**Submission:**
- Screenshot of IAM dashboard showing users/groups
- Test results for each user
- What did you learn about least privilege?

---

### **Exercise 9: S3 + EC2 Integration**

**Difficulty:** ⭐⭐⭐ Advanced  
**Time:** 30 minutes  
**Objective:** EC2 instance uploads files to S3 using IAM role

**Steps:**

1. **Create IAM Role:**
   - [ ] Name: `EC2-S3-Upload-Role`
   - [ ] Trusted entity: EC2
   - [ ] Attach policy: AmazonS3FullAccess

2. **Launch EC2 with Role:**
   - [ ] Instance type: t2.micro
   - [ ] Attach IAM role created above
   - [ ] Connect to instance

3. **Test S3 Access:**
```bash
# No access keys needed! Role provides credentials

# List S3 buckets
aws s3 ls

# Create test file
echo "Hello from EC2!" > test.txt

# Upload to S3
aws s3 cp test.txt s3://your-bucket-name/

# Verify upload
aws s3 ls s3://your-bucket-name/

# Download file
aws s3 cp s3://your-bucket-name/test.txt downloaded.txt

# Show contents
cat downloaded.txt
```

4. **Advanced Task:**
   - Create a bash script that:
     - Creates a backup of /var/log directory
     - Compresses it (tar.gz)
     - Uploads to S3 with timestamp
     - Deletes local copy

```bash
#!/bin/bash
# Save as: s3-backup.sh

TIMESTAMP=$(date +%Y%m%d-%H%M%S)
BACKUP_FILE="backup-$TIMESTAMP.tar.gz"
BUCKET_NAME="your-bucket-name"

# Create backup
sudo tar -czf $BACKUP_FILE /var/log

# Upload to S3
aws s3 cp $BACKUP_FILE s3://$BUCKET_NAME/backups/

# Delete local file
rm $BACKUP_FILE

echo "Backup completed: $BACKUP_FILE"
```

**Submission:**
- IAM role ARN: ________________
- S3 bucket name: ________________
- Screenshot of files in S3
- Bash script code
- Execution screenshot

---

## Mini Projects

### **Project 1: Personal Blog Website**

**Difficulty:** ⭐⭐ Medium  
**Time:** 45 minutes  
**Technologies:** S3, CloudFront (optional)

**Requirements:**
1. Create a multi-page blog website:
   - Home page (index.html)
   - About page (about.html)
   - Blog posts page (blog.html)
   - Contact page (contact.html)
   - Style sheet (style.css)

2. Features:
   - Navigation menu
   - Responsive design
   - Images stored in S3
   - Custom domain (optional)

3. Deployment:
   - Host on S3
   - Enable static website hosting
   - Configure custom error page
   - Make all files public

**Bonus:**
- Add CloudFront CDN
- Custom domain with Route53
- SSL certificate

**Submission:**
- GitHub repo with code
- Live website URL
- Documentation of setup steps

---

### **Project 2: Simple REST API**

**Difficulty:** ⭐⭐⭐ Advanced  
**Time:** 60 minutes  
**Technologies:** EC2, Node.js/Python

**Requirements:**

1. **Create REST API with endpoints:**
```
GET  /api/hello          → Return "Hello World"
POST /api/echo           → Echo back request body
GET  /api/time           → Return current server time
GET  /api/students       → List of students (array)
POST /api/students       → Add new student
GET  /api/students/:id   → Get student by ID
```

2. **Sample Node.js Code:**
```javascript
const express = require('express');
const app = express();
const port = 3000;

app.use(express.json());

let students = [
    { id: 1, name: "Raj", course: "Diploma" },
    { id: 2, name: "Priya", course: "Engineering" }
];

// GET /api/hello
app.get('/api/hello', (req, res) => {
    res.json({ message: "Hello World from EC2!" });
});

// GET /api/time
app.get('/api/time', (req, res) => {
    res.json({ 
        time: new Date().toISOString(),
        timezone: "Asia/Kolkata"
    });
});

// GET /api/students
app.get('/api/students', (req, res) => {
    res.json(students);
});

// POST /api/students
app.post('/api/students', (req, res) => {
    const newStudent = {
        id: students.length + 1,
        name: req.body.name,
        course: req.body.course
    };
    students.push(newStudent);
    res.status(201).json(newStudent);
});

// GET /api/students/:id
app.get('/api/students/:id', (req, res) => {
    const student = students.find(s => s.id === parseInt(req.params.id));
    if (!student) {
        return res.status(404).json({ error: "Student not found" });
    }
    res.json(student);
});

app.listen(port, () => {
    console.log(`API running on port ${port}`);
});
```

3. **Deployment Steps:**
   - Launch EC2 (t2.micro)
   - Install Node.js
   - Upload code
   - Configure security group (port 3000)
   - Test all endpoints

**Submission:**
- API base URL: ________________
- Test all endpoints with Postman/curl
- Screenshots of responses
- Code repository

---

### **Project 3: File Upload System**

**Difficulty:** ⭐⭐⭐ Advanced  
**Time:** 90 minutes  
**Technologies:** EC2, S3, Node.js

**Requirements:**

1. **Web interface for file uploads:**
   - Upload form (HTML)
   - File selection
   - Upload progress
   - Success/error messages

2. **Backend functionality:**
   - Receive file upload
   - Validate file (size, type)
   - Upload to S3
   - Return S3 URL
   - List all uploaded files

3. **Features:**
   - Only allow images (jpg, png)
   - Max size: 5 MB
   - Generate thumbnails
   - Store metadata in JSON file

**Sample Frontend (index.html):**
```html
<!DOCTYPE html>
<html>
<head>
    <title>File Upload System</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
        }
        .upload-form {
            border: 2px dashed #ccc;
            padding: 30px;
            text-align: center;
            border-radius: 10px;
        }
        .btn {
            background: #FF9900;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .file-list {
            margin-top: 30px;
        }
        .file-item {
            padding: 10px;
            border: 1px solid #ddd;
            margin: 5px 0;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <h1>📤 File Upload System</h1>
    
    <div class="upload-form">
        <h2>Upload Image</h2>
        <input type="file" id="fileInput" accept="image/*">
        <br><br>
        <button class="btn" onclick="uploadFile()">Upload</button>
        <p id="status"></p>
    </div>

    <div class="file-list">
        <h2>Uploaded Files</h2>
        <div id="fileList"></div>
    </div>

    <script>
        async function uploadFile() {
            const fileInput = document.getElementById('fileInput');
            const status = document.getElementById('status');
            
            if (!fileInput.files[0]) {
                status.textContent = 'Please select a file';
                return;
            }

            const formData = new FormData();
            formData.append('file', fileInput.files[0]);

            status.textContent = 'Uploading...';

            try {
                const response = await fetch('/upload', {
                    method: 'POST',
                    body: formData
                });

                const result = await response.json();
                
                if (response.ok) {
                    status.textContent = '✅ Upload successful!';
                    loadFiles();
                } else {
                    status.textContent = '❌ Upload failed: ' + result.error;
                }
            } catch (error) {
                status.textContent = '❌ Error: ' + error.message;
            }
        }

        async function loadFiles() {
            const response = await fetch('/files');
            const files = await response.json();
            
            const fileList = document.getElementById('fileList');
            fileList.innerHTML = files.map(file => `
                <div class="file-item">
                    <strong>${file.name}</strong><br>
                    <small>${file.size} bytes | ${file.date}</small><br>
                    <a href="${file.url}" target="_blank">View</a>
                </div>
            `).join('');
        }

        // Load files on page load
        loadFiles();
    </script>
</body>
</html>
```

**Submission:**
- Working web application URL
- Source code repository
- List of uploaded files
- Documentation

---

## Challenge Exercises

### **Challenge 1: Auto-Scaling Setup**

**Difficulty:** ⭐⭐⭐⭐ Expert  
**Objective:** Set up auto-scaling based on CPU usage

**Requirements:**
1. Create launch template
2. Configure auto-scaling group
3. Set scaling policies
4. Generate load to test
5. Monitor CloudWatch metrics

---

### **Challenge 2: Multi-Tier Application**

**Difficulty:** ⭐⭐⭐⭐ Expert  
**Objective:** Deploy full-stack application

**Architecture:**
```
Frontend (S3) 
    ↓
API (EC2 + Load Balancer)
    ↓
Database (RDS)
```

**Requirements:**
1. React/Vue.js frontend on S3
2. Node.js/Python API on EC2
3. MySQL/PostgreSQL on RDS
4. Application Load Balancer
5. IAM roles for security
6. CloudWatch monitoring

---

### **Challenge 3: Serverless Application**

**Difficulty:** ⭐⭐⭐⭐ Expert  
**Objective:** Build serverless image processing app

**Technologies:**
- S3 (storage)
- Lambda (processing)
- DynamoDB (metadata)
- API Gateway (REST API)

**Functionality:**
1. Upload image to S3
2. Lambda triggers automatically
3. Create thumbnail
4. Store metadata in DynamoDB
5. Return processed image URL

---

## Solutions & Hints

### **Exercise 2 Solutions:**
1. **Hospital:** Private Cloud (security & compliance)
2. **Startup:** Public Cloud (low cost, quick start)
3. **E-commerce:** Hybrid Cloud (secure data + scalable web)
4. **Universities:** Community Cloud (shared resources)

---

### **Exercise 3 Solutions:**

| Use Case | Model | Reason |
|----------|-------|--------|
| Host website with OS control | IaaS | Need OS access (EC2) |
| Gmail for business | SaaS | Ready-to-use email service |
| Deploy Node.js quickly | PaaS | Platform handles infrastructure |
| Data analytics custom OS | IaaS | Custom OS requirement |
| Netflix entertainment | SaaS | Consumer application |

---

### **Exercise 5 Solutions:**
- EC2: B (Virtual servers)
- S3: A (Object storage)
- RDS: E (Relational database)
- Lambda: F (Serverless functions)
- IAM: D (Access management)
- DynamoDB: C (NoSQL database)

---

### **Common Mistakes to Avoid:**

1. **S3 Website Hosting:**
   - ❌ Not disabling "Block all public access"
   - ❌ Forgetting bucket policy
   - ❌ Using HTTPS instead of HTTP

2. **EC2 Connection:**
   - ❌ Wrong key file permissions
   - ❌ Using wrong username
   - ❌ Security group not allowing SSH

3. **IAM:**
   - ❌ Giving too many permissions
   - ❌ Using root account for daily work
   - ❌ Not testing permissions

4. **Cost Management:**
   - ❌ Forgetting to stop EC2
   - ❌ Not setting billing alerts
   - ❌ Using wrong instance type

---

## Submission Guidelines

### **For Each Exercise:**

1. **Documentation:**
   - Step-by-step what you did
   - Screenshots of key steps
   - Challenges faced
   - How you solved them

2. **Code:**
   - Well-commented
   - GitHub repository
   - README file with instructions

3. **Testing:**
   - Proof that it works
   - Test results
   - URLs/endpoints

4. **Clean Up:**
   - Stop/terminate resources
   - Document cleanup steps
   - Final cost report

---

## Grading Rubric

| Criteria | Points |
|----------|--------|
| **Functionality** | 40% |
| Code works as expected | |
| All requirements met | |
| **Documentation** | 25% |
| Clear steps | |
| Screenshots | |
| **Code Quality** | 20% |
| Clean code | |
| Comments | |
| **Best Practices** | 15% |
| Security | |
| Cost optimization | |

---

## Additional Practice

### **Daily Practice (15 minutes):**
- Day 1: Create S3 bucket, upload files
- Day 2: Launch EC2, connect via SSH
- Day 3: Install web server on EC2
- Day 4: Create IAM users and groups
- Day 5: Review and clean up

### **Weekly Challenge:**
- Build one mini project each week
- Document everything
- Share with classmates
- Get feedback

---

## Resources for Practice

### **Sample Datasets:**
- [Public AWS Datasets](https://registry.opendata.aws/)
- [GitHub Sample Projects](https://github.com/topics/aws)

### **Practice Platforms:**
- [AWS Skill Builder](https://skillbuilder.aws/)
- [A Cloud Guru Hands-On Labs](https://acloudguru.com/)
- [Qwiklabs AWS](https://www.qwiklabs.com/)

---

**Good luck with your practice! 🚀**

**Remember:**
- Start with easy exercises
- Move to advanced gradually
- Don't skip fundamentals
- Practice daily
- Learn from mistakes
- Help others

---

*AWS Cloud Computing Course*  
*Practice Exercises*  
*Version 1.0 - November 2025*
