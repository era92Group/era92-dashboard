# era92 Group — Live KPI Dashboard

## Quick Start (5 minutes)

### Step 1: Publish your Google Sheets to the web

Both sheets need to be published so the dashboard can read them without login.

**Weekly KPIs Sheet:**
1. Open: https://docs.google.com/spreadsheets/d/1fch4Cy5sj1VQ_iaD2NK0SoOE1EKjsr_7YmZSUt3-ngU
2. Go to **File → Share → Publish to web**
3. Under "Link", select **Entire Document** and **Web page**
4. Click **Publish**
5. Check the box "Automatically republish when changes are made"

**Revenue Tracker Sheet:**
1. Open: https://docs.google.com/spreadsheets/d/1n4eFTqFmyvm9xEY-meoio2v6qFoCow7mwC6BU0wNAhI
2. Same steps as above: **File → Share → Publish to web → Publish**

### Step 2: Deploy to GitHub Pages (free hosting)

1. Go to https://github.com/new and create a new repository named `era92-dashboard`
2. Make it **Public** (required for free GitHub Pages)
3. Upload the `index.html` file from this folder
4. Go to **Settings → Pages**
5. Under "Source", select **Deploy from a branch**
6. Select **main** branch and **/ (root)** folder
7. Click **Save**
8. Your dashboard will be live at: `https://YOUR-USERNAME.github.io/era92-dashboard/`

### Step 3: Share with your team

Send the GitHub Pages URL to your leadership team. They just bookmark it — the data refreshes automatically every time they open the page.

## How It Works

- The dashboard fetches CSV data directly from your published Google Sheets
- No backend server needed — it's a single HTML file
- Data refreshes every time someone opens the page or clicks "Refresh"
- Filters (week, month, quarter, year, brand) update all charts instantly

## Data Sources

| Sheet | What it tracks |
|-------|---------------|
| Weekly KPIs | Elevate enrollment, Employment placements, Microfinance loans, Hub activity, Marketing metrics |
| Revenue Tracker | Revenue by brand (Cafe, CarWash, Creative, Elevate, Finance, Hub) |

## Troubleshooting

**Charts show no data:** Make sure both sheets are published to the web (Step 1).

**Revenue not showing:** The Revenue Tracker sheet name must be "Sheet1". If renamed, update line 206 in index.html.

**Adding a new sheet tab:** Add the tab name to the `SHEETS` config object at line 204 in index.html.
