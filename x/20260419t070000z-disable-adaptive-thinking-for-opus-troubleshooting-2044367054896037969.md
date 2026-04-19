---
title: "Disabling adaptive thinking as an Opus troubleshooting tactic"
url: "https://x.com/hmemcpy/status/2044367054896037969"
timestamp: "Wed Apr 15 10:47:43 +0000 2026"
bookmark_id: "2044367054896037969"
author: "Igal Tabachnik"
author_handle: "hmemcpy"
analyzed_at: "2026-04-19T07:00:00Z"
lang: "en"
confidence: "high"
tags:
  - claude-code
  - adaptive-thinking
  - opus
  - troubleshooting
media_analyzed: false
cost: "~$0.0040"
priority: "normal"
---
## Topic

A community workaround suggesting that some Claude Code sessions feel sharper when adaptive thinking is disabled, especially for users who prefer predictable fixed reasoning behavior.

## Research Summary

- The environment variable is real and documented by Anthropic, so the tweet is pointing at a legitimate control rather than an invented hack.
- That does not mean disabling adaptive thinking is always better, only that it can be a useful troubleshooting move for users who dislike the new behavior profile.
- The main value here is understanding that reasoning style is now a config surface, not just a hidden model trait.

## Key Findings

- Adaptive thinking can improve quality on some tasks while making behavior feel less predictable to some users.
- Turning it off is best understood as a debugging knob, not the official default for everyone.
- Effort, model choice, and verification still matter even if adaptive thinking is disabled.

## Evidence & Sources

1. Original X post: https://x.com/hmemcpy/status/2044367054896037969
2. Claude Code model config docs: https://code.claude.com/docs/en/model-config
3. Anthropic adaptive thinking docs: https://platform.claude.com/docs/en/build-with-claude/adaptive-thinking
4. Independent troubleshooting write-up: https://docs.bswen.com/blog/2026-04-09-claude-code-adaptive-reasoning-settings/

## Practical Relevance (for Gonzalo)

- Useful if Gonzalo feels Opus is drifty or under-thinking on certain tasks and wants a clean variable to test.
- This is a low-cost diagnostic switch compared with rewriting entire prompt stacks.

## Risks / Caveats

- Turning it off can reduce performance on tasks where dynamic reasoning helps.
- Users can misattribute every regression to adaptive thinking when other settings changed too.

## Recommended Next Steps

1. Test the setting on a fixed task suite before adopting it broadly.
2. Record cost and quality changes, not just vibes.
3. Pair any setting change with explicit verification steps.
