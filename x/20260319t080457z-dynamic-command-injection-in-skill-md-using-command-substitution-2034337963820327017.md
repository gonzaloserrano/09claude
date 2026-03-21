---
title: "Dynamic command injection in SKILL.md using command substitution"
url: "https://x.com/lydiahallie/status/2034337963820327017"
timestamp: "2026-03-18T18:35:41Z"
bookmark_id: "2034337963820327017"
author: "Lydia Hallie ✨"
author_handle: "lydiahallie"
analyzed_at: "2026-03-19T08:04:57.803031Z"
lang: en
confidence: "medium"
tags: ['agent-skills', 'dynamic-context', 'prompt-engineering']
media_analyzed: "yes"
cost: "~$0.0042"
priority: "normal"
---

## Topic
Dynamic command injection in SKILL.md using command substitution

## Research Summary
Embedding command outputs in skill docs can provide fresh context, but introduces reliability and security concerns if not constrained.

## Key Findings
- Dynamic context can improve relevance for time-sensitive tasks.
- Unbounded command execution in prompt assembly increases attack surface and nondeterminism.
- Best practice is allowlists, timeouts, and explicit escaping/sanitization.

## Evidence & Sources
- [Anthropic prompt engineering docs](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
- [OpenAI prompt engineering guide](https://platform.openai.com/docs/guides/prompt-engineering)
- [OWASP command injection overview](https://owasp.org/www-community/attacks/Command_Injection)

## Practical Relevance (for Gonzalo)
Useful pattern for live context, but should be gated with strict command controls.

## Risks / Caveats
- Feature details may change quickly during rollout phases.
- Social posts can omit constraints, prerequisites, or edge cases.
- Validate critical claims against official documentation before decisions.

## Recommended Next Steps
- Track official release notes for concrete capability updates.
- Run a small scoped trial before workflow-wide adoption.
- Document what works and what breaks in Gonzalo's environment.
