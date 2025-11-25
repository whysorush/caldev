# GitHub Pages Deployment Guide

## 🚀 Quick Deploy to GitHub Pages

### Step 1: Initialize Git Repository

```bash
cd caldav-standalone
git init
git add .
git commit -m "Initial commit: CalDAV static calendar integration"
```

### Step 2: Connect to GitHub

```bash
git remote add origin https://github.com/whysorush/caldev.git
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository: https://github.com/whysorush/caldev
2. Click on **Settings** tab
3. Scroll down to **Pages** section (left sidebar)
4. Under **Source**, select:
   - Branch: `main`
   - Folder: `/` (root)
5. Click **Save**

### Step 4: Access Your Site

After a few minutes, your site will be live at:

**https://whysorush.github.io/caldev/**

---

## 📁 Files for GitHub Pages

### Required Files:
- ✅ `index.html` - Main static HTML file (already created)
- ✅ `.gitignore` - Ignore node_modules and logs
- ✅ `README.md` - Project documentation

### Optional Files (Not needed for GitHub Pages):
- ❌ `server.js` - Node.js server (not used on GitHub Pages)
- ❌ `package.json` - Node dependencies (not needed)
- ❌ `node_modules/` - Dependencies (excluded)

---

## ✨ Features

The static `index.html` includes:

✅ **Direct Calendar Integration**
  - Google Calendar (one-click)
  - Apple Calendar (data URI)
  - Outlook Calendar (one-click)
  - Download ICS file

✅ **No Backend Required**
  - Pure HTML/CSS/JavaScript
  - Works entirely in browser
  - No server needed

✅ **Easy to Customize**
  - Edit events array in `index.html`
  - Change colors, styles directly
  - Add/remove events easily

---

## 🔧 Customizing Events

To add or modify events, edit the `events` array in `index.html` (around line 200):

```javascript
const events = [
    {
        id: '1',
        uid: 'event-1@caldav-static.com',
        title: 'Your Event Title',
        description: 'Event description',
        location: 'Event location',
        startDate: new Date('2025-12-01T14:00:00Z'),
        endDate: new Date('2025-12-01T15:00:00Z'),
        isAllDay: false,
        category: 'Category'
    },
    // Add more events here...
];
```

After editing:
```bash
git add index.html
git commit -m "Update events"
git push
```

GitHub Pages will automatically update in a few minutes.

---

## 🌐 Custom Domain (Optional)

To use a custom domain:

1. Add a `CNAME` file with your domain:
   ```bash
   echo "yourdomain.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

2. Configure DNS:
   - Add CNAME record: `www` → `whysorush.github.io`
   - Or A records pointing to GitHub Pages IPs

3. Enable HTTPS in GitHub Pages settings

---

## 📊 Differences from Node.js Version

| Feature | Node.js Version | Static Version |
|---------|----------------|----------------|
| Backend Server | ✅ Required | ❌ Not needed |
| Database | ✅ In-memory | ❌ Hardcoded |
| Create Events | ✅ API | ❌ Edit HTML |
| Sync Tracking | ✅ Yes | ❌ No |
| Google Calendar | ✅ Yes | ✅ Yes |
| Apple Calendar | ✅ webcal:// | ✅ data URI |
| Outlook Calendar | ✅ Yes | ✅ Yes |
| Download ICS | ✅ Yes | ✅ Yes |
| Hosting | Node.js host | GitHub Pages |
| Cost | $0-$5/month | **FREE** |

---

## 🎯 Testing Locally

To test before deploying:

1. Open `index.html` in your browser:
   ```bash
   open index.html
   # or
   firefox index.html
   # or
   google-chrome index.html
   ```

2. Or use a simple HTTP server:
   ```bash
   python3 -m http.server 8000
   # Then open http://localhost:8000
   ```

---

## 🔄 Updating Your Site

Whenever you make changes:

```bash
git add .
git commit -m "Describe your changes"
git push
```

GitHub Pages will automatically rebuild and deploy in 1-2 minutes.

---

## 🆘 Troubleshooting

### Site not showing up?
- Wait 2-5 minutes after first push
- Check Settings → Pages for deployment status
- Ensure branch is set to `main` and folder to `/`

### Events not displaying?
- Check browser console for errors (F12)
- Verify `events` array syntax in `index.html`
- Ensure dates are in correct format

### Calendar links not working?
- Google/Outlook: Should open in new tab
- Apple: Downloads ICS file (browser dependent)
- Download: Should download ICS file

---

## 📚 Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Custom Domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [Troubleshooting](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites)

---

## ✅ Checklist

Before deploying:

- [ ] Events data is correct in `index.html`
- [ ] Tested locally by opening `index.html`
- [ ] Git repository initialized
- [ ] Connected to GitHub remote
- [ ] Pushed to `main` branch
- [ ] Enabled GitHub Pages in settings
- [ ] Waited 2-5 minutes for deployment

---

**Your CalDAV calendar integration will be live at:**
**https://whysorush.github.io/caldev/**

🎊 Enjoy your free, static calendar integration!

