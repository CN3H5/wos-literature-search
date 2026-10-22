# Conditional search, recovery and reading notes

Read only relevant sections. Browser examples reflect an observed session on 2026-10-22, not guaranteed WoS behavior. Official reference links are documentation sources, not guarantees that a particular UI, account or index supports every option. Inspect current UI/help if behavior differs; never reuse old selectors or invent endpoints.

## Access and handoff

| Capability/access | Action |
|---|---|
| Connected WoS tool, or authorized browser automation | Use the accessible user/institution entry; inspect current tools/controls and reuse the WoS tab. |
| No live WoS access, but user-provided export | Screen the export, labeling supplied scope/query/date and missing fields; distinguish export-time counts from current counts. Do not imply a live WoS search. |
| Neither access nor export | Give the prepared query, date/type/language criteria and needed export fields. Ask for a WoS export/manual search result and stop dependent selection. Independent public full-text work may continue only if clearly labeled. |

For a login/CAPTCHA handoff, identify the accessible page and what the user needs to complete themselves, without requesting passwords. Save query/filter/sort state and the next intended step. After the user confirms completion, inspect the retained page, confirm restored access and resume there. Do not loop the barrier or make up institutional proxy addresses.

## Query precision

- Topic generally searches title, abstract, author keywords and Keywords Plus. A hit is not necessarily a direct study of the topic; verify the current collection/help and screen topical fit. When a sample is noisy, consider requiring a central concept in Title rather than tightening every group.
- Group OR synonyms with explicit AND and quotes for phrases. Broad wildcards and indiscriminate NOT can distort coverage. Consult the current collection's field tags/operators instead of assuming syntax transfers between collections.
- Declare languages of search terms. “English terms; no additional language filter” accurately describes an English-biased search. Where multilingual coverage matters, add indexed local-language synonyms or translated titles/abstracts and disclose the terms and screening languages; no language filter alone proves no such coverage.
- Verify effective date controls on the result page; separate formal publication, early access, first preprint, revision and indexing dates. Preserve the stated eligibility basis when deduplicating versions.

## Views, eligibility and screening log

Start candidate discovery with the observed relevance sort, or disclose the default view/ranking if unavailable. A topical sanity check diagnoses the query; it does not replace inspecting relevance-ranked candidates. Then inspect citation/date views of the same set, verifying sort and filters after transitions.

With only a supplied export, use its recorded relevance order where available and re-sort only its records for citation/date comparison. Label this as offline subset sorting, not full-WoS ranks; disclose absent views or unverified original ordering rather than making them up.

Retain per-view IDs, visible ranks and sample continuity. In the observed session a nominal 50-record page initially exposed one record; jumping to the bottom exposed parts of the beginning/end without the middle. Incremental scrolling may reveal more. Count inspected unique IDs, not nominal page size or scrolls; a sparse sample is not a top-N sample.

Use a small ledger rather than a systematic-review workflow:

`ID/DOI | view/rank | stage (title-abstract/full-text) | pass/exclude/pending/not-selected | primary reason | evidence pointer`

Apply the criteria declared before screening. Reasons are `off-topic`, `wrong-type`, `out-of-window`, `duplicate/version`, `no-full-text`, `language`, `citation-threshold`, `integrity`, or explained `other`. A review/qualitative/theoretical paper is not automatically the wrong type. Missing text is exclusion only when the requested depth requires full text. Eligible but unselected work stays `not-selected`.

Checkpoint totals distinguish query hits, unique screened records, exclusions by stage/reason, full-text assessed and included. Keep pending/not-selected counts where relevant; do not inflate counts across views or turn uninspected hits into exclusions. An export's visible scope limits any reproducibility claim.

## Citation interpretation

