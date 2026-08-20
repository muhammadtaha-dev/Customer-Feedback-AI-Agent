# n8n AI Customer Feedback Agent

An automated workflow that uses an OpenAI-powered AI agent to capture, analyze, categorize, and route customer feedback in real-time.

---

## 🗺️ Workflow Blueprint

```text
Form Submission ➔ AI Agent ➔ Switch Node ➔ Departmental Routing (Slack, Airtable, Gmail)

```

---

## ⚙️ How It Works

* **Trigger:** Captures submissions instantly via a form trigger.
* **Analysis:** Uses an advanced AI agent node powered by OpenAI to analyze feedback sentiment and intent contextually.
* **Branching & Routing:** A switch node directs data into three core paths:
* **Complaints:** Logs to Airtable, sends a Slack alert, and emails the customer via Gmail.
* **Compliments:** Logs to Airtable and posts to the management Slack channel.
* **Feature Requests:** Logs to Airtable and routes to the development Slack channel.



---

## 🧰 Tech Stack

* **Automation:** n8n
* **AI Model:** OpenAI
* **Database:** Airtable
* **Messaging:** Slack
* **Email:** Gmail
