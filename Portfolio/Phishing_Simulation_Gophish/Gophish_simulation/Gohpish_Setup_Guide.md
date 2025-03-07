# Gophish Setup Guide

# Table of Contents

1. [Introduction](#1-introduction)
   - Why Windows?
2. [Installing Gophish on Windows](#2-installing-gophish-on-windows)
   - Download and Extract Gophish
   - Running Gophish
3. [Setting Up SMTP for Email Sending](#3-setting-up-smtp-for-email-sending)
   - What is SMTP?
   - Steps to Configure SMTP in Gophish
     - Gmail Setup
     - Outlook Setup
   - Troubleshooting SMTP Issues
4. [Creating Phishing Email Templates](#4-creating-phishing-email-templates)
   - Email Templates in Gophish
   - Steps to Create a Phishing Email Template in Gophish
   - Recommendations for a More Convincing Email Template
     - Customize with Company Branding
     - Subject Line
     - Professional Language
     - Personalization
     - Minimalistic Design
     - Spelling and Grammar

---

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
   | **Host**        | `smtp.gmail.com:587`                | SMTP server address |
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
| **Host**        | `smtp.office365.com:587`           | SMTP server address for Outlook/Office 365 |
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

## 🔹 4. Creating Phishing Email Templates

### **📝 Email Templates in Gophish**

Phishing email templates are a crucial part of any phishing simulation campaign. They simulate real-world phishing emails and are designed to trick the target into clicking on a malicious link or attachment. Gophish allows you to create and manage your own email templates to fit your phishing campaign.

### **🛠️ Steps to Create a Phishing Email Template in Gophish**

1. **Navigate to Email Templates**  
   - Click on **Email Templates** in the left-hand menu.
   - Click **+ New Template**.

2. **Enter Template Details**  
   - **Name**: Choose a name for your template (e.g., "Password Reset", "Account Verification").
   - **Subject**: Enter a subject that grabs attention (e.g., "Immediate Action Required: Your Account has been Compromised").

3. **Enter HTML Email Content**  
Paste your **HTML content** into the provided editor. Below is an example of a working and good-looking HTML email template for a phishing simulation:

3. **Enter HTML Email Content**  

### 💡 Recommendations for a More Convincing Email Template

To improve the credibility of your phishing email, consider the following recommendations:

#### Customize with Company Branding:
- **Logo**: Always include the company’s official logo at the top of the email to make it appear legitimate.
- **Colors**: Match the company’s brand colors for buttons, links, and headings to make the email blend in with the company’s actual email designs.
- **Fonts**: Use the same fonts and typography used in the company’s official communications (e.g., Arial, Helvetica, or any other fonts the company uses).

#### Subject Line:
- Create a subject line that mimics urgent or important communications from the company. Common tactics include "Action Required", "Account Security Alert", or "Immediate Action Needed". Make the subject line time-sensitive to increase urgency.

#### Professional Language:
- Use formal language that matches the tone of emails the company typically sends. Avoid using slang or casual phrases.

#### Personalization:
- If possible, personalize the email with the target’s name or their job title. Many organizations use personalized greetings, such as “Dear [First Name]” or “Dear [Job Title]”. This can make the email appear more genuine.

#### Minimalistic Design:
- Avoid cluttered designs with excessive text or images. A clean and minimal layout is often used in legitimate business emails. The focus should be on the call-to-action.

#### Spelling and Grammar:
- Ensure the email is free from spelling or grammatical errors. Poorly written emails are a big red flag that can alert the target that something is off.

---

Paste your **HTML content** into the provided editor. Below is an example of a working and good-looking HTML email template for a phishing simulation:

```html

<!DOCTYPE html>
<html>
<body style="background-color: white; text-align: center; font-family: Arial, sans-serif; margin: 0; padding: 0;">

    <!-- Gift Card Image -->
    <table align="center" width="100%" cellspacing="0" cellpadding="0" border="0">
        <tr>
            <td align="center">
                <img src="https://i.imgur.com/PgVrSxe.png" alt="Gift Card" width="500" style="display: block; margin: auto;">
            </td>
        </tr>
    </table>

    <!-- White Background Section -->
    <table align="center" width="500" cellspacing="0" cellpadding="20" border="0" style="background-color: white; border-radius: 10px; box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1); margin-top: 10px;">
        <tr>
            <td align="center">

                <!-- Claim Button -->
                <a href="https://phishing-website.com" style="display: inline-block; background-color: #007bff; color: white; padding: 15px 30px; font-size: 18px; font-weight: bold; text-decoration: none; border-radius: 5px;">
                    Claim Here
                </a>

                <!-- Offer Validity Text -->
                <p style="margin-top: 15px; font-size: 14px; color: #555;">
                    Offer valid for 24 hours. Click the button and follow the instructions on the screen.
                </p>

            </td>
        </tr>
    </table>

{{.Tracker}}</body>
</html>
