# CalDAV Calendar Integration - Static Version

> **Live Demo:** https://whysorush.github.io/caldev/

A beautiful, static calendar event integration that works with Google Calendar, Apple Calendar, and Outlook Calendar. No backend server required - perfect for GitHub Pages!

## ✨ Features

- 📅 **Google Calendar Integration** - One-click add to Google Calendar
- 🍎 **Apple Calendar Support** - Direct download for Apple Calendar
- 📧 **Outlook Calendar Integration** - One-click add to Outlook Calendar
- ⬇️ **ICS File Download** - Compatible with any calendar app
- 🎨 **Beautiful UI** - Modern gradient design with smooth animations
- 📱 **Responsive** - Works on desktop, tablet, and mobile
- 🚀 **No Backend** - Pure HTML/CSS/JavaScript
- ✅ **No Authentication** - Zero login required
- 🆓 **Free Hosting** - Hosted on GitHub Pages

## 🌐 Live Demo

Visit: **https://whysorush.github.io/caldev/**

## 🚀 Quick Start

### Option 1: View Locally

Simply open `index.html` in your browser:

```bash
open index.html
```

### Option 2: Deploy to GitHub Pages

1. **Initialize Git:**
   ```bash
   cd caldav-standalone
   git init
   git add .
   git commit -m "Initial commit"
   ```

2. **Push to GitHub:**
   ```bash
   git remote add origin https://github.com/whysorush/caldev.git
   git branch -M main
   git push -u origin main
   ```

3. **Enable GitHub Pages:**
   - Go to repository Settings
   - Navigate to Pages section
   - Select branch: `main`, folder: `/`
   - Save

4. **Access your site:**
   - https://whysorush.github.io/caldev/

## 📝 Customizing Events

Edit the `events` array in `index.html` (around line 200):

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
        category: 'Webinar'
    }
];
```

## 🎯 How It Works

### Google Calendar
1. Click "Google Calendar" button
2. Opens Google Calendar with event pre-filled
3. User clicks "Save"
4. Done! (2 clicks)

### Apple Calendar
1. Click "Apple Calendar" button
2. ICS file downloads via data URI
3. File opens in Apple Calendar
4. User clicks "OK"
5. Done! (3 clicks)

### Outlook Calendar
1. Click "Outlook Calendar" button
2. Opens Outlook Calendar with event pre-filled
3. User clicks "Save"
4. Done! (2 clicks)

## 📁 Project Structure

```
caldav-standalone/
├── index.html              # Main static HTML file (ONLY FILE NEEDED!)
├── README_GITHUB_PAGES.md  # This file
├── DEPLOYMENT_GUIDE.md     # Detailed deployment instructions
└── .gitignore              # Git ignore file
```

## 🔧 Technical Details

- **Pure HTML/CSS/JavaScript** - No build process required
- **ICS Generation** - RFC 5545 compliant calendar files
- **Google Calendar API** - Uses public URL scheme
- **Outlook Calendar API** - Uses public URL scheme
- **Apple Calendar** - Uses data URI for direct download
- **No Dependencies** - Everything self-contained

## 🌟 Advantages Over Node.js Version

| Feature | Node.js | Static |
|---------|---------|--------|
| Hosting Cost | $0-$5/mo | **FREE** |
| Setup Time | 15 min | **2 min** |
| Maintenance | Updates needed | **None** |
| Scalability | Limited | **Unlimited** |
| Speed | Fast | **Instant** |
| Deployment | Complex | **Simple** |

## 📊 Browser Support

- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Mobile browsers

## 🆘 Support

For issues or questions:
1. Check `DEPLOYMENT_GUIDE.md` for detailed instructions
2. Open an issue on GitHub
3. Review browser console for errors (F12)

## 📄 License

MIT License - Feel free to use and modify!

## 🎊 Credits

Built with ❤️ for seamless calendar integration

---

**Live at:** https://whysorush.github.io/caldev/

