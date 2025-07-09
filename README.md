# Bulk Mail Dispatcher

This project is a web-based bulk email dispatcher built with Flask. It allows users to send personalized emails to multiple recipients by uploading a CSV file containing email addresses. The application provides a simple web interface for entering email details, composing the message, and tracking successful deliveries.

## Features

- Upload a CSV file of email addresses.
- Enter sender email, password, subject, and email body.
- Sends emails in bulk to all valid addresses in the CSV.
- Displays a list of successfully sent emails.
- Responsive web interface with loading spinner for feedback.

## Folder Structure

| File/Folder        | Description                                      |
|--------------------|--------------------------------------------------|
| `app.py`           | Main Flask application.                          |
| `bulkMail.py`      | Handles email validation and sending logic.      |
| `static/`          | Static files (JS, CSS, images).                  |
| &nbsp;&nbsp;├── `script.js`    | Shows loading spinner during mail send.          |
| &nbsp;&nbsp;├── `styles.css`   | Styles for the web interface.                    |
| &nbsp;&nbsp;└── `ZCum.gif`     | Loading or decorative GIF.                       |
| `templates/`       | HTML templates for the app.                      |
| &nbsp;&nbsp;├── `index.html`   | Main form for email input and file upload.        |
| &nbsp;&nbsp;└── `success.html` | Shows list of emails sent successfully.           |

## Requirements

- Python 3.x
- Flask
- smtplib (standard library)
- ssl (standard library)
- re (standard library)
- csv (standard library)

Install Flask using pip:

```
pip install flask
```


## Usage

1. **Clone the repository** and ensure all files and folders are present.
2. **Run the Flask app:**

    ```
    python app.py
    ```

3. **Open your browser** and go to `http://127.0.0.1:5000/`.
4. **Fill out the form:**
    - Enter your email address and password (ensure you have enabled "App Passwords" or "Less Secure Apps" if using Gmail).
    - Enter the subject and compose your email.
    - Upload a CSV file with recipient email addresses (first column, header row required).
5. **Submit the form.** The app will send emails and display the list of successful deliveries.

## CSV File Format

- The CSV file should have a header row.
- Email addresses must be in the first column.
- Example:

    ```
    Email
    user1@example.com
    user2@example.com
    ```

## Notes

- The sender email and password are required to authenticate with the SMTP server.
- Only valid email addresses are used; invalid addresses are skipped.
- For Gmail, you may need to generate an App Password or enable access for less secure apps.

