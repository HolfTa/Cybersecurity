# Gophish Setup Guide

## 🔹 1. Introduction
Gophish is an open-source phishing framework designed for **security awareness training** and penetration testing. It allows organizations to simulate phishing attacks to educate employees about social engineering threats.

### Why Windows?
Although **Linux is the most widely used operating system for cybersecurity**, I have chosen to work on **Windows** at this stage to **build foundational knowledge and experience**. This aligns with my personal interest and existing familiarity with Windows environments. To bridge the knowledge gap, I actively **rely on free learning resources** to replicate these tasks on **Linux** as well. I am excited to undertake future projects that will focus on **Linux-based skills**.

This guide covers:
- Installing and configuring **Gophish on Windows**
- Setting up **SMTP servers and phishing templates**
- Running **phishing simulations**

---

## 🔹 2. Installing Gophish on Windows

### **🖥️ Download and Extract Gophish**
1. Download the latest Windows release from [Gophish's official site](https://github.com/gophish/gophish/releases).
2. Extract the ZIP file into a directory (e.g., `C:\Gophish`).

### **🔧 Running Gophish**
1. Navigate to the directory where you downloaded the file.
2. Extract the ZIP file.
3. Run the application file.
4. Gophish will start, and you’ll see output similar to:
   ```plaintext
   Starting admin server at https://127.0.0.1:3333
   ```

**Access the Admin Panel:** Open a browser and go to [https://127.0.0.1:3333](https://127.0.0.1:3333).

**Default credentials:**
- **Username:** `admin`
- **Password:** `password found in plaintext above the localhost info`

## 🔹 3. Setting Up SMTP for Email Sending  

To send phishing emails using Gophish, you need to **configure an SMTP server**. This section will guide you through setting up an SMTP profile.  

### 📌 What is SMTP?  
SMTP (**Simple Mail Transfer Protocol**) is the protocol used for sending emails. Gophish requires an SMTP server to deliver phishing emails to targets.  

### 🛠️ Steps to Configure SMTP in Gophish  

1. **Open Gophish Admin Panel**  

2. **Navigate to Sending Profiles**  
   - Click on **Sending Profiles** in the left-hand menu  
   - Click **+ New Profile**  

3. **Enable Less Secure Apps (For Gmail SMTP)**  
   - If using Gmail, **generate an App Password** [here](https://myaccount.google.com/apppasswords).  
   - Type "Mail" and generate a 16-character password.  
   - Use this password in the SMTP settings instead of your normal Gmail password.  
4. **Enter SMTP Details**  
Let's first start with a Gmail setup, later on we move onto an Outlook setup!
### Gmail

   | Field            | Value (Example for Gmail)                     | Description |
   |-----------------|----------------------------------|-------------|
   | **Name**        | `Gmail SMTP`                     | Any name you want |
   | **Interface**   | `SMTP`                           | Select SMTP |
   | **SMTP From**   | `System Notification <your-email@gmail.com>` | The sender name & email displayed to recipients |
   | **Host**        | `smtp.gmail.com`                | SMTP server address |
   | **Username**    | `your-email@gmail.com`          | Your full email address |
   | **Password**    | `Your-App-Password`             | App Password generated for authentication in your Google Account Settings |

5. **Save & Test Connection**  
   - Click **Save**  
   - Click **Send Test Email** to verify the setup to your email

---

### 🔎 Troubleshooting SMTP Issues  

🚨 **Common Errors & Fixes:**  

| Error Message | Solution |
|--------------|----------|
| `535 5.7.8 Username and Password not accepted` | Ensure you’re using an **App Password**, not your regular email password. Ensure you input your own email.|
| `Max connection attempts exceeded` | Check if your SMTP server blocks connections from unknown locations. |
| `Timeout or Connection Refused` | Verify the SMTP server address and **port (587 for TLS, 465 for SSL)**. |

---
### Outlook

#### **1. Enable SMTP Authentication**
Before configuring Gophish, ensure that **SMTP authentication** is enabled for your Outlook account.

1. Sign in to [Microsoft 365 Admin Center](https://admin.microsoft.com/)
2. Navigate to **Users > Active Users**
3. Select your account, then go to **Mail > Email Apps**
4. Ensure that **Authenticated SMTP** is **enabled**
5. If using **Multi-Factor Authentication (MFA)**, create an **App Password** at [Microsoft Security](https://mysignins.microsoft.com/security-info)

---

#### **2. Enter SMTP Details**
Use the following settings for your Outlook SMTP configuration:

| Field            | Value (Example for Outlook)                  | Description |
|-----------------|--------------------------------|-------------|
| **Name**        | `Outlook SMTP`                 | Any name you want |
| **Interface**   | `SMTP`                         | Select SMTP |
| **SMTP From**   | `Your Name <your-email@outlook.com>` | The sender name & email displayed to recipients |
| **Host**        | `smtp.office365.com`           | SMTP server address for Outlook/Office 365 |
| **Username**    | `your-email@outlook.com`       | Your full Outlook email address |
| **Password**    | `Your-App-Password`            | App Password (if MFA enabled) or regular password (if MFA is off) |
| **Port**        | `587`                          | TLS port (recommended) |
| **Use TLS**     | `Yes`                          | Ensure encryption |

---

#### **3. Save & Test Connection**
- Click **Save**  
- Click **Send Test Email** to confirm the setup is working  

---

### 🔎 Troubleshooting Outlook SMTP Issues

🚨 **Common Errors & Fixes:**

| Error Message | Solution |
|--------------|----------|
| `535 5.7.3 Authentication unsuccessful` | Ensure SMTP authentication is enabled in your Microsoft 365 account. |
| `535 5.7.8 Username and Password not accepted` | Use an **App Password** if MFA is enabled. |
| `Server timed out` | Verify that the **host and port (587 for TLS)** are correct. |
| `Connection refused` | Some corporate networks block SMTP traffic—try using a different network or VPN. |

---

After configuring SMTP, you’re ready to start **sending phishing simulations** using Gophish! 🚀  
Next, let's move on to **creating phishing templates** and running campaigns.  

---