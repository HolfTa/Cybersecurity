# Phishing Website Overview

## Introduction

Welcome to the website overview. This project aims to simulate a variety of modern phishing attacks in order to assess human error vulnerabilities within organizations. The simulations will range from basic phishing attempts to more advanced, targeted attacks, helping employees identify and avoid potential threats.

All documentation, files, and materials related to the websites will be in this document, please refer to this document in case of need.

## Step 1: Understanding the Modern Threat Landscape

Modern phishing attacks have become increasingly sophisticated, evolving beyond outdated and easily recognizable tactics (such as gift card offers or fake prizes). Today’s phishing threats are more focused on:

- **Spear-phishing**: Targeting specific individuals based on their role, department, or personal information to make the attack more convincing and difficult to detect.
- **Social engineering**: Manipulating individuals into revealing personal or sensitive information, often by exploiting human psychology or trust.
- **Credential stuffing**: Using stolen usernames and passwords from previous breaches to gain unauthorized access to accounts and systems.
- **Business Email Compromise (BEC)**: Targeting organizations to deceive employees into redirecting payments or sending sensitive information to the attacker by impersonating trusted figures.
- **Malware delivery**: Phishing emails used to deliver malicious software, such as ransomware or trojans, often to compromise systems and steal data.

The goal of this project is to simulate these modern phishing threats at varying levels of complexity. This will allow employees to learn how to identify and avoid these attacks, whether they are basic scams or highly targeted, advanced phishing attempts.

# Step 2: Overview of the Three Phishing Simulation Setups  

This project includes three different phishing simulation setups, each increasing in sophistication. These setups are designed to help organizations test employee awareness and response to phishing attacks at different levels of complexity.  

---

## Scenario: Fake Gift Card Offer  

An email informs employees that they have been awarded a **€50 gift card** as a reward for their outstanding work. To claim the reward, they are required to **click a button** in the email, which redirects them to a website where they must **confirm their identity** by entering their **employee ID and password**.  

## Objective  
This simulation tests employees' awareness of **phishing attempts disguised as company rewards**. The goal is to see how many employees will enter their **credentials on a fake website**, revealing vulnerabilities in security awareness.  

## Simulation Details  
- The email appears to come from a trusted internal source, such as **HR or the Rewards Team**.  
- The subject line may say: **"Congratulations! You've Earned a €50 Gift Card"** to encourage engagement.  
- The **call-to-action button** (e.g., “Claim Your Gift Card”) links to a **fake login page** that mimics an official company website.  
- The login page **requests the employee's ID and password**, which are then captured by the attacker (IT security team for assessment).  

## Key Takeaways  
- **Unexpected rewards should always be verified** with HR or IT before clicking any links.  
- **Legitimate reward programs** do not ask for login credentials to claim a prize.  
- Employees should check for **subtle signs of phishing**, such as **unusual sender email addresses** or **typos in the message or URL**.  

## Helpful Tips for Realism  
- **Use the company's official logo, branding colors, and fonts** to make the email and website look authentic.  
- Create a **URL that closely resembles the company's actual domain** (e.g., `company-rewards.com` instead of `company.com`).  
- Add **a sense of urgency**, such as a **limited-time offer countdown**, to pressure employees into acting quickly. 

---

## 2. Intermediate Setup: Forced Security Update Notice  

### Scenario  
An email notifies employees that their **account security needs to be updated** due to a breach or policy change. The email **creates a sense of urgency**, making employees feel they need to act immediately to maintain access to company resources.  

### Objective  
Employees are **instructed to enter their current credentials and create a new password** to maintain access. This mimics legitimate security update requests but is actually an attempt to steal their credentials.  

### Simulation Details  
- The email appears to come from the **IT department**, stressing the importance of an urgent security update.  
- The **link leads to a phishing page that looks like the company’s official login portal**.  
- Employees are asked to enter their **current credentials** and then set up **new ones** (username, password, multi-factor authentication details).  
- The collected credentials are sent to the company’s **IT security team for assessment**.  

### Key Takeaways  
- **Urgency is a key manipulation tactic in phishing attacks**—employees should take their time and verify such requests.  
- Always confirm **directly with IT support** if an account update request seems suspicious.  
- **Never reuse passwords**—even if employees enter fake new credentials, using the same password elsewhere can still be a security risk.  

### Helpful Tips for Realism  
- Use **official company branding** and **security terminology** to make the email more convincing.  
- **Mimic real IT communications**, such as referencing company security policies or including a “deadline” to update credentials.  
- **Include a warning** in the email that failure to update their credentials will result in **loss of account access**, increasing the likelihood of compliance.  

---

## 3. Advanced Setup: Targeted Social Engineering and Spear-Phishing  

### Scenario  
A **highly targeted phishing email** appears to come from **the CEO, CFO, or IT security lead**. The email references **a specific work task, financial transaction, or company event** to make it highly believable. Example: A finance employee receives an urgent email from what appears to be the **CFO**, stating: *"We are finalizing a critical vendor payment of €250,000, and I need you to process it immediately. Please use the new banking details attached."*  

### Objective  
This test evaluates whether employees will:  
- **Disclose sensitive company information** (e.g., login credentials, internal reports, client data).  
- **Perform unauthorized actions** (e.g., transferring funds, approving security changes).  

### Simulation Details  
- The email appears to be from **a senior executive or key department** (e.g., Finance, HR, IT Security).  
- It contains **realistic details** (e.g., references to current projects, vendors, or financial transactions).  
- Employees will be asked to:  
  - **Enter their credentials** on a fake login page (e.g., "Your session has expired, please re-authenticate"). Data will be forwarded to the "attacker", the IT team conducting the assessment.  

### Key Takeaways  
- **Spear-phishing attacks are highly convincing** because they use personalization and urgency.  
- Employees should **always verify unusual requests** through a separate communication channel (e.g., calling the executive directly).  
- **Executives should be aware** that their identities can be spoofed and should educate their teams on verifying sensitive requests.  

### Helpful Tips for Realism  
- **Use the company's real email signature and branding** to make the phishing email appear authentic.  
- **Spoof the sender’s email** (e.g., `john.smith@company-finance.com` instead of `john.smith@company.com`).  
- Include **previously leaked or publicly available company data** to increase credibility (e.g., past press releases, LinkedIn job titles).  
- Add **a follow-up phishing call ("vishing")** pretending to be the executive, increasing pressure on the target.  
- **Time the phishing attempt** to coincide with **high-stress periods**, such as quarterly financial closings, major product launches, or IT security updates.  

---

## Final Notes on Phishing Simulations  

These phishing simulations are designed to **train employees to recognize real-world attacks** before they fall victim to them. Companies can **use the collected data** to assess employee vulnerabilities and improve security awareness programs.  

### General Best Practices for All Simulations  
- **Monitor engagement metrics** (e.g., click rates, data submissions) to measure effectiveness.  
- **Provide immediate feedback to employees** who fall for the simulation, explaining how they were tricked.  
- **Rotate phishing methods periodically** so employees don’t become accustomed to a single type of attack.  
- **Incorporate phishing awareness training** alongside simulations to build long-term security habits.  

By implementing these phishing tests with a strategic approach, organizations can **significantly reduce their risk of real-world phishing attacks**.  

