---
title: "Claude Code SessionStart hooks and .worktreeinclude for reproducible worktrees"
url: "https://x.com/amorriscode/status/2037303514574290976"
timestamp: "Thu Mar 26 22:59:43 +0000 2026"
bookmark_id: "2037303514574290976"
author: "Anthony Morris ツ"
author_handle: "@amorriscode"
analyzed_at: "2026-03-27T08:01:52Z"
lang: en
confidence: high
tags: ["claude-code", "developer-workflows", "git-worktree", "automation"]
media_analyzed: no
cost: "~$0.0024"
priority: normal
---

## Topic
Use SessionStart hooks to bootstrap dependencies/services per session and .worktreeinclude to replicate ignored-but-required local scaffolding across worktrees.

## Research Summary
Cross-checked the core claim against official docs and independent technical guidance to separate hype from durable practice.

## Key Findings
- Claude Code hooks can run initialization logic at session boundaries, reducing manual setup drift.
- Git worktrees do not automatically carry untracked/ignored local files; a curated include mechanism prevents missing env scaffolding.
- Combining both approaches gives reproducible local state without committing secrets or machine-specific noise.

## Evidence & Sources
- Anthropic docs: Claude Code hooks: https://docs.anthropic.com/en/docs/claude-code/hooks
- Git docs: git-worktree: https://git-scm.com/docs/git-worktree
- Yarn docs: yarn install: https://yarnpkg.com/cli/install
- Atlassian tutorial: Git worktrees in practice: https://www.atlassian.com/git/tutorials/git-worktree

## Practical Relevance (for Gonzalo)
Useful for Gonzalo if juggling multiple branches/agents: faster startup, fewer "works on one worktree" failures, and cleaner local automation standards.

## Risks / Caveats
Hook scripts can become brittle or slow. Keep idempotent and short; avoid secrets in plain-text scripts.

## Recommended Next Steps
Define a minimal SessionStart checklist (deps, containers, checks), version the non-secret scaffolding, and benchmark startup time before/after.