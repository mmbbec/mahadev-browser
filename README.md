# Mahadev Browser — by Dr Mahadev Biradar

A modern, lightweight, privacy-first browser-style web app built with **HTML5 + CSS3 + Vanilla JS**. 100% static, GitHub Pages compatible, no backend, no paid APIs.

### Features
- Custom branding: Mahadev Browser with M logo
- Address bar with URL detection + search (Google/Bing/DuckDuckGo/Yahoo)
- Back, Forward, Reload, Home, Bookmark, History, Settings, Theme toggle
- Home page: live clock, date, greeting (custom name), search box, engine pills, shortcut cards, info cards
- Light / Dark / Auto (system) themes
- Bookmarks: save, remove, list, clear — with active state
- History: local 500 entries, clear
- Shortcuts: add/edit/delete, colorful initials
- Embedded viewer with iframe + graceful fallback: shows clear message + **Open in New Tab** when site blocks embedding via X-Frame-Options/CSP (Google, YouTube, FB etc.)
- Settings: theme, engine, greeting name, new tab mode (Home/Blank), export JSON, clear all data
- Keyboard shortcuts: Ctrl+L (focus address), Ctrl+D (bookmark), Alt+←/→ (back/forward), Alt+H (home), Esc (close panels)
- Privacy: All data in localStorage only: `mahadev_prefs`, `mahadev_history`, `mahadev_bookmarks`, `mahadev_shortcuts`. No tracking, no external server.

### Security Notes
- Does NOT bypass security headers. Respects X-Frame-Options/CSP.
- Does NOT collect passwords or banking data.
- Does NOT claim private/incognito — static site cannot truly emulate it (explained in settings).

### Folder Structure
```
mahadev-browser/
├── index.html
├── style.css
├── script.js
└── README.md
```

### GitHub Pages Deployment
1. Create repo: `mahadev-browser` (public) or use existing `username.github.io`
2. Upload all 3 files (index.html, style.css, script.js) to root — keep relative paths `./style.css` `./script.js`
3. Settings → Pages → Source: Deploy from branch → main / root → Save
4. Wait 1-2 min — URL appears in Pages settings
   - If repo is `username.github.io/mahadev-browser` → https://username.github.io/mahadev-browser/
   - If repo is `username.github.io` → https://username.github.io/
5. Update: edit files locally → git push → auto redeploys

### Testing Checklist
- Home shows clock/date/greeting
- Search box + address bar both work
- Engine selector changes badge G/B/D/Y
- wikipedia.org loads in iframe (allowed)
- google.com shows blocked message + Open in New Tab works
- Back/Forward/Reload/Home
- Ctrl+L, Ctrl+D, Esc
- Bookmark toggle + Bookmarks panel
- Shortcuts add/edit/delete
- History list
- Settings theme/export/clear

### Customization
- Change name: Settings → Greeting name, or edit `state.prefs.name` default in script.js
- Change colors: edit CSS variables `--primary`, `--bg` in style.css
- Add default shortcuts: edit array in `loadState()` in script.js

MIT License — free to customize.

Built for Dr Mahadev Biradar, Bagalkot, Karnataka.
