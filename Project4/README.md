<table>
  <tr>
    <td><img src="./Images/Front.png" alt="IAM Icon" height="100" width="200"/></td>
    <td><h1 align="center">🔐 Exploring AWS IAM – Hands-On Experience! 💻☁️</h1></td>
  </tr>
</table>

<h3 align="center">
  🌐 <strong>AWS IAM (Identity and Access Management)</strong> is a service that helps you securely control access to AWS services and resources. <br>
  With IAM, you can manage users, groups, roles, and permissions within your AWS account. <br>
  It allows you to define who can access which AWS resources and what actions they can perform, ensuring security and compliance.
</h3>

---

## ⚙️ **Why This Practical?**
🎯 While learning IAM, I performed this hands-on activity to understand how **user, group, and permission management** works in AWS.

<p align="center">
  <img src="./Images/archi.png" height="400" width="750"/>
</p>

---

## 1️⃣ IAM USER CREATION WITH S3 FULL ACCESS
- 🧑‍💻 Created a new IAM user from the AWS console.
- 🔐 Assigned a custom password and enforced password reset on first sign-in.

  ![](./Images/createS3role.png)

- ✅ Granted the user the **AmazonS3FullAccess** policy.

  ![](./Images/assignRole.png)

- 🔗 Received and saved the IAM user sign-in URL for login.

  ![](./Images/createdUser.png)

---

## 2️⃣ SIGNING IN AND ATTEMPTING EC2 ACCESS
- 🔑 Logged in using the IAM user via the sign-in URL.

  ![](./Images/hittingUrl.png)

- 🚫 Tried launching an EC2 instance, but received an **unauthorized** or **not authenticated** error.

  ![](./Images/tryToLaunchInstance.png)

> ⚠️ This happened because the user only had S3 access and no permissions for EC2.

---

## 3️⃣ S3 BUCKET OPERATIONS USING IAM USER
- 🪣 Created a new S3 bucket named `s-3-bucket`.

  ![](./Images/bucketCreated.png)

- 📁 Uploaded a file into the bucket.

  ![](./Images/uploadImage.png)

- 🗑️ Deleted an existing S3 bucket (ensured it was empty before deletion).

  ![](./Images/deleteBucket.png)

---

## 🔁 Simplifying Permission Management
- 👨‍👩‍👧 Now, I created a **user group** to streamline permission handling.
- ⏳ Assigning policies to each user individually is time-consuming and error-prone.
- ✅ Group-based access is more **efficient, manageable, and scalable**.

---

## 4️⃣ CREATING AN IAM GROUP FOR EC2 ACCESS
- 🔐 As the root user, created a group named **EC2FullAccessGroup**.
- 🧾 Attached the **AmazonEC2FullAccess** policy for EC2 operations.

  ![](./Images/grpCreated.png)

---

## 5️⃣ ADDING USERS TO EC2 ACCESS GROUP
- 👤 Created two IAM users: `Ec2-user1`, `Ec2-user2`.

  ![](./Images/2users.png)

- ➕ Added both users to the **EC2FullAccessGroup**.  
  _(You can also add users while creating the group, like I did.)_

  ![](./Images/UsersAdded.png)

---

## 6️⃣ VERIFYING EC2 PERMISSIONS FOR GROUP USERS
- 🔓 Logged in as `Ec2-user1` using the IAM URL.
- 🚀 Successfully launched an EC2 instance.

  ![](./Images/ec2byEc2-user.png)

- 🚫 Tried accessing S3 but was denied.

  ![](./Images/Ec2userFails3.png)

- ✔️ Verified that the users only had **EC2 permissions**, with no access to S3 or other services.

---

🎉 That’s how I explored AWS IAM practically – covering users, policies, groups, and access control across services like EC2 and S3!

