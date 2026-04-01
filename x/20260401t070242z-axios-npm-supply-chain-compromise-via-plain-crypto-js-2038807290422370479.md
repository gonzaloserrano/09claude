---
title: "Axios npm supply-chain compromise via malicious plain-crypto-js dependency"
url: "https://x.com/feross/status/2038807290422370479"
timestamp: "2026-03-31T02:35:11Z"
bookmark_id: "2038807290422370479"
author: "Feross"
author_handle: "@feross"
analyzed_at: "2026-04-01T07:02:42Z"
lang: "en"
confidence: "high"
tags: ["security", "npm", "supply-chain", "axios", "malware", "javascript"]
media_analyzed: false
cost: "~$0.0042"
priority: "normal"
---

## Topic
Active npm supply-chain compromise reports affecting axios versions that introduced a malicious transitive dependency (`plain-crypto-js`).

## Research Summary
Multiple security vendors and threat-intel reporting aligned on the same core timeline: malicious dependency injection into axios releases during a narrow time window. This is consistent with a real package ecosystem incident pattern (trusted package + malicious transitive + install-time execution).

## Key Findings
- Reported impacted axios versions: `1.14.1` and `0.30.4` during incident window.
- Malicious dependency: `plain-crypto-js@4.2.1` (with suspicious install behavior reported by multiple sources).
- Attack pattern: dependency confusion/maintainer compromise style insertion into a highly trusted package.
- Operational response for teams: pin to known-safe axios versions, clean lockfiles/caches, rotate credentials on potentially exposed build hosts.

## Evidence & Sources
1. Google Cloud Threat Intelligence report: https://cloud.google.com/blog/topics/threat-intelligence/north-korea-threat-actor-targets-axios-npm-package
2. Socket incident post: https://socket.dev/blog/axios-npm-package-compromised
3. Snyk incident analysis: https://snyk.io/blog/axios-npm-package-compromised-supply-chain-attack-delivers-cross-platform/
4. StepSecurity incident write-up: https://www.stepsecurity.io/blog/axios-compromised-on-npm-malicious-versions-drop-remote-access-trojan

## Practical Relevance (for Gonzalo)
- Any JS project in your ecosystem that installed axios during the incident window should be treated as potentially exposed.
- CI agents and developer machines are both high-risk surfaces due to token/SSH/cloud credential presence.

## Risks / Caveats
- Incident details can evolve (attribution, exact IOCs, additional impacted versions).
- Public posts may lag maintainers' final postmortem.
- Even after version rollback, post-install compromise risk may persist on previously infected machines.

## Recommended Next Steps
1. Audit lockfiles and artifact caches for affected versions immediately.
2. Force dependency re-resolution from clean cache using known-safe versions.
3. Rotate npm tokens, cloud credentials, and SSH keys present on build/developer hosts.
4. Add install-time script monitoring and dependency allow/deny policy in CI.