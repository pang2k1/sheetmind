# SheetMind — AI Sheet Builder Chrome Extension

> Describe any spreadsheet in plain English. SheetMind builds the full structure instantly.

---

## Setup (5 steps)

### 1. Get a Google OAuth Client ID

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project (or use existing)
3. Enable the **Google Sheets API**: APIs & Services → Library → search "Sheets API"
4. Go to **APIs & Services → Credentials → Create Credentials → OAuth 2.0 Client ID**
5. Application type: **Chrome Extension**
6. Get your Extension ID first (see step 2), then add it as an authorized ID
7. Copy the **Client ID**

### 2. Load the extension in Chrome

1. Open Chrome → `chrome://extensions/`
2. Enable **Developer Mode** (top right toggle)
3. Click **Load Unpacked** → select this `sheetmind/` folder
4. Copy your **Extension ID** (shown under the extension name)

### 3. Update manifest.json

Replace `YOUR_GOOGLE_CLIENT_ID.apps.googleusercontent.com` in `manifest.json`:

```json
"oauth2": {
  "client_id": "YOUR_ACTUAL_CLIENT_ID.apps.googleusercontent.com",
  "scopes": ["https://www.googleapis.com/auth/spreadsheets"]
}
```

Reload the extension after saving.

### 4. Get a Claude API Key

1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Create an API key
3. Copy it

### 5. Add API Key to SheetMind

1. Open any Google Sheet
2. Click the **SheetMind tab** on the right edge of the screen
3. Click the ⚙ settings icon
4. Paste your Claude API key → Save

---

## How to Use

1. Open any Google Sheet
2. Click the SheetMind panel on the right
3. Type a description of the spreadsheet you want, e.g.:
   - *"Build a CRM for 50 sales leads with company, contact, deal value, and follow-up date"*
   - *"Create a monthly P&L template for an e-commerce business"*
   - *"Add calculated columns to my existing data for margin, growth rate, and status"*
4. Click **Build Sheet** (or press Cmd/Ctrl + Enter)
5. Watch it build in real time ✨

---

## File Structure

```
sheetmind/
├── manifest.json       # Extension config & permissions
├── background.js       # Service worker: OAuth, Claude API, Sheets API
├── content.js          # Injected into Google Sheets — sidebar UI logic
├── sidebar.css         # Sidebar panel styles
├── popup.html          # Extension toolbar popup
├── popup.js            # Popup logic
├── README.md           # This file
└── icons/              # Extension icons (add 16x16, 48x48, 128x128 PNGs)
```

---

## Tech Stack

- **Chrome Extension Manifest V3**
- **Google Sheets API v4** — read context + batchUpdate to write
- **Chrome Identity API** — OAuth2 for Google auth
- **Claude API** (claude-sonnet-4) — generates sheet structure as JSON
- Vanilla JS — no build step required

---

## Monetization Plan

| Tier | Price | Limit |
|---|---|---|
| Free | $0 | 5 generations/month |
| Pro | $9/month | Unlimited + saved templates |

Add usage tracking via `chrome.storage.sync` (generation count + reset date).
Stripe integration for Pro upgrades via a simple web landing page.

---

## Next Features (roadmap)

- [ ] Usage counter + free tier enforcement
- [ ] Stripe payment integration
- [ ] Saved templates library
- [ ] "Explain this formula" mode — click any cell
- [ ] Multi-sheet generation (builds multiple tabs at once)
- [ ] Export as Google Apps Script
