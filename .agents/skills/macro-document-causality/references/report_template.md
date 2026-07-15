# Markdown Report Template

Use this template only when Report Mode is triggered by an explicit report-style request. Adapt headings to the user's topic, but preserve the causal logic and evidence discipline.

## 标题

Use a concrete title that names the macro claim, geography or sector, and verification angle.

## 摘要结论

- State the bottom-line judgment in 3-5 bullets.
- Include confidence, strongest observed evidence level, missing critical documents, and the data timestamp or period.
- Distinguish `已验证`, `早期信号`, `相关性风险`, and `证据不足`.
- Use explicit time labels such as `截至 YYYY-MM-DD`, `证据日期 YYYY-MM-DD`, and `数据期 YYYY年M月/1-M月`.

## 宏观主张与可证伪表述

- Convert the user's narrative into a testable claim with subject, mechanism, affected sector, expected direction, and time horizon.
- Name what evidence would falsify the claim.
- Avoid treating slogans, meeting language, or aggregate data as proof.

## 政策工具与传导机制

- Identify the concrete policy tool: quota, relending facility, special bond, fiscal subsidy, tax rebate, procurement, administrative target, credit guidance, project approval, or similar.
- Map the intended path from policy issuer to executing entity to beneficiary to macro outcome.
- Separate quota, authorization, contract, payment, delivery, and final demand.

## 单据证据分级表

Use a Markdown table with these columns:

| 层级 | 单据/数据 | 证据状态 | 日期/数据期 | 可能来源 | 已引用来源 | 能证明什么 | 不能证明什么 | 建议检索词 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

For complete reports, use this exact schema. Do not omit, rename, merge, or replace these columns with a shorter evidence table, even when evidence is thin.

`证据状态` must distinguish:

- `observed/cited`: found, cited, or provided in context.
- `observed/no-link`: found or provided, but no verifiable URL/path is available.
- `required`: not yet verified and needed for the next step.
- `non-public/internal`: normally unavailable publicly; provide the closest public proxy.

`日期/数据期` must include the document date for point-in-time evidence or the data period for time series. `已引用来源` must be a URL, local path, filing name, or `not provided`; do not merge it with `可能来源`.

Apply the standard levels:

- Level 0: media narrative, expert opinion, market rumor.
- Level 1: official policy statement, meeting readout, guidance document.
- Level 2: budget, quota, lending facility, project list, bond issuance, implementation plan.
- Level 3: bidding notice, winning bid, procurement contract, loan contract, subsidy list, project contract.
- Level 4: payment, invoice, delivery, customs declaration, completion acceptance, inventory transfer, bank disbursement.
- Level 5: company financial result, bank loan book result, local fiscal result, developer cash-flow result.
- Level 6: confirmed macro time series consistent with the claimed mechanism.

## 微观行为验证

- Trace cash flow: who paid whom, when, amount, source of funds, and whether money was actually disbursed.
- Trace physical flow: delivered goods, acquired homes, project starts or completions, export shipment, inventory movement, or service usage.
- Trace balance-sheet movement: receivables, inventory, debt replacement, capex, leverage, impairment, or order backlog.
- Split price, volume, FX, subsidy, and accounting effects when relevant.

## 财务结果验证

- For companies: revenue, gross margin, cash receipts, receivables, inventory, capex, debt, impairment, and order backlog.
- For local governments: land sales, fiscal revenue, transfer payments, debt service, hidden debt replacement, project spending, and arrears.
- For banks: credit growth, loan mix, facility usage, NPL migration, interest margin, and regional exposure.
- Explain whether Level 5 evidence confirms the claimed micro transmission or only an accounting/proxy effect.

## 宏观数据确认

- Use macro data after document and micro-behavior checks.
- Compare the expected lag with the observed time series.
- Identify whether macro movement is consistent with the mechanism, inconsistent with it, or still too early to judge.
- Flag correlation risk when aggregate improvement lacks Level 3+ execution evidence.
- If Level 6 macro data is not matched to the same city, sector, project group, or beneficiary set as the document chain, call it `相关性背景`, not causal confirmation.
- State each macro series' geography, frequency, and data period.

## 反证与风险

- List the strongest contradictory evidence.
- Include substitution effects, pull-forward effects, nominal vs real effects, local-to-national extrapolation risk, delayed payment risk, fiscal leakage, and accounting distortions where relevant.
- State what future evidence would downgrade or overturn the conclusion.

## 置信度、滞后期、下一步核验清单

- Give confidence as `low`, `medium-low`, `medium`, `medium-high`, or `high`, capped by the strongest available evidence.
- Without Level 4 actual payment, transfer, delivery, acceptance, or bank-disbursement evidence, do not describe the chain as an execution closed loop.
- Without Level 5 financial result and Level 6 matched macro confirmation, do not conclude the policy is already macro-effective; use `早期信号` or `相关性风险` as appropriate.
- State the expected lag from policy to document execution, micro behavior, financial results, and macro confirmation.
- Provide a prioritized checklist of next documents and data series to verify.

## 报告完整性自检

For complete reports, include this section explicitly. Before finalizing, check:

- 标题: names the claim, geography/sector, and verification angle.
- 结论: distinguishes verified evidence, early signals, correlation risk, and evidence gaps.
- 证据层级: every key claim has a level and confidence cap.
- 来源链接: observed evidence has `已引用来源`; missing sources are not implied as verified.
- 日期口径: every document or data series has an evidence date or data period.
- 宏观数据口径: geography, frequency, and period are stated; unmatched macro data is not treated as causal proof.
- 反证: contradictory evidence and falsification conditions are included.
- 置信度上限: conclusion does not exceed the strongest observed evidence.
- 下一步核验: missing Level 3/4/5/6 evidence is listed separately from observed evidence.

## 附录：建议检索词与优先数据源

- Provide Chinese search terms for each evidence level.
- Prioritize primary sources: ministry/local government websites, finance departments, public resource trading centers, government procurement sites, ChinaBond, Shanghai Clearing House, stock exchange filings, customs data, National Bureau of Statistics, local statistics bureaus, and official sector regulators.
- Label non-public documents as `non-public/internal` and suggest public proxies.
