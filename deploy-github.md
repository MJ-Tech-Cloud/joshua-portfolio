# Deploy to GitHub Pages - Step by Step Guide

## Option 1: GitHub Pages (FREE & Recommended)

### Step 1: Create a GitHub Account
1. Go to [github.com](https://github.com) and sign up
2. Verify your email address

### Step 2: Create a New Repository
1. Click the "+" icon in the top right corner
2. Select "New repository"
3. Name it: `joshua-portfolio` (or any name you prefer)
4. Make it **Public** (required for free hosting)
5. Don't initialize with README (we'll upload our files)
6. Click "Create repository"

### Step 3: Upload Your Files
1. In your new repository, click "uploading an existing file"
2. Drag and drop all your files:
   - `index.html`
   - `styles.css`
   - `script.js`
   - `joshua.jpg`
   - `README.md`
3. Add a commit message: "Initial portfolio website"
4. Click "Commit changes"

### Step 4: Enable GitHub Pages
1. Go to your repository settings (Settings tab)
2. Scroll down to "Pages" section
3. Under "Source", select "Deploy from a branch"
4. Choose "main" branch
5. Click "Save"

### Step 5: Your Website is Live!
- Your site will be available at: `https://yourusername.github.io/joshua-portfolio`
- It may take a few minutes to go live
- You can customize the domain later

## Alternative: Netlify (Also FREE)

### Step 1: Create Netlify Account
1. Go to [netlify.com](https://netlify.com)
2. Sign up with GitHub

### Step 2: Deploy
1. Click "New site from Git"
2. Choose GitHub
3. Select your repository
4. Click "Deploy site"

### Step 3: Custom Domain (Optional)
- Netlify gives you a random URL like: `https://amazing-site-123.netlify.app`
- You can add a custom domain later

## 🚀 **Quick Start Commands**

If you're comfortable with Git, here are the commands:

```bash
# Initialize Git repository
git init

# Add all files
git add .

# Commit changes
git commit -m "Initial portfolio website"

# Add GitHub remote (replace with your repository URL)
git remote add origin https://github.com/yourusername/joshua-portfolio.git

# Push to GitHub
git push -u origin main
```

## 📝 **Next Steps After Hosting**

1. **Test your website** - Make sure everything works
2. **Add a custom domain** (optional but professional)
3. **Set up Google Analytics** (optional)
4. **Share your URL** with potential clients

## 💡 **Pro Tips**

- **GitHub Pages** is perfect for portfolios and free forever
- **Netlify** offers more features and better performance
- Both options are completely free for personal projects
- You can always upgrade to paid hosting later

Your portfolio will be live and accessible to anyone with the URL! 