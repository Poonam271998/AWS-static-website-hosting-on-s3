# 🌐 AWS S3 Static Website Hosting

## 📌 Project Overview

This project demonstrates how to create an Amazon S3 bucket, configure permissions, and host a static website using S3.

---

## 👤 Author

**Name:** Poonam Langote
**AWS Region:** us-east-1

---

## 🚀 Steps Performed

### 1️⃣ Create S3 Bucket

* Navigate to **S3 Console**
* Click **Create Bucket**
* Bucket Name: `static-site-poonam`
* Region: `us-east-1`
* Uncheck **Block all public access**
* Acknowledge warning and create bucket

---

### 2️⃣ Create Website Files

#### index.html

```html
<html>
<body>
<h1>My AWS S3 Website</h1>
<p>Hosted on Amazon S3 by Poonam</p>
</body>
</html>
```

#### about.html

```html
<html>
<body>
<h1>About Page</h1>
<p>This is the about page of my S3 hosted website.</p>
</body>
</html>
```

---

### 3️⃣ Upload Files

* Upload `index.html` to S3 bucket
* Upload `about.html` to S3 bucket

---

### 4️⃣ Enable Static Website Hosting

* Go to **Properties**
* Enable **Static Website Hosting**
* Index document: `index.html`
* Save changes

---

### 5️⃣ Configure Bucket Policy

Add the following policy to allow public access:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::static-site-poonam/*"
    }
  ]
}
```

---

## 🌍 Website URLs

### Main Website

```
http://static-site-poonam.s3-website-us-east-1.amazonaws.com
```

### About Page

```
https://static-site-poonam.s3.us-east-1.amazonaws.com/about.html
```

---

## ✅ Result

* S3 bucket successfully created
* Static website hosting enabled
* Files are publicly accessible via URLs

---

## 📷 Screenshots

* Bucket created and files uploaded
* Bucket policy configuration
* Static website hosting enabled
* Website accessed via endpoint

---

## 📚 Conclusion

This project successfully demonstrates hosting a static website on AWS S3 by configuring bucket policies and enabling public access.

---
