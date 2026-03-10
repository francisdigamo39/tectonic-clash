# 🚀 DEPLOYMENT GUIDE - Step by Step

## Complete guide to deploy Tectonic Clash to the web

---

## 🎯 CHOOSE YOUR PLATFORM

Pick ONE deployment method:

1. **GitHub Pages** - Best for schools, free forever
2. **Netlify** - Easiest, drag & drop
3. **Vercel** - Fast, modern
4. **School Server** - If you have one

---

## 📘 METHOD 1: GITHUB PAGES (Recommended)

### **Why GitHub Pages?**
- ✅ Completely free
- ✅ Reliable (99.9% uptime)
- ✅ Automatic HTTPS
- ✅ Easy updates
- ✅ Professional URL

### **Step-by-Step:**

#### **1. Create GitHub Account**
1. Go to https://github.com
2. Click "Sign up"
3. Use your school email
4. Verify email
5. ✅ Account created!

#### **2. Create Repository**
1. Click "+" (top right) > "New repository"
2. **Repository name:** `tectonic-clash`
3. **Description:** "Interactive plate tectonics game for Grade 10"
4. **Public** (leave checked)
5. **DON'T** check "Add README"
6. Click "Create repository"
7. ✅ Repository created!

#### **3. Upload Files**
1. Click "uploading an existing file"
2. Drag ALL files from `/PRODUCTION/` folder:
   - index.html
   - manifest.json
   - service-worker.js
3. **Commit message:** "Initial upload"
4. Click "Commit changes"
5. ✅ Files uploaded!

#### **4. Enable GitHub Pages**
1. Click "Settings" tab
2. Scroll to "Pages" (left sidebar)
3. **Source:** Deploy from a branch
4. **Branch:** `main`
5. **Folder:** `/ (root)`
6. Click "Save"
7. Wait 1-2 minutes
8. ✅ Site published!

#### **5. Get Your URL**
Your URL will be:
```
https://YOUR-USERNAME.github.io/tectonic-clash/
```

**Example:** `https://mrsanchez.github.io/tectonic-clash/`

#### **6. Test Your Site**
1. Open URL in browser
2. Game should load
3. Test on phone
4. Try teacher login
5. ✅ Working!

### **Updating Later:**
1. Go to repository
2. Click file to edit
3. Click pencil icon (edit)
4. Make changes
5. Commit
6. Site updates in ~1 minute!

---

## 📗 METHOD 2: NETLIFY (Easiest)

### **Why Netlify?**
- ✅ Drag & drop deployment
- ✅ Instant URL
- ✅ Free SSL
- ✅ Auto-updates from GitHub (optional)
- ✅ Custom domains easy

### **Step-by-Step:**

#### **1. Sign Up**
1. Go to https://www.netlify.com
2. Click "Sign up"
3. Use GitHub/Email
4. ✅ Account created!

#### **2. Deploy**
1. Click "Add new site" > "Deploy manually"
2. **Drag entire `/PRODUCTION/` folder** onto the drop zone
3. Wait 30 seconds
4. ✅ Site deployed!

#### **3. Get Your URL**
Netlify gives you:
```
https://RANDOM-NAME.netlify.app/
```

**Example:** `https://tectonic-clash-school.netlify.app/`

#### **4. Customize URL (Optional)**
1. Click "Site settings"
2. Click "Change site name"
3. Enter: `yourschool-tectonic`
4. Save
5. New URL: `https://yourschool-tectonic.netlify.app/`

#### **5. Add Custom Domain (Optional)**
1. Buy domain: `tectonicclash.yourschool.edu`
2. In Netlify: Domain settings > Add domain
3. Follow DNS instructions
4. ✅ Custom domain!

### **Updating Later:**
1. Drag new `/PRODUCTION/` folder
2. Site updates instantly!

**OR** connect to GitHub for auto-updates.

---

## 📙 METHOD 3: VERCEL

### **Why Vercel?**
- ✅ Super fast
- ✅ Great developer tools
- ✅ Free tier generous
- ✅ Easy GitHub integration

### **Step-by-Step:**

#### **1. Sign Up**
1. Go to https://vercel.com
2. Sign up with GitHub
3. ✅ Account created!

#### **2. Deploy**
1. Click "Add New..." > "Project"
2. **Import from GitHub:** Upload your repo
   OR
   **Upload folder:** Drag `/PRODUCTION/`
3. Click "Deploy"
4. Wait 30 seconds
5. ✅ Deployed!

#### **3. Get URL**
```
https://tectonic-clash.vercel.app/
```

#### **4. Custom Domain (Optional)**
Same as Netlify - easy to add.

### **Updating:**
- Push to GitHub = auto-deploy
- Or drag new folder

---

## 📕 METHOD 4: SCHOOL SERVER

### **Requirements:**
- Web server access
- FTP/SFTP or file upload
- HTTPS recommended (for PWA)

### **Step-by-Step:**

#### **1. Upload Files**
1. Connect via FTP (FileZilla, etc.)
2. Upload to public folder:
   ```
   /public_html/tectonic-clash/
   ```
3. Upload ALL files from `/PRODUCTION/`

#### **2. Set Permissions**
- Files: 644
- Folders: 755

#### **3. Test**
Visit: `https://yourschool.edu/tectonic-clash/`

#### **4. HTTPS Setup**
If no HTTPS:
- Contact IT department
- Request SSL certificate
- Or use Cloudflare (free)

---

## 🔧 POST-DEPLOYMENT SETUP

### **After deploying, do these:**

#### **1. Change Admin Password**
1. Download your deployed `index.html`
2. Open in text editor
3. Find (around line 2773):
   ```javascript
   const ADMIN_CONFIG={password:'teacher2026',...
   ```
