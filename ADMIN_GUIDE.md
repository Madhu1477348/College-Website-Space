# Admin Content Management Guide

This guide explains how to manage dynamic content on the College Website, including removing pre-populated data and adding new content for Notifications, Staff, Materials, and Examinations.

## 1. Managing Notifications, Staff, and Materials

You can manage these directly from the **Frontend Admin Dashboard**.

### Accessing the Dashboard

1. Open the website: `http://localhost:5173` (or your deployed URL).
2. Navigate to the **Login** page.
3. Enter your admin credentials.
4. You will be redirected to the **Admin Dashboard**.

### Removing Pre-populated (Static-looking) Data

If you see data that was there by default (test data), you can remove it easily:

1. Go to the relevant tab (e.g., **Manage Notifications**).
2. Look at the list of existing items.
3. Click the **Delete** button next to the item you want to remove.
4. Confirm the deletion.
   - _Note: This permanently removes the data from the database._

### Adding New Content

1. Go to the relevant tab (e.g., **Manage Notifications**).
2. Fill out the form at the top of the section (Title, Content, Category, etc.).
3. Click the **Submit** or **Add** button.
4. The new item will appear in the list immediately.

---

## 2. Managing Examinations

Since the "Examinations" tab is not yet visible on the Frontend Dashboard, you can manage this content via the **Backend Django Admin Panel**.

### Accessing Django Admin

1. Open your browser and go to: `http://localhost:8000/admin/`
2. Log in with your superuser credentials (created via terminal).

### Adding an Examination

1. Under the **CORE** section, click on **Examinations**.
2. Click the **Add Examination +** button in the top right.
3. Fill in the details:
   - **Title**: Name of the exam (e.g., "Inter 1st Year Final Exams").
   - **Category**: Select `Inter` or `Degree`.
   - **File**: Upload the exam schedule or question paper file.
   - **Date**: Select the exam date.
   - **Description**: (Optional) Add extra details.
4. Click **Save**.

### Removing an Examination

1. In the **Examinations** list, click the checkbox next to the exam(s) you want to delete.
2. From the "Action" dropdown at the top, select **Delete selected examinations**.
3. Click **Go** and confirm.

---

## 3. Summary

- **Frontend Dashboard** (`/dashboard`): Use this for day-to-day updates of Notifications, Staff, and Study Materials.
- **Backend Admin** (`/admin`): Use this for managing Examinations and other advanced data until the frontend is updated.
- **Dynamic Data**: All data shown on the website is now dynamic. If you delete an item from the dashboard, it is gone from the website. You do not need to edit any code to change this content.
