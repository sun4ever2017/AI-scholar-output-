# Review 4 — Feasibility, data and execution risk

**Pitch:** "Generative AI and the Productivity of Finance and Accounting Scholars" (Pitching Research template, 23 October 2026). **Review date:** 30 October 2026. **Lens:** research engineer / empirical coauthor.

**Verification.** This sandbox could not reach api.openalex.org or api.crossref.org (network egress blocked), so the pitch's coverage numbers could not be re-run live. Facts marked **[verified: web]** were confirmed from documentation or published analyses found by web search; facts marked **[memory]** come from my working experience and must be checked.

---

## 1. Verdict

**Feasibility: 6/10 as written; about 8/10 if cut to the stage-1 core** (Crossref/OpenAlex scholar panel + LLM method classification + PPML event studies).

The core design is cheap and buildable: all metadata are free, the panel is roughly 10–15k scholars × 35 quarters, and estimation is trivial, so a credible first working paper in 4–5 months is realistic with one engineer-coauthor at about half time plus an RA. The problem is scope: the pitch bundles eight data components, and three rest on routes that are broken or unverified. ICSR Lab, named as the licensed abstract route for 2025, closed on 31 December 2023 **[verified: web]**; whether the Scopus APIs return SSRN preprints at all is unconfirmed; and "JEL codes where authors report them" cannot be obtained without the SSRN scraping the pitch rightly forgoes. The abstract-coverage figures conflict with an independent CWTS analysis of Crossref and must be re-derived with a documented query. The largest execution risk is not data access but author identity: the outcome is a per-scholar count built on OpenAlex author IDs, whose inputs change at exactly the 2021/22 boundary. Build the MVP, defer the rest, circulate v1 in Q1 2027.

---

## 2. Major issues (ranked by severity)

### M1. The licensed-abstract route for 2025 is broken as described
**(a)** (F): "the Scopus API or an ICSR Lab project provides licensed coverage, including 2025"; (K) risk 7: "The 2025 abstract gap needs Scopus or ICSR Lab."
**(b)** Elsevier's research-collaborations record lists ICSR Lab as running 20 March 2019 to 31 December 2023 and states "The ICSR Lab is now closed" **[verified: web]**. Scopus has ingested SSRN preprints since 2021, but initially only into author profiles of authors with an existing Scopus publication history, with API support "to be evaluated based on customer feedback" **[verified: web]**. Whether the Scopus Search or Abstract Retrieval APIs return SSRN preprints today is unconfirmed **[memory: when I last used them they did not]**. The 2025 gap therefore has no confirmed licensed route.
**(c)** Week-1 test: with Adelaide's Scopus API key, request 20 known 2025 SSRN DOIs through the Abstract Retrieval API; if nothing returns, the route is dead. Alternatives: Dimensions (no-cost API access for non-commercial scientometric research after review and a signed agreement **[verified: web]**; SSRN coverage unverified) or Semantic Scholar. Above all, decouple the MVP from 2025 abstracts: the outcome needs none; report the AI-vocabulary first stage for 2023–24 and 2026 with 2025 shown as a gap, and compute the writing-release Wald ratio on 2023–24.

### M2. The abstract-coverage claims are unverified and conflict with independent evidence
**(a)** (F): "Free Crossref abstracts cover about half of SSRN finance and accounting papers in 2021–2024 and about 90% in 2026, but only 17–34% in 2025."
**(b)** CWTS Leiden's analysis of the January 2025 Crossref snapshot (posted-content preprints, 2023–2024) states: "Abstracts are not included in the Crossref metadata of SSRN preprints" **[verified: web]**. That is hard to reconcile with "about half in 2021–2024" unless the figure is OpenAlex's `has_abstract` (OpenAlex harvests abstracts from sources beyond Crossref **[memory]**) or refers to older SSRN records deposited as journal-article type. The number matters twice: classifying 2018–2021 papers needs abstracts for those years, and the pitch does not report 2018–2020 coverage at all.
**(c)** Re-derive and document (appendix): Crossref prefix 10.2139 by year with and without `has-abstract:1` and by `type-name`; OpenAlex SSRN works with `has_abstract:true` by year. State 2018–2021 coverage in the pitch and plan title-only classification where abstracts are missing, with accuracy reported separately.

