# 🎯 FocusBoard — Chrome New Tab Extension

[![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-4285F4?style=flat-square&logo=google-chrome&logoColor=white)](https://developer.chrome.com/docs/extensions/)
[![Manifest V3](https://img.shields.io/badge/Manifest-V3-brightgreen?style=flat-square)](https://developer.chrome.com/docs/extensions/mv3/intro/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![HTML/CSS](https://img.shields.io/badge/HTML%2FCSS-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Built with AI](https://img.shields.io/badge/Built%20with-Antigravity%20AI-blueviolet?style=flat-square)](https://antigravity.ai)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)]()

> A productivity-first Chrome new tab extension that replaces the default blank tab with a focused personal dashboard — featuring daily focus goals, a task list, Focus Mode (site blocker), motivational quotes, and a customizable wallpaper. Built using the **Scope → PRD → tasks.md → Phased Build → Test** methodology from Codebasics AI Pro.

---

## 📸 Dashboard Preview

<!-- Add your screenshot here after uploading to assets/ folder -->
![FocusBoard Dashboard](assets/dashboard-preview.png)

> *Replace the image above with your actual dashboard screenshot. See [How to Add Screenshots](#-how-to-add-screenshots) below.*

---

## 🧠 What is FocusBoard?

Every time you open a new tab in Chrome, you are hit with a blank page — or worse, a distracting news feed. FocusBoard replaces that with something intentional: **your goals, your tasks, and a system that keeps you focused**.

FocusBoard answers one question when you open a new tab: *"What am I working on today?"*

---

## ✨ Features

| Feature | Description |
|---|---|
| 🎯 **Daily Focus Goal** | Set one primary focus for the day. It greets you every time you open a tab. |
| ✅ **Task List** | Add, complete, and clear daily tasks — persists across sessions |
| 🚫 **Focus Mode** | Block distracting websites (YouTube, Instagram, Twitter, etc.) with one toggle |
| 💬 **Motivational Quotes** | A new quote every day to start with the right mindset |
| 🖼️ **Custom Wallpaper** | Upload your own background image to personalize the dashboard |
| 🌤️ **Live Clock & Greeting** | Real-time clock with time-based greeting (Good morning / afternoon / evening) |
| 💾 **Persistent Storage** | All data saved via `chrome.storage.local` — survives browser restarts |
| ⚙️ **Settings Panel** | Configure blocked sites, wallpaper, and preferences |

---

## 🏗️ How It Was Built — The Methodology

This project was built following the **AI-assisted development flow** taught in the Codebasics AI Pro program:

```
1. SCOPE
   Write what you want in plain English.
   "I want a Chrome extension that replaces my new tab with a focus dashboard..."
         │
         ▼
2. PRD (Product Requirements Document)
   Fed the scope into Claude AI → generated a structured PRD with:
   - Feature list
   - User flows
   - Edge cases
   - Technical constraints
         │
         ▼
3. tasks.md
   Fed the PRD into Antigravity AI → generated a phased task breakdown:
   - Phase 1: Core layout + clock
   - Phase 2: Focus goal input + persistence
   - Phase 3: Task list
   - Phase 4: Focus Mode (site blocker)
   - Phase 5: Wallpaper + Settings
   - Phase 6: Quotes + polish
         │
         ▼
4. PHASED BUILD
   Built one phase at a time. Tested each before moving forward.
   Used Antigravity AI to generate code for each task.
         │
         ▼
5. TEST
   Loaded as unpacked extension in Chrome (chrome://extensions/)
   Verified each feature against the success criteria in tasks.md
```

> This methodology is the real skill. The extension is the output. The flow is what transfers to every future project.

---

## 🧰 Tech Stack

| Technology | Purpose |
|---|---|
| **HTML5** | Extension UI structure (newtab.html, settings panel) |
| **CSS3** | Styling, animations, responsive layout |
| **Vanilla JavaScript** | All logic — no frameworks, no dependencies |
| **Chrome Extension APIs** | `chrome.storage`, `chrome.tabs`, `chrome.declarativeNetRequest` |
| **Manifest V3** | Modern Chrome extension format (required for new extensions) |
| **Antigravity AI** | AI-assisted task planning and code generation |

---

## 📁 Project Structure

```
Focus-Board-Chrome-Extension/
│
├── manifest.json              # Extension config — permissions, scripts, new tab override
├── newtab.html                # The new tab page HTML
├── newtab.js                  # Main dashboard logic (clock, focus, tasks, quotes)
├── newtab.css                 # Dashboard styles
│
├── settings.html              # Settings panel
├── settings.js                # Settings logic (blocked sites, wallpaper, theme)
├── settings.css               # Settings styles
│
├── background.js              # Service worker — Focus Mode site blocking logic
│
├── icons/                     # Extension icons (required by Chrome)
│   ├── icon16.png
│   ├── icon48.png
│   └── icon128.png
│
└── assets/                    # Screenshots and demo images (for README)
    ├── dashboard-preview.png
    ├── focus-mode-demo.png
    └── settings-preview.png
```

---

## 🚀 Installation — Load as Unpacked Extension

Since this extension is not published to the Chrome Web Store yet, install it manually:

### Step 1 — Download the code
```bash
# Option A: Clone via git
git clone https://github.com/Shubh1015/Focus-Board-Chrome-Extension.git

# Option B: Download ZIP
# Click the green "Code" button above → "Download ZIP" → Extract it
```

### Step 2 — Open Chrome Extensions
1. Open Chrome and go to: **`chrome://extensions/`**
2. Toggle **"Developer mode"** ON (top-right corner)

### Step 3 — Load the extension
1. Click **"Load unpacked"**
2. Select the folder you downloaded/extracted (`Focus-Board-Chrome-Extension/`)
3. The extension loads instantly — no restart needed

### Step 4 — Open a new tab
Press **Ctrl+T** (or **Cmd+T** on Mac). FocusBoard replaces the default new tab page.

---

## 🎮 How to Use

**Setting your daily focus:**
1. Click the focus input at the top of the dashboard
2. Type your primary goal for the day (e.g., "Complete the SQL project")
3. Press Enter — it saves automatically and greets you with it on every new tab

**Using the Task List:**
1. Click "+ Add task" in the task panel
2. Type a task and press Enter
3. Click the checkbox when done — the task strikes through
4. Completed tasks can be cleared with "Clear completed"

**Enabling Focus Mode:**
1. Click the **Focus Mode** toggle on the dashboard
2. Any attempt to visit a blocked site redirects back to FocusBoard
3. Add or remove sites from the blocked list in ⚙️ Settings

**Customizing your wallpaper:**
1. Open ⚙️ Settings (gear icon)
2. Click "Upload Wallpaper"
3. Select any image from your computer
4. It saves and applies immediately

---

## 📷 How to Add Screenshots

To make this README look professional with actual screenshots:

### Option 1 — Drag and drop (easiest)
1. Take a screenshot of your FocusBoard dashboard
2. Go to this repository on GitHub
3. Click **"Add file" → "Upload files"**
4. Create a folder called `assets/` and upload your screenshots there
5. The `![FocusBoard Dashboard](assets/dashboard-preview.png)` line in this README will automatically display it

### Option 2 — Via git
```bash
# After cloning the repo locally:
mkdir assets
# Copy your screenshot into the assets folder
cp ~/Desktop/focusboard-screenshot.png assets/dashboard-preview.png
git add assets/
git commit -m "📸 Add dashboard screenshots"
git push
```

### Recommended screenshots to take:
| Screenshot | File name | What to capture |
|---|---|---|
| Main dashboard | `dashboard-preview.png` | Full new tab view with a focus goal set and tasks visible |
| Focus Mode ON | `focus-mode-demo.png` | Dashboard with Focus Mode toggled on |
| Settings panel | `settings-preview.png` | The settings page open |
| Blocked site | `blocked-site.png` | What users see when they try to visit a blocked site |

> **Pro tip:** Use Chrome's built-in screenshot tool: Press **F12** → Click the three-dot menu → "Capture full size screenshot" for a clean, full-page capture.

---

## 🔧 How Focus Mode Works (Technical)

Focus Mode uses Chrome's `declarativeNetRequest` API (Manifest V3) to block sites at the network level — before the page even loads:

```javascript
// manifest.json — permissions required
"permissions": ["declarativeNetRequest", "storage", "tabs"],
"host_permissions": ["<all_urls>"]

// background.js — dynamic rule creation
chrome.declarativeNetRequest.updateDynamicRules({
  addRules: blockedSites.map((site, index) => ({
    id: index + 1,
    priority: 1,
    action: { type: "redirect", redirect: { extensionPath: "/newtab.html" } },
    condition: { urlFilter: site, resourceTypes: ["main_frame"] }
  }))
});
```

This is more reliable than content scripts because it works even when Chrome is freshly opened.

---

## 💾 Data Storage Architecture

All user data is stored locally using `chrome.storage.local` — nothing goes to any server:

```javascript
// Data stored:
{
  focusGoal: "Complete the SQL project",          // Today's focus
  tasks: [{ text: "...", done: false }],          // Task list
  focusModeEnabled: true,                          // Focus mode state
  blockedSites: ["youtube.com", "instagram.com"], // User's blocked list
  wallpaper: "data:image/jpeg;base64,...",         // Base64 encoded image
  streak: { count: 5, lastDate: "2024-01-15" },   // Focus streak
  theme: "dark"                                    // UI theme preference
}
```

---

## Features

Built from the Codebasics AI Pro FocusBoard assignments:

- [x] Daily focus goal
- [x] Task list with persistence
- [x] Focus Mode (site blocker)
- [x] Custom wallpaper
- [x] Daily motivational quote
- [x] Daily focus streak counter 🔥
- [x] Dark mode / light mode toggle 🌙
- [X] Pomodoro timer widget ⏱️
- [X] Wallpaper rotation 🖼️
- [X] Task categories with colored tags 🏷️
- [X] Focus mode schedule (auto-enable) 📅
- [X] Daily focus time KPI ⏳
- [X] Analytics dashboard 📊

---

## 🤝 Contributing

This is a personal learning project built as part of the Codebasics AI Pro program. Suggestions, bug reports, and ideas are welcome!

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/pomodoro-timer`)
3. Make your changes
4. Open a Pull Request describing what you built and why

---

## 📄 License

MIT License — free to use, modify, and build on.

---

## 🙏 Acknowledgements

- **[Codebasics AI Pro](https://codebasics.io)** — For the build methodology and assignment structure
- **Antigravity AI** — For AI-assisted task planning and phased code generation
- **Chrome Extensions Documentation** — For Manifest V3 guides and API reference

---

## 🏷️ Topics

`chrome-extension` `manifest-v3` `javascript` `productivity` `focus` `new-tab` `site-blocker` `task-manager` `pomodoro` `codebasics` `antigravity-ai` `ai-assisted-development`

---

<div align="center">

**Built with the Scope → PRD → tasks.md → Build → Test flow**

*Codebasics AI Pro | #CBAIPro #Codebasics #AIPROs*

</div>
