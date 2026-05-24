# SheetMind — AI Sheet Builder for Google Sheets

> Describe any spreadsheet in plain English. SheetMind builds the full structure instantly.

---

## What is SheetMind?

SheetMind is a Chrome extension that lives inside Google Sheets. Instead of setting up columns, writing formulas, and formatting rows from scratch — you just describe what you need, and SheetMind builds it for you in seconds.

**Example prompts:**
- *"Build a CRM tracker for sales leads with company, contact, deal value, status, and follow-up date"*
- *"Create a monthly budget with income sources, expense categories, and a variance column"*
- *"Influencer campaign tracker with platform, followers, CPE, and ROI"*

---

## Getting Started

### 1. Install the extension
Add SheetMind from the [Chrome Web Store](https://chromewebstore.google.com) and pin it to your toolbar.

### 2. Get a Claude API key
SheetMind uses the Claude AI API to generate your sheet structure. You'll need your own API key — it's free to start.

1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign up and create a new API key
3. Copy it

### 3. Add your API key to SheetMind
1. Open any [Google Sheet](https://docs.google.com/spreadsheets)
2. Click the **SheetMind tab** on the right edge of the screen
3. Click the **⚙ settings icon** (top right of the panel)
4. Paste your Claude API key → click **Save**

You're ready to go.

---

## How to Use

1. Open any Google Sheet
2. Click the **SheetMind panel** on the right side of the screen
3. Type a description of the spreadsheet you want
4. Click **Build Sheet** — or press `Cmd+Enter` (Mac) / `Ctrl+Enter` (Windows)

SheetMind will read your current sheet, generate the structure, and write it directly into your spreadsheet — headers, sample rows, formulas, and formatting included.

### Quick Starts
Not sure what to type? Use the **Quick Starts** chips in the panel to instantly load common use-case prompts like Sales CRM, Content Calendar, Budget Tracker, and more.

---

## Tips for Better Results

- **Be specific.** "Build a project tracker with task name, owner, priority, due date, status, and % complete" works better than "project tracker."
- **Mention calculations you need.** If you want totals or averages, say so — e.g. "include a total row at the bottom."
- **Describe existing data.** If you already have data in the sheet, SheetMind will read it and extend your structure rather than overwrite it.

---

## Pricing

| Plan | Price | Generations |
|---|---|---|
| Free | $0 | 5 per month |
| Pro | $9/month | Unlimited + saved templates |

---

## Privacy

- SheetMind only reads and writes to the Google Sheet that is currently open.
- Your prompts are sent to the Claude API (Anthropic) to generate the sheet structure. See [Anthropic's privacy policy](https://www.anthropic.com/privacy).
- Your Claude API key is stored locally in your browser and never sent to our servers.

---

## Support

Having an issue? Email us at **support@sheetmind.app** and we'll get back to you within 24 hours.
