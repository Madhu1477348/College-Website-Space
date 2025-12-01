---
description: How to generate a Google App Password for sending emails via Django
---

# How to Generate a Google App Password

To send emails from your application using Gmail, you need an "App Password". This is more secure than using your real password.

## Prerequisites
- You must have a Google Account.
- **2-Step Verification MUST be enabled** on your account.

## Steps

1.  **Log in to your Google Account**:
    - Go to [https://myaccount.google.com/](https://myaccount.google.com/).

2.  **Enable 2-Step Verification**:
    - Click **Security** on the left sidebar.
    - Under "How you sign in to Google", look for **2-Step Verification**.
    - If it is "Off", click it and follow the steps to turn it on.

3.  **Find App Passwords**:
    - Once 2-Step Verification is enabled, go back to the **Security** page.
    - Use the search bar at the top to search for **"App passwords"**.
    - Click on the result **App passwords**.

4.  **Create a New App Password**:
    - You may be asked to sign in again.
    - Under "App name", enter a name like `College Website`.
    - Click **Create**.

5.  **Copy the Password**:
    - A 16-character password will appear (e.g., `abcd efgh ijkl mnop`).
    - **Copy this password**. You will not be able to see it again after you close the window.

6.  **Update Your Django Settings**:
    - Open `backend/college_backend/settings.py`.
    - Update the `EMAIL_HOST_PASSWORD` setting:
      ```python
      EMAIL_HOST_PASSWORD = 'your-16-char-password'
      ```
    - Ensure you remove any spaces if you want (though Google usually accepts it with spaces too, it's safer to remove them or keep it exactly as copied).

## Troubleshooting
- **"App passwords" option missing?**
  - Ensure 2-Step Verification is definitely **ON**.
  - Ensure you are not using a "Security Key" for 2-Step Verification exclusively.
  - If you are on a work/school account, your administrator might have disabled this feature.
