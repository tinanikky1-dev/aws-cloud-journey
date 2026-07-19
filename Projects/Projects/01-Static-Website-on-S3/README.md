# Project 1: Hosting a Static Website on Amazon S3

## Project Overview

This project demonstrates how to host a static website using Amazon Simple Storage Service (Amazon S3).

The objective was to learn how AWS S3 can be used to host static websites by configuring bucket settings, enabling static website hosting, adjusting permissions, and publishing a website to the internet.

This is my first hands-on AWS Cloud project.

---

## Project Objectives

- Create an Amazon S3 bucket
- Upload website files
- Enable Static Website Hosting
- Configure Bucket Policy
- Disable Block Public Access
- Publish the website
- Verify public accessibility

---

## AWS Services Used

- Amazon S3

---

## Project Architecture

```
Local Computer
       │
       ▼
Upload HTML & CSS Files
       │
       ▼
Amazon S3 Bucket
       │
       ▼
Enable Static Website Hosting
       │
       ▼
Bucket Policy
       │
       ▼
Public Website Endpoint
       │
       ▼
Live Website
```

---

## Files Used

- index.html
- style.css

---

## Implementation Steps

### Step 1

Created an S3 bucket for hosting the website.

---

### Step 2

Uploaded the website files into the bucket.

- index.html
- style.css

---

### Step 3

Enabled Static Website Hosting.

Configured:

- Host Static Website
- Index document: index.html
- ### Screenshot

![Enable Static Website Hosting](screenshots/1000345570.jpg)

---

### Step 4

Disabled Block Public Access.

This allowed the bucket contents to become publicly accessible.

---

### Step 5

Configured the Bucket Policy.

The bucket policy grants public read access to all website files.

---

### Step 6

Copied the Website Endpoint.

AWS generated a public endpoint that serves the website.

---

### Step 7

Opened the website endpoint in the browser.

The website loaded successfully.

---

## Challenges Encountered

During this project I encountered several issues, including:

- Invalid Bucket Policy Resource
- Access permission errors
- Static website configuration issues
- Public access configuration

Each problem helped me understand how Amazon S3 permissions work.

---

## Lessons Learned

Through this project I learned:

- How Amazon S3 stores website files
- How Static Website Hosting works
- The importance of Bucket Policies
- Why Block Public Access affects website accessibility
- How public website endpoints are generated
- Basic troubleshooting of S3 hosting issues

---

## Final Result

The website was successfully deployed and made publicly accessible using Amazon S3 Static Website Hosting.

This project marks the beginning of my AWS Cloud Engineering portfolio.

---

## Skills Demonstrated

- Amazon S3
- Static Website Hosting
- Bucket Policies
- IAM Concepts
- Cloud Storage
- Troubleshooting
- AWS Console Navigation
