---
name: macro-document-causality
description: Analyze China macro news, policy language, and economic claims through a falsifiable document-based causal chain. Use when evaluating whether a China macro narrative is actually implemented, when comparing policy intent versus execution, when tracing policies into project documents, cash flows, physical flows, company financials, fiscal results, or macro data, and when answering questions about real estate destocking, special bonds, local debt resolution, new productive forces, credit cycles, exports, consumption stimulus, or similar China macro transmission mechanisms.
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

## Required Output

Use this structure for every analysis:

```text
macro_claim:
policy_tool:
causal_chain:
document_evidence:
micro_behavior:
financial_result:
macro_confirmation:
contradictions:
confidence:
expected_lag:
next_checks:
```

Each `document_evidence` entry should include document type, evidence level, what it proves, and what it does not prove.

Format `document_evidence` entries like this:

```text
- level:
  document_type:
  likely_source:
  verifies:
  does_not_verify:
  suggested_search:
```

`likely_source` should be concrete enough for the user to check, such as "财政部官网/地方财政厅预算公开", "中国政府采购网", "省市公共资源交易中心", "上海证券交易所/深圳证券交易所/港交所公告", "中国债券信息网/上清所募集说明书", "海关总署统计数据", or "国家统计局/地方统计局". If a source is not public, label it as `non-public/internal` and suggest the closest public proxy.
