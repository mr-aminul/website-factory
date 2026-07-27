# Daily client-demo website playbook

Follow this every run. Each ship is a **portfolio demo for a believable business or institution** — the kind of site that makes a visitor think “he can build mine.” Not a utility tool, not a fake SaaS landing page.

## Mission

- Attract web-development clients by shipping complete niche demos.
- Mix verticals over time (~40% local commerce, ~40% institutions, ~20% professional services). Do not repeat the same category two days in a row.
- One demo per run: public GitHub repo + Vercel production URL + case-study README.

## Product bar

- Ship one complete multi-page site a real owner could use as a starting point.
- Invent a **believable brand** (name, city/neighborhood, niche copy). No “Acme Corp”, no “coming soon”, no lorem ipsum.
- Required information architecture (adapt to niche):
  - Home (brand-first hero)
  - About / story
  - Core offering pages (products, services, programs, prayer/events, admissions, etc.)
  - Contact (and when relevant: cart/checkout UI, donate, book, apply)
- Working primary CTA on first load (WhatsApp link, tel: link, inquiry form with success state, add-to-cart, donate, or apply — pick what fits the niche).
- Forms may be front-end only (success UI / `mailto:`) — no fake backend required.
- Mobile and desktop both polished.
- Prefer real niche imagery (Unsplash/Pexels with attribution in README, or strong illustrated/texture atmosphere). Decorative gradients alone are not enough as the main visual idea.

## Do not ship

- Calculators, converters, timers, generators, checklists-as-products.
- Generic “AI startup” or purple SaaS marketing shells.
- Single-page thin brochures with no real sections.
- Duplicate of a niche already live on the GitHub account unless the queue explicitly asks for a fresh brand angle.

## Design bar (anti-generic)

- One composition in the first viewport: **brand name as hero-level signal**, one headline, one short supporting sentence, one CTA group, one dominant visual (product, place, or institution atmosphere).
- No purple-on-white / purple-indigo gradient clichés, no warm-cream + terracotta serif cliché, no broadsheet newspaper layout cliché.
- No Inter/Roboto/Arial/system as the expressive display face — pick a distinctive font pairing that fits the niche.
- Backgrounds need atmosphere (imagery, gradient + texture, pattern) — not a flat single-color dump.
- Default: no cards in the hero. Cards only when they hold real navigation or product/service interaction.
- No pill clusters, stat strips, icon rows, floating badges, or promo stickers on the hero.
- Include 2–3 intentional motions (entrance, hover/focus, or section reveal) that create hierarchy — not noise.
- Define a clear CSS variable color system from one brand direction that fits the vertical (e.g. florist ≠ pharmacy ≠ mosque).

## Content bar

- Write like a hired designer who interviewed the owner: specific services, hours, neighborhood, phone, email, WhatsApp.
- Use consistent fake-but-plausible contact details for the demo brand.
- Include an inquiry or order path a client would recognize.
- README must work as a **case study**: niche, what was built, stack, local run steps, live URL, and 2–3 lines on what you’d customize for a paying client.

## Stack defaults

- Prefer Next.js (App Router) + TypeScript + Tailwind unless the topic truly needs something smaller (then Vite + React is fine).
- Public GitHub repo under `mr-aminul`.
- Production deploy on Vercel team `aminulislamborhans-projects`.
- Repo name = topic slug; Vercel project name = same slug when possible.

## Definition of done

1. Multi-page demo live on Vercel (production URL loads).
2. Public GitHub repo with polished README case study + live URL.
3. Topic checked off in `topics/queue.md`.
4. Row appended to `ship-log.md`.
