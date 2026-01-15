# Contact Form Troubleshooting Guide

## 🔍 Current Error: "Sorry, there was an error sending your message"

This error means EmailJS is trying to send but something is failing. Let's fix it step by step.

## ✅ Step 1: Check Browser Console

1. Open your website
2. Press **F12** (or right-click → Inspect)
3. Go to **Console** tab
4. Try submitting the form
5. Look for **red error messages**
6. **Copy the exact error message** you see

## ✅ Step 2: Verify EmailJS Template Variables

The most common issue is **template variables not matching**.

### In Your EmailJS Dashboard:

1. Go to **Email Templates**
2. Click on your template: `template_uhkxkff`
3. Check what variables you're using in the template

### Your Template Should Use:

**Subject Line:**
```
New Contact Form Message from {{name}}
```

**Email Body:**
```
You have received a new message from your portfolio website.

Name: {{name}}
Email: {{email}}

Message:
{{message}}

---
Reply to: {{email}}
```

### Important:
- Use `{{name}}` (not `{{from_name}}`)
- Use `{{email}}` (not `{{from_email}}`)
- Use `{{message}}` (exactly as shown)

## ✅ Step 3: Verify EmailJS Service

1. Go to **Email Services** in EmailJS dashboard
2. Make sure `service_smoy6yt` is:
   - ✅ **Active** (not paused)
   - ✅ **Connected** to your email
   - ✅ **Verified** (green checkmark)

## ✅ Step 4: Check EmailJS Account

1. Go to **Account** → **General**
2. Verify:
   - ✅ Account is active
   - ✅ Public Key matches: `8eGa_zxTA7wQwtGWy`
   - ✅ You haven't exceeded free tier (200 emails/month)

## ✅ Step 5: Test EmailJS Directly

1. Go to EmailJS dashboard
2. Click **Email Templates**
3. Click **Test** on your template
4. Fill in test values:
   - name: Test User
   - email: test@example.com
   - message: This is a test
5. Click **Send Test Email**
6. Check if you receive the email

**If test email works:** The issue is in the website code
**If test email fails:** The issue is in EmailJS configuration

## 🚨 Common Errors & Fixes

### Error: "Service not found"
**Fix:** 
- Verify Service ID: `service_smoy6yt`
- Make sure service is active in EmailJS dashboard

### Error: "Template not found"
**Fix:**
- Verify Template ID: `template_uhkxkff`
- Make sure template is saved and active

### Error: "Invalid public key"
**Fix:**
- Check Public Key in Account → General
- Should be: `8eGa_zxTA7wQwtGWy`

### Error: "Template variables don't match"
**Fix:**
- Make sure template uses: `{{name}}`, `{{email}}`, `{{message}}`
- Check for typos in variable names

### Error: "Email service not connected"
**Fix:**
- Go to Email Services
- Reconnect your email service (Gmail/Outlook)
- Verify connection is active

## 🔧 Quick Fix: Update Template Variables

If your template uses different variable names, update `script.js`:

Find this section (around line 136):
```javascript
const templateParams = {
    name: name,
    email: email,
    message: message,
    from_name: name,
    from_email: email,
    reply_to: email
};
```

**Change the variable names to match your EmailJS template.**

For example, if your template uses `{{user_name}}` instead of `{{name}}`, change:
```javascript
const templateParams = {
    user_name: name,  // Changed from 'name'
    user_email: email, // Changed from 'email'
    user_message: message // Changed from 'message'
};
```

## 📧 Alternative: Check EmailJS Logs

1. Go to EmailJS dashboard
2. Click **Email Logs** (or **Activity**)
3. Look for recent attempts
4. Check error messages there

## 🆘 Still Not Working?

1. **Check browser console** - Copy the exact error
2. **Check EmailJS dashboard** - Look for error messages
3. **Verify all IDs are correct:**
   - Service ID: `service_smoy6yt`
   - Template ID: `template_uhkxkff`
   - Public Key: `8eGa_zxTA7wQwtGWy`
4. **Test with EmailJS test feature** - See if template works
5. **Check email service connection** - Make sure it's connected

## 💡 Pro Tip

The browser console will now show **detailed error messages**. After you submit the form:
1. Open Console (F12)
2. Look for error messages
3. Copy the error and share it for more specific help

---

**Most likely issue:** Template variables don't match. Make sure your EmailJS template uses `{{name}}`, `{{email}}`, and `{{message}}` exactly as shown above.
