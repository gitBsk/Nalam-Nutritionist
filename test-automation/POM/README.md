# 🚀 Universal Test Automation POM Generator (n8n Workflow)

This n8n workflow **automatically scans a website via its sitemap and generates Page Object Model (POM) code** following industry best practices for Test Automation.

It is designed for **QA Engineers, Automation Architects, and Engineering Teams** who want to accelerate test framework creation using AI while keeping the output clean, maintainable, and production-ready.

---

## ✨ What This Workflow Does

1. Accepts a **website URL** as input
2. Discovers valid sitemap URLs (`sitemap.xml`, `sitemap_index.xml`, etc.)
3. Extracts all **actual page URLs** (filters out sitemap links)
4. Fetches each page’s DOM / HTML
5. Uses an **AI Agent** to generate:
   - Cypress Page Object Model (POM) code
   - Following strict design & automation best practices
6. Outputs the generated POM files in an **organized folder structure**

---

## 🧠 Why This Is Useful

- Eliminates manual POM creation
- Enforces **consistent automation standards**
- Reduces flaky selectors
- Saves hours of repetitive work
- Ideal for **framework bootstrapping**, audits, or migrations

---

## 🧱 Supported Automation Stacks

Currently implemented:
- ✅ **Cypress (TypeScript)**

Prompt already includes guidance for:
- Playwright (TypeScript)
- Selenium (Java)

(You can easily extend the agent to support them.)

---

## 🗂 Folder Structure Generated

```text
cypress/
 └── pages/
     ├── HomePage.ts
     ├── LoginPage.ts
     ├── ProductsPage.ts
     └── ...
````

Each file:

* One class per page
* Stable selectors
* High-level user actions
* No assertions inside POMs

---

## 🔧 How to Use This Workflow

### 1️⃣ Import the Workflow

* Open **n8n**
* Click **Import Workflow**
* Upload `Test_Automation_POM_Generator_FULLY_SANITIZED.json`

---

### 2️⃣ Configure Credentials

* Create an **OpenAI credential** in n8n
* Assign it to the **GPT / Agent node**
* Replace placeholders like:

  ```
  {{API_KEY_GOES_HERE}}
  ```

---

### 3️⃣ Set Website Input

Edit the **“Set Website To Scrape”** node and provide:

```
https://example.com
```

---

### 4️⃣ Execute

Click **Execute Workflow** and let the automation:

* Crawl the sitemap
* Generate POMs
* Output files per page

---

## 🧪 Design Principles Followed

The AI agent enforces:

* 📦 One POM per page
* 🎯 Stable selectors first (data-testid > id > role > text)
* 🧼 No hard waits / sleeps
* 🧠 High-level intent methods
* 🚫 No assertions inside POMs
* 🔄 Reusable, maintainable code

---

## 📌 Customization Ideas

You can extend this workflow to:

* Push files directly to GitHub
* Write files to local filesystem
* Support Playwright / Selenium
* Generate test specs alongside POMs
* Add visual comparison / accessibility scanning

---

## 🧑‍💻 Author

**Balaji Santhana Krishnan**
🔗 LinkedIn: [https://www.linkedin.com/in/balaskrishnan/](https://www.linkedin.com/in/balaskrishnan/)

Built with ❤️ using **n8n + AI + Automation Best Practices**

---

## ⭐ If You Find This Useful

* Star the repo ⭐
* Share on LinkedIn
* Fork and extend
* Contribute improvements

Happy Automating 🚀

```
