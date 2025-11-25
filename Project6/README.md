
# =>AWS Serverless S3 Upload Notification using Lambda & SNS 📨

<br>
---
In this mini-project, I built a **serverless notification system** that triggers an email alert every time a file is uploaded to an S3 bucket using **AWS Lambda** and **Amazon SNS**.

---

## 🔹 1. Created an S3 Bucket
- **Bucket Name:** `img-15`  
- Purpose: Storing uploaded files (e.g., images)

---
<img width="1577" height="647" alt="addingTriiger" src="https://github.com/user-attachments/assets/d2ecd76a-42c0-409f-b523-d8b89e05a41e" />


## 🔹 2. Created a Lambda Function
- **Function Name:** `myfunction`  
- **Trigger:** S3 Event - *All object create events*

<img width="830" height="412" alt="confirmSub" src="https://github.com/user-attachments/assets/ed50b825-0b3b-4316-a327-defb3f2dfbe3" />

<img width="1920" height="517" alt="createdBucket" src="https://github.com/user-attachments/assets/3ac5ed2d-140b-40e2-b606-00ab2983a787" />

---


## 🔹 3. Set Up SNS Topic
- **Topic Name:** `mytopic`  
- **Subscription:** Email 📩  
- Confirmed the subscription via email link

<img width="1439" height="718" alt="createdDestination" src="https://github.com/user-attachments/assets/906ef180-ac53-4b3f-be56-47089ee38704" />

<img width="1622" height="829" alt="creatingLambda" src="https://github.com/user-attachments/assets/f935a70d-b5f5-4fc0-8000-df69d9f951fb" />




---


## 🔹 4. Connected SNS as Lambda Destination
- Set SNS topic as Lambda's **destination on success**
- Provided **Destination ARN** during setup

<img width="1276" height="470" alt="creatingSub" src="https://github.com/user-attachments/assets/3ffa8ef9-b5cf-40cf-8ae6-92cd9de4c89c" />


<img width="1200" height="507" alt="destinationAdded" src="https://github.com/user-attachments/assets/eed32ced-2a58-4904-8230-e558abd3f1d8" />

---

## 🔹 5. Testing the Workflow
- Uploaded an image to the S3 bucket
- Lambda function was triggered successfully
- SNS sent a notification email with event details:
  - File name
  - Timestamp
  - Bucket information

![edit](https://github.com/user-attachments/assets/801b7375-127c-44e0-accf-a164cf06f134)

<img width="932" height="710" alt="emailPopup" src="https://github.com/user-attachments/assets/7f776461-31ed-433a-8980-666f9cfe8945" />

<img width="1914" height="655" alt="imageUploaded" src="https://github.com/user-attachments/assets/b93d3b7c-03aa-42c4-99b8-df96213993ad" />

<img width="1874" height="596" alt="lambdaCreated" src="https://github.com/user-attachments/assets/03d7e68c-5fd8-458e-9849-3ebacc7307ac" />

<img width="275" height="183" alt="sns" src="https://github.com/user-attachments/assets/e4e5f61b-7e45-40e5-bf02-3ba4c5edaeb3" />

<img width="1305" height="540" alt="snsCreatingTopic" src="https://github.com/user-attachments/assets/c7888f79-1f2b-4740-9a4d-113dd74f5158" />
<img width="1108" height="496" alt="triggerCreated" src="https://github.com/user-attachments/assets/f4b267ea-2822-47c9-922f-09e8ed1fdef2" />


---


A **serverless event-driven notification system** was successfully implemented using core AWS services **without managing any servers!**