### M3. Author identity over time is the biggest measurement risk, and it is confounded with the treatment date
**(a)** (F): "via OpenAlex, which provides author identifiers, ORCID (on 92% of 2024 SSRN works), institutions, citations and links to journal versions".
**(b)** Every error in assigning an SSRN record to a scholar enters the outcome directly, and OpenAlex's inputs for SSRN records change at the pre/post boundary: pre-2022 records arrived through Microsoft Academic Graph, which parsed SSRN pages (affiliations, abstracts); post-2021 records come from Crossref deposits that, in my experience, carry author names only **[memory]**. OpenAlex's documentation says ORCID matching is not applied retroactively, profiles are both split and merged, and authorships with different ORCIDs can still be merged on name, institution and coauthor signals **[verified: web]**. The "92%" is almost certainly OpenAlex's `has_orcid` filter, true when at least one author's *profile* carries an ORCID propagated from other works, not an ORCID on the SSRN deposit **[memory]**; it says nothing about record-level identity quality. Any drift in split/merge rates around 2022 produces a spurious pre/post shift in measured output.
**(c)** Treat OpenAlex IDs as a seed, not truth: (i) build the SSRN spine from Crossref; (ii) attach OpenAlex author IDs by DOI lookup; (iii) build an independent within-spine assignment (normalised name + coauthor overlap + topic similarity) and report agreement; (iv) hand-validate 150–200 scholars stratified by name frequency and field, checking pre- and post-2022 attributions separately; (v) report authorship-level and scholar-level ORCID shares; (vi) run a robustness sample of ORCID-bearing scholars with uncommon names.

### M4. "No scraping" rules out more than the pitch admits: JEL codes, eJournal classes, download counts, pipeline flags, conference PDFs
**(a)** (F): "JEL codes where authors report them; otherwise an LLM classifies"; (G): "AI referee scores ... computed where conference PDFs are public"; "composition checks for SSRN's journal-submission pipelines".
**(b)** SSRN's terms require users to warrant that they "will not run software that sends repeated queries to SSRN or otherwise send automated queries of any sort", with a dedicated section on "Abstract Usage Statistics and Automated Querying" **[verified: web]**. JEL codes and eJournal classifications exist only on SSRN pages; Crossref has no JEL field and OpenAlex carries none **[memory, high confidence]**. AFA and WFA programs link to SSRN-hosted PDFs, so "where conference PDFs are public" is a small, selected set. The pipeline point is the serious one: Elsevier's SSRN First Look posts manuscripts at submission or when sent to review for participating journals **[verified: web; 2021 description, current journal list unknown]**. If Elsevier finance and accounting journals (JFE, JAE, JBF, AOS and others) participate, a scholar's SSRN count rises mechanically with each submission, more so for archival submitters, mimicking H1.
**(c)** Delete the JEL clause. Quantify the pipeline early: tabulate by year the share of finance/accounting SSRN records carrying affiliations or ORCIDs (submission-system deposits carry full author metadata, author uploads typically do not **[memory]**), and the share whose journal version is in an Elsevier journal with an SSRN posting within 14 days of the article's received date. Add a specification excluding candidate pipeline postings. Drop AI referee scores.

### M5. Eight data components for a 3–6 month horizon, with no MVP defined
**(a)** (F) lists eight data items plus "the Pangram detector ... if licensed"; (G) adds conference acceptance, near-duplicates, AI referee scores and 2027/2028 updates.
**(b)** The table in §3 sums to roughly 40–50 person-weeks of engineering and RA time, i.e. 12–18 months at realistic allocations, against a competition risk the pitch itself names. Conference programs, editor reports (JoF publishes annual reports, 2023: median turnaround 43 days, desk rejection 43%; Review of Finance publishes 2022–24 reports **[verified: web]**; TAR, CAR and JAR publish some form of report, JFE, RFS, JAE and RAST do not consistently **[memory]**) and the posting-rate measure are each multi-week, and none is needed for the headline β_km.
**(c)** Adopt the staged plan in §4 and state the stage-1 scope in the pitch.

### M6. The SSRN posting-rate control cannot be measured for the years that matter
**(a)** (E): "I measure this posting rate directly, as the share of each field's and method's journal articles that also appear on SSRN, by year, and add it as a control if it changes over time."
**(b)** An article published in year t was posted to SSRN two to four years earlier. Dated by journal year, the measure describes 2020–22 posting behaviour; dated by posting year, it is right-truncated because recent working papers are unpublished. Either way, 2024–26, the period of the reasoning and agentic releases, is unmeasurable before 2028. It also requires method-classifying ~100k journal articles whose abstracts are missing in OpenAlex for Elsevier journals (Elsevier does not deposit abstracts to Crossref **[memory]**), so it needs Scopus abstracts, another three weeks.
**(c)** Replace with a ceiling test (scholars whose pre-period posting propensity, the share of their 2015–21 journal articles with an SSRN version, is near one cannot raise it; if β_km is similar for them, posting habits do not drive the result) plus the any-platform outcome already planned.

