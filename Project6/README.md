
# AWS Serverless S3 Upload Notification using Lambda & SNS 📨

In this mini-project, I built a **serverless notification system** that triggers an email alert every time a file is uploaded to an S3 bucket using **AWS Lambda** and **Amazon SNS**.

---

## 🔹 1. Created an S3 Bucket
- **Bucket Name:** `img-15`  
- Purpose: Storing uploaded files (e.g., images)

---

## 🔹 2. Created a Lambda Function
- **Function Name:** `myfunction`  
- **Trigger:** S3 Event - *All object create events*

---

## 🔹 3. Set Up SNS Topic
- **Topic Name:** `mytopic`  
- **Subscription:** Email 📩  
- Confirmed the subscription via email link

---

## 🔹 4. Connected SNS as Lambda Destination
- Set SNS topic as Lambda's **destination on success**
- Provided **Destination ARN** during setup

---

## 🔹 5. Testing the Workflow
- Uploaded an image to the S3 bucket
- Lambda function was triggered successfully
- SNS sent a notification email with event details:
  - File name
  - Timestamp
  - Bucket information

---

## ✅ Result
A **serverless event-driven notification system** was successfully implemented using core AWS services **without managing any servers!**
