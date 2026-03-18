---
title: "Claude Code system design and health-audit skill (tw93/claude-health)"
url: "https://x.com/HiTw93/status/2033911478466843115"
timestamp: "2026-03-17T14:20:59Z"
bookmark_id: "2033911478466843115"
author: "Tw93"
author_handle: "HiTw93"
analyzed_at: "2026-03-18T08:04:30.720689Z"
lang: en
confidence: "high"
tags: ["claude-code", "systems-design", "skills", "quality-audit"]
media_analyzed: "no"
cost: "~$0.0048"
priority: "normal"
---

## Topic
Claude Code system design and health-audit skill (tw93/claude-health)

## Research Summary
The tweet reframes Claude Code failures as architecture/process issues rather than prompt tweaks, and points to a concrete remediation path via an audit skill.

## Key Findings
- The referenced `claude-health` skill operationalizes a six-layer review model (config/rules/skills/hooks/subagents/verifiers).
- This aligns with broader agent engineering guidance: reliability usually depends more on harness design and governance than on single prompts.
- Packaging the checks as a skill lowers adoption friction (`npx skills add ...` + command invocation).

## Evidence & Sources
- [tw93/claude-health repository](https://github.com/tw93/claude-health)
- [Tw93 deep dive article](https://tw93.fun/en/2026-03-12/claude.html)
- [Claude Code docs: Skills](https://code.claude.com/docs/en/skills)

## Practical Relevance (for Gonzalo)
- Useful as a recurring quality gate for Claude Code project setups.
- Could catch drift early (missing hooks, weak verifier strategy, inconsistent skill loading).

## Risks / Caveats
- Community skills vary in maintenance quality; pin versions and review before broad rollout.
- A checklist can improve baseline health, but it cannot replace domain-specific test coverage.

## Recommended Next Steps
1. Run `/health` on one active project and capture findings.
2. Convert high-value findings into project defaults/templates.
3. Re-run after any major workflow/tooling change.

### Bookmark Text
> Most Claude Code problems are not prompting problems. They are systems-design problems.

I wrote a deep dive on Claude Code's architecture, governance, and engineering internals. If you want the practical takeaway: `npx skills add tw93/claude-health`, then run `/health`.
