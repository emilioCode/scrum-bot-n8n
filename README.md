# scrum-bot
# Scrum Master Bot 🤖

An AI-powered Scrum Master bot built with n8n and OpenAI GPT-4o-mini that automates core Scrum ceremonies and rituals.

## Overview

This bot substitutes key Scrum Master functions through intelligent automation. It handles daily standups, analyzes blockers with actionable recommendations, and generates professional end-of-sprint reports — all powered by AI.

## Features

### Daily Standup
Collects the 3 classic standup questions from a team member and generates a concise AI summary:
- What did you do yesterday?
- What will you do today?
- Do you have any blockers?

### Blocker Alert
Analyzes reported blockers and provides:
- Impact assessment
- Step-by-step resolution recommendations
- Escalation path suggestions

### Sprint Summary
Generates a professional end-of-sprint report including:
- Sprint highlights
- Accomplished work
- Incomplete stories and reasons
- Key blockers encountered
- Recommendations for next sprint

### Unified Flow
Single endpoint (`/scrum-bot`) that routes to the correct function based on a `type` field (`standup`, `blocker`, `sprint-summary`). Returns a helpful error message for invalid types.

---

## Why n8n

- **Visual workflow builder** — flows are easy to understand, maintain and extend without deep coding knowledge
- **Native OpenAI integration** — built-in node for GPT models, no custom HTTP calls needed
- **Version control friendly** — flows export as JSON and commit cleanly to git
- **Extensible** — ready to integrate with Slack, Teams, email and more
- **Runs locally** — no cloud dependency required for development and demo

---

## How to Run

### Prerequisites
- Node.js 18+
- npm

### Install & Start
```bash
npm install -g n8n
n8n start
```

Open `http://localhost:5678` in your browser.

### Import Flows
1. In n8n go to **Workflows → Import**
2. Import each file from the `/flows` folder
3. Configure your OpenAI credentials in **Credentials → New → OpenAI**
4. Activate the workflow

---

## Flow Files

| File | Description |
|---|---|
| `flows/daily-standup.json` | Standalone daily standup flow |
| `flows/blocker-alert.json` | Standalone blocker analysis flow |
| `flows/sprint-summary.json` | Standalone sprint summary flow |
| `flows/scrum-master-bot.json` | Unified flow with all 3 functions |

---

## API Usage

### Daily Standup
