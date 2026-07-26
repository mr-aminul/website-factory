# website-factory

Control plane for the daily useful-website autopilot.

## How it works

1. You write topics in `topics/queue.md` (one per day, top to bottom).
2. Every day at 1:20 AM, a Cursor Automation takes the **first unchecked** topic.
3. It ships a new public GitHub repo + Vercel production deploy.
4. It marks that topic done and appends a row to `ship-log.md`.

## Before autopilot

1. Fill at least 30 topics in `topics/queue.md`.
2. Save the Cursor Automation with Cloud Agents + GitHub + Vercel connected.
3. Do not leave empty topics above filled ones — the agent always takes the first `- [ ]` line.

## Files

| File | Purpose |
|------|---------|
| `topics/queue.md` | Your ordered topic list |
| `PLAYBOOK.md` | Quality bar so sites do not look AI-generic |
| `ship-log.md` | What shipped (repo URL, Vercel URL, date) |
