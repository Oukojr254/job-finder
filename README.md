# 🤖 AI Job Finder Automation

> Built by Shawn Ouko — AI Automation Developer, Nairobi, Kenya

An end-to-end automated job search system that runs every morning at 8am, finds the best matching jobs on LinkedIn, scores them against my CV using AI, writes tailored cover letters, and delivers everything to my Gmail inbox — completely hands-free.

 🚀 What it does

- Runs automatically every morning at **8am EAT** via Windows Task Scheduler + n8n
- Searches LinkedIn daily for **AI, IT, and remote jobs** (rotates 7 keyword sets + page numbers so results are always fresh)
- Scores each job **(0–100)** against my CV profile using **Groq AI (Llama 3.3-70b)**
- Logs **all scored jobs** to Google Sheets with title, company, location, score, reason, and URL
- Selects the **top 5 matching jobs**
- Writes a **tailored cover letter** for each top job using AI
- Sends a **formatted HTML digest email** to Gmail with all 5 jobs + cover letters


 🛠️ Tech stack

| Tool | Purpose |
|------|---------|
| **n8n** (self-hosted) | Workflow orchestration |
| **LinkedIn Jobs API** (RapidAPI) | Real-time job listings |
| **Groq AI / Llama 3.3-70b** | CV matching + cover letter generation |
| **Google Sheets** | Job logging and history |
| **Gmail** | Daily digest delivery |
| **Windows Task Scheduler** | Auto-start n8n at 7:55am daily |



🏗️ Architecture


⚙️ How to use

1. Install n8n locally:
```bash
npm install -g n8n
n8n start
```

2. Import `job-finder-automation.json` into your n8n instance

3. Add your credentials:
   - RapidAPI key (LinkedIn Jobs Scanner API)
   - Groq API key (free at console.groq.com)
   - Google OAuth Client ID + Secret (Sheets + Gmail)

4. Update the CV profile text inside the Groq scoring node with your own details

5. Create a Google Sheet with headers: `Job Title | Company | Location | Posted Date | Score | Reason | Job URL | Date Added`

6. Activate the workflow in n8n

7. Set Windows Task Scheduler to run `n8n start` at 7:55am daily


 💡 Key design decisions

- **Groq instead of Gemini** — Gemini API key creation is geo-restricted in Kenya; Groq is fully accessible and free
- **RapidAPI Jobs Scanner** — LinkedIn has no public job API; this provides reliable real-time scraping
- **Daily keyword rotation** — 7 different search terms cycle through the week so results never repeat
- **Page rotation** — API page number changes daily so even same-keyword searches return fresh listings
- **Self-hosted n8n** — zero monthly cost vs n8n Cloud ($20+/month)



📁 Files

| File | Description |
|------|-------------|
| `job-finder-automation.json` | Full n8n workflow export (import directly into n8n) |
| `.env.example` | API key configuration template |
| `README.md` | This file |


 👤 Built by

Shawn Ouko — AI Automation Developer
- 🌍 Nairobi, Kenya
- 🔗 Portfolio: oukezzz-50db3.web.app](https://oukezzz-50db3.web.app
- 💼 LinkedIn: http://linkedin.com/in/shawn-ouko-352ab823a/
- 📧 oukoedi@gmail.com



 📌 Related projects

- https://github.com/Oukojr254/AISELA-LOGISTICS-TRACKER - Container Tracking & Billing Automation — Google Apps Script system for logistics operations
- Shawn Talks AI — Content series educating Kenyan SMEs on AI tools  http://linkedin.com/in/shawn-ouko-352ab823a/
