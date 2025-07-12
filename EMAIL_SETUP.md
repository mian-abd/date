# Email Setup Guide

To make the email functionality work, you need to set up EmailJS. Follow these steps:

## 1. Sign up for EmailJS
- Go to https://www.emailjs.com/
- Create a free account
- Verify your email address

## 2. Add Email Service
- In EmailJS dashboard, go to "Email Services"
- Click "Add New Service"
- Choose your email provider (Gmail, Outlook, etc.)
- Follow the setup instructions
- Note down your **Service ID**

## 3. Create Email Template
- Go to "Email Templates"
- Click "Create New Template"
- Use this template:

```
Subject: New Date Plan Submission

Hello!

Someone has completed the date planning form. Here are their selections:

Answer: {{answer}}
Selected Date: {{selected_date}}
Food Choices: {{selected_food}}
Dessert Choices: {{selected_dessert}}
Activities: {{selected_activities}}
Timestamp: {{timestamp}}

Best regards,
Your Date Planning App
```

- Save the template and note down your **Template ID**

## 4. Get Your Public Key
- Go to "Account" → "API Keys"
- Copy your **Public Key**

## 5. Update the Code
Replace the following placeholders in all HTML files:

- `YOUR_PUBLIC_KEY` → Your EmailJS Public Key
- `YOUR_SERVICE_ID` → Your Email Service ID  
- `YOUR_TEMPLATE_ID` → Your Email Template ID

## 6. Test the Setup
- Open index.html in a web browser
- Complete the form
- Check if you receive the email at maabhai549@gmail.com

## Files to Update:
- index.html
- date.html
- food.html
- dessert.html
- activities.html
- lastpage.html

## Example:
```javascript
emailjs.init("abc123def456"); // Your Public Key
emailjs.send('service_xyz', 'template_abc', templateParams); // Your Service ID and Template ID
```

## Troubleshooting:
- Make sure all IDs are correct
- Check browser console for errors
- Verify your email service is properly connected
- Ensure you're not exceeding EmailJS free tier limits (200 emails/month) 