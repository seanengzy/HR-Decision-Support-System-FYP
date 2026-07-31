# HR Analytics DSS — Pure HTML/CSS/JS Version

## Project Structure

```
your-project-folder/
├── index.html              ← Home / Landing Page
├── statistics.html         ← Statistics Overview Dashboard
├── prediction.html         ← Attrition Prediction + Gemini AI
├── dataset.html            ← Employee Dataset Browser
├── HR-Emp-Att.csv          ← Your employee data (copy here)
└── feature_importance.csv  ← Feature importance file (copy here)
```

## Setup Instructions

### Step 1: Copy Data Files
Place these files in the **same folder** as the HTML files:
- `HR-Emp-Att.csv`
- `feature_importance.csv`

### Step 2: Run a Local Server
Since the app loads CSV files via `fetch()`, you **cannot** just open HTML files directly in a browser (file:// protocol blocks this).

Run one of these in your project folder:

**Python (recommended):**
```bash
python -m http.server 8000
```

Then open: `http://localhost:8000`

**Node.js (if you have npx):**
```bash
npx serve .
```

**VS Code:** Install the "Live Server" extension, right-click `index.html` → "Open with Live Server"

### Step 3: Gemini AI Setup
1. Get a free API key from: https://aistudio.google.com/apikey
2. On the **Prediction** page, paste your API key in the sidebar
3. Click **"Connect to Gemini"** — a green "Connected" status will appear
4. Search for an employee and click **"Generate Insight"**

## Pages

| Page | File | Description |
|------|------|-------------|
| Home | `index.html` | Landing page with navigation |
| Statistics | `statistics.html` | 8 charts: attrition, departments, income, age groups, feature importance, overtime, job satisfaction, tenure |
| Prediction | `prediction.html` | Search employee by ID, view risk gauge, risk factors, Gemini AI HR recommendations |
| Dataset | `dataset.html` | Full filterable/searchable table with column toggle and CSV export |

## Technical Notes

- **No Python/Streamlit required** — pure browser-based
- **Charts**: Chart.js 4.4 (via CDN)
- **CSV Parsing**: PapaParse 5.4 (via CDN)
- **AI**: Google Gemini 2.0 Flash via REST API (key entered by user)
- **Risk scoring**: Weighted algorithm based on feature importances from your trained model
- **Fonts**: Syne (display) + Manrope (body) + JetBrains Mono (code/labels) via Google Fonts

## Deployment

To deploy publicly (e.g. GitHub Pages, Netlify, Vercel):
1. Push all files to a repository
2. Make sure `HR-Emp-Att.csv` and `feature_importance.csv` are included
3. Deploy — no build step needed

**Note on CORS**: If deploying to a domain, make sure CSV files are served from the same origin. 
Gemini API calls are made from the browser directly using the user's own API key.