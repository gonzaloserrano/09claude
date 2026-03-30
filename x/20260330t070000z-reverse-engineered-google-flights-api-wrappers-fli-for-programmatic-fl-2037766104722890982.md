---
title: "Direct Google Flights API access without scraping"
url: "https://x.com/tom_doerr/status/2037766104722890982"
timestamp: "Sat Mar 28 05:37:53 +0000 2026"
bookmark_id: "2037766104722890982"
author: "Tom Dörr"
author_handle: "tom_doerr"
analyzed_at: "2026-03-30T07:00:00Z"
lang: "en"
confidence: "medium"
tags: ['x-bookmark', 'travel-tech', 'api', 'google-flights', 'python', 'research', '2026']
media_analyzed: true
cost: "~$0.0041"
priority: "normal"
---

## Topic

Reverse-engineered Google Flights API wrappers (fli) for programmatic flight search

## Research Summary

The bookmark claims direct Google Flights API access via the fli project, which appears to use reverse-engineered endpoints rather than an official public API.

## Key Findings

- The fli repository markets itself as Google Flights MCP/Python tooling with reverse-engineered access.
- No broadly documented official public Google Flights API currently appears available for general developers.
- Third-party providers often monetize scraping or unofficial access layers with reliability/compliance trade-offs.

## Evidence & Sources

- https://x.com/tom_doerr/status/2037766104722890982
- https://github.com/punitarani/fli
- https://punitarani.github.io/fli/
- https://apify.com/api/google-flights-api

## Practical Relevance (for Gonzalo)

- Could be useful for quick travel automation experiments, but production risk is non-trivial.
- Good candidate for prototype-only usage with strict fallback behavior.

## Risks / Caveats

- Unofficial endpoints may break without notice.
- Potential ToS/compliance concerns for commercial use.

## Recommended Next Steps

1. Treat as experimental dependency, not core infrastructure.
2. Add monitoring + fallback provider before any operational usage.
3. Review legal/compliance constraints before deployment.
