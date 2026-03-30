---
title: "2/ Move sessions back and forth between mobile/web/desktop and terminal"
url: "https://x.com/bcherny/status/2038454339933548804"
timestamp: "Mon Mar 30 03:12:41 +0000 2026"
bookmark_id: "2038454339933548804"
author: "Boris Cherny"
author_handle: "bcherny"
analyzed_at: "2026-03-30T07:00:00Z"
lang: "en"
confidence: "high"
tags: ['x-bookmark', 'claude-code', 'remote-control', 'developer-workflow', 'research', '2026']
media_analyzed: false
cost: "~$0.0042"
priority: "normal"
---

## Topic

Claude Code session mobility (teleport + remote control)

## Research Summary

The post highlights moving Claude Code sessions across terminal, web, and mobile using teleport and remote-control features.

## Key Findings

- Claude Code supports moving active work between environments instead of restarting context from scratch.
- Remote Control keeps the local terminal session running while controlling it from another device.
- This pattern is especially useful for long-running tasks and asynchronous review while away from desk.

## Evidence & Sources

- https://x.com/bcherny/status/2038454339933548804
- https://code.claude.com/docs/en/remote-control
- https://code.claude.com/docs/en/claude-code-on-the-web
- https://www.datacamp.com/tutorial/claude-code-remote-control

## Practical Relevance (for Gonzalo)

- Lets Gonzalo start tasks on desktop and check/steer from phone without losing local tool access.
- Reduces interruption cost during commute or context switches.

## Risks / Caveats

- Remote-control sessions can expose local workspace if links are mishandled.
- Feature behavior may change during preview phases.

## Recommended Next Steps

1. Pilot on one non-sensitive repo this week.
2. Define a simple rule: remote-control only on trusted network/VPN.
3. Document preferred handoff flow in personal notes.
