# Instructions
You will need to create oauth consent credentials in order to use gmail api.
## ✅ Prerequisites

- A Google account
- A project using the Gmail API (e.g. Flask + Gmail automation)
- `google-api-python-client`, `google-auth`, `google-auth-oauthlib`, and `google-auth-httplib2` installed

---

## 🔐 Step 1: Create a Google Cloud Project

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Click the **project selector** in the top bar.
3. Click **"New Project"**, give it a name (e.g. `My Gmail API Project`), and click **Create**.

---

## 📦 Step 2: Enable the Gmail API

1. While in your project, go to: [Gmail API](https://console.cloud.google.com/apis/library/gmail.googleapis.com).
2. Click **"Enable"**.

---

## 🔑 Step 3: Configure OAuth Consent Screen

1. In the left sidebar, go to **APIs & Services > OAuth consent screen**.
2. Choose **External**, then click **Create**.
3. Fill in the basic details:
   - App name
   - User support email
   - Developer contact info
4. Click **Save and Continue** through the scopes section (you can leave it blank for testing).
5. Add yourself (your Google email) as a **test user** and click **Save and Continue** again.

---

## 🔧 Step 4: Create OAuth Client ID Credentials

1. Go to **APIs & Services > Credentials**.
2. Click **"+ CREATE CREDENTIALS"** → **OAuth client ID**.
3. Choose **Application Type** → **Desktop App**.
4. Give it a name (e.g. `Gmail Desktop Client`), then click **Create**.
5. On the next screen, click **Download JSON** — this is your `credentials.json` file.

💾 **Save the file as `credentials.json`** in your project folder.

---

## ✅ Step 5: First-Time Authentication Flow

When your app runs the first time, it will open a browser asking you to authorize Gmail access. Once authorized:
- A `token.json` file will be generated and reused automatically for future runs.
