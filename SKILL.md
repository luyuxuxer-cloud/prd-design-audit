---
name: prd-design-audit
description: 面向互联网交互设计师的 PRD 设计诊断、风险审查、Success Metrics 校验、设计需求转译和商业化术语沉淀。Use when the user provides or references a PRD, demand document, product requirement, business requirement, commercial product spec, feature proposal, or asks to review whether a requirement is clear enough for design, identify risks, evaluate metrics, produce a design overview, or extract domain terms/acronyms into a knowledge base.
---

# PRD Design Audit

## Overview

Use this skill to turn a PRD into design-ready judgment: determine whether the requirement is sound, whether metrics are usable, where design risk hides, what the interaction designer should design, and which commercial/domain terms should be captured as reusable knowledge.

Default to Chinese output unless the user asks otherwise. Be precise, critical, and useful for an internet product interaction designer working on complex commercial/business scenarios.

## Workflow

1. **Collect source material**
   - Read the PRD from the provided text, file, cloud note, document, or pasted excerpt.
   - If only a partial PRD is available, still audit what is present and mark missing sections explicitly.
   - If working inside the user's Obsidian vault and the user asks to persist notes, store raw PRD material under `30_资料库/PRD与需求/`, not under `40_知识库/`.

2. **Extract the PRD skeleton**
   - Identify: background, business goal, user problem, target users, scenarios, scope, non-goals, flow, states, dependencies, metrics, experiment plan, launch plan, and open questions.
   - Separate facts stated by the PRD from inferences.
   - Preserve original product/business terms before translating them.

3. **Run the design audit**
   - Use `references/audit-rubric.md` for the scoring criteria.
   - Judge the PRD across: problem clarity, user/scenario clarity, business logic, success metrics, interaction completeness, state coverage, data/permission rules, commercial risk, dependencies, and design actionability.
   - For every meaningful issue, include: evidence from the PRD, why it matters for design, risk level, and the concrete question or change to ask from PM/business/engineering/data.

4. **Evaluate Success Metrics**
   - Check whether each metric has definition, baseline, target, time window, attribution path, owner, event/data source, and guardrail.
   - Flag vanity metrics, conflicting metrics, unmeasurable goals, and metrics that cannot guide design choices.
   - In commercial PRDs, look for funnel metrics, conversion quality, ROI/ROAS, budget consumption, revenue impact, merchant/advertiser experience, user experience guardrails, and platform risk.

5. **Translate into a design overview**
   - Produce a design-facing brief, not a generic product summary.
   - Include: one-line requirement, design objective, target roles, core scenarios, task flow, key modules/pages, interaction rules, required states, edge cases, data fields, permission/entry rules, instrumentation needs, risks, and PM questions.
   - Make the overview directly usable for kickoff, design exploration, or Figma annotation.

6. **Extract and maintain terminology**
   - Use `references/glossary-capture.md` for term taxonomy and output format.
   - Extract acronyms, domain terms, metrics, role names, system names, product objects, strategy names, and commercial concepts.
   - Mark terms as `confirmed`, `inferred`, or `needs-confirmation`.
   - If the user asks to save knowledge in the vault, append or update reusable terms in `40_知识库/业务领域/商业化术语库.md`. Do not place raw PRD content there.

## Output Format

Use this structure unless the user requests a different format:

```markdown
## 结论
- PRD 状态：Ready / Conditional / Not ready
- 设计可开工判断：...
- 最大风险：...

## 评分概览
| 维度 | 评分 | 判断 |
|---|---:|---|

## 关键问题与风险
| 优先级 | 问题 | 设计影响 | 建议追问/动作 |
|---|---|---|---|

## Success Metrics 诊断
| 指标 | 问题 | 是否能指导设计 | 建议 |
|---|---|---|---|

## 设计 Overview
- 需求一句话：
- 目标用户/角色：
- 核心场景：
- 用户任务链路：
- 关键页面/模块：
- 必须覆盖的状态：
- 数据/权限/规则：
- 设计决策点：

## 待确认问题
1. ...

## 术语与缩写
| 术语 | 类型 | PRD 上下文 | 暂定解释 | 状态 |
|---|---|---|---|---|
```

## Quality Bar

- Do not merely summarize. Diagnose whether the PRD is good enough for design.
- Do not invent missing business rules. Mark them as unknown and ask concrete questions.
- Prefer actionable design implications over broad comments.
- Keep raw PRD evidence short and paraphrased when possible.
- In Obsidian notes, use frontmatter for formal notes and do not leave an empty line after frontmatter.
- Use wikilinks for stable knowledge notes when saving into the vault.

## References

- Read `references/audit-rubric.md` when performing the PRD audit.
- Read `references/glossary-capture.md` when extracting terms or updating the user's terminology knowledge base.
