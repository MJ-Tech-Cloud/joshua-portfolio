# Contact Form Setup Guide

## 📧 How Your Contact Form Works

When someone fills out the contact form on your website, the message will be sent directly to your email: **joshuamwila2004@gmail.com**

## ✅ Solution 1: PHP Email (Recommended for Imbra)

I've set up a PHP solution that should work with Imbra hosting.

### Files Created:
- `contact.php` - Handles form submissions and sends emails

### How It Works:
1. User fills out the form on your website
2. Form data is sent to `contact.php`
3. PHP script sends an email to your address
4. You receive the email in your inbox

### Setup Steps:

1. **Upload `contact.php` to Imbra**
   - Upload it to the same folder as your `index.html`
   - Make sure PHP is enabled on your Imbra account

2. **Test the Form**
   - Visit your website
   - Fill out the contact form
   - Check your email inbox

3. **If Emails Don't Arrive:**
   - Check your spam/junk folder
   - Verify PHP is enabled in Imbra
   - Contact Imbra support to enable PHP mail function
   - Some hosts require SMTP configuration

### Email Format You'll Receive:
```
Subject: New Contact Form Message from [Name]

You have received a new message from your portfolio website.

Name: [Visitor's Name]
Email: [Visitor's Email]

Message:
[Visitor's Message]
```

---

## 🔄 Solution 2: EmailJS (Alternative - No Backend Required)

If PHP doesn't work on Imbra, use EmailJS instead.

### Advantages:
- ✅ No server-side code needed
- ✅ Works on any hosting
- ✅ Free tier available
- ✅ Easy to set up

### Setup Steps:

1. **Sign Up for EmailJS**
   - Go to [https://www.emailjs.com](https://www.emailjs.com)
   - Create a free account
   - Free tier: 200 emails/month

2. **Set Up Email Service**
   - Go to "Email Services" in dashboard
   - Click "Add New Service"
   - Choose your email provider (Gmail recommended)
   - Connect your email account
   - Copy your Service ID

3. **Create Email Template**
   - Go to "Email Templates"
   - Click "Create New Template"
   - Use this template:
   
   ```
   Subject: New Contact Form Message from {{name}}
   
   You have received a new message from your portfolio website.
   
   Name: {{name}}
   Email: {{email}}
   
   Message:
   {{message}}
   ```
   
   - Save and copy your Template ID

4. **Get Your Public Key**
   - Go to "Account" → "General"
   - Copy your Public Key

5. **Update Your Website**
   - Open `script.js`
   - Find the EmailJS section (I'll add it)
   - Replace these values:
     - `YOUR_SERVICE_ID`
     - `YOUR_TEMPLATE_ID`
     - `YOUR_PUBLIC_KEY`

6. **Add EmailJS Script**
   - Add this to your `index.html` before `</body>`:
   ```html
   <script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
   ```

---

## 🎯 Which Solution Should You Use?

### Use PHP (Solution 1) if:
- ✅ Imbra supports PHP (most hosting does)
- ✅ You want a simple, self-contained solution
- ✅ You don't want to sign up for another service

### Use EmailJS (Solution 2) if:
- ✅ PHP doesn't work on Imbra
- ✅ You want more reliable email delivery
- ✅ You want email analytics
- ✅ You don't mind signing up for a free service

---

## 📬 Where Messages Go

**All messages will be sent to:** `joshuamwila2004@gmail.com`

### Email Details:
- **To:** joshuamwila2004@gmail.com
- **From:** [Visitor's email address]
- **Subject:** New Contact Form Message from [Name]
- **Reply-To:** [Visitor's email address] (so you can reply directly)

---

## 🔍 Troubleshooting

### Problem: Emails not arriving

**Check:**
1. ✅ Spam/Junk folder
2. ✅ PHP is enabled on Imbra
3. ✅ `contact.php` is uploaded correctly
4. ✅ Email address in `contact.php` is correct

**Solutions:**
- Contact Imbra support to enable PHP mail
- Try EmailJS solution instead
- Check Imbra's email settings

### Problem: Form shows error

**Check:**
1. ✅ All fields are filled
2. ✅ Email format is valid
3. ✅ JavaScript is enabled
4. ✅ `contact.php` file exists

---

## 📝 Testing Your Form

1. Visit your website
2. Scroll to Contact section
3. Fill out the form:
   - Name: Test User
   - Email: test@example.com
   - Message: This is a test message
4. Click "Send Message"
5. Check your email inbox (and spam folder)

---

## 💡 Pro Tips

1. **Check Spam Folder**: Form emails often go to spam initially
2. **Reply Directly**: Use the Reply button to respond to visitors
3. **Monitor Regularly**: Check your email daily for new messages
4. **Set Up Filters**: Create email filters to organize form submissions
5. **Backup**: Keep a copy of `contact.php` file

---

## 📞 Need Help?

If you have issues:
1. Check Imbra's documentation
2. Contact Imbra support
3. Try the EmailJS alternative
4. Test with a different email address

Your contact form is now ready to receive messages! 🎉
