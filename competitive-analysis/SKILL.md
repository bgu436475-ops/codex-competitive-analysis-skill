---
name: competitive-analysis
description: Use when Codex needs competitor research, battlecards, positioning, feature and pricing comparisons, content gaps, market opportunities, or evidence-backed recommendations.
---

# Evidence-First Competitive Analysis

Build decision-ready competitive analysis in which a reader can trace every material claim to dated evidence. Separate what sources say, what was experienced, what is inferred, and what should be done.

> **Adaptation note:** Adapted from Anthropic's [historical competitive-analysis Skill](https://github.com/anthropics/knowledge-work-plugins/blob/1316b6508366108158cf08503363d4b4cbc699e5/marketing/skills/competitive-analysis/SKILL.md) and informed by its [current competitive-brief successor](https://github.com/anthropics/knowledge-work-plugins/blob/47caa757e4730eb8daf7d335470f692d4a68b59e/marketing/skills/competitive-brief/SKILL.md). This file is modified for Codex and an evidence-first workflow. The upstream material is licensed under Apache License 2.0; see the [pinned upstream license](https://github.com/anthropics/knowledge-work-plugins/blob/1316b6508366108158cf08503363d4b4cbc699e5/marketing/LICENSE).

## Workflow

### 1. Frame the decision

Record:

- Competitors, category, and the user's company or product context
- Decision, audience, and requested deliverable
- Focus areas, geography, customer segment, and research date
- Time horizon and material assumptions

Ask only for missing information that would materially change the work. Otherwise, state assumptions and proceed.

### 2. Build the source plan

Prioritize direct evidence before commentary about it.

- **Primary:** official homepage, product and pricing pages, documentation, filings, newsroom, demos, trials, webinars, events, social profiles, and job postings.
- **Secondary:** reputable news and analyst coverage, transparent benchmarks, review sites, customer communities, social discussion, SEO data, and market datasets.

Use available web search, browser control, connected apps, and code or file tools when relevant. Do not assume a specific connector is installed. If a useful capability or source is unavailable, continue with accessible evidence and record the limitation.

Capture the exact page link and access date for every source. Prefer the page supporting the claim over a homepage, search result, or unsourced summary. Treat syndicated copies and reports derived from the same underlying source as one support.

### 3. Research the competitive dimensions

Cover the dimensions relevant to the decision:

1. Company overview, target customer, business model, and recent developments
2. Positioning and messaging: category, promise, audience, differentiators, tone, proof, and calls to action
3. Product capabilities, workflows, integrations, packaging, and feature limits
4. Pricing, billing unit, tiers, overages, contract assumptions, and regional variation
5. Content and channels: themes, formats, frequency, freshness, distribution, and keyword or audience gaps
6. Customer and social proof: case studies, adoption claims, review themes, community sentiment, and win/loss evidence
7. Strengths, weaknesses, threats, underserved needs, market opportunities, and recommendations

Use concise frameworks when they improve the comparison:

- **Value proposition:** promise, evidence, mechanism, uniqueness
- **Messaging matrix:** headline, value proposition, audience, differentiation, tone, proof, category, CTA
- **Content audit:** topic, format, audience, keyword, freshness, depth, and gap
- **Positioning:** reverse-engineered positioning statement or a decision-relevant two-axis map
- **Battlecard:** dated overview, pitch, honest strengths and weaknesses, proven differentiators, objection handling, and win/loss themes

### 4. Apply the claim contract

Create one claim ID for each material claim and assign exactly one type to that claim. If a sentence combines a sourced fact with a comparison, evaluation, or strategic meaning, split it into a **FACT** claim and a separate **INFERENCE** claim before writing the narrative.

| Claim type | Required output shape |
|---|---|
| **FACT** | Directly supported, verifiable statement + citation |
| **OBSERVATION** | Firsthand result + reproducible experience record |
| **INFERENCE** | Interpretation + cited supports + confidence |
| **RECOMMENDATION** | Action + decision served + supporting claim IDs |

Grade the evidence behind each claim:

| Grade | Meaning |
|---|---|
| **A** | Firsthand observation or direct official source |
| **B** | Transparent, reputable, independently checkable third party |
| **C** | Community, aggregator, or single anecdote |
| **D** | Unverified lead; cannot support a definitive conclusion |

Apply these gates:

