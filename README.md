# Trading Journal Setup Instructions

## 📁 Folder Structure

Your project should be organized like this:

```
your-repo/
├── index.html          (rename Trading_Journal_v0_23.htm to this)
├── data/
│   └── database.json   (your trade data file)
└── README.md           (this file)
```

## 🚀 Setup Steps

### 1. Rename the HTML file
Rename `Trading_Journal_v0_23.htm` to `index.html`

### 2. Create the data folder
Create a folder called `data` in the same directory as `index.html`

### 3. Move the database file
Move `database.json` into the `data` folder

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

### Database Structure (database.json)

```json
{
  "settings": {
    "usdToZarRate": 18.50,
    "lastUpdated": "2026-02-14",
    "challengeGoal": 10000,
    "monthlyGoal": 10000
  },
  "accounts": {
    "Main Account": [],
    "Small Account": [],
    "Challenge Account": [
      {
        "id": "c001",
        "date": "2026-02-15",
        "pair": "XAUUSD",
        "direction": "BUY",
        "resultUSD": 45.50,
        "entry": 5100.00,
        "exit": 5145.50,
        "lots": 0.02,
        "quality": "Clean Win",
        "manualClose": false,
        "partialClose": false,
        "notes": "Morning session"
      }
    ]
  }
}
```

### Adding New Trades

**Method 1: Edit JSON directly on GitHub**
1. Navigate to `data/database.json` in your repo
2. Click the ✏️ pencil icon to edit
3. Add new trade objects to the appropriate account array
4. Commit changes
5. Your journal updates automatically!

**Method 2: Use the web interface**
1. Add trades via the "Quick Add Trade" form
2. Trades saved to localStorage
3. Go to Settings ⚙️
4. Click "💾 Save to database.json"
5. Download the file
6. Replace `data/database.json` in your repo
7. Commit to GitHub

### Trade Object Fields

```json
{
  "id": "unique-id",           // Auto-generated
  "date": "2026-02-15",        // YYYY-MM-DD format
  "pair": "XAUUSD",            // Trading symbol
  "direction": "BUY",          // BUY or SELL
  "resultUSD": 45.50,          // P&L in USD (negative for losses)
  "entry": 5100.00,            // Entry price (optional)
  "exit": 5145.50,             // Exit price (optional)
  "lots": 0.02,                // Position size (optional)
  "quality": "Clean Win",      // Clean Win, BE, Loss, or "" (optional)
  "manualClose": false,        // true/false (optional)
  "partialClose": false,       // true/false (optional)
  "notes": "Morning session"   // Any notes (optional)
}
```

### Quality Values
- `"Clean Win"` - Perfect execution win
- `"BE"` - Break even trade
- `"Loss"` - Losing trade
- `""` - Not specified (empty string)

## 🧮 PIP Calculator

Click the 🧮 button in the header to access your custom PIP calculator at:
https://russ-bytes.github.io/STS-Signal/

## 🎯 Features

- ✅ JSON database for clean data management
- ✅ Automatic trade loading from database.json
- ✅ Period filters (Week, Month, Year, All time)
- ✅ Monthly goal tracking with progress bar
- ✅ Calendar view with daily P&L
- ✅ Detailed statistics
- ✅ Charts (Equity, Daily, Win/Loss)
- ✅ Trade quality tracking (Clean Win, BE, Loss)
- ✅ Manual close tracking
- ✅ Export to JSON/CSV
- ✅ Multi-account support

## 💾 Data Flow

1. **Page loads** → Reads `/data/database.json`
2. **Trades load** → All accounts and settings loaded
3. **Add trade** → Saved to localStorage (temporary)
4. **Export** → Generate new database.json with all data
5. **Replace file** → Update your repo's database.json
6. **Commit** → Push to GitHub, done!

## 🔄 Workflow

### Recommended: GitHub Web Editor
1. Go to your repo on GitHub
2. Navigate to `data/database.json`
3. Click ✏️ Edit
4. Add your trade to the appropriate account array
5. Commit directly to main branch
6. Refresh your journal page
7. Trades appear automatically!

### Alternative: Local Development
1. Clone your repo
2. Edit `data/database.json` locally
3. Add/remove trades as needed
4. Commit and push
5. GitHub Pages updates automatically

## 🛠️ Troubleshooting

**Trades not loading?**
- Check that `data/database.json` exists
- Verify the file path is correct: `./data/database.json`
- Open browser console (F12) for error messages
- Make sure JSON is valid (use JSONLint.com)

**Invalid JSON error?**
- Missing comma between objects
- Extra comma after last item
- Check all quotes are proper double quotes `"`
- Validate at: https://jsonlint.com

**Calendar not showing trades?**
- Date format must be YYYY-MM-DD
- Direction must be "BUY" or "SELL" (uppercase)
- resultUSD must be a number (no quotes)

## 📝 Tips

- **Always validate JSON** before committing (use JSONLint)
- **Keep backups** using the "📥 JSON Backup" button
- **Test locally** before pushing to production
- **Use meaningful IDs** (e.g., "trade_2026_02_15_001")
- **Add notes** to remember context of trades

## 📱 Mobile Friendly

The journal is fully responsive and works great on mobile devices!

## 🎨 Why JSON?

✅ **Structured** - Proper data types (numbers, booleans)  
✅ **Validated** - Easy to catch errors  
✅ **Flexible** - Easy to add new fields  
✅ **Standard** - Works everywhere  
✅ **Clean** - No parsing needed  
✅ **GitHub-friendly** - Easy to edit directly

---

Happy Trading! 📈
