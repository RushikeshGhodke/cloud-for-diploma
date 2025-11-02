# Session 1: Quick Reference Guide

## 🚀 Quick Revision Cheat Sheet

---

## Cloud Computing Basics

### **What is Cloud Computing?**
> Using internet-based servers to store data and run applications - pay only for what you use

### **5 Key Characteristics:**
1. **On-Demand Self-Service** - Get resources instantly (24/7)
2. **Broad Network Access** - Access from anywhere, any device
3. **Resource Pooling** - Shared infrastructure, multiple customers
4. **Rapid Elasticity** - Scale up/down instantly
5. **Measured Service** - Pay-per-use (like electricity meter)

---

## Service Models (IaaS, PaaS, SaaS)

### **Quick Comparison:**

| Model | You Manage | Provider Manages | Example | Use Case |
|-------|------------|------------------|---------|----------|
| **IaaS** | OS, Apps, Data | Infrastructure | AWS EC2 | Servers, Storage |
| **PaaS** | Apps, Data | OS + Infrastructure | Heroku | App Development |
| **SaaS** | Just use it | Everything | Gmail | End Users |

### **Pizza Analogy:**
- **IaaS** = Take & Bake (kitchen provided, you cook)
- **PaaS** = Pizza Delivery (just eat)
- **SaaS** = Dine at Restaurant (full service)

---

## Deployment Models

### **4 Types:**

| Model | Description | Best For | Example |
|-------|-------------|----------|---------|
| **Public** | Shared, Internet | Startups | AWS, Azure |
| **Private** | Dedicated, Secure | Banks | Own Data Center |
| **Hybrid** | Public + Private | Enterprises | E-commerce |
| **Community** | Shared by group | Universities | NPTEL |

### **Quick Decision Tree:**
```
Sensitive data? 
  └─ No → Public Cloud ✅
  └─ Yes → Afford private?
      └─ Yes → Private Cloud ✅
      └─ No → Hybrid Cloud ✅
```

---

## AWS Quick Facts

### **Market Share (2024):**
- 🥇 AWS: **32%** (Leader)
- 🥈 Azure: 23%
- 🥉 Google Cloud: 10%

### **Why AWS?**
- ✅ First mover (2006)
- ✅ 200+ services
- ✅ Global leader
- ✅ Best for jobs
- ✅ Free Tier available

### **Free Tier Highlights:**
```
EC2:    750 hrs/month (12 months)
S3:     5 GB storage (12 months)
Lambda: 1M requests (Always free)
```

### **AWS India Regions:**
- 🇮🇳 **Mumbai** (ap-south-1) ⭐ Use this
- 🇮🇳 Hyderabad (ap-south-2)

---

## Key Formulas & Concepts

### **Cloud Cost Savings:**
```
Traditional: ₹5,00,000 (server) + ₹33,000/month (maintenance)
Cloud:       ₹2,000/month

Annual Savings: ₹8,76,000+ 💰
```

### **Responsibility Matrix:**
```
        Traditional | IaaS     | PaaS     | SaaS
Apps    You         | You      | You      | Provider
OS      You         | You      | Provider | Provider
Servers You         | Provider | Provider | Provider
```

---

## Practice Questions - Quick Answers

**Q: Which is NOT a cloud service model?**  
**A:** DaaS ✅ (Only IaaS, PaaS, SaaS exist)

**Q: Best deployment for bank?**  
**A:** Private Cloud ✅ (Security & compliance)

**Q: EC2 is which model?**  
**A:** IaaS ✅ (Infrastructure as a Service)

**Q: Main benefit of cloud?**  
**A:** Pay-as-you-go ✅ (No upfront cost)

**Q: Largest cloud provider?**  
**A:** AWS ✅ (32% market share)

---

## Common Terms - Glossary

| Term | Definition |
|------|------------|
| **Cloud** | Internet-based computing services |
| **IaaS** | Rent infrastructure (servers, storage) |
| **PaaS** | Platform for app development |
| **SaaS** | Ready-to-use software |
| **Public Cloud** | Shared infrastructure (AWS, Azure) |
| **Private Cloud** | Dedicated infrastructure |
| **Hybrid Cloud** | Mix of public + private |
| **EC2** | AWS virtual servers |
| **S3** | AWS storage service |
| **Free Tier** | AWS free usage limits |
| **Region** | Geographic location of data centers |

