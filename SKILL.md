---
name: research-orchestrator
description: Use for any market, policy, technology, competitor or customer research on any country, sector or topic. Routes to installed research skills and enforces sourcing and evidence rules.
---

# Research orchestrator (meta skill)

This skill orchestrates research on any topic: a country, a sector, a market, a regulator, a technology or a customer group. It does not do the research itself. It sets the research context, routes the work to the best available skill or tool, and applies sourcing and evidence rules to everything that comes back.

## Step 1. Set the research context

Before searching, write down in two or three lines:

- **Question:** what exactly needs answering, and for what decision
- **Scope:** geography (country, region, sub-national areas), sector, time frame
- **Languages:** which languages the important sources are likely to be in. Plan to search in each, not only English
- **Local gotchas:** anything that commonly distorts data for this scope, for example sub-national differences, multiple exchange rates, informal or cash economies, recent regulatory changes, sparse or outdated official statistics

If the question is ambiguous, state the interpretation in one line and proceed.

## Step 2. Classify the question

Put the request into one or more research types:

| Type | Typical questions |
|---|---|
| A. Benchmarking and competitors | Who are the players? How do they compare on products, pricing, features, ratings, scale? |
| B. Policy and regulation | What do the regulator and the law require? Licensing, compliance, data, consumer protection |
| C. Technology and infrastructure | What platforms, rails, vendors, standards and infrastructure exist and are used? |
| D. Customers | Needs, behaviours, preferences, demographics, sentiment, interview or survey synthesis |
| E. Market and sector overview | Size, growth, structure, trends, themes |
| F. Decision support | Comparing named options against criteria, or stress-testing a conclusion |

## Step 3. Route to the best available skill

Check which skills and tools are available in the session. Use the first available option in each row; fall back to the next. If a skill is not installed, say so in one line and use the fallback. Do not stop.

| Type | First choice | Then | Fallback |
|---|---|---|---|
| A. Benchmarking | market-researcher: competitive-analysis (comps-analysis for public-company financials) | exa: exa-agent for list-building and enrichment | WebSearch + WebFetch |
| B. Policy and regulation | exa: search, official sources first | research-desk: citation-check on the final sources | WebSearch + WebFetch, official domains first |
| C. Technology | market-researcher: sector-overview | exa: search | WebSearch + WebFetch |
| D. Customers (user-provided material) | customer-research: feedback-analysis (short items), interview-synthesis (transcripts), icp-profile, churn-analysis | | Manual coding with quotes and counts |
| D. Customers (published evidence) | exa: search for surveys, studies and app reviews | | WebSearch + WebFetch |
| D. Planning customer interviews | customer-research: interview-guide | | |
| E. Market overview | market-researcher: sector-overview | exa: search | WebSearch + WebFetch |
| F. Decision support | research-desk: decision-matrix | research-desk: llm-council for a second opinion | A weighted table built directly |

For anything that will be shared externally, run research-desk: citation-check (or a manual check) on the final sources before delivery.

Do the research first. Only then hand over to an output skill (pptx, docx, xlsx) if a formatted deliverable is needed.

## Step 4. Apply the source hierarchy

Search and weight sources in this order. Always try tier 1 before relying on tier 3 or 4.

1. **Official primary sources.** Regulators, central banks, ministries, official gazettes, national statistics offices, courts, and sub-national authorities where relevant.
2. **Multilateral, standard-setting and academic sources.** IMF, World Bank, OECD, UN agencies, regional development banks, industry standard-setters (for example FATF), peer-reviewed research.
3. **Company and industry primary sources.** Annual reports, stock exchange filings, company websites and documentation, app store listings and reviews, industry association data.
4. **Media and commentary.** Reputable international and local outlets, including local-language press. Use for recent events and signals, never as the only source for a regulatory or numeric claim.

Record the original title for any non-English source alongside the translation.

## Step 5. Evidence rules (non-negotiable)

- **Every fact carries a source and a date:** URL, publisher, publication date and date accessed.
- **Flag age.** Mark any source older than 24 months as "dated", unless the topic changes slowly and you say why.
- **Triangulate numbers.** Any figure used in a deliverable needs two independent sources, or is labelled "single source".
- **Separate fact from estimate.** Label estimates, projections and your own calculations explicitly.
- **Regulation is time-sensitive.** State the latest version, circular or amendment found, and that a newer one may exist.
- **State the geography and basis.** Say which country or region a fact applies to, and for money figures, the currency, exchange rate basis and date.
- **Never fabricate.** If something cannot be found or verified, say so plainly and list it under gaps.

Grade each key finding:
- **High:** official or multilateral source, recent, corroborated
- **Medium:** single credible source, or dated but still indicative
- **Low:** media, inference or proxy (for example, app reviews as a proxy for customer preferences)

## Step 6. Using client context in searches

- Client names, project names and client context may be used in web searches and research tools wherever they help find more relevant insights, for example news about the client and its shareholders, partners, vendors, competitors or regulators.
- Combine client-specific searches with generic ones so the research is not limited to what mentions the client.
- Mark anything intended for an external audience as draft until the user has reviewed it.

## Step 7. Output format

Unless the user asks for something else, return a research note with these sections:

1. **Question and scope.** One or two lines, including geography and time frame.
2. **Key findings.** Three to seven bullets, each with a confidence grade.
3. **Evidence table.** Finding | Source | Publisher | Published | Accessed | Tier | Confidence.
4. **Gaps and caveats.** What could not be verified, what is dated, what conflicts.
5. **So what.** Two to four implications for the user's decision or work.

If a project or shared knowledge base is attached, check it first for earlier research on the same topic, and save the new note there afterwards so later work can build on it.

## Quick checklist before delivering

- [ ] Context set: question, scope, languages, local gotchas
- [ ] Question classified and routed; missing skills noted with fallback used
- [ ] Tier 1 sources tried first; local-language sources searched where relevant
- [ ] Every fact has source, publication date and access date
- [ ] Key numbers triangulated or labelled single source
- [ ] Geography, currency and exchange rate basis stated where relevant
- [ ] Client-specific and generic searches both run where relevant
- [ ] Gaps listed honestly
- [ ] Implications stated
