---
title: "AI code auditing strategy: why single-pass reviews miss severe defects"
url: "https://x.com/sterlingcrispin/status/2035031512123678994"
timestamp: "Fri Mar 20 16:31:36 +0000 2026"
bookmark_id: "2035031512123678994"
author: "Sterling Crispin 🕊️"
author_handle: "@sterlingcrispin"
analyzed_at: "2026-03-22T08:02:45Z"
lang: en
confidence: medium
tags: [code-quality, ai-auditing, secure-coding, review-process]
media_analyzed: "photo (not OCR-transcribed)"
cost: "~$0.0028"
priority: normal
---

## Topic
AI code auditing strategy: why single-pass reviews miss severe defects

## Research Summary
The tweet claims severe bugs frequently survive single-model audits and recommends repeated Codex-based reviews. The deeper topic is defect-detection reliability in AI-assisted code review pipelines.

## Key Findings
- Empirical literature on code review shows non-trivial defect leakage even with human processes; expecting one LLM pass to catch everything is unrealistic.
- Recent automated-review research focuses on defect-oriented pipelines and multi-pass/context-enriched checks, aligning with the tweet's recommendation directionally.
- Operationally, combining tests + static analysis + independent LLM review is more robust than relying on one auditor model.

## Evidence & Sources
- https://github.com/sterlingcrispin/claude_slash_commands/blob/main/auditcodex/SKILL.md
- https://arxiv.org/html/2505.17928v2
- https://openreview.net/forum?id=mEV0nvHcK3
- https://en.wikipedia.org/wiki/Code_review

## Practical Relevance (for Gonzalo)
For Gonzalo: add a gate where high-risk diffs (auth, billing, data deletion) require at least one independent AI audit plus CI checks before merge.

## Risks / Caveats
Running many audit passes can inflate cost and still miss logic bugs without strong tests/specs; over-trusting AI critiques can also create churn.

## Recommended Next Steps
Define critical-change criteria and enforce a mandatory second-auditor + targeted regression tests for those commits.