### M7. Classification validation is under-sized and part of the taxonomy is unobservable from abstracts
**(a)** (F): "About 300 papers are hand-coded for validation"; Table 1: "archival, by data source (standard databases, text, hand-collected records)".
**(b)** 300 papers over two fields, five to six areas and six-plus method cells leaves fewer than ten papers in many cells and no human–human reliability ceiling. "Hand-collected" is rarely stated in an abstract; expect κ around 0.5 on that split against 0.8+ for the coarse method split **[memory/experience]**. Error in Share_im attenuates β_km, differentially for the rare methods (theory, experiments) that carry H2 and H3. Reviewer optics: an LLM-built exposure measure in a paper about LLMs invites the objection that the instrument is endogenous to the technology studied; the answer is human double coding plus a non-LLM baseline.
**(c)** 600 papers stratified by predicted class and field; two human coders blind to the LLM label; report Cohen's κ (human–human and human–LLM), the confusion matrix and per-class precision/recall; adjudicate disagreements; collapse archival sub-types in the main specification; replicate with a second model family and a supervised baseline trained on the 600 labels; correct β for misclassification using the confusion matrix. Cost is small: at October 2026 list prices (Claude Opus 5.5 US$4/US$20 per million input/output tokens, Sonnet 5.5 US$2/US$10, batch at 50%, cached prefix reads about US$0.20 per million), a 35k-paper pass (~1,200-token cached prompt, ~350 input and ~120 output tokens per paper) costs roughly US$70–140 (Opus-class, batch) or US$40–75 (Sonnet); US$1,000–1,500 covers development, two model families, repeat runs and a later journal-article pass. RA coding: 600 × 2 × ~5 minutes ≈ 100 hours plus adjudication, about A$6–8k.

---

## 3. Feasibility table

| Component | First draft? | Effort (person-weeks) | Main risk | Fallback |
|---|---|---|---|---|
| Crossref SSRN spine (all 10.2139 DOIs: dates, titles, authors, type) | Yes | 1 | Posting-date field (`created` vs `issued`); deposit type changes | Use `created`; hand-check 50 records |
| OpenAlex enrichment (DOI lookup, author IDs, topics, profiles, all works of panel authors) | Yes | 1.5 | ID churn and merges; 100k calls/day | Dated snapshot; raw JSON |
| Panel definition + identity validation (M3) | Yes | 2–3 | Disambiguation quality shifts at 2022 | ORCID/uncommon-name subsample; own matcher |
| LLM classification + 600 double-coded (M7) | Yes | 2 + RA 120 h | Low κ on fine methods; 2018–21 abstract gaps | Collapse taxonomy; title-only accuracy reported |
| PPML, event studies, placebos | Yes | 2 | Career-age term collinear with FE | Binned age with normalisation |
| First Look diagnostic (M4) | Yes | 1 | No explicit flag in metadata | Affiliation/ORCID heuristic; exclusion spec |
| AI-vocabulary first stage | Descriptive only | 1 | 2025 gap | Report 2023–24 and 2026 |
| SSRN ↔ journal linkage (title/author, blocked by author ID) | Stage 2 | 2–3 | Title changes cut recall to ~75–85% | Add OpenAlex merged locations, Crossref relations, Semantic Scholar clusters |
| Publication within 24 months | Stage 2 | 1–2 | Low shares for recent cohorts | Descriptive in v1; 36/48-month updates |
| Journal congestion: editor reports | Stage 2 | 1–2 RA | Inconsistent coverage | Received/accepted dates from Elsevier XML (TDM API) |
| Conference programs (AFA, WFA, EFA, Cavalcade, FIRS, AAA, FARS) | Stage 3 | 3–4 | Heterogeneous PDFs; name matching | Restrict to AFA, WFA, AAA |
| Posting-rate measure (M6) | Replace | 3 | Truncation; journal abstracts | Ceiling test |
| Licensed abstracts (Scopus test; Dimensions application) | No | 0.5 + 4–8 weeks elapsed | Route may not exist | Accept the 2025 gap |
| HREC low-risk application | Yes (critical path) | 0.5 + 4–8 weeks elapsed | Escalation to full review | Submit now; aggregate-only reporting |

Cash budget: stage 1 about A$8–10k (LLM US$1–1.5k, RA coding A$6–8k, no data fees); full programme about A$18–25k.

---

## 4. Staged plan (from November 2026)

**Stage 1 — MVP (November 2026 to February 2027).** Deliverable: working paper v1 with β_km estimates, event studies, placebos and a validation appendix.
- November: submit the HREC low-risk application in week 1. Adelaide routes lower-risk research to one of six lower-risk committees; approval or exemption must be in place before research starts, and a low-risk application can be escalated to full review **[verified: web]**, so allow 4–8 weeks and ask the ethics office in writing whether aggregate bibliometric analysis of public records needs review at all. Build the Crossref spine and coverage tabulations; run the Scopus test; OpenAlex enrichment and snapshot; develop the classification prompt on 200 papers.
- December: panel construction and identity validation; full classification run; RA double coding; First Look diagnostics.
- January 2027: PPML estimates, event studies by method, placebo dates, pipeline-exclusion specification, first-stage descriptives.
- February: draft v1, circulate, submit to AFA 2028 (March deadline) and the European and FMA meetings.

