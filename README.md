# 📧 Email Extractor

A simple **Streamlit web app** to securely log in using your **Google account** and view your Gmail inbox.

## 🎯 Features
- **Google OAuth2 Login**: Securely log in via Google.
- **View Emails**: Fetch and display inbox emails dynamically.
- **Pagination**: Navigate through emails with Next and Previous buttons.

## 🚀 How to Run

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-repo/email-extractor.git
   cd email-extractor
   ```

2. **Set Up Virtual Environment and Install Requirements:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # macOS/Linux
   venv\Scripts\activate   # Windows
   pip install -r requirements.txt
   ```

3. **Set Up Google API Credentials:**
   - Enable **Gmail API** on [Google Cloud Console](https://console.cloud.google.com/).
   - Create **OAuth credentials** and download `client_secret.json`.
   - Place it in the project root.

4. **Run the App:**
   ```bash
   streamlit run app.py
   ```

## 📖 Project Structure
```
email-extractor/
├── app.py
├── requirements.txt
├── client_secret.json
└── README.md
```

## 🔐 Security
- Keep your `client_secret.json` secure.
- OAuth tokens are temporary and stored only for session use.

## 📚 How It Works
1. **Login:** Secure Google login via OAuth2.
2. **Fetch Emails:** Retrieve recent inbox emails.
3. **Pagination:** Navigate through multiple pages.
4. **Logout:** End the session securely.


