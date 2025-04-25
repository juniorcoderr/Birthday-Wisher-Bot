## 🎉 Birthday Wisher Bot 🎂

This repository contains a simple yet effective Python script that automatically sends birthday wishes via email to your friends or loved ones. By maintaining a list of birthdays in a `.csv` file, the script checks daily for matches and sends a personalized birthday message using a pre-written letter template.

### 💡 Features

- Automatically checks for birthdays every day
- Sends personalized birthday wishes via email
- Uses SMTP (Gmail) for sending emails securely
- Easily extendable with multiple letter templates

### 🛠 Technologies Used

- **Python**
- `datetime` for date handling
- `pandas` for reading and processing the CSV file
- `smtplib` for sending emails

### 📁 Project Structure

```
birthday-wisher/
├── birthdays.csv               # CSV file with birthday data
├── letter_templates/
│   └── letter_1.txt            # Template with a placeholder [NAME]
├── main.py                     # Main script
```

### 📝 `birthdays.csv` Format

Make sure your `birthdays.csv` file is formatted like this:

```csv
name,email,year,month,day
John Doe,john@example.com,1995,4,25
Jane Smith,jane@example.com,1990,12,31
```

### ✉️ Email Template (`letter_1.txt`)

The template should contain the placeholder `[NAME]` which will be replaced by the birthday person's name:

```
Dear [NAME],

Wishing you a fantastic birthday filled with joy and laughter! 🥳

Best wishes,
Your Friend
```

### 🔒 Environment Setup

Update the following variables in the script with your own email credentials:

```python
MY_EMAIL = "your_email@gmail.com"
MY_PASSWORD = "your_app_password"  # Use an app-specific password if using Gmail
```

💡 **Tip:** For Gmail, enable 2FA and generate an [App Password](https://support.google.com/accounts/answer/185833?hl=en) for secure access.

---

### 🚀 How to Run

1. Clone the repo
2. Install dependencies (only `pandas` needed):
   ```bash
   pip install pandas
   ```
3. Schedule the script to run daily using a scheduler:
   - **Windows**: Task Scheduler
   - **macOS/Linux**: `cron` job
4. Sit back and let the script do the wishing! 🎉

---

### 📌 TODO (Optional Enhancements)

- Support for multiple letter templates
- Logging of sent emails
- HTML emails for better design
- Notification for upcoming birthdays
