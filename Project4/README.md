 <table>
  <tr>
    <td><img src="./Images/Front.png" alt="IAM Icon" /></td>
    <td><h1 align="center">🔐 Exploring AWS IAM – Hands-On Experience! 💻☁️</h1></td>
  </tr>
</table>



   <td><h3 align="center">**AWS IAM (Identity and Access Management)** is a service that helps you securely control access to AWS services and resources. With IAM, you can manage users, groups, roles, and permissions within your AWS account. It allows you to define who can access which AWS resources and what actions they can perform, ensuring security and compliance.</h3></td>

---
## ⚠️**Basically, while learning IAM, I performed this practical to better understand how user, group, and permission management works in AWS.**
 ![](./Images/archi.png)

---
<br>
<br>

## 1. IAM USER CREATION WITH S3 FULL ACCESS
- Created a new IAM user from the AWS console.
- Assigned a custom password and ensured password reset on first sign-in.
- Granted the user the **AmazonS3FullAccess** policy.
- Received and saved the IAM user sign-in URL for login.

---

## 2. SIGNING IN AND ATTEMPTING EC2 ACCESS
- Logged in using the IAM user via the provided sign-in URL.
- Tried to launch an EC2 instance, but received an **unauthorized access** or **not authenticated** error.
- This was because the user had S3 access only and no EC2 permissions.

---

## 3. S3 BUCKET OPERATIONS USING IAM USER
- Created a new S3 bucket named `s-3-bucket`.
- Uploaded a file into the bucket successfully.
- Deleted an existing S3 bucket (ensured no objects were inside before deletion).

---

### 🔄 To simplify permission management:
- Now, I am creating a user group to simplify the permission management process.
- Assigning the same policy to each user individually is time-consuming and can lead to mistakes.
- This approach is more organized, efficient, and easier to manage when dealing with multiple users.

---

## 4. CREATING AN IAM GROUP FOR EC2 ACCESS
- As the root user, created a new IAM user group named **EC2FullAccessGroup**.
- Attached the **AmazonEC2FullAccess** policy to the group to allow EC2 actions.

---

## 5. ADDING USERS TO EC2 ACCESS GROUP
- Created two new IAM users (e.g., `Ec2-user1`, `Ec2-user2`).
- Added both users to the previously created group `EC2FullAccessGroup`  
  *(You can also add existing users while creating the group, as I did.)*

---

## 6. VERIFYING EC2 PERMISSIONS FOR GROUP USERS
- Logged in as `Ec2-user1` using the IAM sign-in URL.
- Successfully created a new EC2 instance.
- Attempted to perform S3 operations but access was denied.
- Confirmed that users only had **EC2 permissions**, and no access to S3 or other AWS services.

---

