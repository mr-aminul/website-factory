# AGENTS.md

## Cursor Cloud specific instructions

### What this repo is (read before "setting up" or "running" anything)

This repository (`website-factory`) is a **Markdown-only control plane**, not a runnable
application. It contains only `README.md`, `PLAYBOOK.md`, `ship-log.md`, and
`topics/queue.md`. There is no `package.json`, lockfile, build system, or service to
start, so there is nothing to install, lint, build, or serve for this repo itself.
Do not run `npm install` / `pip install` here or look for a dev server — there isn't one.

The actual **product** is produced by a scheduled Cursor Automation: each run reads the
first unchecked topic in `topics/queue.md`, scaffolds a brand-new standalone website,
ships it as a **separate public GitHub repo** (under `mr-aminul`), deploys it to Vercel
(team `aminulislamborhans-projects`), then marks the topic done and appends a row to
`ship-log.md`. See `README.md` and `PLAYBOOK.md` for the workflow and quality bar.

### Toolchain available in this environment

Node 22, npm 10, pnpm 10, yarn 1, `npx`, `git`, and `gh` are preinstalled. That is
everything needed to scaffold and run the Next.js sites this factory produces.

### Exercising the factory's output locally (the real "run"/test)

The generated sites use the `PLAYBOOK.md` stack default: **Next.js (App Router) +
TypeScript + Tailwind**. To validate the environment can build/run what the factory
ships, scaffold a topic **outside this repo** and run it, e.g.:

```
cd ~ && npx --yes create-next-app@latest <topic-slug> \
  --typescript --tailwind --eslint --app --src-dir --use-npm --turbopack --yes
cd <topic-slug> && npm run lint && npm run build && npm run dev   # dev serves on :3000
```

Important: never commit generated site code into this control-plane repo. Generated
projects live in their own repos; this repo only tracks the queue, playbook, and log.

### Editing the control plane

"Development" here means editing the Markdown files (add topics to `topics/queue.md`
keeping unchecked items above checked ones, tune `PLAYBOOK.md`, append to `ship-log.md`)
and committing via git. That is the entire day-to-day workflow for this repo.
