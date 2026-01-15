# Deploy Your Portfolio to GitHub - Step by Step Guide

## 🚀 Quick Steps to Deploy to GitHub

### Option 1: Using GitHub Desktop (Easiest - No Commands)

1. **Download GitHub Desktop**
   - Go to [desktop.github.com](https://desktop.github.com)
   - Download and install GitHub Desktop

2. **Sign In**
   - Open GitHub Desktop
   - Sign in with your GitHub account (or create one)

3. **Create Repository**
   - Click "File" → "New Repository"
   - Name: `joshua-portfolio` (or any name you like)
   - Choose your website folder location
   - Click "Create Repository"

4. **Commit Files**
   - You'll see all your files listed
   - Write a commit message: "Initial portfolio website"
   - Click "Commit to main"

5. **Publish to GitHub**
   - Click "Publish repository"
   - Make it Public (required for free hosting)
   - Click "Publish"

6. **Done!** Your code is now on GitHub!

---

### Option 2: Using Command Line (Terminal/PowerShell)

#### Step 1: Open Terminal in Your Project Folder

**Windows:**
- Right-click your folder → "Open in Terminal"
- OR Open PowerShell in your folder

**Mac/Linux:**
- Right-click folder → "Open in Terminal"

#### Step 2: Initialize Git Repository

```bash
git init
```

#### Step 3: Add All Files

```bash
git add .
```

#### Step 4: Create First Commit

```bash
git commit -m "Initial portfolio website"
```

#### Step 5: Create GitHub Repository

1. Go to [github.com](https://github.com)
2. Click the "+" icon → "New repository"
3. Name it: `joshua-portfolio`
4. Make it **Public**
5. **Don't** initialize with README
6. Click "Create repository"

#### Step 6: Connect and Push

GitHub will show you commands. Use these:

```bash
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/joshua-portfolio.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username!

---

## 📁 Files That Will Be Uploaded

Your GitHub repository will include:
- ✅ `index.html` - Main website
- ✅ `styles.css` - Styling
- ✅ `script.js` - Functionality
- ✅ `joshua.jpg` - Your photo
- ✅ `README.md` - Documentation
- ✅ `netlify.toml` - Netlify config
- ✅ `.gitignore` - Git ignore file

---

## 🔗 After Uploading to GitHub

### Deploy to Netlify from GitHub:

1. **Go to Netlify**
   - Visit [netlify.com](https://netlify.com)
   - Sign up/login (use GitHub to connect)

2. **Import from GitHub**
   - Click "Add new site" → "Import an existing project"
   - Choose GitHub
   - Select your `joshua-portfolio` repository
   - Click "Deploy site"

3. **Configure Build Settings**
   - Build command: Leave empty (no build needed)
   - Publish directory: Leave empty (or `/`)
   - Click "Deploy"

4. **Set Up Forms** (After deployment)
   - Go to Forms → Form notifications
   - Add email: `joshuamwila2004@gmail.com`

---

## ✅ Benefits of GitHub

- ✅ **Version Control** - Track changes to your code
- ✅ **Backup** - Your code is safe in the cloud
- ✅ **Easy Updates** - Update site by pushing changes
- ✅ **Collaboration** - Share with others if needed
- ✅ **Free Hosting** - Can use GitHub Pages too

---

## 🔄 Updating Your Website Later

### Using GitHub Desktop:
1. Make changes to your files
2. In GitHub Desktop, write commit message
3. Click "Commit to main"
4. Click "Push origin"

### Using Command Line:
```bash
git add .
git commit -m "Updated portfolio"
git push
```

Then Netlify will automatically redeploy!

---

## 🎯 Your GitHub Repository URL

After pushing, your repository will be at:
`https://github.com/YOUR_USERNAME/joshua-portfolio`

---

## 💡 Pro Tips

1. **Commit Often** - Save your progress regularly
2. **Write Good Commit Messages** - Describe what you changed
3. **Keep Repository Public** - Required for free hosting
4. **Use GitHub Desktop** - Easier than command line

---

## 🚨 Troubleshooting

### Problem: "Repository not found"
- Check your GitHub username is correct
- Make sure repository is Public

### Problem: "Permission denied"
- Make sure you're logged into GitHub
- Check your GitHub credentials

### Problem: Files not uploading
- Make sure you're in the correct folder
- Check `.gitignore` isn't excluding files

---

## 📞 Need Help?

- **GitHub Docs**: [docs.github.com](https://docs.github.com)
- **GitHub Desktop Help**: Check Help menu
- **Git Basics**: [git-scm.com/doc](https://git-scm.com/doc)

Your portfolio will be on GitHub and ready to deploy! 🎉
