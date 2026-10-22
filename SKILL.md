---
name: wos-literature-search
description: Build a rapid, relevance-first Web of Science paper shortlist balancing citation influence and recency, then locate lawful publisher/repository full text and summarize it. Use for WoS检索、高被引近期论文、检索并下载阅读. Not an exhaustive search or systematic-review protocol.
---

# Web of Science literature shortlist

Respond in the user's language. Keep criteria/evidence reproducible within a rapid shortlist; do not claim measured time/token savings without measurement.

## Scope and access

- Extract topic, exclusions, date basis/window, types/languages, number, citation threshold and access/read depth. Defaults: 5 papers, current year plus previous 4 calendar years, relevance first, balanced influence/recency. Do not impose journal/original-only filters; explain preferences. Ask only for blocking ambiguity.
- State exact date bounds and calendar-year/rolling interpretation. Normally use formal publication; distinguish early access, preprint, revision and indexing dates. Versions are not independent studies.
- Declare query languages separately from filters: English terms without language filters remain English-biased. Add local-language terms/translations when relevant; no language filter does not establish multilingual coverage.
- Prefer a user/institution WoS entry, otherwise an available official entry (`webofscience.com` or `webofscience.clarivate.cn`). Use a connected WoS tool or supported browser; failing both, screen a supplied export with provenance/date. With neither access nor export, provide a manual query/export handoff and stop dependent selection. Never invent proxy URLs or silently substitute general-web results.
- At login/CAPTCHA barriers, request user action once with page, required action and resume point. Preserve state and resume after restored access; never collect credentials. Public-fetch 403 does not prove an authorized browser is blocked.

## Search and eligibility

1. State inclusion criteria: topic, dates, types/languages, user citation threshold and required access. **Relevance and user criteria are gates**; citations cannot rescue ineligible work.
2. Build 2–4 concept groups in declared query languages: OR within, AND between. Use Topic/advanced search, e.g. `TS=(("concept A" OR synonym*) AND ("concept B" OR synonym))`, replacing examples. Prefer Core Collection. Record database/available editions, query, verified filters, hits and access date; refine a broadly off-topic sample within the recovery limit.
3. Inspect relevance-ranked results **first**, then citation/date-descending views of the same set. If unavailable, disclose the observed initial/default sort or unverified ranking; never invent a relevance control. Query sanity checking does not replace this discovery view. Export-only sorting covers supplied records, not reconstructed full-WoS ranks. Scale samples to the request; log actual ranks/IDs and continuity per view. Page size is not inspected count; sparse samples are not top N.
4. Screen titles/abstracts, then required full text. Deduplicate by DOI, otherwise title/author/year and version history. Log stage and primary exclusion: `off-topic`, `wrong-type`, `out-of-window`, `duplicate/version`, `no-full-text`, `language`, `citation-threshold`, `integrity`, or explained `other`. `no-full-text` applies only when access is required. Eligible unchosen papers are `not-selected`.
5. Checkpoint hits, unique screened IDs, exclusions by stage/reason, full-text assessed, included and pending/not-selected as needed. Never count uninspected hits as screened/excluded.

## Shortlist and citation handling

- Record title/authors, formal year, type, DOI/WoS ID, index/edition, record URL and needed abstract evidence. Verify finalist raw citations, metric/scope/date; keep missing counts unknown. Never mix Core Collection, All Databases, publisher or Google Scholar counts.
- “Well-cited” is relative to comparable field, year/age and type. Record available normalized metrics with source/cohort/definition; verify official badges separately. Otherwise state **raw count, not field-normalized**. Do not derive normalization from a small sample or relabel external percentiles as normalized WoS counts. Older/review papers cannot displace stronger topical fit solely through raw totals. Citations do not prove quality.
- For the default 5, roughly 3 established and 2 from the latest 2 calendar years is a starting heuristic, not a quota. Explain the actual balance. If a hard user citation threshold leaves no eligible recent papers, report that conflict and preserve the threshold; do not lower it to fill a recency slot.
- Expand only for eligibility/access failures or missing coverage. Stop when the requested number has been assessed to the requested depth; disclose unmet criteria rather than relaxing them silently.

## Full-text retrieval and reading

1. Start with verified WoS/resolver/DOI links; use available Crossref/OpenAlex/Unpaywall discovery assistance as needed. Publisher/repository copies precede optional Google/Bing fallback; honor requested engines. Confirm **title, authors, year and DOI (or WoS ID)**. Failed engine discovery is not failed full-text access; disclose the actual route.
2. Use lawful public/institutional access without bypassing paywall, login, session restrictions or DRM. Read sufficient HTML; download when needed/requested. Direct fetch is only for a verified public URL, never guessed/private session endpoints. Verify local PDF content and identity. Record read version/date separately from formal publication.
3. Orient with question/conclusion, then evidence/limitations. **Extract as applicable to study type** using [templates](references/search-notes.md#full-text-evidence-by-study-type). Inspect relevant figures/tables/captions before declaring details unreported. Preserve units, absolute/relative changes, uncertainty and page/section pointers; separate author claims from your assessment.
4. Before delivery check finalists for correction, retraction or expression of concern via publisher notices/Crossmark or an authoritative notice source. Record source/date and applicable statuses: `no-notice-found`, `corrected`, `retracted`, `expression-of-concern`, `unknown` or `unchecked`. No notice found is not a guarantee of “clean” status; if not checked, state **retraction status unchecked**. Do not synthesize retracted work as valid supporting evidence; see [integrity handling](references/search-notes.md#integrity-and-version-status).
5. Label reading status: metadata only, abstract only, selected full-text sections (pages/sections), or full paper read. Full text acquired is not full paper read. Keep analysis copies in the task workspace; do not upload full text to additional services without authorization. Preserve requested deliverables and identify intermediate paths for cleanup; never cache credentials/session tokens.

## Recovery and output

- Split slow navigation/submission/extraction into separate bounded calls; serialize shared-tab actions. Timeout means unknown outcome: inspect retained state, reconnect after reset, do not rebuild blindly. Allow **at most two failed attempts per operation/path** (initial plus one evidence-based changed attempt), then stop without new evidence/access. Optional export failure switches to page extraction; core access failure needs export/manual handoff. Details: [recovery](references/search-notes.md#browser-and-export-recovery).
- Save state before slow exports/downloads/recovery. Prefer targeted DOM/structured fields and small verified exports without cited-reference lists. Retrieve needed text locally; report verified findings rather than repeated intentions.
- Return query/languages, database/editions, effective filters, hits, access date, criteria and actual sampling method/counts/limits. Use [output fields](references/search-notes.md#output-fields-and-cleanup), in linked compact tables if needed: identity/DOI/type/index; raw citations/scope/date and normalization/badge; selection reason; read version/full-text link/read level; access/license; integrity/source/date. Mark unknowns explicitly. Add evidence-based summaries and working saved-file links. Link excluded IDs/reasons or summarize their counts; do not imply exhaustive coverage.

For syntax, partial rendering, exports, extraction problems or domain-specific examples, read only the relevant section of [search-notes.md](references/search-notes.md). This skill produces a rapid shortlist, not a systematic-review protocol.
