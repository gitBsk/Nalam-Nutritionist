# 🥗 Nalam – Daily Nutritionist Bot (n8n + AI)

Ever got stuck with the daily question:
**“What should we cook today?”**

This project is a simple, practical example of how you can use **AI to solve everyday problems**.

**Nalam** is a Telegram bot built using **n8n + AI** that:

* Thinks for you every day 🤖
* Suggests **2 meal options** (South Indian + North Indian)
* Avoids repeating dishes from recent days
* Shares the suggestions directly to a Telegram channel

No fancy architecture.
No buzzwords.
Just a useful solution to a real problem.

---

## 👋 About the Creator

Built with ❤️ by **Balaji Santhana Krishnan**
🔗 LinkedIn: [https://www.linkedin.com/in/balaskrishnan/](https://www.linkedin.com/in/balaskrishnan/)

---

## ✨ What This Bot Does

Every day, the bot:

* Triggers automatically (scheduled)
* Uses AI to suggest **simple, home-style meals**
* Includes basic nutrition info (calories, protein, fiber)
* Avoids repeating dishes from the last few days
* Sends the final suggestion to Telegram

Perfect for:

* Families
* Busy professionals
* Anyone tired of daily decision fatigue

---

## 🛠️ Tech Stack

* **n8n** – Workflow automation
* **OpenAI** – Meal planning & reasoning
* **Telegram Bot** – Daily delivery
* **YouTube Data API** (optional) – Recipe videos

---

## 🚀 Getting Started (Step-by-Step)

### 1️⃣ Install / Access n8n

You can use **any one** of the following:

* 🌐 **n8n Cloud** → [https://n8n.io](https://n8n.io)
* 🐳 **Docker**
* 💻 **Local install (Node.js)**

👉 Official install guide:
[https://docs.n8n.io/hosting/](https://docs.n8n.io/hosting/)

---

### 2️⃣ Import the Workflow

1. Open **n8n**
2. Click **Workflows**
3. Select **Import from File**
4. Upload the provided JSON file from this repo
5. Save the workflow

You’ll now see the full flow visually 🎉

---

## 🔑 Configure Required Credentials

This workflow is **sanitized**, so you must add your own credentials.

### 🔹 OpenAI

* Create an OpenAI API key
* In n8n → **Credentials → OpenAI**
* Attach it to the AI nodes

---

### 🔹 Telegram Bot

1. Create a bot via **@BotFather**
2. Copy the bot token
3. Create a **Telegram credential** in n8n
4. Add:

   * Your bot token
   * Your channel ID or `@channelname`

---

### 🔹 YouTube Data API (Optional)

If you want recipe videos:

1. Create a Google Cloud project
2. Enable **YouTube Data API v3**
3. Generate an API key
4. Replace this placeholder in the HTTP Request node:

```text
{{ YOUTUBE_API_KEY }}
```

---

## ✏️ Customizing the Bot

This is where the fun starts 👇

You can easily:

* Change meal rules (veg / non-veg / calories)
* Adjust nutrition logic
* Change schedule time
* Modify Telegram message format
* Add WhatsApp / Email / Slack instead of Telegram

Just open the nodes and tweak the prompts — no heavy coding needed.

---

## 🧠 Why This Project Exists

This is not a “startup idea”.

It’s a reminder that:

> The best AI use cases are hiding in your daily frustrations.

If you can:

* Identify a problem
* Automate the thinking
* Deliver a simple output

You’re already building with AI 🚀

---

## ⚠️ Security Note

Before sharing or deploying:

* Never commit real API keys
* Always use n8n credentials
* Rotate keys if you accidentally expose them

This repo is safe and sanitized by design ✅

---

## 🙌 Contribute / Fork / Learn

Feel free to:

* Fork this repo
* Improve the prompts
* Add new channels
* Build your own version

If this helped you think differently about AI — that’s a win.

---

## ⭐ Final Thought

Build small.
Build useful.
Build for yourself first.

Happy building! 😊
