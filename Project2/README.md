# 🚀 Accelerating Static Content Delivery Using CloudFront + S3 ⚡️

🔹 Created an **S3 bucket** with ACL enabled to upload static files (images, videos, etc.)  
🔹 Uploaded a sample **image** file to the S3 bucket  
🔹 Tested the **S3 Object URL** by accessing it through the browser  
🔹 Used browser **Inspect → Network tab** to check image load time (~300ms observed)  
🔹 Set up an **AWS CloudFront Distribution** with the S3 bucket as the origin  
🔹 Re-tested the same image by replacing the S3 URL with the **CloudFront domain URL**  
🔹 Observed improved **latency** and reduced image load time  


