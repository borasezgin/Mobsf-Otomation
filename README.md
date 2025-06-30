# MobSF Auto Scanner

This repository contains a Python-based automation script that interacts with the [MobSF (Mobile Security Framework)](https://github.com/MobSF/Mobile-Security-Framework-MobSF) API to perform automated static security analysis for Android applications (APK files).

## 🔍 Features

- Automatically scans all APK files in a directory
- Downloads PDF reports for each scan
- Sends reports via email with a styled HTML message
- Deletes old scan records from MobSF
- Stores reports in date-based folders

## ⚙️ Requirements

- Python 3.7+
- A running instance of MobSF with API access
- `requests`, `python-dotenv`, `smtplib`, and `email` libraries

## 📦 🛠 Setup Instructions

1. **Clone this repository**

```bash
git clone https://github.com/borasezgin/mobsf-auto-scan.git
cd mobsf-auto-scan

```bash
2. **Configure Environment**

Create a .env file in the root directory and add the following:

API_KEY=your_mobsf_api_key
UPLOAD_URL=http://localhost:8000/api/v1/upload
SCAN_URL=http://localhost:8000/api/v1/scan
PDF_URL=http://localhost:8000/api/v1/download_pdf
DELETE_URL=http://localhost:8000/api/v1/delete_scan
SMTP_SERVER=smtp.yourmail.com
SMTP_PORT=587
EMAIL_SENDER=sender@example.com
EMAIL_RECIPIENT=recipient@example.com
SCAN_DIRECTORY=apk_files
REPORTS_DIRECTORY=reports

3. Prepare APK Files
Place your APKs into the folder defined in SCAN_DIRECTORY (e.g., apk_files/).

4. Run the Script
python mobsf_auto.py

📬 Output
PDF reports saved under reports/{DD-MM-YYYY}/

Email sent with all scan reports as attachments

Console output for progress tracking

💌 Email Template
Each email includes:

A summary message with the scan date

All reports as attachments

A styled HTML layout for clarity

🧼 Old Scan Cleanup
The script removes outdated scan hashes from MobSF before starting a new scan session.

🔐 Security Tip
Avoid hardcoding sensitive data. This project uses .env to safely handle API keys and email credentials.

👩‍💻 Author
Created by Bora Sezgin
For feedback or contributions, feel free to open an issue or PR.


