# Cloud-Computing
# Introduction to Cloud Platforms: AWS

**Objective:** Familiarize students with the Amazon Web Services (AWS) platform, its management interface, and core cloud infrastructure components.

---

## Step 1: Create an AWS Free-Tier Account

1.  **Navigate to AWS:** Open your browser and go to [aws.amazon.com/free](https://aws.amazon.com/free).
2.  **Start Registration:** Click on **Create a Free Account**.
3.  **Account Credentials:** Enter your email address and an account name. Verify your email using the verification code sent to your inbox.
4.  **Set Password:** Create a strong password for your Root User.
5.  **Contact Information:** Select **Personal** as the account type. Fill in your full name, phone number, and address.
6.  **Billing Information:** Enter your credit or debit card details. AWS will perform a temporary $1.00 hold to verify your identity.
7.  **Identity Verification:** Complete the SMS or voice call verification process.
8.  **Support Plan:** Select the **Basic Support – Free** option.
9.  **Completion:** Wait for the confirmation email stating your account is ready for use.

> **[INSERT SCREENSHOT: AWS ACCOUNT REGISTRATION CONFIRMATION]**

---

## Step 2: Explore the AWS Management Console

1.  **Login:** Sign in to the AWS Management Console as the **Root User**.
2.  **Home Dashboard:** Familiarize yourself with the search bar, the "Recently visited" widgets, and the "Console Home" layout.
3.  **Identify Key Services:** Use the search bar at the top to locate the following three pillars:

### A. Compute: EC2 (Elastic Compute Cloud)
* Search for **EC2**. 
* This service allows you to launch virtual servers.
* Navigate to the **Instances** link on the left sidebar to see where virtual machines are managed.

> **[INSERT SCREENSHOT: EC2 DASHBOARD]**

### B. Storage: S3 (Simple Storage Service)
* Search for **S3**.
* This is an object storage service for storing files (images, backups, static websites).
* Look for the **Create bucket** button which is the first step in storing data.

> **[INSERT SCREENSHOT: S3 BUCKETS INTERFACE]**

### C. Networking: VPC (Virtual Private Cloud)
* Search for **VPC**.
* This defines your private, isolated network in the cloud.
* View your **Your VPCs** section to see the default network AWS created for you.

> **[INSERT SCREENSHOT: VPC DASHBOARD]**

---

## Step 3: Understand the AWS Pricing Calculator

Before deploying resources, you must estimate costs to stay within the free tier or budget.

1.  **Access the Tool:** Go to [calculator.aws](https://calculator.aws/).
2.  **Create Estimate:** Click **Create estimate**.
3.  **Search for Service:** Search for **EC2** and click **Configure**.
4.  **Select Specifications:**
    * **Region:** Choose `US East (N. Virginia)`.
    * **Operating System:** `Linux`.
    * **Instance Type:** `t3.micro`.
5.  **Calculate:** Set the usage to **730 hours per month**.
6.  **Review Summary:** Observe the monthly cost breakdown at the bottom of the page.

> **[INSERT SCREENSHOT: AWS PRICING CALCULATOR ESTIMATE FOR EC2]**
