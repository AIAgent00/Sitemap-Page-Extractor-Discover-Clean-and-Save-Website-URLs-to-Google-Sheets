<img width="716" height="263" alt="image" src="https://github.com/user-attachments/assets/f927eaa9-0ef7-4d4a-b94c-fddd1ff01cef" />

# 🕸️ Website Sitemap Crawler & URL Extractor 🌐

Automate the discovery and extraction of **all page URLs** from a website’s sitemap structure and save them directly to **Google Sheets** 📄—perfect for SEO audits, content indexing, or competitor research!

---

## ⚙️ How It Works

This n8n workflow automates the process in a series of smart steps:

### 🔗 Step 1: URL Input
Submit a website URL through a **simple form interface** — this kicks off the workflow!

### 🧭 Step 2: Sitemap Discovery
The system intelligently tests multiple common sitemap patterns:
- `/sitemap.xml`
- `/sitemap_index.xml`
- `/robots.txt`
- Other popular variations

### ✅ Step 3: Valid Sitemap Identification
Each potential sitemap URL is pinged via HTTP. The workflow filters out:
- ❌ Empty responses
- ❌ Invalid formats  
Only valid, accessible sitemaps are kept! 🗂️

### 🧬 Step 4: Nested Sitemap Processing
If a sitemap index is found, the workflow:
- Extracts all nested sitemaps
- Processes them **individually** for full coverage 🌐

### 📄 Step 5: Page URL Extraction
From each valid sitemap:
- Parses XML `<loc>` tags
- Crawls for valid HTML page links
- Extracts all individual page URLs 🔍

### 🚫 Step 6: URL Filtering
Cleans the results by removing any URLs that:
- Contain the word `"sitemap"`
- Are not actual content pages (e.g., product, blog, service pages are retained)

### 📊 Step 7: Google Sheets Integration
All clean URLs are:
- Pushed into a **Google Sheet**
- Auto-checked for duplicates 🧹
- Ready for easy analysis, sharing, and reporting 📈

---

## 🛠️ Setup Steps

🕒 **Estimated Setup Time:** 10–15 minutes

### 1️⃣ Import the Workflow
- Import the provided `.json` file into your **n8n** instance

### 2️⃣ Configure Google Sheets Integration
- Set up Google Sheets **OAuth2 credentials** in n8n 🔐
- Create or choose your **Google Sheet**
- Update the `Save Page URLs to Sheet` node with your:
  - Sheet URL
  - Tab name (e.g., `"Your sheet tab name"`)
  - Column header (e.g., `"Column name"`)

### 3️⃣ Test the Workflow
- Activate the workflow ✅
- Use the **form trigger URL** to submit a test website
- Watch the magic happen ✨ — extracted URLs appear in your sheet!

### 4️⃣ Customize (Optional)
- 🛠 Modify sitemap patterns in the `Build sitemap URLs` node
- 🧹 Adjust filters in the `Exclude the Sitemap URLs` node
- 🧾 Update Google Sheets column mapping if needed

---

## 📝 Important Notes

- 🔐 Make sure your Google credentials have **read/write access**
- 🧠 Handles both **XML sitemaps** and **robots.txt** references
- 🚫 Automatically **prevents duplicate entries**
- 🛡️ Continues even if some sitemap URLs fail or return errors

---

## 🧩 Perfect For:
- SEO specialists 📈
- Web developers 💻
- Digital marketers 📣
- Anyone needing **structured access** to site URLs!

---

🚀 Get started, automate the boring stuff, and unlock insights with every crawl!