- Verify the finalist panel's exact metric label and citation universe, lookup date, and record index. Core Collection and All Databases counts differ; usage metrics, journal impact factor and citation class are not replacements for a paper's citation count.
- Interpret well-cited against comparable field, year/age and type. Capture normalized percentile/cohort definition if an accessible source reports it; badges are a separate observed signal. Do not invent a percentile or normalize by dividing a small convenience sample.
- For absent normalization report `raw count, not field-normalized`; do not imply raw cross-field/type/year comparability. External normalized metrics keep their own source/citation base, not a WoS label. Absence of a badge is not exclusion evidence.
- The established/recent mix is a starting heuristic. A hard threshold outranks it: if no recent paper in the inspected eligible pool meets the threshold, report that limited finding and any coverage limit, not an unsupported claim that no such paper exists anywhere. Do not count unknown citations as passing a hard threshold.

## Browser and export recovery

Use the same limit throughout query revision, UI/export recovery and full-text lookup: at most two failed attempts on the same operation/path, initial plus one changed attempt supported by observed state. A successful operation ends recovery; no need to exhaust a quota. New access or material evidence permits a new attempt. Distinguish optional export failure from unavailable core access.

1. Before slow work save query, bounds, filters, hit count, view/URL, inspected IDs and intended next action. Split slow navigation/submission/large reads into separate bounded calls; serialize shared-tab actions.
2. On timeout inspect current URL/controls/results before replay. Runtime reset may discard handles while the page retains successful changes. Rebind the existing tab per tool documentation; avoid unnecessary reopening, cookie handling or retyping.
3. Prefer targeted DOM/control reads over repeatedly reacquiring a valid tab and full accessibility trees. For duplicate/template labels, use observed unique attributes and verify values; never guess selectors. Effective result filters are the final confirmation.
4. For export, choose a small range with necessary fields; Author/Title/Source may omit citations. Use supported custom fields or Full Record without cited-reference lists where appropriate. Verify a readable file's record coverage/fields; a clicked button, closed dialog or download event is insufficient.
5. If optional export still fails, use targeted on-page extraction. If core WoS access fails, use a supplied export or manual handoff and disclose the gap. Do not keep retrying solely to obtain a bulk file for a small shortlist.

## Full-text routes and access controls

Use known DOI/WoS/resolver links first, with available Crossref/OpenAlex/Unpaywall metadata assistance as needed. These are discovery aids, not proof that a copy matches or is licensed. Follow verified publisher/repository links; use Google/Bing or another available engine only when helpful or requested. No mandatory visit to every service/engine, and no preference for ACM over the actual publisher.

If an engine is used, inspect the actual query/results and identity, not AI-overview prose alone. Failed discovery can coexist with successful retrieval from a verified repository. Report the engine step as failed/not used/unavailable as appropriate, separately from full-text access.

Use public, lawful or institutionally authorized access. Do not bypass paywalls, login/session restrictions or DRM. Keep session-restricted downloads in the authorized browser; direct fetch is only for an observed verified public URL, never a guessed endpoint or reused private session URL. For a saved PDF, check accessible path, nonempty PDF content, title/authors/year and DOI or WoS-linked identity; filenames alone do not suffice. Capture source/version/date, including corrected versions. Do not assume a preprint is identical to the final publication.

## Full-text evidence by study type

Extract as applicable, omitting inapplicable fields rather than declaring them missing:

| Type | Minimum useful reading notes |
|---|---|
| Empirical | Question, design, sample/data, comparator where relevant, outcomes, effect/uncertainty where reported, limitations. |
| Review | Question/scope, search date if reported, included studies, selection/synthesis method, limitations. Do not supply an invented search protocol for a narrative review. |
| Qualitative | Setting/participants, data collection/analysis, themes and supporting evidence, reflexivity where reported, limitations. |
| Theoretical | Argument/question, assumptions, contribution/proof or reasoning, scope and limitations. |

Read question/conclusion to orient, then the sections supporting the requested claims. Keep page/section pointers and separate author claims from your assessment. A downloaded file is not a read paper; label metadata/abstract/selected sections/full-paper status precisely.

Extraction failures, UTF-8 issues, null bytes, rotated text or missing spacing are not evidence of absent content. Check affected pages. Key details can exist only in diagrams, tables or captions; inspect those before claiming the paper does not report them. Confirm table headers, units and footnotes. Distinguish absolute/relative changes, example/training samples from evaluation samples, and theoretical complexity from measured performance; do not invent uncertainty, causality or external validity.

