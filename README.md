# AWS 3-Tier Terraform Production
> **Automated provisioning of a highly available, secure, and scalable AWS ecosystem.**

---

## 🏗️ Architecture Overview
The system follows a classic 3-Tier Architecture pattern, decoupled for maximum security and performance.

<p align="center">
  <img src="https://github.com/user-attachments/assets/215214bd-dde9-4014-834d-9c9af3938057" alt="Architecture Diagram" width="800">
</p>

* **Edge/Frontend Tier:** Global content delivery via **Amazon CloudFront** integrated with **S3** for static asset hosting.
* **Application Tier:** Logic processed by **EC2** instances within an **Auto Scaling Group (ASG)**, managed by an **ALB**.
* **Database Tier:** Persistent storage via **Amazon RDS (MySQL)** isolated in a private subnet.

---

## 📊 Key Learnings & Takeaways
* **State Management:** Handled complex resource dependencies and state locking to prevent deployment conflicts.
* **Drift Resolution:** Debugged and resolved **AWS STS authentication failures** caused by local environment clock drift.
* **Security Hardening:** Implemented modern **Origin Access Control (OAC)** for S3, replacing legacy OAI methods.
* **IaC Best Practices:** Transitioned from monolithic scripts to a structured, modular-ready HCL configuration.

---

## 🚀 Getting Started (New Users)

### 1. Prerequisites
* [Terraform](https://www.terraform.io/downloads) installed locally.
* AWS CLI configured with `AdministratorAccess`.

### 2. Deployment Steps
```bash
# Clone the repository
git clone [https://github.com/Mohammadakhil/aws-3tier-terraform-production.git](https://github.com/Mohammadakhil/aws-3tier-terraform-production.git)
cd aws-3tier-terraform-production

# Initialize Terraform providers
terraform init

# Deploy the infrastructure
terraform apply
