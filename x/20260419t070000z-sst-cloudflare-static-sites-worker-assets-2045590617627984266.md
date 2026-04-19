---
title: "Deploying Cloudflare static sites in SST with Worker assets"
url: "https://x.com/vimtor/status/2045590617627984266"
timestamp: "Sat Apr 18 19:49:43 +0000 2026"
bookmark_id: "2045590617627984266"
author: "vimtor"
author_handle: "vimtor"
analyzed_at: "2026-04-19T07:00:00Z"
lang: "en"
confidence: "high"
tags:
  - sst
  - cloudflare
  - workers
  - static-sites
media_analyzed: false
cost: "~$0.0040"
priority: "normal"
---
## Topic

SST has added a higher-level path for deploying Cloudflare static sites using Worker assets, which matters because it brings redirects and static-asset behavior closer to Cloudflare’s native model.

## Research Summary

- SST now documents a StaticSiteV2 component for Cloudflare, and Cloudflare itself documents static assets and redirects as native Worker capabilities.
- That makes the tweet’s claim about better defaults and improved redirects plausible and well grounded.
- The real win is not just deployment, but getting Cloudflare-native static routing behavior without hand-rolling a Worker wrapper.

## Key Findings

- Cloudflare static assets can serve files directly without invoking Worker logic on every request.
- SST is converging on a more Cloudflare-native abstraction instead of treating static sites as an afterthought.
- Redirect and header support is a meaningful operational detail for production sites, not cosmetic polish.

## Evidence & Sources

1. Original X post: https://x.com/vimtor/status/2045590617627984266
2. SST StaticSiteV2 docs: https://sst.dev/docs/component/cloudflare/static-site-v2/
3. Cloudflare static assets docs: https://developers.cloudflare.com/workers/static-assets/
4. Cloudflare redirects docs: https://developers.cloudflare.com/workers/static-assets/redirects/
5. Independent walkthrough: https://thefridaydeploy.substack.com/p/a-minimal-static-site-with-cloudflare

## Practical Relevance (for Gonzalo)

- Useful if Gonzalo wants a cleaner path for shipping marketing or docs sites on Cloudflare without custom glue.
- It is also relevant for projects that want static performance plus Worker-powered extensions later.

## Risks / Caveats

- Abstractions can drift from underlying platform behavior if SST changes faster than Cloudflare docs.
- Migrating existing Workers Sites setups may still require testing around redirects and asset routing.

## Recommended Next Steps

1. Use StaticSiteV2 for new Cloudflare-hosted static properties.
2. Validate redirects, headers, and fallback behavior in preview before switching production traffic.
3. Keep the underlying Cloudflare asset model in mind so debugging stays straightforward.
