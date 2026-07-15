---
name: macro-document-causality
description: Analyze China macro news, policy language, and economic claims through a falsifiable document-based causal chain. Use when evaluating whether a China macro narrative is actually implemented, when comparing policy intent versus execution, when tracing policies into project documents, cash flows, physical flows, company financials, fiscal results, or macro data, when generating Markdown research reports for explicit report-style China macro requests, and when answering questions about real estate destocking, special bonds, local debt resolution, new productive forces, credit cycles, exports, consumption stimulus, or similar China macro transmission mechanisms.
---

# Macro Document Causality

## Core Rule

Convert every macro narrative into this chain:

`宏观叙事 -> 政策工具 -> 单据证据 -> 微观行为 -> 财务结果 -> 宏观确认 -> 反证/置信度`

Do not treat policy language, expert opinion, media framing, announced quotas, or aggregate data as proof of realized transmission. The answer must separate:

- policy intent vs execution
- funding quota vs actual payment
- project announcement vs physical progress
- nominal amount vs real demand
- national aggregate vs local or industry detail

For detailed reusable templates, read `references/china_macro_chains.md` when the user asks about one of the covered chains or when you need concrete document types.

Use Report Mode only when the user explicitly asks for a report-style deliverable, such as `报告`, `研究`, `深度分析`, `专题分析`, or an equivalent long-form research request. In Report Mode, also read `references/report_template.md`.

## Workflow

1. State the falsifiable `macro_claim`.
   - Convert vague language into a testable claim with subject, mechanism, expected affected sector, direction, and time horizon.
   - Example: "房地产收储有效" becomes "local government or state-owned platforms are buying completed inventory at scale, converting developer inventory into cash and reducing local saleable stock within N months."

2. Identify the policy tool and intended transmission path.
   - Name the concrete tool: quota, relending facility, special bond, fiscal subsidy, tax rebate, procurement, administrative target, credit guidance, reserve requirement change, export policy, or project approval.
   - Name the affected entities: local governments, policy banks, commercial banks, developers, LGFVs, manufacturers, exporters, households, or listed companies.

3. Grade evidence by document level before accepting execution.
   - Level 0: media narrative, expert opinion, market rumor.
   - Level 1: official policy statement, meeting readout, guidance document.
   - Level 2: budget, quota, lending facility, project list, bond issuance, implementation plan.
   - Level 3: bidding notice, winning bid, procurement contract, loan contract, subsidy list, project contract.
   - Level 4: payment, invoice, delivery, customs declaration, completion acceptance, inventory transfer, bank disbursement.
   - Level 5: company financial result, bank loan book result, local fiscal result, developer cash-flow result.
   - Level 6: confirmed macro time series consistent with the claimed mechanism.
   - For each evidence item, name the likely source where the user can verify it. Prefer official or primary sources: ministry/local government websites, public resource trading centers, government procurement sites, bond prospectuses, stock exchange announcements, listed company filings, bank announcements, customs/statistics databases, and official data portals.
   - For each observed evidence item, include `evidence_date`, `data_period`, `verification_status`, and `source_url_or_path`. Use `data_period: n/a` for point-in-time documents and `source_url_or_path: not provided` only when the source was not accessible in the current task.
   - Separate `observed_evidence` from `required_evidence`. `observed_evidence` is evidence actually found, cited, or provided in context. `required_evidence` is the next document or data needed to verify the causal chain.

4. Map documents to micro behavior.
   - Cash flow: who paid whom, when, amount, source of funds, actual disbursement vs quota.
   - Physical flow: goods delivered, homes acquired, project started/completed, export volume, inventory movement.
   - Balance sheet: debt replacement, receivables reduction, inventory reduction, capex increase, leverage shift.
   - Price/volume split: nominal growth from price, FX, subsidy, or accounting effects vs real demand.

