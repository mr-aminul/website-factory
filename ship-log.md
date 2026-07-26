# Ship log

Append one row after each successful daily run.

| Date (UTC) | Topic slug | GitHub | Vercel | Notes |
|------------|------------|--------|--------|-------|
| 2026-07-26 | tip-split-fair | — | — | FAILED: GitHub App installation can only access `mr-aminul/website-factory` and cannot create new public repos (`createRepository` → Resource not accessible by integration). Retried via `gh repo create`, REST `/user/repos`, GraphQL `createRepository`, and template generate — all 403/404. Topic left unchecked. Fix: grant the Cursor GitHub App permission to create repositories under `mr-aminul` (or install on all repos + administration), then re-run. |
