---
title: "Postgres as the gateway drug before open table formats and streams"
url: "https://x.com/viggy28/status/2045532786350788682"
timestamp: "Sat Apr 18 15:59:55 +0000 2026"
bookmark_id: "2045532786350788682"
author: "Vignesh Ravichandran"
author_handle: "viggy28"
analyzed_at: "2026-04-19T07:00:00Z"
lang: "en"
confidence: "medium"
tags:
  - data-platforms
  - postgres
  - kafka
  - iceberg
media_analyzed: false
cost: "~$0.0040"
priority: "normal"
---
## Topic

A data-platform argument that many teams start with Postgres, then graduate toward lakehouse or streaming patterns only when scale and organizational complexity force it.

## Research Summary

- The linked article argues that Postgres increasingly becomes the default starting point because it already sits where operational data is created.
- That does not eliminate Kafka or open table formats, but it does shift where teams begin and when they feel pain strongly enough to add more infrastructure.
- The attached streambed repository suggests the author is thinking about how stream processing and simpler developer ergonomics meet in practice.

## Key Findings

- For many teams, Postgres remains the most credible first system because it is already in production and easy to query.
- Kafka is still valuable when durability, replay, fan-out, and decoupled event pipelines matter more than warehouse simplicity.
- Iceberg plus object storage can displace some warehouse patterns, but not every queueing or eventing use case.

## Evidence & Sources

1. Original X post: https://x.com/viggy28/status/2045532786350788682
2. Postgres Is the Gateway Drug: https://viggy28.dev/article/postgres-gateway-drug/
3. streambed repository: https://github.com/viggy28/streambed

## Practical Relevance (for Gonzalo)

- Relevant if Gonzalo wants a sane progression path instead of prematurely adopting a full data platform.
- The framing is useful when deciding whether a project really needs Kafka or just cleaner extraction from Postgres.

## Risks / Caveats

- The claim is directional, not universal. High-scale streaming workloads still need specialized infrastructure.
- The evidence here is more practitioner argument than rigorous comparative benchmark.

## Recommended Next Steps

1. Use Postgres-first designs by default when the data volume and coupling are still small.
2. Promote to Kafka or lakehouse tooling only when replay, fan-out, or analytical scale clearly justify it.
3. Document the trigger conditions for that migration before the team needs them.
