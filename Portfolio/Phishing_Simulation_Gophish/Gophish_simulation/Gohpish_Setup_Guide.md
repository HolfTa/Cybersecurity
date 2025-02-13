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