## ML/IR examples

Use only for relevant papers; these are not universal extraction requirements.

- A model family may be named only in an architecture diagram; that does not establish an exact dated model snapshot.
- MRR 6.21% to 6.41% is 0.20 percentage points, about 3.22% relative. A full ablation-chain gain is not wholly attributable to its LLM component.
- A candidate pool used for training-example generation need not be the final ranking evaluation pool. Verify all-item versus sampled-negative/candidate evaluation; unspecified details remain unknown.
- Four domains from one platform are not four independent platform datasets. Offline score gains do not establish online benefit; asymptotic complexity does not measure latency, throughput or deployment cost.

## Integrity and version status

For finalists make a focused check of publisher notices/Crossmark or an authoritative correction/retraction source such as Retraction Watch. Use current supported links/tools, match notice to article DOI/title, and record source/date. An integrity check is a publication-status check, not a comprehensive quality audit.

| Status | Interpretation/action |
|---|---|
| `no-notice-found` | No relevant notice found in the named sources on the stated date; not a guarantee of clean status. |
| `corrected` | Link the correction, identify the version read, and check whether quoted findings are affected. If unresolved, state that uncertainty. |
| `retracted` | Exclude as valid supporting evidence. If retractions themselves are the user's topic, retain only as a clearly labeled object of study. |
| `expression-of-concern` | Link the notice, flag uncertainty, and avoid unqualified use of the affected findings; prefer an eligible alternative where appropriate. |
| `unknown` | A check was inconclusive or sources conflict; explain the uncertainty. |
| `unchecked` | No check completed; explicitly say `retraction status unchecked`. |

No Crossmark button, empty metadata or an inaccessible publisher page does not prove absence of a notice. Do not turn an unavailable check into `clean`. Keep correction/version status distinct from access/license status.

Statuses can coexist: a supplied correction can support `corrected` while an unavailable current retraction check remains `retraction status unchecked`. Knowing a correction exists does not establish that no later retraction or concern exists.

## Output fields and cleanup

Before the shortlist state query and query languages, database/editions, effective filters, access date, hits, inclusion criteria, sampled views/ranks/counts/continuity and limits. Provide all fields below; two linked tables are usually more readable than a single very wide table:

| # | Paper (formal year) | DOI/WoS ID | Type; index/edition | WoS raw citations (metric/scope/date) | Normalization/badge (source/cohort) | Selection reason |
|---|---|---|---|---|---|---|

| # | Read version/date | Publisher/full-text/local link | Read level/pages | Access/license | Integrity (source/date) |
|---|---|---|---|---|---|

Use explicit unknowns. Public accessibility does not imply a Creative Commons license; report stated terms or license unknown without guessing. Keep exclusion reasons in the linked ledger or compact stage/reason summary, not a list pretending to cover unscreened hits. Add evidence-grounded notes, author versus reviewer limitations, saved-file links and the rapid-shortlist boundary.

Keep local full-text/working extracts for this task's analysis and requested deliverables, not unrelated reuse or persistent memory. Do not upload full text to additional external services without explicit authorization. Use a separate workspace directory for intermediates; record its path so cleanup can target only generated extracts/previews. Preserve original/user-supplied and requested PDF deliverables unless deletion is requested. Provide a list of removable intermediate paths when cleanup is requested; never cache credentials/session tokens. These notes do not confer redistribution rights.

## Official references

Consult relevant current documentation as needed; session observations above are not official guarantees:

- [WoS Core Collection search fields](https://webofscience.zendesk.com/hc/en-us/articles/26916258216209-Web-of-Science-Core-Collection-Search-Fields)
- [WoS search operators](https://webofscience.zendesk.com/hc/en-us/articles/20016122409105-Search-Operators)
- [WoS results, filters and sorting](https://webofscience.zendesk.com/hc/en-us/articles/20135124532113-Search-Results)
- [Crossref Crossmark](https://www.crossref.org/services/crossmark/) describes publication-status updates such as corrections and retractions; source coverage/availability must still be checked.
