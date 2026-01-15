# EmailJS Setup Guide - Make Your Contact Form Work Everywhere!

## 🚨 Why Your Form Isn't Working

Your contact form is currently set up for **Netlify Forms**, which only works when your site is deployed on Netlify. If your site is only on GitHub or not deployed yet, the form won't work.

## ✅ Solution: EmailJS (Works Everywhere!)

EmailJS is a free service that sends emails directly from your website without needing a backend server. It works on:
- ✅ GitHub Pages
- ✅ Netlify
- ✅ Any hosting platform
- ✅ Even locally!

**Free Tier:** 200 emails/month (perfect for portfolios!)

---

## 🚀 Quick Setup (5 Minutes)

### Step 1: Sign Up for EmailJS

1. Go to **[emailjs.com](https://www.emailjs.com)**
2. Click "Sign Up" (use Google/GitHub for quick signup)
3. Verify your email address

### Step 2: Connect Your Email Service

1. In EmailJS dashboard, go to **"Email Services"**
2. Click **"Add New Service"**
3. Choose **"Gmail"** (recommended) or your email provider
4. Click **"Connect Account"** and authorize EmailJS
5. **Copy your Service ID** (you'll need this!)

### Step 3: Create Email Template

1. Go to **"Email Templates"**
2. Click **"Create New Template"**
3. Use these settings:

**Template Name:** `Portfolio Contact Form`

**Subject:**
```
New Contact Form Message from {{name}}
```

**Content:**
```
You have received a new message from your portfolio website.

Name: {{name}}
Email: {{email}}

Message:
{{message}}

---
Reply to this email to contact: {{email}}
```

4. **To Email:** `joshuamwila2004@gmail.com`
5. **From Name:** `Portfolio Website`
6. **From Email:** `noreply@emailjs.com` (or your email)
7. Click **"Save"**
8. **Copy your Template ID**

### Step 4: Get Your Public Key

1. Go to **"Account"** → **"General"**
2. Find **"Public Key"**
3. **Copy your Public Key**

### Step 5: Update Your Website

1. Open `script.js` in your code editor
2. Find these lines (around line 80-85):
   ```javascript
   await emailjs.send(
       'YOUR_SERVICE_ID',      // Replace with your EmailJS Service ID
       'YOUR_TEMPLATE_ID',     // Replace with your EmailJS Template ID
   ```

3. Replace the three values:
   - `YOUR_SERVICE_ID` → Your EmailJS Service ID
   - `YOUR_TEMPLATE_ID` → Your EmailJS Template ID  
   - `YOUR_PUBLIC_KEY` → Your EmailJS Public Key

4. Save the file

### Step 6: Push to GitHub

```bash
git add script.js
git commit -m "Add EmailJS contact form support"
git push
```

### Step 7: Test Your Form!

1. Visit your website
2. Fill out the contact form
3. Click "Send Message"
4. Check your email inbox!

---

## 📧 Where Messages Go

**All messages will be sent to:** `joshuamwila2004@gmail.com`

### Email Format:
```
Subject: New Contact Form Message from [Name]

You have received a new message from your portfolio website.

Name: [Visitor's Name]
Email: [Visitor's Email]

Message:
[Visitor's Message]

---
Reply to this email to contact: [Visitor's Email]
```

---

## 🔍 Finding Your IDs

### Service ID
- Location: Email Services → Your Service → Service ID
- Format: `service_xxxxxxx`

### Template ID
- Location: Email Templates → Your Template → Template ID
- Format: `template_xxxxxxx`

### Public Key
- Location: Account → General → Public Key
- Format: `xxxxxxxxxxxxx`

---

## ✅ Testing Checklist

After setup:
- [ ] EmailJS account created
- [ ] Email service connected
- [ ] Template created
- [ ] IDs copied to script.js
- [ ] Form tested on website
- [ ] Email received in inbox
- [ ] Can reply to email

---

## 🚨 Troubleshooting

### Problem: "EmailJS not loaded" error

**Solution:**
- Make sure EmailJS script is in `index.html`
- Check browser console for errors
- Verify internet connection

### Problem: Form shows error message

**Solution:**
- Check that all three IDs are correct in `script.js`
- Verify EmailJS account is active
- Check EmailJS dashboard for errors

### Problem: Emails not arriving

**Solution:**
- Check spam/junk folder
- Verify email address in template: `joshuamwila2004@gmail.com`
- Check EmailJS dashboard → Email Logs
- Verify email service is connected

### Problem: "Service ID not found"

**Solution:**
- Double-check Service ID is correct
- Make sure service is active in EmailJS dashboard
- Try disconnecting and reconnecting email service

---

## 💡 Pro Tips

1. **Test First**: Send a test email to yourself before going live
2. **Monitor Usage**: Check EmailJS dashboard for email count (200/month free)
3. **Spam Protection**: EmailJS includes basic spam protection
4. **Email Logs**: View all sent emails in EmailJS dashboard
5. **Upgrade**: If you exceed 200/month, upgrade is affordable

---

## 📊 EmailJS Dashboard Features

- **Email Logs**: See all sent emails
- **Usage Stats**: Track email count
- **Service Status**: Monitor email service health
- **Template Management**: Edit templates anytime

---

## 🎯 Quick Reference

- **EmailJS Website**: [emailjs.com](https://www.emailjs.com)
- **Your Email**: joshuamwila2004@gmail.com
- **Free Tier**: 200 emails/month
- **Setup Time**: 5 minutes
- **Works On**: Any hosting platform

---

## ✅ After Setup

Once EmailJS is configured:
1. ✅ Form works everywhere (GitHub, Netlify, any hosting)
2. ✅ Emails sent directly to your inbox
3. ✅ No backend server needed
4. ✅ Free and reliable

Your contact form will work perfectly! 🎉

---

**Need Help?**
- EmailJS Docs: [emailjs.com/docs](https://www.emailjs.com/docs)
- EmailJS Support: Available in dashboard
- Check EmailJS dashboard for detailed logs
