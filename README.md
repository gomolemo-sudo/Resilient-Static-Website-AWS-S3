# Building a Resilient Static Website on Amazon S3: Step-by-Step Guide  

## Introduction  
In this project, I set up a static website for a café business using Amazon Simple Storage Service (Amazon S3). The goal was to host the website, protect its data, optimize storage costs, and implement disaster recovery (DR) strategies using best practices. This guide walks through each step to achieve a scalable, secure, and cost-efficient solution for a small business.

## Step 1: Creating an S3 Bucket for Website Hosting
I started by creating an S3 bucket in the us-east-1 region. To make the website publicly accessible, I disabled the "Block all public access" setting and enabled static website hosting with index.html as the main entry point. This configuration provided a unique endpoint URL, allowing the website to be accessible online.
![image](https://github.com/user-attachments/assets/1067bef7-4115-444e-962b-fcf73efb0e0c)



## Step 2: Uploading Website Content
I uploaded the static files, including index.html and folders for CSS and images, to the bucket. After uploading, I tested the endpoint URL in a browser to confirm that the website was accessible and displayed correctly.
![image](https://github.com/user-attachments/assets/2e543ff5-9578-40b5-85a6-568df34cf633)



## Step 3: Setting Up a Bucket Policy for Public Access
To simplify managing public access, I created a bucket policy that grants read-only permissions to all users. This policy automatically ensures that any new files uploaded to the bucket are publicly accessible without needing manual adjustments, streamlining the process for future updates.

![image](https://github.com/user-attachments/assets/910cd8d0-b3b1-4725-b6fe-42b280f66cbe)



## Step 4: Step 4: Protecting Data with Versioning
To safeguard against accidental deletions or overwrites, I enabled versioning on the bucket. I then made some modifications to the index.html file and re-uploaded it. By enabling versioning, I could see multiple versions of the file, which allows easy recovery of previous content if needed.

![image](https://github.com/user-attachments/assets/957b1e13-0e30-4b16-aa44-aa22ecc3488c)



## Step 5: Implementing a Lifecycle Policy for Cost Optimization
Since versioning can lead to increased storage usage, I implemented lifecycle policies to control costs. The first rule moves previous versions to the S3 Standard-Infrequent Access class after 30 days, and the second rule deletes them after 365 days. This approach optimizes storage expenses while maintaining data availability.
![image](https://github.com/user-attachments/assets/128eced9-1026-46df-8cde-f2d5fe45d192)


## Step 6: Setting Up Cross-Region Replication for Disaster Recovery
For enhanced durability and disaster recovery, I enabled cross-region replication. I created a second bucket in another AWS region, enabled versioning, and configured a replication rule. This ensures that all updates in the source bucket are automatically replicated, providing redundancy in case of regional outages.


## Skills Demonstrated  
- AWS S3 Management and Static Hosting  
- Bucket Policies and Permissions  
- Versioning and Lifecycle Management  
- Cross-Region Replication for Resilience  

## Conclusion  
By leveraging Amazon S3 features like static website hosting, bucket policies, versioning, lifecycle rules, and cross-region replication, I successfully set up a highly available, cost-efficient, and resilient static website for the café business. These strategies can be scaled to meet the needs of any small business looking to establish an online presence while ensuring data protection and cost management. 
 

## Author  
**Gomolemo Hlatshwayo**  
- [LinkedIn](https://www.linkedin.com/in/gomolemo-hlatshwayo-2b844522a/)  
- [GitHub](https://github.com/gomolemo-sudo)  
