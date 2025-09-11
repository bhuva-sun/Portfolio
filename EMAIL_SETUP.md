# Email Setup Guide

## Current Setup ✅
Your contact form now works with **mailto** functionality:
- When someone clicks "Send Message", it opens their email client
- Pre-fills your email (bhuvanmadhur@gmail.com) and the message
- Works immediately without any setup

## Upgrade to Professional Email Service

For a more professional experience (emails sent directly from your website), choose one of these free options:

### Option 1: Formspree (Recommended - Free)
1. Go to [formspree.io](https://formspree.io)
2. Sign up with your Gmail account
3. Create a new form
4. Copy the form URL (looks like: `https://formspree.io/f/abc123xyz`)
5. In your `index.html`, change line 395 from:
   ```html
   <form id="contact-form">
   ```
   to:
   ```html
   <form id="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
6. Replace `YOUR_FORM_ID` with your actual form ID

### Option 2: Netlify Forms (If deployed on Netlify)
1. Add `netlify` attribute to your form:
   ```html
   <form id="contact-form" netlify>
   ```
2. Deploy to Netlify - forms will automatically work

### Option 3: EmailJS (More complex but powerful)
1. Go to [emailjs.com](https://emailjs.com)
2. Sign up and configure your Gmail
3. Add their JavaScript library to your site
4. Update the form submission code

## Testing
- **Current (mailto)**: Works immediately - test by filling the form
- **After upgrade**: Emails will be sent directly to your Gmail inbox

The current setup is perfect for getting started! Upgrade when you want a more seamless user experience.