---

## Important Numbers

### **Durability & Availability:**
- S3 Durability: **99.999999999%** (11 nines)
- S3 Availability: 99.99%

### **AWS Scale:**
- **200+** services
- **30+** regions worldwide
- **99+** availability zones
- Launched: **2006**

### **Job Market (India):**
- Without AWS: ₹3-5 LPA
- With AWS: ₹6-12 LPA ⬆️
- Certified: ₹8-15 LPA ⬆️⬆️

---

## Study Tips

### **For Theory Exam:**
1. Remember 5 characteristics of cloud
2. Understand service models (pizza analogy)
3. Know deployment model differences
4. AWS market leadership facts
5. Free Tier benefits

### **For Practical:**
1. Practice AWS Console navigation
2. Create S3 bucket
3. Launch EC2 instance
4. Create IAM user
5. Follow hands-on labs

### **Memorization Tricks:**

**5 Characteristics (OBRRE):**
- **O**n-demand
- **B**road access
- **R**esource pooling
- **R**apid elasticity
- **E**conomy (measured service)

**Service Models (IPS):**
- **I**nfrastructure (IaaS)
- **P**latform (PaaS)
- **S**oftware (SaaS)

**Deployment Models (PPHC):**
- **P**ublic
- **P**rivate
- **H**ybrid
- **C**ommunity

---

## 1-Minute Revision

**Cloud Computing:**
- Internet-based computing
- Pay-as-you-go
- 5 characteristics: On-demand, Broad access, Resource pooling, Elasticity, Measured

**Service Models:**
- IaaS = Infrastructure (EC2)
- PaaS = Platform (Elastic Beanstalk)
- SaaS = Software (Gmail)

**Deployment:**
- Public = Shared (AWS)
- Private = Dedicated (Banks)
- Hybrid = Both (Enterprises)
- Community = Group (Universities)

**AWS:**
- Leader (32%)
- 200+ services
- Free Tier available
- Best for career

---

## Exam Tips

### **Multiple Choice Strategy:**
- Read question twice
- Eliminate wrong answers
- Look for keywords
- AWS-specific: remember facts

### **Short Answer Strategy:**
- Define term first
- Give example
- Explain benefit
- Keep concise

### **Long Answer Strategy:**
- Introduction (definition)
- Explanation (details)
- Examples (real-world)
- Comparison (if asked)
- Conclusion (summary)

---

## Quick Practice Test

**Test yourself (2 minutes):**

1. What is cloud computing? (1 line)
2. Name 3 service models
3. Which deployment for banks?
4. AWS market share?
5. What is Free Tier?

**Answers:**
1. Internet-based computing, pay-per-use
2. IaaS, PaaS, SaaS
3. Private Cloud
4. 32% (largest)
5. Free AWS usage limits (12 months)

**Score:**
- 5/5: Excellent! ⭐⭐⭐
- 3-4/5: Good, review once 👍
- 0-2/5: Study again 📚

---

## Important Links

### **AWS Resources:**
- Console: https://console.aws.amazon.com
- Free Tier: https://aws.amazon.com/free/
- Pricing: https://aws.amazon.com/pricing/

### **Learning:**
- AWS Skill Builder: https://skillbuilder.aws/
- Documentation: https://docs.aws.amazon.com/
- YouTube: AWS Official Channel

---

## Before Session 2

### **Checklist:**
- [ ] Understand all Session 1 concepts
- [ ] Can explain service models
- [ ] Know deployment models
- [ ] AWS Free Tier benefits clear
- [ ] Have credit/debit card ready
- [ ] Email for AWS account ready

### **Homework:**
- [ ] Complete practice questions
- [ ] Watch AWS intro video
- [ ] Read Free Tier documentation
- [ ] Prepare questions for next session

---

## Quick Contact

**Need Help?**
- Ask instructor in class
- Check AWS documentation
- AWS Forums: forums.aws.amazon.com
- Reddit: r/aws

---

**Print this page for quick revision! 📄**

---

*Session 1 Quick Reference*  
*Version 1.0*  
*Last Updated: November 2025*
