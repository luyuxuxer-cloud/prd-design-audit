# PRD Design Audit Rubric

Use this rubric to judge whether a PRD is ready for interaction design. Score each dimension from 0 to 3.

## Score Scale

- **3 - Strong**: Clear, specific, measurable, and directly usable for design decisions.
- **2 - Usable with gaps**: Direction is mostly clear, but some design-critical details require confirmation.
- **1 - Weak**: Important information is vague, contradictory, or too high-level to guide design.
- **0 - Missing/blocking**: The PRD lacks the information needed to proceed safely.

## Readiness Verdict

- **Ready**: No blocking gaps; design can start with normal follow-up questions.
- **Conditional**: Design can start only after specific assumptions are accepted or questions are answered.
- **Not ready**: Core problem, scope, metrics, users, or rules are too unclear for responsible design work.

## Dimensions

### 1. Problem and Background
Check whether the PRD explains why this requirement exists now, what business/user problem it solves, and what happens if it is not done.

Red flags:
- Only describes a feature request, not the underlying problem.
- Uses vague business pressure such as "提升效率" or "提升转化" without causal explanation.
- Has no target user pain point or business trigger.

### 2. Target Users and Scenarios
Check whether user roles, segments, entry points, motivations, and scenario boundaries are explicit.

Red flags:
- Says "用户" but mixes consumer, merchant, advertiser, operator, reviewer, or sales roles.
- No primary/secondary scenario.
- No frequency, timing, or context of use.

### 3. Scope and Non-goals
Check whether in-scope, out-of-scope, launch phases, platform/device coverage, and dependencies are defined.

Red flags:
- Scope expands across multiple systems without ownership.
- No non-goals.
- No explanation of MVP versus later phases.

### 4. Business Logic and Commercial Model
For commercial work, inspect money flow, advertiser/merchant/platform/user incentives, billing, budget, bidding, ranking, inventory, eligibility, audit, and settlement logic.

Red flags:
- Monetization goal conflicts with user experience.
- ROI/ROAS, GMV, budget, cost, or conversion terms lack definition.
- No guardrails for abuse, low-quality traffic, mis-selling, or advertiser loss.

### 5. Success Metrics
Check whether metrics are measurable, attributable, owned, and useful for design.

Required properties:
- Definition and formula
- Baseline and target
- Measurement window
- Event/data source
- Attribution logic
- Primary metric, secondary metrics, and guardrails
- Experiment or launch evaluation method

Red flags:
- Only lists high-level outcomes such as revenue or retention.
- Metrics can move for reasons unrelated to this design.
- No negative metrics for user harm, complaint rate, task failure, or quality.

### 6. Core Flow and Interaction Completeness
Check whether the user journey, key decisions, operations, feedback, confirmation, undo/cancel, and completion states are clear.

Red flags:
- Only lists pages, not user tasks.
- No entry/exit conditions.
- No explanation of what happens after user action.

### 7. State and Edge Case Coverage
Check whether default, loading, empty, error, disabled, permission denied, audit pending, rejected, expired, paused, insufficient data, and offline/network states are covered where relevant.

Red flags:
- Assumes happy path only.
- No error reason or recovery path.
- No state ownership between client/server/operator.

### 8. Data, Permission, and System Rules
Check whether fields, data sources, freshness, permissions, visibility, editability, audit logs, and privacy/compliance constraints are specified.

Red flags:
- Shows a field but does not define source or empty value.
- No role-based permissions.
- No compliance/legal requirement for commercial claims or user data.

### 9. Dependencies and Delivery Risk
Check engineering, backend, algorithm, strategy, data, ops, legal, finance, and localization dependencies.

Red flags:
- Critical dependency has no owner or timeline.
- Design depends on an algorithm/strategy not yet defined.
- Launch plan omits migration, rollback, gray release, or experiment config.

### 10. Design Actionability
Check whether an interaction designer can identify pages/modules, information architecture, flows, states, and decision points from the PRD.

Red flags:
- Designer must invent product rules.
- PRD has no decision hierarchy.
- Success criteria cannot inform UX tradeoffs.