4. Change to:
   ```javascript
   const ADMIN_CONFIG={password:'YourNewPassword123',...
   ```
5. Save
6. Re-upload to server

#### **2. Test Everything**
- [ ] Game loads
- [ ] Sounds work
- [ ] Teacher login works (new password)
- [ ] Questions display
- [ ] Admin panel accessible
- [ ] CSV export works
- [ ] Install to home screen works

#### **3. Create Student Materials**
- Print URL as QR code
- Create instruction sheet
- Demo in class

---

## 📱 STUDENT ACCESS INSTRUCTIONS

### **Create this handout for students:**

---

**TECTONIC CLASH - How to Install**

**Your URL:** `https://your-url-here.com`

**On iPhone/iPad:**
1. Open **Safari** browser
2. Go to URL above
3. Tap **Share** button (⎆)
4. Scroll and tap **"Add to Home Screen"**
5. Tap **"Add"**
6. Find "Tectonic Clash" icon on home screen!

**On Android:**
1. Open **Chrome** browser
2. Go to URL above
3. Tap **"Install app"** when it pops up
   - OR: Menu (⋮) > "Install app"
4. Tap **"Install"**
5. Find app in app drawer!

**On Computer:**
1. Open Chrome or Edge
2. Go to URL above
3. Click install icon in address bar
4. Click "Install"

**Works Offline!**
After first visit, you can play without internet.

---

---

## 🎯 TESTING CHECKLIST

Before sharing with students:

### **Desktop Testing:**
- [ ] Chrome - loads correctly
- [ ] Firefox - loads correctly
- [ ] Edge - loads correctly
- [ ] Safari - loads correctly

### **Mobile Testing:**
- [ ] iPhone (Safari) - loads and installs
- [ ] Android (Chrome) - loads and installs
- [ ] Sounds work after tap
- [ ] Touch events responsive
- [ ] Admin panel works on mobile

### **Functionality Testing:**
- [ ] All 3 levels accessible
- [ ] Questions randomize
- [ ] Scoring works
- [ ] Teacher login works
- [ ] Question CRUD works
- [ ] CSV export downloads
- [ ] Offline mode works (airplane mode test)

---

## 🔄 UPDATING YOUR DEPLOYED GAME

### **GitHub Pages:**
1. Go to repository
2. Click file to edit
3. Make changes
4. Commit
5. Wait 1 minute
6. ✅ Updated!

### **Netlify:**
**Option A:** Drag new folder
**Option B:** Git push (if connected)

### **Vercel:**
**Option A:** Import new version
**Option B:** Git push (if connected)

### **School Server:**
FTP upload new files

---

## 📊 MONITORING USAGE

### **View Student Progress:**
1. Go to your URL
2. Click "Teacher Login"
3. Enter password
4. View Dashboard

### **Export Data:**
1. Teacher Dashboard
2. Click "📥 Export CSV"
3. Open in Excel/Sheets
4. Analyze student performance

---

## 🎨 CUSTOMIZATION TIPS

### **Add School Branding:**
1. Edit `index.html`
2. Find game title section
3. Add school name:
   ```html
   <div class="game-subtitle">
     Your School Name - Earth Science
   </div>
   ```

### **Add Custom Questions:**
1. Teacher Login
2. Manage Questions
3. Add your content!

### **Change Colors (Advanced):**
1. Edit CSS variables in `<style>` section
2. Find `:root` section
3. Change color codes

---

## 🐛 TROUBLESHOOTING DEPLOYMENT

### **Site won't load:**
- Check all files uploaded
- Verify file names exact (case-sensitive)
- Check browser console (F12)

### **GitHub Pages 404 error:**
- Wait 2-3 minutes after enabling
- Check branch is `main` not `master`
- Verify files in root folder

### **Netlify deploy fails:**
- Check folder contains index.html
- Re-drag folder
- Try uploading files individually

### **No HTTPS (HTTP only):**
- GitHub Pages has auto HTTPS
- Netlify has auto HTTPS
- School server: contact IT

---

## 📞 GETTING HELP

### **GitHub Pages Issues:**
- Docs: https://docs.github.com/pages
- Status: https://www.githubstatus.com

### **Netlify Issues:**
- Docs: https://docs.netlify.com
- Support: https://answers.netlify.com

### **General Issues:**
- Check browser console (F12)
- Verify file paths
- Test in incognito mode

---

## ✅ DEPLOYMENT COMPLETE!

**You did it!** 🎉

Your game is now:
- ✅ Live on the internet
- ✅ Accessible to students
- ✅ Installable to devices
- ✅ Ready for classroom use

**Next steps:**
1. Share URL with students
2. Demo installation in class
3. Monitor progress via admin panel
4. Collect and analyze data

---

## 🌟 BONUS: ADVANCED SETUPS

### **Custom Domain:**
Purchase domain like `tectonics.yourschool.edu`

**GitHub Pages:**
1. Buy domain
2. Repository Settings > Pages > Custom domain
3. Add CNAME record in DNS
4. Done!

**Netlify/Vercel:**
Similar process, follow their docs.

### **Analytics (Optional):**
Add Google Analytics to track usage:
1. Get tracking ID
2. Add code to `<head>` section
3. Redeploy

### **Cloud Sync Setup:**
For multi-device syncing:
1. Get JSONBin account (free)
2. Teacher Login > Setup
3. Add API key
4. Create bins
5. ✅ Synced!

---

**Congratulations on your deployment!** 🎊

**Your students can now learn plate tectonics anywhere, anytime!** 🌍