- Classify comparative, evaluative, causal, risk, opportunity, customer-need, and market-gap statements as **INFERENCE** unless a disclosed method directly measures that exact statement.
- Treat source grade and claim type as separate fields. An official grade A source supports the direct fact it states; the source does not by itself support an analyst's comparison or interpretation.
- Give every critical fact a direct page link and access date.
- Give every material strategic inference two independent supports. If only one support is available, label it lower confidence and explain the gap.
- When reviewed sources do not disclose a metric or capability, write the scoped **FACT**: “The reviewed sources did not disclose X,” naming the sources and review date. Express “customers lack X” or “X is a market gap” only with direct customer evidence. Otherwise, express it as a lower-confidence **INFERENCE** and label it an opportunity hypothesis.
- Use grade C evidence to identify patterns or hypotheses, not to generalize from a single account.
- Preserve grade D items as leads or limitations, not findings.
- Keep vendor claims attributed until independently corroborated.
- Ensure every recommendation names the decision it advances and the evidence it depends on.

Build the claim register before drafting the narrative or comparison tables:

1. Write every **FACT** row with this atomic schema: `subject + exactly one audit unit + scoped value/date + source`. Start a new row whenever the audit unit changes. Treat product coverage, price, adoption, performance/productivity, revenue, and cost as different units. Multiple tiers from one price table may share one price row.
2. Create a separate **INFERENCE** row for each strength, weakness, comparison, risk, opportunity hypothesis, or customer need. Give every inference's critical factual premise its own FACT row.
3. Write each Claim field as the complete proposition that the ID will support, at the same specificity intended for the report.
4. Generate the executive summary, findings, comparisons, strengths/weaknesses, opportunities, and recommendations by directly reusing the complete proposition from the matching Claim field. Translation, grammatical adjustment, and non-substantive connecting words are allowed; preserve the claim's meaning and scope exactly. For a more specific proposition, update or add that exact claim row before drafting it. Cite every matching ID when one sentence contains multiple propositions.

Illustrative atomic sequence:

- `F-01 FACT adoption` — Vendor A reported 12,000 active teams as of 2026-06-30. `[adoption source]`
- `F-02 FACT performance` — Benchmark B reported Vendor A's audited task completion was 18% faster as of 2026-06-30. `[performance source]`
- `I-01 INFERENCE` — Vendor A shows both organizational reach and measured workflow improvement. `Supports: F-01, F-02; confidence: medium.`

### 5. Verify product experience

For every firsthand test, record:

- Environment and device or software context
- Date and entry point
- Reproducible steps
- Observed result
- Account, plan, geography, permissions, and other limitations

For a failed or blocked path, create two distinct records:

1. Create an **OBSERVATION** claim for checks actually performed, including the environment, date, entry point, numbered steps, observed result, and raw error or output.
2. Mark the unexecuted product-internal path **`Not firsthand-verified`** and state the account, plan, geography, permissions, or tool limitation that blocked it.

Keep related marketing copy, documentation, demos, reviews, or community reports as sourced facts or inferences rather than experience claims.

### 6. Synthesize for the decision

Compare like with like and distinguish absence of evidence from evidence of absence. State the strongest opportunity and threat, then connect gaps to specific customer needs. Prioritize recommendations by expected impact, confidence, effort, and time horizon. Include quick wins and longer-term moves when useful.

Before delivery, run a claim-to-narrative mapping scan:

1. Scan every sentence and table cell for comparisons, evaluations, causes, risks, opportunities, and customer needs.
2. Highlight every substantive phrase in the narrative or table cell that is absent from the cited Claim field.
3. Register every added meaning first. When a sentence contains multiple material propositions, cite all corresponding IDs.
4. For each material proposition, compare its wording, scope, and specificity with the cited row's Claim field.
5. If no row states the exact proposition, add the correctly typed row with its own evidence or remove that proposition from the report. Re-read every cited Claim field and confirm it supports the complete sentence or cell.

## Output

For a concise answer, cite claims inline and include the research date, limitations, and enough source detail to audit critical facts.

For a formal report, battlecard, reusable deliverable, or explicit source register, read and use [references/report-template.md](references/report-template.md). Adapt its optional rows and sections to the user's decision, but retain the firsthand experience, source register, and claim register sections. Populate one claim-register row per material claim with every required template field: ID, claim, claim type, evidence grade, exact source link, access date, confidence, and notes. Add source IDs in notes when useful; keep the required fields explicit in the claim row. Complete the register before drafting the other report sections, even when the final document displays the register last.
