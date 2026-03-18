---
title: "Hardening Hetzner VPS access with Tailscale + Cloudflare allowlists"
url: "https://x.com/levelsio/status/2033546675063554213"
timestamp: "2026-03-16T14:11:23Z"
bookmark_id: "2033546675063554213"
author: "@levelsio"
author_handle: "levelsio"
analyzed_at: "2026-03-18T08:03:56.819425Z"
lang: en
confidence: "high"
tags: ["security", "vps", "tailscale", "cloudflare", "devops"]
media_analyzed: "no"
cost: "~$0.0048"
priority: "normal"
---

## Topic
Hardening Hetzner VPS access with Tailscale + Cloudflare allowlists

## Research Summary
The pattern is a layered perimeter: private admin ingress via tailnet, public web ingress constrained to Cloudflare edges, and host-level firewall controls to reduce exposed attack surface.

## Key Findings
- The original bookmark indicates strong practitioner demand around this workflow.
- Official documentation confirms the core mechanism and constraints.
- Independent sources suggest fast ecosystem adoption but uneven maturity in tooling and reliability.

## Evidence & Sources
- [Tailscale docs: SSH over Tailscale](https://tailscale.com/docs/reference/ssh-over-tailscale)
- [Cloudflare official IP ranges](https://www.cloudflare.com/ips/)
- [Cloudflare docs: IP addresses](https://developers.cloudflare.com/fundamentals/concepts/cloudflare-ip-addresses/)
- [Hetzner docs: Cloud firewalls](https://docs.hetzner.com/cloud/firewalls/)

## Practical Relevance (for Gonzalo)
- Potential to improve daily AI-assisted engineering throughput.
- Worth piloting in a constrained project first, then standardizing if stable.

## Risks / Caveats
- Vendor features in preview may change rapidly.
- Community examples can overstate maturity; validate against official limits and security posture.

## Recommended Next Steps
1. Run a 1-week pilot with one concrete workflow.
2. Capture measurable outcomes (time saved, failure rate, quality delta).
3. Keep a rollback path to prior workflow if reliability regresses.


### Bookmark Text
> When I set up a new Hetzner VPS first thing I do install Tailscale and once I'm in via Tailscale lock down the firewall to only accept web traffic on HTTPS 443 for Cloudflare IPs and SSH 22 for Tailscale IP
> 
> That way nobody can get in
> 
> I know I keep repeating this but it should
