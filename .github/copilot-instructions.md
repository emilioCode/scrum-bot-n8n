# Scrum Master Bot — Copilot Instructions

## Project Overview
A Scrum Master bot built with n8n that automates core Scrum ceremonies and rituals.

## Purpose
Substitute core Scrum Master functions through automation:
- Daily standup collection and summarization
- Blocker detection and escalation
- Sprint progress tracking
- Team notifications

## Platform
- n8n (workflow automation)
- OpenAI GPT-4o-mini for AI summarization
- Webhook triggers for standup collection

## Bot Flows
1. **Daily Standup** — collects 3 standup questions from team members and generates AI summary
2. **Blocker Alert** — detects blockers and escalates automatically
3. **Sprint Summary** — generates end-of-sprint report

## Flow Files
- All n8n flows exported as JSON in /flows directory
- Each flow has a descriptive filename

## Design Decisions
- Webhook-based triggers for flexibility
- OpenAI for natural language summarization
- Modular flows — each ceremony is a separate flow

## Commit conventions
- feat: new flow or feature
- fix: bug fix in flow
- chore: configuration or setup
