# bingecast-site

Marketing / legal site for the [Binge Cast](https://bingecast.mlev.app) iOS app.

Two pages, zero JS, ~100 lines of HTML+CSS each. Deployed via GitHub Pages
with a custom domain.

## Structure

- `index.html` — landing page
- `privacy/index.html` — privacy policy, linked from App Store Connect
- `CNAME` — `bingecast.mlev.app`

## Deploying

1. Push to the `main` branch on the public GitHub repo.
2. GitHub Pages serves from root; the custom domain is set in repo
   Settings → Pages.
3. Cloudflare DNS on `mlev.app` has a CNAME record pointing
   `bingecast` → `levenick-enterprises.github.io` (DNS-only while GH
   provisions the TLS cert, optionally flip to proxied afterwards).

## Editing

Both pages share the same inline CSS with system font stack and
`color-scheme: light dark` for automatic dark-mode support. No build
step, no dependencies. Edit the HTML, commit, push, deploy.
