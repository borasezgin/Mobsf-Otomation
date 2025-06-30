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

### 1. Clone this repository

```bash
git clone https://github.com/borasezgin/mobsf-auto-scan.git
cd mobsf-auto-scan
