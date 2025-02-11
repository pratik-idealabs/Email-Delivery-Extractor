# 📧 Email Delivery Extractor

## About the Project
The **Email Delivery Extractor** is a simple **Streamlit web application** that securely connects to your **Gmail account** using OAuth2. It scans your inbox and filters out **delivery-related emails**, displaying them in one convenient location.

---

## How It Works

### Overview
The app securely logs into Gmail using **Google OAuth2**, retrieves delivery-related emails through the **Gmail API**, and presents them in an organized format.

### Logic Breakdown
- **User Login:** Users log in through Google OAuth2.
- **Email Filtering:** The app scans the user’s inbox and retrieves emails related to deliveries.
- **Display Delivery Emails:** Shows delivery-related email subjects, senders, and content.

---

## 🔑 OAuth2 Setup Steps

### Step 1: Enable Gmail API in Google Cloud Console
1. **Go to Google Cloud Console:** [Google Cloud Console](https://console.cloud.google.com/).
2. **Create a project:**
   - Navigate to the top-left menu → Project selector → **New Project**.
3. **Enable the Gmail API:**
   - Go to **APIs & Services → Library**.
   - Search for **Gmail API** and enable it for your project.

### Step 2: Set Up OAuth Consent Screen
1. Go to **APIs & Services → OAuth consent screen**.
2. Choose **External** if you’re allowing public users.
3. Fill out basic details like the app name and user support email.
4. Ensure you add the scope for reading Gmail:

https://www.googleapis.com/auth/gmail.readonly

5. Save and publish the consent screen.

### Step 3: Create OAuth2 Credentials
1. Go to **APIs & Services → Credentials → Create Credentials → OAuth client ID**.
2. Choose **Desktop App** (for local testing).
3. Download the `client_secret.json` file.

### Step 4: Place `client_secret.json` in Your Project Directory
- Place it in the same directory as `app.py`.

---

## Step-by-Step Explanation

1. **User Login:**
   - The user clicks the **Sign in with Google** button.
   - OAuth2 authenticates and retrieves access to Gmail.

2. **Filtering Emails:**
   - The app scans the inbox and filters delivery-related emails.

3. **Display Delivery Emails:**
   - Shows delivery-related email subjects, senders, and email content.

4. **Logout:**
   - Ends the session and securely removes stored tokens.

---

## Requirements
- streamlit
- google-auth
- google-auth-oauthlib
- google-auth-httplib2
- google-api-python-client

---

## Expected Output
1. **Filtered Emails:** Displays all delivery-related emails.
2. **Secure Login:** Users log in safely through Google’s OAuth2.

---

## 🔐 Security Considerations
- Keep `client_secret.json` secure and never expose it publicly.
- OAuth tokens are only stored temporarily for the session.

---
