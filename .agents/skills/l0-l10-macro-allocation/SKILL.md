---
name: l0-l10-macro-allocation
description: Analyze China macro policy, industrial trends, asset allocation, local debt and LGFV risk, real estate, AI supply chains, regional risk, CCDI crack signals, audit and fiscal signals, and personal decision questions through an L0-L10 layered macro-allocation framework. Use when the user asks about China macro regimes, policy transmission, province or city risk, buying property, equity or bond allocation, sector rotation, long-cycle judgment, or explicit L0-L10 layered analysis.
---

# L0-L10 Macro Allocation

## Core Rule

Analyze from structural constraints down to tradeable or personal decisions:

`L0 -> L1 -> L6/L8 -> L9 -> L10 optional -> operational conclusion`

Do not let stories, market chatter, short-term price action, or single-source signals override higher-level constraints. The priority order is:

`L0 > L6/L8 > L9 > L10 > L7 > story machine`

Use this skill for judgment and allocation, not for personalized financial advice. State uncertainty, required validation, and the conditions that would change the conclusion.

For the full terminology, layer definitions, examples, forbidden moves, and initialization prompt, read `references/original-framework.md` when the user asks for framework detail, disputes a term, requests examples, or the task requires a complete L0-L10 mapping.

## Layer Definitions

- `L0`: hard constraints and base regime. Demographics, balance sheets, political economy, external constraints, fiscal capacity, leverage structure, and unavoidable tradeoffs.
- `L1`: official central policy intent and policy tools. State Council, ministries, PBOC, NDRC, MOF, official plans, budget tools, financial regulation, and binding administrative priorities.
- `L6`: money and fiscal implementation. Credit, fiscal revenue, land sales, transfer payments, special bonds, debt swaps, bank behavior, and actual funding flows.
- `L8`: industrial and corporate implementation. Order books, capex, capacity, margins, inventories, supply-chain bottlenecks, procurement, exports, and listed-company financials.
- `L9`: crack signals. CCDI, audit, fiscal disclosure, court enforcement, local bond documents, procurement arrears, salary or payment stress, unusual personnel changes, and policy-friction evidence.
- `L10`: long-cycle reference layer. Use only as a slow background lens for regime, geography, and historical analogy. Never use L10 alone to time markets, judge individual stocks, or make short-term trading calls.
- `L7`: market pricing and narrative temperature. Prices, valuations, positioning, liquidity, and consensus expectations.
- `story machine`: media, experts, social platforms, slogans, themes, and rumor. Use only for topic discovery and noise observation.

## Workflow

1. Define the decision question.
   - Convert the user request into a concrete question about allocation, risk, policy effect, sector selection, regional exposure, or personal action.
   - Name the geography, sector, asset class, time horizon, and decision boundary when available.

2. Start with `L0`.
   - Identify the non-negotiable structural constraints.
   - Separate what policy can change from what it can only smooth, delay, transfer, or reprice.
   - If L0 contradicts a popular story, make that contradiction explicit before moving lower.

3. Read `L1`.
   - Identify the official policy objective and the actual tool, not only the slogan.
   - Distinguish central intent from local implementation capacity.
   - For current facts, browse or otherwise verify the latest official source. Do not hard-code "current latest" policy, person, quota, rule, statistic, or price.

4. Check `L6/L8` implementation.
   - For macro or allocation questions, prioritize fiscal, credit, debt, land, and banking data in L6.
   - For industry or equity questions, prioritize orders, capex, capacity, margins, inventories, export volume, and filings in L8.
   - Treat announced plans without money flow or corporate results as unproven.

5. Validate with `L9` crack signals.
   - Before making a strong L9 conclusion, cross-check at least two primary-source families such as CCDI, audit offices, finance bureaus, budget final accounts, bond prospectuses, public resource trading centers, court enforcement systems, exchange filings, or official statistics.
   - Label the signal as `single-point`, `clustered`, or `systemic`.
   - State what the crack signal proves and what it does not prove.

6. Use `L10` only if useful.
   - Apply it for long-cycle framing, regional path dependence, and slow regime comparison.
   - Do not use it for short-term market timing, individual-stock calls, day trading, or precise event prediction.

7. Compare with `L7` and stories.
   - Ask whether market pricing already reflects the layered conclusion.
   - Use story-machine material only to identify consensus, hype, fear, or possible topics for evidence checks.
   - Do not cite story-machine material as proof of a conclusion.

8. Produce an operational conclusion.
   - Give a clear action posture: avoid, observe, small test, hold, add only after validation, reduce, hedge, wait for documents, or no conclusion.
   - Include validation triggers, invalidation triggers, expected lag, and confidence.

## Evidence Rules

- Time-sensitive facts require current verification from official or primary sources.
- For L9 claims, require at least two primary-source families before calling the signal systemic.
- Separate `observed evidence` from `needed evidence`.
- Prefer original-source documents over media summaries.
- Never infer national conclusions from one local case unless you label it as local evidence.
- Never infer policy success from policy intent alone.
- Never infer solvency from refinancing access alone.
- Never infer demand from nominal revenue without checking price, subsidy, FX, accounting, and volume.

## Required Output

Use this compact structure unless the user asks for a long report:

```text
decision_question:
L0_base_regime:
L1_policy_intent:
L6_L8_implementation:
L9_crack_signals:
L10_long_cycle_optional:
L7_pricing_and_story:
cross_layer_conflicts:
operational_conclusion:
confidence:
validation_triggers:
invalidation_triggers:
next_sources_to_check:
```

For user-facing Chinese analysis, answer in Chinese unless the user asks otherwise. Keep the conclusion actionable but conditional; avoid promising returns or giving personalized legal, tax, medical, or financial advice.

## Common Triggers

- "成都/某城市债务风险大吗？"
- "现在能买新房吗？"
- "中纪委信息对资产配置有什么用？"
- "地方债、城投债、化债怎么看？"
- "AI 产业链是不是有持续行情？"
- "房地产政策是否见效？"
- "某省市财政、人口、产业和房价风险怎么判断？"
- "用 L0-L10 框架分析..."
