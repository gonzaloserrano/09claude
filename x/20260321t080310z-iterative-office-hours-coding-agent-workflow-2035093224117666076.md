---
title: "Iterative office-hours style prompting for coding agents"
url: "https://x.com/Voxyz_ai/status/2035093224117666076"
timestamp: "Fri Mar 20 20:36:49 +0000 2026"
bookmark_id: "2035093224117666076"
author: "Vox"
author_handle: "@Voxyz_ai"
analyzed_at: "2026-03-21T08:03:10Z"
lang: en
confidence: medium
tags: [ai-coding, prompting, agent-workflows, debugging]
media_analyzed: "image (screenshot with command list)"
cost: "~$0.0032"
priority: normal
---

## Topic
Iterative office-hours style prompting for coding agents

## Research Summary
The post highlights a structured “office-hours” agent workflow: challenge problem framing, propose alternatives, and debug to root cause. This aligns with emerging best practices in agentic software development where plan-review loops outperform one-shot code generation.

## Key Findings
- Structured prompt routines (plan/review/debug commands) reduce shallow output and improve implementation quality.
- Root-cause-first debugging is now a recommended pattern in modern AI coding workflows.
- The trend is toward reusable “skills”/command packs that encode team process, not just prompt text.

## Evidence & Sources
- Official: https://code.claude.com/docs/en/scheduled-tasks
- Official: https://cloud.google.com/blog/topics/developers-practitioners/five-best-practices-for-using-ai-coding-assistants
- Independent: https://addyosmani.com/blog/ai-coding-workflow/
- Independent: https://codescene.com/blog/agentic-ai-coding-best-practice-patterns-for-speed-with-quality

## Practical Relevance (for Gonzalo)
Useful for your own OpenClaw/Codex workflows: formalize prompt “skills” for planning, CEO-style critique, and root-cause debugging before implementation.

## Risks / Caveats
Hype risk: screenshots are anecdotal. Without evaluation benchmarks, perceived quality may overstate real gains.

## Recommended Next Steps
Create 2-3 reusable internal skills: `/plan-review`, `/root-cause-debug`, `/implementation-options`, then compare outputs vs baseline prompts for one week.
