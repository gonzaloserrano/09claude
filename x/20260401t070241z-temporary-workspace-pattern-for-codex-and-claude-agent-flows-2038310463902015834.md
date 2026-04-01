---
title: "Temporary-workspace pattern for Codex/Claude agent workflows (Cubby-style)"
url: "https://x.com/simonbs/status/2038310463902015834"
timestamp: "2026-03-29T17:40:59Z"
bookmark_id: "2038310463902015834"
author: "Simon B"
author_handle: "@simonbs"
analyzed_at: "2026-04-01T07:02:41Z"
lang: "en"
confidence: "medium-high"
tags: ["coding-agents", "codex", "claude", "developer-tools", "workspaces"]
media_analyzed: true
cost: "~$0.0036"
priority: "normal"
---

## Topic
A local UX pattern that lets developers drag files into a temporary shelf/workspace and launch coding agents (Codex/Claude) with focused context instead of full-repo context.

## Research Summary
The product mentioned (Cubby) appears to be a personal/new tool demo. The broader pattern is well aligned with official guidance from coding-agent tooling: constrain context, isolate execution, and keep reproducible workspace boundaries. This improves signal quality, reduces accidental context leakage, and can lower token/cost usage.

## Key Findings
- Scoped temporary workspaces reduce context noise and produce more deterministic agent behavior.
- Isolated per-task directories are safer for experimentation and easier to clean up.
- Passing curated instructions/context files (e.g., AGENTS.md-like conventions) tends to improve action quality over dumping whole repositories.
- "Spawn in empty workspace" is useful for greenfield prototyping and avoids coupling to legacy project state.

## Evidence & Sources
1. OpenAI Codex docs (agent project instructions/context): https://developers.openai.com/codex/guides/agents-md
2. OpenAI Codex repository (CLI workflow and local-agent model): https://github.com/openai/codex
3. Anthropic docs (Claude Code concepts and workflows): https://docs.anthropic.com/en/docs/claude-code/overview
4. Simon Willison writing on coding-agent workflows/research projects: https://simonw.substack.com/p/code-research-projects-with-async

## Practical Relevance (for Gonzalo)
- For your daily research automation, a temp-workspace launcher can separate ingestion/output tasks from your main repo and prevent accidental commits.
- Could be reused for "one bookmark = one workspace" when deep-diving technical threads.

## Risks / Caveats
- New single-developer tools may change quickly and lack long-term support.
- Workspace isolation helps, but credentials in environment variables can still leak to spawned processes.
- UX convenience can hide complexity (cleanup, provenance, and audit trail).

## Recommended Next Steps
1. Pilot a minimal local wrapper: create temp dir, copy selected files, launch agent, then archive outputs.
2. Add automatic provenance metadata (input files, model, timestamp, token/cost estimate).
3. Enforce default-deny network access for sensitive analysis runs when possible.