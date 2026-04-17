# Launch Your First Amazon EC2 Instance
**Objective:** Deploy and connect to a virtual machine on AWS using the Amazon Elastic Compute Cloud (EC2) service.

---

## Step A & B: Launch an EC2 Instance with a Pre-configured AMI

1.  **Login:** Sign in to the [AWS Management Console](https://console.aws.amazon.com/) and search for **EC2** in the search bar.
2.  **Launch Instance:** On the EC2 Dashboard, click the **Launch instance** button.
3.  **Name and Tags:** Enter a name for your server (e.g., `My-First-Web-Server`) in the "Name" field.
4.  **Application and OS Images (AMI):** Select the **Amazon Linux** tab. Ensure **Amazon Linux 2023 AMI** (or Amazon Linux 2) is selected. Look for the label **"Free tier eligible"** to avoid charges.
5.  **Instance Type:** Select **t2.micro** (or **t3.micro**, depending on your region's free tier eligibility).





## Step C: Configure Security Groups and Key Pairs

1.  **Key Pair:** Click **Create new key pair**. 
    * Name it `my-aws-key`.
    * Select **RSA** and **.pem** (for OpenSSH/Mac/Linux) or **.ppk** (for PuTTY/Windows).
    * **Important:** Download and save this file securely; you cannot download it again.
2.  **Network Settings (Security Groups):** * Ensure **Allow SSH traffic from** is checked.
    * Change the dropdown from "Anywhere" to **My IP**. This is a security best practice that restricts access to only your current computer.
    * Leave "Allow HTTP/HTTPS traffic" unchecked for now unless you plan to host a website immediately.

## Step D: Connect to the Instance using SSH

1.  **Launch:** Click **Launch instance** at the bottom of the summary panel. Wait a few minutes for the "Instance state" to change to **Running**.
2.  **Locate Public IP:** Click on your Instance ID and copy the **Public IPv4 address**.
3.  **Terminal Connection:**
    * **For Mac/Linux/Windows (PowerShell/CMD):**
        1. Open your terminal and navigate to the folder where you saved the `.pem` file.
        2. Set permissions (Linux/Mac only): `chmod 400 my-aws-key.pem`
        3. Run the following command:
           ```bash
           ssh -i "my-aws-key.pem" ec2-user@<Your-Public-IP-Address>
           ```
    * **For Windows (PuTTY):**
        1. Load your `.ppk` file into PuTTYgen if conversion is needed, then open PuTTY.
        2. Enter the Public IP in "Host Name."
        3. Go to **Connection > SSH > Auth > Credentials** and browse for your private key file.
        4. Click **Open**.
4.  **Verification:** When prompted "Are you sure you want to continue connecting?", type **yes**. You should now see the Amazon Linux AMI terminal prompt.



---

## Step E: Termination (Cleanup)

To ensure you do not exhaust your free tier hours:
1.  Go back to the **Instances** dashboard.
2.  Select your instance.
3.  Click **Instance state > Terminate instance**. 
4.  Confirm termination to permanently delete the VM and stop all billing.
