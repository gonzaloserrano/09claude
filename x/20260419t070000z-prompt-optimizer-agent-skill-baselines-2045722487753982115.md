---
title: "Prompt optimizer skills for agent baseline behavior"
url: "https://x.com/zeeg/status/2045722487753982115"
timestamp: "Sun Apr 19 04:33:43 +0000 2026"
bookmark_id: "2045722487753982115"
author: "David Cramer"
author_handle: "zeeg"
analyzed_at: "2026-04-19T07:00:00Z"
lang: "en"
confidence: "high"
tags:
  - agents
  - prompt-engineering
  - skills
  - claude-code
media_analyzed: false
cost: "~$0.0040"
priority: "normal"
---
## Topic

A concrete example of turning prompt-engineering heuristics into a reusable skill so agents start with a better operating baseline instead of re-learning the same guidance in every session.

## Research Summary

- Claude Code skills are a first-class mechanism for bundling reusable instructions and supporting files, so the concept behind the tweet is real rather than just prompt folklore.
- The Sentry pull request shows a live implementation of a prompt-optimizer skill, which is useful evidence that teams are operationalizing agent guidance as code and documentation.
- The practical value is consistency: a skill can encode best practices once and make them available whenever an agent needs them.

## Key Findings

- Skills are a better home for durable agent rules than repeating long setup prompts in every task.
- A prompt-optimizer skill is effectively a meta-tool for improving future prompts, not a guarantee of better model quality by itself.
- The strongest use case is standardizing team conventions around planning, evidence gathering, and output structure.

## Evidence & Sources

1. Original X post: https://x.com/zeeg/status/2045722487753982115
2. Claude Code skills docs: https://code.claude.com/docs/en/skills?search=what+is+the+best+practive+regarding+leng#add-supporting-files
3. Sentry skills PR: https://github.com/getsentry/skills/pull/116

## Practical Relevance (for Gonzalo)

- Useful if Gonzalo wants stable agent behavior without bloating every prompt.
- Worth borrowing for repeated workflows like reviews, research digests, and release checklists.

## Risks / Caveats

- A bad skill can fossilize weak assumptions and spread them everywhere.
- Prompt optimization still needs evaluation, not just elegant wording.

## Recommended Next Steps

1. Extract any repeated research or coding rules into one local skill.
2. Keep the skill small and test it on a few real tasks before expanding it.
3. Prefer evidence-backed guidance over generic “be better” prompting advice.
