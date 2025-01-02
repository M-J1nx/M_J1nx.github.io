---
title:  "Gmail 2fa App Password"
excerpt: "Blocked by 2FA Error when I making program that can send emails."
categories: 
- Algorithm
- Back-end
- Cloud
- Front-end
- Game
- Git & Github
- Security
tags:
- Debug
- Theory
 
toc_label: Contents
toc: true
toc_sticky: true
 
date: 2025-01-01
last_modified_at: 2025-01-02
---

# Sending Email Using Google Account with 2FA Enabled

If you're encountering the error:  
`535-5.7.8 Username and Password not accepted.`  

This might be due to Google removing the "Less Secure App Access" option as of May 30, 2022. Instead, you need to use **App Passwords** with **2-Factor Authentication (2FA)** enabled. Here's how you can set it up:

---

## Step 1: Enable 2FA (Two-Factor Authentication)
1. Go to your Google Account settings.
2. Follow the steps to enable 2FA (Two-Factor Authentication).  
   Refer to the [official guide](https://support.google.com/accounts/answer/185833?hl=ko&utm_source=google-account&utm_medium=search-screen) for assistance.

---

## Step 2: Generate an App Password
1. Open the following link: [App Passwords](https://myaccount.google.com/apppasswords)
2. Log in to your Google account if prompted.
3. Choose or enter an app name (e.g., "Email Service").
4. Click **Generate** to create the app password.

---

## Step 3: Save the App Password
- Once created, the password will be displayed **only once**.  
  ⚠️ **Save it securely**, as you won’t be able to view it again.


---

## Step 4: Use the App Password
Replace your Google account password in your email-sending service with this app password.

---

### Notes:
- This method is more secure and aligns with Google’s updated security policies.
- Ensure that your email-sending application or library supports app passwords.

Now you’re ready to send emails securely using your Google account! 😊
