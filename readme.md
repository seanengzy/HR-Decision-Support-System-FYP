# HR Analytics Notebook

All the data science work for this project lives in one notebook:
👉 [Attrition Analytics](Attrition_Analytics_Code.ipynb)

The [HR Analytic Attrition](HR-Emp-Att.csv) Dataset is an edited version CSV (by Me).

You can get the original dataset from [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset/data).

# HR Analytics Decision Support System: User Guide

A simple web tool that helps HR teams answer one question: **which employees are likely to leave, and what should we do about it?**

It runs in your normal web browser. No special software knowledge needed.

---

## What's inside

The system has **4 screens**:

| Screen | What it's for |
|---|---|
| **Home Page** | Your starting point, where you choose where to go |
| **Statistics Overview** | A company-wide dashboard (like a Power BI report) |
| **Attrition Prediction** | Look up one employee and see their risk of leaving |
| **Employee Dataset** | Browse, filter and export the full employee list |

---

## Getting started

### Step 1: Open the system

👉 **Click here: [seanengzy.github.io/HR-Decision-Support-System-FYP](https://seanengzy.github.io/HR-Decision-Support-System-FYP/)**

That's it. The system opens straight in your browser. Nothing to install, nothing to download.

Works on any modern browser (Chrome, Edge, Firefox, Safari) on desktop or laptop. You just need an internet connection.

> 💡 Tip: bookmark the link so you can get back to it quickly.

### Step 2: You'll land on the Home Page

From here, click any of the three cards to go to that screen. Every screen also has a menu so you can jump between them at any time.

---

## Screen 1 · Home Page

This is the front door. Nothing to do here except choose where to go:

- **Statistics Overview**: company-wide charts and trends
- **Attrition Prediction**: risk check for one specific employee
- **Employee Dataset**: the full employee table

---

## Screen 2 · Statistics Overview

Think of this as your **HR summary dashboard**, similar to Power BI. It gives you the big picture of your workforce at a glance.

### The 6 summary boxes at the top

| Box | Meaning |
|---|---|
| **Total Employees** | How many people are in the data |
| **Attrition Rate** | The % of employees who have left |
| **Average Age** | Average age of the workforce |
| **Avg Monthly Income** | Average salary per month |
| **Avg Tenure** | Average number of years employees stay |
| **Overtime Rate** | The % of employees working overtime |

### Filtering by department

At the top of the page there are four buttons:

> **All** · **R&D** · **Sales** · **HR**

Click one and **every number and chart on the page instantly updates** to show only that department. Click **All** to go back to the whole company.

*Example: click **Sales** to see the Sales team's attrition rate, average salary and top risk factors on their own.*

### The charts

Charts are grouped into three sections:

**Attrition Overview**
- Who stayed vs who left
- Attrition rate by department
- Attrition rate by age group

**Risk Factors**
- Top 10 things that most predict someone leaving
- Overtime vs attrition (do people working overtime leave more?)
- Business travel vs attrition

**Workforce Profile**
- Job satisfaction levels
- Attrition by how long people have been with the company
- Marital status vs attrition
- Headcount by department

Hover your mouse over any bar or slice to see the exact numbers.

---

## Screen 3 · Attrition Prediction

This is where you check **one employee at a time**.

### Step 1: Search for an employee

Type the **Employee ID** into the search box at the top and press Enter.

> Example: **EMP0001**

Don't know the ID? Go to the **Employee Dataset** screen, search by name or job role, and copy the ID from there.

### Step 2: Read the results

Once found, four sections appear:

**1. Employee Profile**
Their basic details: name, age, department, job role, salary, years at the company, satisfaction scores, overtime status and so on.

**2. Risk Assessment**
A dial showing the **Attrition Probability**, which is the chance this person leaves, shown as a percentage:

| Score | Meaning |
|---|---|
| **Below 40%** | 🟢 Low risk, no action needed for now |
| **40% to 70%** | 🟡 Medium risk, worth keeping an eye on |
| **Above 70%** | 🔴 High risk, act soon |

**3. Key Risk Factors**
A plain-English list of *why* the score is what it is, sorted from most to least serious. For example: *"Currently working overtime"*, *"No promotion in 7 years"*, or *"Salary 22% below department median"*.

You'll also see **Retention Strengths**, the good things keeping this person here, like long tenure or high job satisfaction.

**4. Groq AI Recommendation**
Your action plan, written for you automatically.

### Step 3: Generate the AI action plan

Click the **"Generate Insight"** button.

Wait a few seconds, and the AI writes a tailored retention plan for that specific employee:

- **Assessment**: a short summary of who this person is and what's driving their risk
- **Immediate Actions (0 to 30 days)**: what to do right now
- **Short-Term Actions (1 to 3 months)**: what to follow up with
- **Long-Term Actions (3 to 6 months)**: bigger structural fixes
- **Retention Leverage**: the single most impactful thing you can do for this person

Every recommendation is based on that employee's real numbers, not generic advice.

> 💡 If you see a message about being *rate-limited*, the free AI service is just busy. Wait about a minute and click the button again.

---

## Screen 4 · Employee Dataset

The full employee list, in a table you can slice however you like.

### Filtering: narrowing down who you see

Use the filter panel on the left:

| Filter | Options |
|---|---|
| **Department** | All, or pick one |
| **Job Role** | All, or pick one (updates based on the department you chose) |
| **Attrition** | All / Yes / No |
| **Gender** | All / Male / Female |
| **Overtime** | All / Yes / No |

There's also a **search box** at the top right. Type a name, employee ID or job role to find someone fast.

The counter shows **"Showing X of Y employees"** so you always know how much you've narrowed things down.

Made a mess? Click **"↺ Reset Filters"** to start over.

*Example: Department = Sales, Attrition = Yes, Overtime = Yes gives you everyone in Sales who left while working overtime.*

### Choosing your columns

Under the search bar is a row of column buttons. Click any one to **show or hide** that column. Highlighted = visible.

This lets you build exactly the view you need, for instance just *Name, Department, Salary and Attrition*.

You can also click any **column heading** to sort the table by it. Click again to reverse the order.

### Exporting to Excel

Click **"↓ Export CSV"** at the top right.

The file downloads as **`employees.csv`** and contains **exactly what you're looking at**: your chosen columns and your filtered rows. Open it in Excel or Google Sheets.

---

## Quick reference: common tasks

| I want to... | Go here |
|---|---|
| See how many people left last year | Statistics Overview → *Attrition Rate* box |
| Compare Sales vs R&D turnover | Statistics Overview → click each department button |
| Check if one specific person might quit | Attrition Prediction → search their Employee ID |
| Get a retention plan for someone | Attrition Prediction → **Generate Insight** |
| Find an employee's ID | Employee Dataset → search by name |
| Pull a list of high-overtime staff for a meeting | Employee Dataset → filter → Export CSV |

---

## Good to know

- **Nothing you do changes the data.** Filtering, searching and exporting are all read-only, so you can't break anything by clicking around.
- **The risk score is a guide, not a verdict.** It's based on patterns in past employee data. Use it to start a conversation, not to make a decision on its own.
- **You need an internet connection.** The system is hosted online, so it won't work offline.
- **No login needed.** Just open the link and start using it.

---

## For the person who set this up

<details>
<summary>Technical setup notes (click to expand)</summary>

### Files in the folder

```
index.html         Home page
statistics.html    Statistics dashboard
prediction.html    Attrition prediction + AI
dataset.html       Employee data browser
data.js            Employee data (generated from HR-Emp-Att.csv)
model.js           Trained SVM model + feature importances
config.js          Groq API key (auto-generated, do not edit by hand)
setup.js           Reads .env and writes config.js
.env               Where you put GROQ_API_KEY
attAnalytics.ipynb Data analysis and model training notebook
HR-Emp-Att.csv     Source employee data
requirements.txt   Python packages needed by the notebook
```

### Python setup (only for the notebook)

The web app is pure HTML/CSS/JS and needs no Python. Python is only required to
re-run `attAnalytics.ipynb` and regenerate `data.js` / `model.js`.

Built and tested on **Python 3.13.7**:

```bash
python -m venv .venv
.venv\Scripts\activate          # Windows
source .venv/bin/activate       # macOS / Linux
pip install -r requirements.txt
```

### Where it's hosted

Live on GitHub Pages: <https://seanengzy.github.io/FYP/> (repo: `seanengzy/FYP`, branch `main`).
Push to `main` and the site redeploys automatically, with no build step.

### Running it locally

Because the pages load `data.js` and `model.js` as local scripts, double-clicking `index.html` works in most browsers. If anything fails to load, serve the folder over HTTP instead:

```bash
python -m http.server 8000     # then open http://localhost:8000
```

or `npx serve .`, or the VS Code "Live Server" extension.

### AI setup

1. Get a free API key at <https://console.groq.com>
2. Put it in `.env` as `GROQ_API_KEY=your_key_here`
3. Run `node setup.js` to regenerate `config.js`
4. Open the Prediction page; the badge should read **"Groq AI Ready"**

The app calls Groq's chat API from the browser and falls back through
`llama-3.3-70b-versatile` → `llama-3.1-8b-instant` → `mixtral-8x7b-32768`
if a model is unavailable or rate-limited.

### How the prediction works

`model.js` contains an SVM (RBF kernel) exported from the training notebook, with
sklearn-matched probability calibration. The risk percentage is the model's
predicted probability of attrition. If `model.js` fails to load, the page falls
back to a simpler weighted rule-based score.

### ⚠️ Security note: API key exposure

`config.js` embeds the Groq API key directly in client-side code. The repo is
**public**, and `.env` and `config.js` were uploaded despite being listed in
`.gitignore` (drag-and-drop upload on github.com ignores `.gitignore`).

That means the key is readable by anyone, both in the repo and in the deployed
page's source. It should be rotated at <https://console.groq.com>, and the two
files removed from the repo *and* its commit history.

For a public deployment the key cannot be kept secret on the front end at all.
The proper fix is to proxy the Groq call through a small backend (Vercel or
Netlify function) that holds the key server-side.

</details>
