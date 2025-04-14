# 🚀 Auto Scaling Architecture with Instance Refresh on AWS

## 🔧 Step-by-Step Setup

### 1. Create a Custom AMI
- Launched an EC2 instance with a pre-installed web server and application (basic HTML template).
- Configured the application and then created a **Custom AMI** from this instance to reuse for scaling.
  ![](./images/1.png)

### 2. Build a Launch Template
- Created a **Launch Template** using the above AMI.
- This template includes instance type, AMI ID, key pair, security groups, and other settings needed for launching new instances.

### 3. Set Up Elastic Load Balancer (ELB)
- Created an **Application Load Balancer (ALB)**.
- Set up a **Target Group** to manage backend EC2 instances.
- Configured listeners on port 80 (HTTP) to forward traffic to the Target Group.

### 4. Configure Auto Scaling Group (ASG)
- Used the Launch Template to configure an ASG.
- Set the **Desired Capacity to 2**, **Maximum to 3**, and **Minimum to 1**.
- Registered the Target Group so new instances are automatically added.
- Enabled **Instance Refresh** for zero-downtime updates.

---

## 🧪 Load Testing and Scaling Behavior

- Connected to two EC2 instances via **SSH using PowerShell**.
- Manually applied CPU stress to simulate high load.
- Observed that when CPU crossed threshold, **Auto Scaling launched a third instance** automatically.
- This showed that scaling policy works as expected!

---

## 🔁 Instance Refresh for Smooth Updates

To simulate a real-world update (e.g., app or config change):

1. **Updated Launch Template** with new version (e.g., changed HTML content).
2. **Triggered Instance Refresh** with **50% batch size**.
3. AWS gracefully terminated 1 instance and launched a new one using updated template.
4. After replacement, reloaded the browser — the **new app version was live** without any downtime.

---

## ✅ Final Outcome

- Web application scaled based on load automatically.
- Instance Refresh allowed safe updates without service interruption.
- Real-time, hands-on understanding of scaling, updating, and AWS orchestration.

---

## 📌 Key Learnings

- Launch Templates and AMIs make deployments consistent and reusable.
- Auto Scaling ensures high availability and performance during traffic spikes.
- Instance Refresh enables rolling updates without disturbing running apps.
- Combining ELB, ASG, and monitoring offers robust cloud-native architecture.

---

## 🧰 Tools Used

- AWS EC2
- AWS Load Balancer
- Auto Scaling Group
- PowerShell SSH
- Stress Testing via CPU Load
- Markdown for documentation

---
