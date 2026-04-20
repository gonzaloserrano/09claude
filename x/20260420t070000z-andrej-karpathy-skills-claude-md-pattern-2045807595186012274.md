---
title: "Encoding Karpathy-style coding discipline in one CLAUDE.md file"
url: "https://x.com/Sumanth_077/status/2045807595186012274"
timestamp: "Sun Apr 19 10:11:54 +0000 2026"
bookmark_id: "2045807595186012274"
author: "Sumanth_077"
author_handle: "Sumanth_077"
analyzed_at: "2026-04-20T07:00:00Z"
lang: "en"
confidence: "high"
tags:
  - claude-code
  - prompt-files
  - coding-discipline
  - karpathy
media_analyzed: true
cost: "~$0.0040"
priority: "normal"
---
## Topic

A repo that packages a coding philosophy into a single `CLAUDE.md` file for Claude Code to follow.

## Research Summary

- The repository and raw files support the core claim that the project is distilling a recognizable coding discipline into an instruction file.
- Its four stated principles are Think Before Coding, Simplicity First, Surgical Changes, and Goal-Driven Execution.
- The pattern is interesting less because it is novel prompt engineering and more because it makes coding norms explicit, portable, and reviewable.

## Key Findings

- The repo explicitly frames itself as translating Karpathy-style observations into four operational principles.
- A single `CLAUDE.md` file can act as a lightweight policy layer for agent coding behavior.
- The value here is consistency and guardrails, not a guarantee of better output in every context.

## Evidence & Sources

1. Original X post: https://x.com/Sumanth_077/status/2045807595186012274
2. Repo: https://github.com/forrestchang/andrej-karpathy-skills
3. Raw CLAUDE.md: https://raw.githubusercontent.com/forrestchang/andrej-karpathy-skills/main/CLAUDE.md
4. Repo README raw: https://raw.githubusercontent.com/forrestchang/andrej-karpathy-skills/main/README.md

## Practical Relevance (for Gonzalo)

- Relevant if Gonzalo wants clearer defaults for agent behavior without building a heavier harness.
- It is a good reminder that many failures come from missing norms, not missing model capability.

## Risks / Caveats

- A neat instruction file can still be too generic for a specific repo or team's workflow.
- Packaging a philosophy into one file does not remove the need for review and verification.

## Recommended Next Steps

1. Use the repo as a reference pattern for making coding norms explicit.
2. Adapt any such file to the actual project constraints instead of copying it blindly.
3. Measure whether the rules reduce rework and overengineering in practice.
