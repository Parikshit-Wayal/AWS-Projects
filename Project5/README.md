<table>
  <tr>
    <td><img src="images/pic.png" alt="WordPress Logo" width="120"></td>
    <td><h2>🚀 Deploying WordPress on AWS: EC2 vs Lightsail Experience</h2></td>
  </tr>
</table>
<br>


<p align="center">
  Recently, I set up a WordPress instance manually on an <strong>EC2 server</strong>. Here's the process I followed:
</p>

<br>
---
## 📥 Downloaded WordPress

```bash
sudo wget https://wordpress.org/latest.tar.gz
```

## 📦 Extracted the archive

```bash
sudo tar -xvf latest.tar.gz
```

## 🛠️ Created MySQL Database

- Created a MySQL database named `wordpress`
- Set a password and saved the credentials

## 🌐 Accessed WordPress

- Opened the EC2 instance’s public IP in a browser
- Entered the database credentials
- ✅ WordPress was ready to build the website!

---

## 🌟 But here’s the best part

While exploring AWS services deeply, I came across **Amazon Lightsail** — and it made everything even easier!

---

## 🧠 Lightsail Overview

Lightsail is built for developers who want a **quick and simple** way to deploy cloud servers without diving deep into AWS's full setup.

### 💡 Pre-configured stacks available:

- NGINX  
- WordPress  
- PHPMyAdmin  
- LAMP  
- And more...

---

## 🎯 My Experience with Lightsail

1. Launched a **WordPress** instance via Lightsail (uses **Bitnami** under the hood)
2. Connected to the instance via SSH
3. Ran the following to get the admin credentials:

```bash
cat bitnami_credentials
```

4. Copied the username and password
5. Created the database (in some cases, it’s auto-created)
6. Opened the instance’s public IP in the browser
7. Entered the credentials

✅ **WordPress was live instantly — no manual extraction or config required!**

---

## 💬 Final Thoughts

If you're new to cloud hosting or want to deploy fast, **Lightsail is a game-changer**.  
It’s:

- Simple to use  
- Fast to deploy  
- Focused on what matters: **building your website**

---
