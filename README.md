# Resume Analyzer – AI-Powered Screening with Gemini AI

A fully automated resume analyzer that evaluates resumes based on a job description, stores results in Google Sheets, sends email notifications, and provides a chat interface using Gemini AI.

---

## Table of Contents

1. Project Overview
2. Features
3. Project Structure
4. Setup Instructions
5. How to Get Gemini API Key
6. How to Get Google Sheet ID
7. Environment Variables
8. Running the Project
9. Screenshots
10. License

---

## Project Overview

This project allows users to:

* Upload resumes (PDF/DOC/DOCX).
* Automatically analyze resumes against a job description.
* Calculate a score and provide a recommendation (Accepted/Rejected).
* Store all submissions in a Google Sheet.
* Send automated emails to applicants.
* Chat with Gemini AI assistant for project queries.

The front-end is a modern, animated interface with a gradient background, floating bubbles, and transparent cards.

---

## Features

* Resume parsing (PDF, DOC, DOCX).
* Keyword-based scoring against job description.
* Google Sheets integration to save results.
* Email notifications using Gmail SMTP.
* Gemini AI chatbot integration.
* Responsive design with animated background and loading indicators.
* Enter key submission for forms and chat.

---

## Project Structure

```
resume-analyzer/
│
├─ uploads/                # Folder to store uploaded resumes
├─ main.py                 # Flask backend
├─ abc.html                # Frontend HTML file
├─ credentials.json        # Google service account credentials
├─ linkedin.png            # LinkedIn logo for header
├─ gemini.png              # Gemini logo for header
├─ .env                    # Environment variables
└─ README.md               # Project documentation
```

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/resume-analyzer.git
cd resume-analyzer
```

### 2. Create Python Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate   # Linux/macOS
venv\Scripts\activate    # Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Environment Variables

Create a `.env` file in the root folder with:

```
EMAIL_ADDRESS=your-email@gmail.com
EMAIL_PASSWORD=your-app-password
API_KEY=<Your Gemini API Key>
```

* **EMAIL\_PASSWORD:** Use a Gmail App Password, not your normal password.

---

## How to Get Gemini API Key

1. Go to [Google Cloud Console](https://console.cloud.google.com/).
2. Create or select a project.
3. Enable **Generative AI API**.
4. Go to **API & Services > Credentials**.
5. Click **Create API Key**.
6. Copy the API Key and add it to `.env` as `API_KEY`.

---

## How to Get Google Sheet ID

1. Create a Google Sheet (any name).
2. Copy the ID from URL:

```
https://docs.google.com/spreadsheets/d/<THIS_IS_THE_ID>/edit#gid=0
```

3. Share the Sheet with your service account email from `credentials.json` with **Editor** access.
4. Add the Sheet ID to `SHEET_ID` in `main.py`.

---

## Environment Variables

* `EMAIL_ADDRESS`: Gmail address to send emails.
* `EMAIL_PASSWORD`: Gmail App Password.
* `API_KEY`: Gemini API Key.

---

## Running the Project

1. Start the Flask server:

```bash
python main.py
```

2. Open in browser:

```
http://127.0.0.1:5000
```

3. Upload resumes and interact with Gemini AI.

---

## Screenshots

* Animated background with floating bubbles.
* Transparent cards for form and chat.
* Resume analysis with loading indicator.
* Chat interface with Gemini AI responses.

---

## License

MIT License © 2025 Abrar Ahmad
