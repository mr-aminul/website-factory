# Daily website quality playbook

Follow this every run. The site must look intentionally designed by a human product designer, not like a default AI template.

## Product bar

- Ship one complete, useful tool or resource people can use in under 60 seconds.
- No fake testimonials, no placeholder company, no “coming soon” marketing shell.
- Working core interaction on first load (form, calculator, generator, converter, checklist, etc.).
- Mobile and desktop both usable.

## Design bar (anti-generic)

- One composition in the first viewport: brand/product name as hero-level signal, one headline, one short supporting sentence, one CTA/control group, one dominant visual idea.
- No purple-on-white / purple-indigo gradient clichés, no warm-cream + terracotta serif cliché, no broadsheet newspaper layout cliché.
- No Inter/Roboto/Arial/system as the expressive display face — pick a distinctive font pairing.
- Backgrounds need atmosphere (gradient, texture, or real imagery), not a flat single color dump.
- Default: no cards. Never card-ify the hero. Cards only if they hold a real interaction.
- No pill clusters, stat strips, icon rows, floating badges, or promo stickers on the hero.
- Include 2–3 intentional motions (entrance, hover/focus, or state change) that create hierarchy — not noise.
- Define a clear CSS variable color system from one brand direction.

## Stack defaults

- Prefer Next.js (App Router) + TypeScript + Tailwind unless the topic truly needs something smaller (then Vite + React is fine).
- Public GitHub repo under `mr-aminul`.
- Production deploy on Vercel team `aminulislamborhans-projects`.
- README in the new repo: what it does, how to run locally, live URL.

## Naming

- Repo name = topic slug from the queue.
- Vercel project name = same slug when possible.
