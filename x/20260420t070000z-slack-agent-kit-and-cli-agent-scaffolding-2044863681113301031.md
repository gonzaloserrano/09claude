---
title: "Slack is making agent deployment and UI scaffolding more native"
url: "https://x.com/SlackHQ/status/2044863681113301031"
timestamp: "Thu Apr 16 19:41:07 +0000 2026"
bookmark_id: "2044863681113301031"
author: "SlackHQ"
author_handle: "SlackHQ"
analyzed_at: "2026-04-20T07:00:00Z"
lang: "en"
confidence: "high"
tags:
  - slack
  - agents
  - block-kit
  - developer-tools
media_analyzed: true
cost: "~$0.0040"
priority: "normal"
---
## Topic

Slack is pushing agents deeper into its own platform, with native scaffolding, SDK support, and UI building blocks.

## Research Summary

- The official Slack materials support the basic claim that agent workflows are becoming a first-class part of Slack's developer story.
- The quickstart and CLI notes confirm that `slack create agent` is a real command and that Slack is offering multiple ways to build agents.
- The practical implication is less about a single feature and more about Slack trying to keep agent creation, deployment, and interaction inside its own ecosystem.

## Key Findings

- Slack documents an agent quickstart and multiple SDK paths for building agents.
- The CLI now includes `slack create agent`, which makes agent scaffolding a supported workflow.
- Richer Block Kit and in-Slack workflow grounding make agents feel more native than bolt-on bots.

## Evidence & Sources

1. Original X post: https://x.com/SlackHQ/status/2044863681113301031
2. Slack blog: https://slack.com/blog/news/slack-is-where-agents-work
3. Slack quickstart: https://docs.slack.dev/ai/agent-quickstart/
4. Slack CLI release notes: https://docs.slack.dev/changelog/2026/04/10/slack-cli/

## Practical Relevance (for Gonzalo)

- Relevant if Gonzalo wants to build internal agents where the chat surface, approval flow, and UI all live inside Slack.
- It suggests Slack is a stronger target now for team-facing agent products than it was when bots felt more peripheral.

## Risks / Caveats

- Platform-native agent tooling can create lock-in around Slack-specific workflows and components.
- Announcements can make the path look smoother than the day-to-day integration work really is.

## Recommended Next Steps

1. Evaluate Slack's agent quickstart before building a custom integration layer.
2. Check whether the required workflow fits Gonzalo's preferred stack and deployment model.
3. Treat Slack-native UI as a product advantage only if the target users already live there.