5. Connect micro behavior to financial results.
   - For companies: revenue, gross margin, cash receipts, receivables, inventory, capex, debt, impairment, order backlog.
   - For local governments: land sales, fiscal revenue, transfer payments, debt service, hidden debt replacement, project spending.
   - For banks: credit growth, loan mix, NPL migration, interest margin, policy facility usage.

6. Confirm or reject with macro data.
   - Use macro time series only after checking whether document evidence supports the causal path.
   - Treat macro improvement without document support as correlation risk.
   - Treat document execution without macro confirmation as an early signal.
   - State the data timestamp: "截至 YYYY-MM-DD" for current state, and "数据期为 YYYY年M月/1-M月" for time series.

7. State contradictions, confidence, lag, and next checks.
   - Include evidence that would disprove the claim.
   - Cap confidence according to the strongest evidence actually available.

## Confidence Caps

- News-only or market-commentary claims: confidence cannot exceed `low`.
- Policy intent without Level 3+ execution evidence: do not call the policy effective.
- Execution evidence without Level 6 macro confirmation: label as `early signal`, not confirmed macro transmission.
- Macro improvement without Level 3+ document support: label as `correlation risk`.
- Local documents without national coverage: label as `local evidence`, not national confirmation.
- Nominal amount without price/volume adjustment: confidence cannot exceed `medium-low` for real demand.
- Without Level 4 actual payment, transfer, delivery, acceptance, or bank-disbursement evidence, do not call a policy an `execution closed loop` or claim the transmission has fully occurred.
- For real-estate destocking, without Level 4 payment/deed-transfer evidence, do not judge acquisition as an execution closed loop.
- Level 6 macro data without city-, sector-, or project-level match to the document chain is only correlation background, not causal confirmation.

## Report Mode

When Report Mode is triggered:

- Default to Markdown output.
- Produce a long-form Chinese report, normally around 3000+ Chinese characters when evidence availability supports that depth.
- Keep the core causal chain intact: `宏观叙事 -> 政策工具 -> 单据证据 -> 微观行为 -> 财务结果 -> 宏观确认 -> 反证/置信度`.
- Use `references/report_template.md` for the report structure and section expectations.
- Mark timestamps for all key evidence and data: "截至 YYYY-MM-DD", "证据日期 YYYY-MM-DD", or "数据期 YYYY年M月/1-M月".
- In the summary, state the strongest observed evidence level, missing critical documents, and macro data period.
- Distinguish observed evidence from required evidence throughout the report.
- Include a `单据证据分级表` using the exact columns in `references/report_template.md`; do not replace it with a shorter custom table for complete reports.
- Include the `报告完整性自检` section from the template for complete reports, even if some checks fail.
- If evidence is thin, write a shorter report and explicitly state which sections are constrained by missing Level 3+ or Level 4+ evidence.

## Required Output

For ordinary non-report analysis, use this structure:

```text
macro_claim:
policy_tool:
causal_chain:
observed_evidence:
required_evidence:
micro_behavior:
financial_result:
macro_confirmation:
contradictions:
confidence:
expected_lag:
next_checks:
```

Each `observed_evidence` entry should include document type, evidence level, evidence date, data period, verification status, source URL or path, what it proves, and what it does not prove. Each `required_evidence` entry should name the missing document or data, where to verify it, and why it matters.

Format `observed_evidence` entries like this:

```text
- level:
  document_type:
  likely_source:
  evidence_date:
  data_period:
  verification_status:
  source_url_or_path:
  verifies:
  does_not_verify:
  suggested_search:
```

Format `required_evidence` entries like this:

```text
- level:
  missing_document_or_data:
  likely_source:
  why_needed:
  public_access:
  public_proxy:
  suggested_search:
```

`likely_source` should be concrete enough for the user to check, such as "财政部官网/地方财政厅预算公开", "中国政府采购网", "省市公共资源交易中心", "上海证券交易所/深圳证券交易所/港交所公告", "中国债券信息网/上清所募集说明书", "海关总署统计数据", or "国家统计局/地方统计局". If a source is not public, label it as `non-public/internal` and suggest the closest public proxy.
