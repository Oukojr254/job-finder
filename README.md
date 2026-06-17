# job-finder
Automated job finder using n8n, LinkedIn API, Groq AI, Google Sheets and Gmail

# AI Job Finder Automation

An end-to-end automated job search system built with n8n, Groq AI, LinkedIn Jobs API, Google Sheets, and Gmail.

## What it does
- Runs automatically every morning at 8am
- Searches LinkedIn for AI, IT, and remote jobs matching my profile
- Scores each job (0–100) against my CV using Groq AI (Llama 3.3-70b)
- Logs all scored jobs to Google Sheets for tracking
- Selects the top 5 matching jobs
- Writes a tailored cover letter for each top job using AI
- Sends a formatted digest email with job details and cover letters to Gmail

## Tech stack
- **n8n** — workflow automation (self-hosted, free)
- **LinkedIn Jobs API** (via RapidAPI) — job data source
- **Groq AI / Llama 3.3-70b** — CV matching and cover letter generation
- **Google Sheets** — job logging and history
- **Gmail** — daily digest delivery
- **Windows Task Scheduler** — automatic daily trigger at 7:55am

## Architecture
