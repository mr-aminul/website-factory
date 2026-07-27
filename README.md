# website-factory

Control plane for the daily **client-demo website** autopilot.

## How it works

1. You write niche business/institution demos in `topics/queue.md` (one per run, top to bottom).
2. A Cursor Automation takes the **first unchecked** topic.
3. It ships a new public GitHub repo + Vercel production deploy under the portfolio brand.
4. It marks that topic done and appends a row to `ship-log.md`.

## Before autopilot

1. Fill at least 30 unchecked client-demo topics in `topics/queue.md`.
2. Save the Cursor Automation with Cloud Agents + GitHub + Vercel connected.
3. Do not leave empty topics above filled ones — the agent always takes the first `- [ ]` line.

## Files

| File | Purpose |
|------|---------|
| `topics/queue.md` | Ordered client-demo topic list |
| `PLAYBOOK.md` | Quality bar so sites look hire-worthy, not AI-generic |
| `ship-log.md` | What shipped (repo URL, Vercel URL, date) |