**Stage 2 (March to June 2027).** SSRN–journal linkage; 24-month publication analysis for the 2018–2024Q3 cohorts; congestion measure from Elsevier received/accepted dates plus available editor reports; heterogeneity (H4) from author-level affiliation histories; v2 for journal submission by about July 2027.

**Stage 3 (second half of 2027 to 2028).** Conference-program matching; licensed abstracts for 2025 if a route exists; descriptive posting rate to 2023; 36- and 48-month updates in September 2027 and 2028; replication package.

---

## 5. Minor issues

- OpenAlex's Finance (2003) and Accounting (1402) subfields miss finance papers filed under Economics and Econometrics or Strategy and Management; OpenAlex's reported top-1 topic accuracy is 0.72 with full metadata **[verified: web]** and lower without abstracts, i.e. much of 2025. Define scholars by journal portfolio (an article in an ABDC finance or accounting journal, 2015–21) rather than by SSRN topic labels.
- Posting dates: check `created` versus `issued` on SSRN Crossref records; year-only dates default to 1 January and corrupt quarterly timing.
- The last one or two quarters are incomplete (SSRN screening, deposit and ingestion lags); end the main sample at 2026Q2.
- Career-age effects λ_a are collinear with scholar and quarter fixed effects (age–period–cohort); use coarse bins with an explicit normalisation.
- A threshold of two pre-period papers gives shares of 0, 0.5 or 1 and invites mean reversion; use three or four in robustness.
- Release dating: GitHub Copilot was generally available in June 2022, before ChatGPT; reasoning models date from o1-preview (September 2024) and DeepSeek-R1 (January 2025) **[memory]**.
- Abstract copyright: Australia has no general text-and-data-mining exception; fair dealing for research plausibly covers computing word frequencies if abstracts are neither retained beyond the project nor redistributed.

---

## 6. What works and should be kept

- Crossref as the complete list of SSRN DOIs and posting dates, with no scraping: correct, sufficient for the core outcome, and defensible to SSRN.
- The outcome (paper counts) needs no abstracts, so the headline result is immune to the 2025 gap.
- Pre-period method shares as exposure, PPML with field×quarter fixed effects, and event-study plots by method: cheap to run and the right core check.
- AI vocabulary as a first stage rather than treatment, which avoids the Renault et al. timing problem.
- The fixed panel, the practitioner robustness group, the any-platform outcome, the planned 2027/2028 updates, and the ethics framing.

---

## 7. Must fix before circulating to coauthors vs fix later

**Must fix now**
1. Replace the ICSR Lab/Scopus sentence with a tested route or an explicit statement that the 2025 abstract gap is accepted and how the first stage handles it (M1).
2. Re-derive the abstract-coverage numbers with documented queries, separating Crossref from OpenAlex and deposit types, and add 2018–2021 coverage (M2).
3. Add an author-identity validation plan; replace "ORCID on 92% of 2024 SSRN works" with authorship-level and scholar-level shares (M3).
4. Delete "JEL codes where authors report them"; describe the classification as LLM plus 600 double-coded papers with κ, confusion matrix and a non-LLM baseline (M4, M7).
5. Add the First Look pipeline diagnostic and exclusion specification (M4).
6. State the stage-1 scope and a Q1 2027 target; move conference programs, Pangram, AI referee scores and the posting-rate control to later stages or drop them (M5, M6).

**Fix later:** congestion-measure choice; conference-matching details; Dimensions application; HREC wording; replication package.

---

## Appendix: queries to run before circulating

OpenAlex (confirm the SSRN source with `sources?search=SSRN`; from memory it is "SSRN Electronic Journal", ISSN 1556-5068, id S4210172589):
1. `works?filter=primary_location.source.issn:1556-5068&group_by=publication_year`, and the same with `locations.source.issn` — the difference is SSRN papers filed under another primary location.
2. Add `,has_abstract:true` — abstract coverage by year; add `,primary_topic.subfield.id:2003` or `1402` — reproduce the counts in (D).
3. `...,publication_year:2024&group_by=has_orcid` — counts works with at least one ORCID-bearing author.
4. `...,publication_year:2024&sample=200&seed=1&select=authorships` — count authorships with non-empty `institutions` and `orcid`.

Crossref:
5. `prefixes/10.2139/works?rows=0&facet=published:*,type-name:*` — records by year and deposit type; repeat with `&filter=has-abstract:1`, `has-orcid:1`, `has-affiliation:1`.
6. `works/10.2139/ssrn.<id>` for ten known papers — compare `created`, `issued` and `posted` with the SSRN posting date; inspect `abstract`, `affiliation`, `ORCID`.
