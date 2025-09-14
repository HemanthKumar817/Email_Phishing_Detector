# Phishing Email Detector with Quarantine and Alerts

This project is a Python-based tool to detect suspicious phishing emails, quarantine them, and notify the security team. It integrates with the VirusTotal API to analyze URLs found in emails and helps organizations stay protected from phishing attacks.

---

## Features

* **Automatic Email Scanning** – Fetches unread emails from an inbox.
* **Phishing Detection** – Extracts URLs from emails and checks them with VirusTotal.
* **Email Quarantine** – Moves suspicious emails to a quarantine folder.
* **Alert System** – Sends an alert email to the security team when a phishing attempt is detected.
* **Logging** – Records details of flagged emails for future review.

---

## Requirements

* Python 3.6+
* Packages: `requests`, `imaplib`, `email`, `re`, `base64`
* A VirusTotal API key

Install required packages with:

```bash
pip install requests
```

---

## Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/email-phishing-detector.git
   cd email-phishing-detector
   ```

2. **(Optional) Create a Virtual Environment**

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Configure Email and VirusTotal API**

   * Open `email_handler.py` and update:

     ```python
     EMAIL_ADDRESS = 'your_email@example.com'
     EMAIL_PASSWORD = 'your_password'
     IMAP_SERVER = 'imap.example.com'
     ```
   * Open `phishing_detection.py` and update:

     ```python
     api_key = 'your_virustotal_api_key'
     ```

---

## Usage

Run the program:

```bash
python main.py
```

The script will:

1. Connect to your email inbox and fetch unread messages.
2. Scan each email for URLs.
3. Use VirusTotal to check if URLs are malicious.
4. Quarantine flagged emails.
5. Send an alert to the security team.
6. Log the details.

---

## Project Files

* `main.py` – Entry point for running the system
* `email_handler.py` – Handles connecting to email and fetching messages
* `phishing_detection.py` – Uses VirusTotal API to scan URLs
* `quarantine.py` – Moves flagged emails into quarantine
* `alert.py` – Sends alert notifications
* `logger.py` – Records details of flagged emails

---

## Disclaimer

This tool is for educational and security awareness purposes. **Only use it with email accounts you are authorized to monitor.** Unauthorized use may be illegal or against organizational policies.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
