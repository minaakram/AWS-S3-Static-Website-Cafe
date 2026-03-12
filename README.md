# ☕ Café Static Website Hosting on AWS S3

## 📝 Project Overview
This project demonstrates the deployment of a secure and durable static website for a local café using **Amazon S3**. It goes beyond simple hosting by implementing cloud best practices for data protection, cost optimization, and disaster recovery.



## 🛠️ Key Cloud Architectures Implemented

### 1. Static Web Hosting & Public Access
* **Hosting:** Configured an S3 bucket as a web server using `index.html` as the entry point.
* **Security:** Implemented a **Bucket Policy** to grant `s3:GetObject` permissions to public users while maintaining bucket security.

### 2. Data Protection (Versioning)
* Enabled **Object Versioning** to prevent accidental deletions or overwrites.
* Tested rollback capabilities by updating the website's theme and maintaining multiple versions of the source code.

### 3. Cost Optimization (Lifecycle Management)
Implemented a data retention strategy to save storage costs:
* **Transition:** Automatically move previous versions to **S3 Standard-IA** after 30 days.
* **Expiration:** Permanently delete old versions after 365 days.

### 4. Disaster Recovery (Cross-Region Replication)
* **High Availability:** Configured **CRR** to automatically replicate every upload from the Source Region (N. Virginia) to a Destination Region (Oregon).
* **Reliability:** Ensures data safety even in the event of a regional AWS outage.

## 📊 System Gallery

### 1. Project Architecture
![Architecture](./cafe%20arch.png)
*Detailed architecture showing S3 replication and hosting setup.*

### 2. Website Preview
![Café Website](./cafe.png)
*The final static website as seen by the customers.*

## 📁 Technical Skills Demonstrated
* **Storage:** Amazon S3 (Bucket Policies, Versioning, Lifecycle, CRR).
* **IAM:** Configuring `CafeRole` for cross-region replication permissions.
* **Automation:** Implementing lifecycle rules for cost efficiency.

## 🚀 Repository Contents
* `static-website.zip`: Original source files for the café website.
* `index.html`: The main entry point for the static site.
* `cafe arch.png` & `cafe.png`: Visual evidence of the project setup.
