---
title: "The hidden clear-context toggle matters when using opusplan with Claude Code"
url: "https://x.com/validatedev/status/2045546302646170079"
timestamp: "Sat Apr 18 16:53:37 +0000 2026"
bookmark_id: "2045546302646170079"
author: "validatedev"
author_handle: "validatedev"
analyzed_at: "2026-04-20T07:00:00Z"
lang: "en"
confidence: "high"
tags:
  - claude-code
  - context-management
  - prompt-caching
  - settings
media_analyzed: false
cost: "~$0.0040"
priority: "normal"
---
## Topic

A Claude Code setting restores a hidden clear-context option in plan mode, which can matter for users who care about context hygiene.

## Research Summary

- The raw Claude Code changelog explicitly confirms the setting: `{"showClearContextOnPlanAccept": true}` restores the plan-mode clear-context option.
- That makes the post's core tip factual.
- The stronger claim, that this directly improves prompt-cache behavior in a guaranteed way, is better treated as practitioner guidance than official performance doctrine.

## Key Findings

- Anthropic's raw changelog documents that the clear-context option is hidden by default in plan mode and can be restored with a setting.
- Clear-context controls plausibly matter for users who want tighter prompt-cache hygiene or cleaner handoff into execution.
- The causal claims about cache misses are plausible, but not presented in the sources as a formal guarantee.

## Evidence & Sources

1. Original X post: https://x.com/validatedev/status/2045546302646170079
2. Claude Code raw changelog: https://raw.githubusercontent.com/anthropics/claude-code/main/CHANGELOG.md
3. Claude Code model config docs: https://code.claude.com/docs/en/model-config
4. Prompt caching docs: https://platform.claude.com/docs/en/build-with-claude/prompt-caching
5. GitHub issue about compact/clear context in plan mode: https://github.com/anthropics/claude-code/issues/38244

## Practical Relevance (for Gonzalo)

- Relevant if Gonzalo uses plan mode and wants more deliberate control over what context survives into the next phase.
- It is especially useful for long sessions where stale context can quietly accumulate.

## Risks / Caveats

- Clearing context can also remove useful state, so the control is not automatically beneficial in every workflow.
- Prompt caching behavior depends on more than one UI toggle.

## Recommended Next Steps

1. Enable the setting if plan-mode clear-context control fits Gonzalo's workflow.
2. Compare output quality and session cleanliness with and without clearing before execution.
3. Treat cache benefits as a hypothesis to test, not a guaranteed optimization.
