# Trading Journal Setup Instructions

## 📁 Folder Structure

Your project should be organized like this:

```
your-repo/
├── index.html          (rename Trading_Journal_v0_21.htm to this)
├── data/
│   └── database.md     (your trade data file)
└── README.md           (this file)
```

## 🚀 Setup Steps

### 1. Rename the HTML file
Rename `Trading_Journal_v0_21.htm` to `index.html`

### 2. Create the data folder
Create a folder called `data` in the same directory as `index.html`

### 3. Move the database file
Move `database.md` into the `data` folder

### 4. Push to GitHub
```bash
git add .
git commit -m "Initial trading journal setup"
git push
```

### 5. Enable GitHub Pages
1. Go to your repository settings
2. Navigate to "Pages" section
3. Select "main" branch as source
4. Save

Your journal will be live at: `https://your-username.github.io/your-repo-name/`

## 📊 Managing Your Trades

### Adding New Trades

Edit `data/database.md` and add new rows to the table:

```markdown
| Date | Pair | Direction | Result | Entry | Exit | Lots | Quality | Manual | Notes |
|------|------|-----------|--------|-------|------|------|---------|--------|-------|
| 2026-02-15 | XAUUSD | BUY | 45.50 | 5100.00 | 5145.50 | 0.02 | Clean Win | NO | Morning trade |
```

### Field Guide

- **Date**: YYYY-MM-DD format (e.g., 2026-02-15)
- **Pair**: Trading symbol (XAUUSD, EURUSD, etc.)
- **Direction**: BUY or SELL
- **Result**: P&L in USD (use negative for losses: -10.50)
- **Entry**: Entry price
- **Exit**: Exit price  
- **Lots**: Position size (0.01, 0.02, 0.03, etc.)
- **Quality**: Clean Win, BE, Loss (or leave empty)
- **Manual**: YES or NO (whether you manually closed)
- **Notes**: Any notes or timestamps

### Quick Edit in GitHub

1. Navigate to `data/database.md` in your repo
2. Click the ✏️ pencil icon to edit
3. Add your new trades
4. Commit changes
5. Your journal will update automatically!

## 🧮 PIP Calculator

Click the 🧮 button in the header to access your custom PIP calculator at:
https://russ-bytes.github.io/STS-Signal/

## 🎯 Features

- ✅ Automatic trade loading from markdown file
- ✅ Period filters (Week, Month, Year, All time)
- ✅ Monthly goal tracking with progress bar
- ✅ Calendar view with daily P&L
- ✅ Detailed statistics
- ✅ Charts (Equity, Daily, Win/Loss)
- ✅ Trade quality tracking (Clean Win, BE, Loss)
- ✅ Manual close tracking
- ✅ Export to CSV
- ✅ Multi-account support

## 💾 Local Storage

The journal uses localStorage for settings and local trades. The `database.md` file serves as your primary trade record and will override the Challenge Account trades on each load.

## 🔄 Workflow

### Option 1: Use the markdown file (Recommended for GitHub)
1. Edit `data/database.md` to add trades
2. Commit and push to GitHub
3. Journal automatically loads trades on page refresh

### Option 2: Use the web interface
1. Add trades using the "Quick Add Trade" form
2. Trades are saved to localStorage
3. Use "Export CSV" to backup your data

## 📝 Tips

- Keep your `database.md` file in sync with your actual trades
- Use the export feature to backup your data regularly
- The markdown format is easy to edit in any text editor
- You can even edit directly on GitHub!

## 🛠️ Troubleshooting

**Trades not loading?**
- Check that `data/database.md` exists
- Verify the file path is correct: `./data/database.md`
- Check browser console (F12) for errors

**Calendar not showing trades?**
- Make sure date format is YYYY-MM-DD
- Check that Direction is BUY or SELL (uppercase)
- Verify Result is a valid number

## 📱 Mobile Friendly

The journal is fully responsive and works great on mobile devices!

---

Happy Trading! 📈
