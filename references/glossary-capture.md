# Glossary Capture

Use this guide to extract and maintain reusable terminology from PRDs, especially commercial/business PRDs with dense domain language.

## What to Extract

Capture terms that are likely to recur or affect design decisions:

- Acronyms and abbreviations: ROI, ROAS, GMV, CPA, CVR, LTV, SKU, CRM.
- Metrics: conversion rate, budget consumption, effective revenue, click-through rate, retention, complaint rate.
- Commercial concepts: advertiser, merchant, campaign, ad group, bidding, billing, rebate, settlement, promotion, inventory.
- Product objects: task, order, asset, creative, audience package, strategy, rule, template, lead.
- Roles: user, advertiser, seller, operator, reviewer, sales, admin, agent.
- Systems and platforms: internal tools, data platforms, moderation systems, billing systems.
- Strategy names and experiment names.
- Compliance, risk, or audit terms.

Avoid capturing ordinary UI words unless they have a specific domain meaning.

## Term Status

- **confirmed**: PRD explicitly defines the term or provides enough context.
- **inferred**: Meaning is strongly implied but not formally defined.
- **needs-confirmation**: Term is important but ambiguous, overloaded, or unsupported by context.

## Output Columns

Use this table in audit output:

| 术语 | 类型 | PRD 上下文 | 暂定解释 | 状态 | 建议沉淀位置 |
|---|---|---|---|---|---|

Term types:

- `acronym`
- `metric`
- `role`
- `product-object`
- `commercial-concept`
- `system`
- `strategy`
- `risk-compliance`
- `other`

## Obsidian Persistence

When the user asks to save terms into the vault:

1. Save reusable glossary knowledge under `40_知识库/业务领域/商业化术语库.md`.
2. Do not save raw PRD excerpts under `40_知识库/`.
3. If a raw PRD needs to be archived, place it under `30_资料库/PRD与需求/`.
4. Preserve uncertainty instead of pretending a term is confirmed.
5. Prefer wikilinks when a term connects to a stable project, business domain, or design pattern note.

Suggested entry format:

```markdown
### Term Name
- 类型：
- 中文解释：
- 英文/缩写：
- 适用场景：
- 设计影响：
- 常见混淆：
- 来源：
- 状态：confirmed / inferred / needs-confirmation
```

## Design Lens

For each important term, ask:

- Does this term affect what the user sees?
- Does it change permissions, states, or available actions?
- Is it a metric that affects design success?
- Is it a business rule that needs UI explanation?
- Is it a risk/compliance term that constrains copy, layout, or flow?
