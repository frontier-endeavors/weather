# Manhattan Weather

Personal Manhattan, Kansas weather and Wildcat Creek dashboard, deployed as a static Cloudflare site.

## Frontier Endeavors Standards

This repository adopts [Frontier Endeavors Standards](https://github.com/frontier-endeavors/standards) version `1.0.0`. It has no database and therefore does not use a database profile.

Shared standards supplement the repository-specific rules below. Preserve the application's intentionally small, static architecture unless a requested feature demonstrates the need for a backend or framework.

## Project shape

- `index.html` contains the application HTML, CSS, JavaScript, and embedded first-paint snapshot.
- `wrangler.toml` configures Cloudflare static assets.
- Live browser data comes from NWS, MET Norway, USGS, and RainViewer.
- There is no package manager, build step, application server, or database.

## Working agreements

- Keep secrets and private credentials out of the browser and repository; all browser-called data sources must be safe for public clients.
- Preserve a useful embedded snapshot and graceful fallback when a live provider is slow or unavailable.
- Treat external responses as untrusted input and tolerate missing or malformed fields.
- Maintain responsive behavior and basic accessibility when changing layout or interactions.
- Avoid introducing dependencies, a framework, or a backend without a concrete requirement and an explicit architecture decision.
- Keep Cloudflare-specific configuration in `wrangler.toml` and do not add generated `.wrangler/` content to Git.

## Verification

- Preview through HTTP as documented in `README.md`; do not rely on opening `index.html` directly for live-data checks.
- Exercise loading, partial-provider failure, narrow mobile layout, and desktop layout after material UI or data changes.
- Validate `wrangler.toml` after changing deployment configuration.
