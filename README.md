# website-factory

Control plane for the daily **client-demo website** autopilot.

The goal is a resourceful GitHub + live demos that win web-development work: shops, schools, mosques, clinics, firms, and other institutional sites — not utility tools.

## How it works

1. You write niche demo topics in `topics/queue.md` (one per day, top to bottom).
2. A Cursor Automation takes the **first unchecked** topic.
3. It ships a new public GitHub repo under `mr-aminul` + Vercel production deploy on `aminulislamborhans-projects`.
4. It marks that topic done and appends a row to `ship-log.md`.

## Before autopilot

1. Keep at least ~30 unchecked client-demo topics in `topics/queue.md`.
2. Save the Cursor Automation with Cloud Agents + GitHub + Vercel connected.
3. Do not leave empty topics above filled ones — the agent always takes the first `- [ ]` line.
4. Follow `PLAYBOOK.md` (portfolio demos, not calculators).

## Suggested mix

| Share | Type | Examples |
|------:|------|----------|
| ~40% | Local commerce | florist, pharmacy, sneakers, bakery, boutique |
| ~40% | Institutions | school, mosque, university, library, church |
| ~20% | Professional services | dental, legal, coaching, accounting, physio |

## Files

| File | Purpose |
|------|---------|
| `topics/queue.md` | Ordered client-demo list |
| `PLAYBOOK.md` | Quality bar for portfolio-ready demos |
| `ship-log.md` | What shipped (repo URL, Vercel URL, date) |
