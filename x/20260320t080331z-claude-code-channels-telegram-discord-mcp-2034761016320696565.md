---
title: "Claude Code channels for Telegram/Discord via MCP"
url: "https://x.com/trq212/status/2034761016320696565"
timestamp: "2026-03-19T22:36:44Z"
bookmark_id: "2034761016320696565"
author: "Thariq"
author_handle: "trq212"
analyzed_at: "2026-03-20T08:03:31.585709Z"
lang: en
confidence: "high"
tags: ['claude-code', 'mcp', 'telegram', 'discord', 'agent-ops']
media_analyzed: "yes"
cost: "~$0.0049"
priority: "normal"
---

## Topic
Anthropic's new Claude Code channels feature: bridging a live coding session to Telegram/Discord through MCP plugins.

## Research Summary
The post announces a new remote-control workflow where Claude Code sessions can receive and respond to external chat events. Official docs describe channels as MCP servers/plugins (research preview) that can push events into an active session and optionally send replies back to the same platform.

## Key Findings
- Channels are tied to a **running** Claude Code session; they are not store-and-forward inboxes.
- Access control exists at multiple layers: platform account pairing/allowlists and session/org-level channel enablement.
- The mechanism is consistent with MCP's host-client-server model over JSON-RPC-style structured interactions.
- Telegram and Discord transport constraints (bot APIs, interaction/webhook patterns, rate limits) materially affect latency/reliability for mobile-first usage.

## Evidence & Sources
- Claude Code docs (official): https://code.claude.com/docs/en/channels
- MCP specification (official): https://modelcontextprotocol.io/specification/2025-11-25
- Telegram Bot API (official): https://core.telegram.org/bots/api
- Discord interactions docs (official): https://discord.com/developers/docs/interactions/receiving-and-responding
- Independent coverage: https://venturebeat.com/orchestration/anthropic-just-shipped-an-openclaw-killer-called-claude-code-channels

## Practical Relevance (for Gonzalo)
- Strong fit for on-the-go triage: check CI/test outcomes, request quick edits, or ask for status without opening laptop IDE.
- Best used for bounded tasks and approvals; keep high-risk operations guarded (e.g., require explicit confirmation before deploy/file deletes).
- If adopted daily, define a small command vocabulary for mobile prompts to reduce ambiguity and token waste.

## Risks / Caveats
- Research preview: behavior and flags may change quickly.
- Session availability dependency: no active session means no replies/events handled.
- Chat-platform noise or unauthorized senders can create distraction/risk without tight allowlists and channel scoping.
- Third-party reporting may overstate parity with other tools; validate on your own workload.

## Recommended Next Steps
1. Run a 7-day pilot using one repository and low-risk tasks only.
2. Create a minimal runbook: allowed commands, escalation rules, and "never do" actions.
3. Measure latency, task completion quality, and interruption rate across Telegram vs Discord.
4. Reassess after preview updates and decide whether to expand scope.
