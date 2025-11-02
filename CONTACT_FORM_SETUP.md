# Contact Form Setup Guide

The contact form on `about.html` is configured to use **Formspree**, a free form backend service that handles email delivery.

## Quick Setup (5 minutes)

### Step 1: Sign Up for Formspree
1. Go to [https://formspree.io](https://formspree.io)
2. Click "Get Started" (free tier available)
3. Sign up with your email or GitHub account

### Step 2: Create a New Form
1. Once logged in, click "New Form"
2. Give it a name (e.g., "StratoSentinel Contact Form")
3. Set the email address where you want to receive messages (e.g., michael@stratosentinel.com)
4. Click "Create Form"

### Step 3: Get Your Form Endpoint
After creating the form, you'll see an endpoint URL like:
```
https://formspree.io/f/xyzabc123
```

Copy this URL.

### Step 4: Update about.html
1. Open `about.html`
2. Find line 834 (approximately):
   ```html
   <form id="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
3. Replace `YOUR_FORM_ID` with your actual form ID from Step 3
4. Save the file

### Step 5: Test the Form
1. Open `about.html` in your browser
2. Fill out the contact form
3. Click "Send Message"
4. You should see a green success message
5. Check your email for the form submission

## Features Implemented

✅ **AJAX Form Submission** - No page reload required
✅ **Success Message** - Green notification appears after successful submission
✅ **Error Handling** - Red error message if submission fails
✅ **Loading State** - Button shows "Sending..." while processing
✅ **Form Reset** - Form clears after successful submission
✅ **Auto-hide** - Success message disappears after 5 seconds
✅ **Email Notifications** - You receive an email for each submission

## Success Message
When the form is successfully submitted, users see:
```
✓ Thank you for your message! We'll get back to you shortly.
```

## Error Messages
If something goes wrong, users see helpful error messages:
- Network issues: "Network error. Please check your connection and try again."
- Server issues: "Oops! There was a problem sending your message. Please try again or email us directly."

## Formspree Free Tier Limits
- 50 submissions per month
- Email notifications
- Spam filtering included
- No credit card required

## Alternative: Use Your Own Email Directly
If you don't want to use Formspree, you can replace the form action with:
```html
<form action="mailto:michael@stratosentinel.com" method="POST" enctype="text/plain">
```

However, this opens the user's email client instead of sending via web, which is not as user-friendly.

## Need Help?
- Formspree Documentation: https://help.formspree.io
- Contact: michael@stratosentinel.com
