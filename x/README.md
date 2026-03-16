# X Bookmark Analyses

This folder stores one markdown file per bookmarked X post.

## Naming convention

- lowercase
- hyphen-separated
- descriptive slug from meaning (not raw `t.co` tokens)
- include analyzed timestamp prefix + bookmark id suffix to keep chronological ordering and avoid collisions

Example:

`20260316t011430z-openclaw-update-ai-agent-capabilities-2032758640285995314.md`

## Required frontmatter

- title
- url
- timestamp
- bookmark_id
- author
- author_handle
- analyzed_at
- lang
- confidence (low|medium|high)
- tags (array)
- cost (estimated USD cost for this single bookmark analysis)

## Required sections

- Summary
- Key Insights
- Evidence & Links
- Practical Relevance (for Gonzalo)
- Risks / Caveats
- Actions
