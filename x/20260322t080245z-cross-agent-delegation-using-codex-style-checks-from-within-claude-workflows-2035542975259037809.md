---
title: "Cross-agent delegation: using Codex-style checks from within Claude workflows"
url: "https://x.com/t_blom/status/2035542975259037809"
timestamp: "Sun Mar 22 02:23:58 +0000 2026"
bookmark_id: "2035542975259037809"
author: "Tom Blomfield"
author_handle: "@t_blom"
analyzed_at: "2026-03-22T08:02:45Z"
lang: en
confidence: medium
tags: [ai-coding-agents, workflow-design, claude-code, codex]
media_analyzed: "none"
cost: "~$0.0024"
priority: normal
---

## Topic
Cross-agent delegation: using Codex-style checks from within Claude workflows

## Research Summary
The tweet suggests a practical workflow where Claude delegates verification or secondary checks to Codex via a reusable skill. The core topic is not the specific gstack implementation but the broader pattern of multi-agent coding loops (builder + auditor).

## Key Findings
- Official Codex docs now describe CLI + Skills patterns that fit an auditor role in terminal workflows.
- Anthropic Claude Code docs support extensibility through skills, making cross-tool delegation operable in practice.
- Independent coverage and practitioner posts increasingly recommend role-splitting (implementer vs reviewer) to reduce blind spots in AI-assisted coding.

## Evidence & Sources
- https://developers.openai.com/codex/cli
- https://developers.openai.com/codex/skills
- https://code.claude.com/docs/en/skills
- https://www.producttalk.org/how-to-use-claude-code-features/

## Practical Relevance (for Gonzalo)
For Gonzalo, this pattern is useful for higher-assurance tasks: code with one agent, then run focused audit/critique pass with another before merge.

## Risks / Caveats
Agent-to-agent loops can increase latency/cost and create false confidence if both models share similar blind spots or weak test harnesses.

## Recommended Next Steps
Create a lightweight /audit step in your local workflow that runs after each meaningful commit and records findings in PR notes.
