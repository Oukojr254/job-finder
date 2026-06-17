# 🤖 AI Job Finder Automation

> Built by **Shawn Ouko** — AI Automation Developer, Nairobi, Kenya

An end-to-end automated job search system that runs every morning at 8am, finds the best matching jobs on LinkedIn, scores them against my CV using AI, writes tailored cover letters, and delivers everything to my Gmail inbox — completely hands-free.

---

## 🚀 What it does

- Runs automatically every morning at **8am EAT** via Windows Task Scheduler + n8n
- Searches LinkedIn daily for **AI, IT, and remote jobs** (rotates 7 keyword sets + page numbers so results are always fresh)
- Scores each job **(0–100)** against my CV profile using **Groq AI (Llama 3.3-70b)**
- Logs **all scored jobs** to Google Sheets with title, company, location, score, reason, and URL
- Selects the **top 5 matching jobs**
- Writes a **tailored cover letter** for each top job using AI
- Sends a **formatted HTML digest email** to Gmail with all 5 jobs + cover letters

---

## 🛠️ Tech stack

| Tool | Purpose |
|------|---------|
| **n8n** (self-hosted) | Workflow orchestration |
| **LinkedIn Jobs API** (RapidAPI) | Real-time job listings |
| **Groq AI / Llama 3.3-70b** | CV matching + cover letter generation |
| **Google Sheets** | Job logging and history |
| **Gmail** | Daily digest delivery |
| **Windows Task Scheduler** | Auto-start n8n at 7:55am daily |

---

## 🏗️ Architecture
