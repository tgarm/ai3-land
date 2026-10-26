# ai3.land

Landing page for the ai3.land tool family — open-source, pure-frontend tools for the Autonomys Network (AI3):

- **[PermaDrive](https://permadrive.ai3.land/)** — permanent on-chain file storage · [source](https://github.com/tgarm/permadrive)
- **[XDM Bridge](https://xdm-bridge.ai3.land/)** — cross-domain AI3 transfers, consensus ↔ Auto EVM · [source](https://github.com/tgarm/ai3-xdm-bridge)

Plain static HTML + CSS: no build step, no frameworks, no external requests.
Dual theme (dark default, light optional) following the same token set as the family's apps;
the choice is applied before first paint and persisted in `localStorage`.

## Deploy (Vercel)

The repository root **is** the site — no configuration needed:

1. Push to GitHub
2. Import the repo at [vercel.com/new](https://vercel.com/new) → Deploy (change nothing)
3. Project Settings → Domains: add `ai3.land` — at your DNS provider set the apex record
   `A` | `@` | `76.76.21.21`, and optionally `www` as `CNAME` → `cname.vercel-dns.com`

GitHub Pages / any static host works equally well.

## Adding a tool

Duplicate one `<article class="card tool">` block in `index.html` and fill in the name,
description and links. Keep the page dependency-free.
