---
title: "Which Research Does Generative AI Speed Up? Evidence from Finance and Accounting Working Papers"
author: "Mingwei Sun · School of Accounting and Finance, College of Business and Law, Adelaide University"
date: "Research pitch · revised draft for coauthors · 30 October 2026"
---

*Prepared with the Pitching Research template of Faff (2024). This draft revises the pitch of 23 October 2026 after an internal round of critique. Protocol detail is in Appendix A; items to settle before wider circulation are in Appendix B.*

# Project Summary

Finance and accounting working papers on SSRN have roughly doubled since ChatGPT arrived in late 2022, after years of flat output. Is generative AI making scholars more productive, or mainly multiplying the kinds of paper that are easiest to automate? The main scholar-level estimate (Kusumegi et al. 2025, *Science*) is partly an artefact of how AI adoption was dated (Renault, Bergeaud & Bosquet 2026). We avoid that problem with an exposure design: we follow a fixed panel of scholars who were posting on SSRN before ChatGPT, classify their earlier papers by research area and method, and ask whose output rose in each wave of AI tools (text and code assistants, 2022--23; reasoning models, late 2024; agentic coding tools, 2025). Because the method mix is measured before these tools existed, the comparison cannot depend on who chose to use AI or when. We expect the largest gains in archival work on standard databases, none in experiments, surveys and hand-collected work, and gains in theory only after reasoning models, with a lag. A second part asks who gains most, scholars with fewer resources or scholars whose papers are counted, and whether the extra papers reach conferences and journals; the answers matter to promotion committees, journal editors and doctoral programs.

# (A) Working Title

Which Research Does Generative AI Speed Up? Evidence from Finance and Accounting Working Papers (alternative: More Papers or More Research?)

# (B) Basic Research Question

Which kinds of finance and accounting research has generative AI accelerated, by research method and by wave of AI tools, and by how much relative to the least-exposed methods? Who has gained most: scholars with fewer resources, or scholars facing the strongest incentives to count papers? A secondary question is whether the additional working papers clear the bars the profession uses, conference acceptance, citations and eventual publication, once slower peer review is taken into account.

# (C) Key Papers

1.  **Kusumegi, Yang, Ginsparg, de Vaan, Stuart & Yin (2025, *Science*); Renault, Bergeaud & Bosquet (2026, *PNAS*); Kusumegi et al. (2026, reply).** Across 2.1 million arXiv, bioRxiv and SSRN preprints, scholars post more papers after their first abstract is flagged as LLM-assisted, most of all on SSRN (+59.8%). Renault et al. show that dating adoption by the first flagged paper produces an apparent jump even when AI has no effect, because busy months are more likely to contain a flagged paper; the reply defends the direction of the association, not its magnitude. How large the effect is, and where it comes from, is open.
2.  **Arcila (2026).** Twenty-six OpenAlex fields ranked by predetermined AI exposure; output rises only in computer science. Closest in spirit, but at the level of fields, where finance and accounting are not separate units and new authors cannot be separated from established scholars.
3.  **Walther & Dutordoir (2025).** Articles in 34 finance journals: readability falls after ChatGPT, and authors whose post-ChatGPT papers score higher on AI use publish more, in lower-ranked journals. Published articles only; AI use measured from the authors' own papers.
4.  **Nee, Zhong & Ni (2026).** Twenty arXiv archives to August 2026: a 2026 surge in mathematics, about a third above 2025, read by the authors as delayed diffusion and capability thresholds. Closest on method-level timing; archive counts, no scholar panel, no quality outcome.

# (D) Motivation/Puzzle

**Facts.** OpenAlex assigns about 4,400 SSRN papers a year to Finance from 2015 to 2022, then 7,393 in 2025 and 9,125 by early October 2026; Accounting rose from 2,683 in 2022 to 5,653 in 2025 (author's tabulation; 2023--24 counts and a check against SSRN's own statistics pending, Appendix B). Novy-Marx & Velikov (2026) generate hundreds of return-predictability papers from accounting signals and warn that AI industrialises HARKing (Kerr 1998); Ciconte, Rozario & Urcan (2026) show AI writing polished archival accounting papers, many with spurious results. Editors report "more versus better": submissions to *Organization Science* are up 42% since ChatGPT, with lower quality (Gartenberg et al. 2026), and across fields output growth is concentrated in computer science (Arcila 2026).

**Puzzle.** The more-versus-better hypothesis has its sharpest prediction in finance and accounting: the multiple-testing problem of archival research is documented (Harvey, Liu & Zhu 2016; Harvey 2017; Mitton 2022), p-hacking varies by method (Brodeur, Cook & Heyes 2020), and AI pushes the cost of one more specification toward zero exactly where data are standardised. Yet the evidence is thin. The scholar-level estimate is in doubt. The only finance evidence (Walther & Dutordoir 2025) uses published articles, which appear years after a paper is written and after journals have filtered out weaker work, so it cannot see the working papers that are never published. And no existing design says *which* research is being accelerated, because each measures AI use rather than what AI can do for each kind of work. The puzzle: where in finance and accounting does the post-2022 boom come from, by method and by type of scholar, and does the marginal paper hold up?

# (E) Idea

**Core idea.** AI tools arrived in waves with different capabilities: text and code (2022--23), formal reasoning (late 2024) and agentic coding (2025; dates in Appendix A1). Research methods bundle tasks differently: theory rests on derivations, archival work on data handling and code, experiments and surveys on collecting data from people. The task-based view of AI exposure (Felten, Raj & Seamans 2021; Eloundou et al. 2024; Korinek 2023) therefore predicts that each wave raises output in different methods at different times. We measure each scholar's method mix before ChatGPT and use it as a predetermined exposure, so the design needs no adoption date and never conditions on a scholar's own later output or text.

**Classifying research.** Every paper from 2014 to 2026 is classified by area and method, so both the pre-period method mix (the exposure) and the method of each later paper (the composition of output) are observed.

-   *Areas.* Finance: JEL G1 markets and asset pricing, G2 institutions, G3 corporate finance, G4 behavioral, G5 household, G0/other (AEA). Accounting: financial accounting and disclosure, auditing, managerial, tax, information systems, other (Coyne, Summers, Williams & Wood 2010).
-   *Methods.* Analytical; archival with standard databases, with text, or with hand-collected records; structural estimation; machine learning or LLM as method; experimental (lab, online, field); survey, interview or field study; review or commentary. The core categories follow Coyne et al. (2010) and Oler, Oler & Skousen (2010); the data-source and finance-method splits are this project's extension, with a written rule separating an LLM used to build a variable (archival-text) from a paper whose contribution is the pipeline (LLM-as-method).

**Model.** Log expected papers posted by a scholar in a period equals a scholar effect, a career-stage effect, a field-by-period effect and, for each method, a period effect multiplied by the scholar's pre-period share of that method:

$$\mathrm{E}\left[\text{Papers}_{it}\right] = \exp\left( \alpha_{i} + \lambda_{c(i,t)} + \tau_{f(i),t} + \sum_{m \neq m_0} \sum_{s \neq s_0} \delta_{ms}\, \mathbf{1}[t \in s] \times \text{Share}_{im} \right)$$

Here *i* indexes scholars and *t* quarters; the field-by-period effect (finance or accounting) absorbs anything common to the field, including SSRN's own growth, COVID and SSRN screening changes; Share is the share of the scholar's 2014--2018 papers using method *m*, fixed before any generative-AI tool existed; and the coefficient on method *m* in half-year *s* is the output of a scholar whose earlier papers all used that method, relative to the base period 2019H2 and to the reference methods (primary-data methods: experiments, surveys and field studies). Coefficients are plotted by half-year (Figure 1) and averaged over four windows fixed in advance, W1 2022Q4--2023Q2 (ChatGPT, GPT-4), W2 2023Q3--2024Q3 (diffusion of text and code tools), W3 2024Q4--2025Q1 (reasoning models) and W4 2025Q2--2026Q2 (agentic coding tools); the window averages, written $\beta_{wm}$ below, are the headline estimates. The labels are interpretations the estimates can reject, not identifying assumptions: text and code help arrived together in 2022--23, so only the 2024--25 waves separate reasoning from coding (Appendix A1).

**What is identified.** Because a scholar's shares sum to one, an effect of AI common to all methods is absorbed by the field-by-period effects. The design identifies the *method gradient* of AI's effect, under the assumption that scholars with different pre-period method mixes would have followed parallel paths within their field, checked over the clean pre-period 2019Q1--2022Q3, which lies outside the window used to select the sample and measure shares, with sensitivity bands for violations (Rambachan & Roth 2023). A level effect needs an anchor (primary-data methods unaffected through 2024) and is reported only as a secondary exhibit with bands for anchor effects of ±10 and ±25% (Appendix A2).

**Hypotheses.** Methods: T analytical; AS archival with standard databases; AH archival hand-collected; R review or commentary; the reference is primary-data methods.

-   **H1 (data and code tools speed up database-driven archival work).** $\beta_{w,\mathrm{AS}}$ is positive and the largest of all methods from W2 onward; in W1, the writing wave, $\beta_{w,\mathrm{R}}$ is the largest (mechanism: Novy-Marx & Velikov 2026; Ciconte et al. 2026).
-   **H2 (theory responds only to reasoning models, with a lag).** $\beta_{\mathrm{W1},\mathrm{T}} = \beta_{\mathrm{W2},\mathrm{T}} = 0$ and $\beta_{\mathrm{W3},\mathrm{T}}$ or $\beta_{\mathrm{W4},\mathrm{T}} > 0$. This is the sharpest timing test the design offers; it fails if theory output rises in 2023.
-   **H3 (primary-data and hand-collected work are least exposed).** $\beta_{w,\mathrm{AH}}$ is near zero and below $\beta_{w,\mathrm{AS}}$ in every window, and in the paper-level model papers that use primary data do not rise.
-   **H4 (who gains: democratisation or count-gaming).** Democratisation predicts larger gains where constraints bind (early-career scholars, institutions outside the UT Dallas and BYU top 50, non-English-speaking institutions, small teams) with unchanged marginal quality, a sequel to Kim, Morse & Zingales (2009) and Agrawal & Goldfarb (2008); count-gaming predicts larger gains where papers are counted (list-based evaluation regimes: ABDC, ABS, AACSB-driven counts) with lower marginal quality. Tested as window × share × group interactions with the quality outcomes of (G).

**Two complements.** A paper-level model (scholar × method × quarter) shows whether exposed scholars produce more of their own method or switch methods; it is descriptive, since post-2022 method choice is endogenous. The share of abstracts with AI-style vocabulary (Gardner, Krupa & Mammadov 2026; Kobak et al. 2025) is a mechanism check, expected to rise after W1 most in review and least in primary-data methods, not a first stage: it captures AI-assisted writing only, and dating adoption from a scholar's own AI words would recreate the Renault et al. problem.

# (F) Data

-   **Working papers.** Spine: every SSRN DOI (prefix 10.2139) from Crossref, with posting dates. Enrichment: OpenAlex (Priem, Piwowar & Orr 2022) by DOI lookup for author identifiers, topics, institutions, citations and journal versions; the OpenAlex SSRN series is validated against SSRN's published statistics before any figure uses it. No scraping: SSRN's terms prohibit automated queries, so SSRN's JEL codes, eJournal classifications and download counts are not used.
-   **Scholar identity.** OpenAlex author identifiers are a seed, not the truth: profiles split and merge, and OpenAlex's inputs for SSRN records change at the 2021/22 boundary. An independent assignment is built and hand-validated on 150--200 scholars (Appendix A4).
-   **Sample.** Academic authors with at least three finance or accounting SSRN papers in 2014--2018 (also the share window), observed 2014Q1--2026Q2; 2026Q3 is reported but incomplete. Robustness: the 2018--2021 definition (more junior scholars, shorter clean pre-period) and thresholds of two and five papers. Practitioner authors form a comparison group; journal-pipeline postings (preprints posted at submission by participating journals) are excluded in a robustness specification; attrition is handled with an activity indicator (Appendix A4).
-   **Abstracts and classification.** Abstracts from Crossref and OpenAlex where present; the 2025 gap is accepted for now because the outcome needs no abstracts. An LLM classifies every paper from title and abstract; 600 papers are double-coded by two human coders blind to the LLM label, with agreement, confusion matrix and misclassification correction reported (Appendix A4).
-   **Outcome.** New SSRN papers per quarter, as full and coauthor-fractional counts; as robustness, new working papers on any platform indexed by OpenAlex (SSRN, NBER, CEPR, arXiv), de-duplicated.
-   **Heterogeneity.** Career age, institution rank (UT Dallas and BYU), country, the institution's evaluation regime (list-based or top-journal), coauthor structure and international collaboration, all measured before 2022.
-   **Quality outcomes (second part).** Acceptance at AFA, WFA, EFA, SFS Cavalcade and FIRS, and at the AAA Annual Meeting, FARS Midyear and the JAR and RAST conferences, from public programs matched by title and authors; citations at 24 months against same-cohort, same-method papers; within-author near-duplicates; journal versions (top-3/top-6, ABDC and FT50 lists); journal turnaround from editor reports where published.

# (G) Tools

-   **Estimation.** Poisson pseudo-maximum likelihood on the scholar--quarter panel with high-dimensional fixed effects (Correia, Guimarães & Zylkin 2020; Cohn, Liu & Wardlaw 2022). The main exhibit is Figure 1: event-study coefficients by method and half-year, base period 2019H2, the 2020--21 quarters shown separately, and the window averages W1--W4 as the headline estimates, reported as $\exp(\beta) - 1$.
-   **Inference.** Scholar-clustered and exposure-robust standard errors (Adão, Kolesár & Morales 2019); randomisation inference over placebo release dates and permuted shares; four pre-registered primary contrasts with Romano--Wolf adjustment for the rest; a power statement computed before estimation (Appendix A5).
-   **Identification checks.** Pre-trends over 2019Q1--2022Q3 with Rambachan & Roth (2023) confidence sets; placebo release dates; area-by-period fixed effects; the pre-period share of AI and machine-learning topics interacted with period (AI as a tool versus AI as a topic); the practitioner group, the any-platform outcome and the journal-pipeline exclusion.
-   **Posting versus production.** A posting-rate control built from journal articles cannot be observed for recent cohorts and is a function of the outcome. It is replaced by a ceiling test (scholars whose pre-period papers were almost all on SSRN cannot raise their posting rate) and a real-time posting propensity from conference programs; for accounting, where posting is stage-dependent, versions per paper and the gap between first posting and conference appearance are tracked by method.
-   **Second part: do the extra papers hold up?** Journal slots are roughly fixed in the short run, so a larger supply lowers the share published within any window even if quality is unchanged: a lower 24-month share is the null, not evidence of weaker papers (Appendix A3). We therefore use outcomes that do not depend on journal queues (conference acceptance within 12 months; citations at 24 months against same-cohort, same-method papers; near-duplicates) and model publication as a discrete-time hazard with right-censoring and journal turnaround as a covariate. The more-versus-better prediction: the methods whose output rose most show lower marginal quality on the slot-free outcomes. AI referee scores (Lu, Luo & Yu 2026) enter only if a test on pre-2022 papers shows no preference for AI-style text; the 36- and 48-month outcomes (2027, 2028) form a pre-registered companion paper.

# (H) What's New?

| Study | Unit | Outcome | AI measure | What changes here |
|:-----------|:-------|:--------|:----------|:----------------------|
| Kusumegi et al. (2025); reply (2026) | scholar | preprints, incl. SSRN | first LLM-flagged abstract (adoption date) | exposure instead of adoption: no adoption date; identification never uses the scholar's own output or text |
| Arcila (2026) | field (26 OpenAlex fields) | works per field | predetermined field AI intensity | scholar-level exposure inside finance and accounting; established scholars separated from new entrants |
| Walther & Dutordoir (2025) | article | published finance articles | AI vocabulary in the authors' papers | working-paper stage; predetermined exposure; both fields |
| Nee, Zhong & Ni (2026) | arXiv archive | preprint counts | capability-wave timing | scholar panel in business fields; method mix within scholar; quality outcomes |
| Gardner et al. (2026); Barrick, Summers & Wood (2025) | paper; survey | AI use in accounting | vocabulary; self-reports | effects on output and quality |

: Table 1. The closest studies and what this project changes

Three additions: an exposure design rather than an adoption design, so the Renault et al. mechanism cannot operate and the estimand is the response of established scholars, net of the entry that drives field-level counts; method-by-wave timing, including the test that theory responds to reasoning models and not to the 2023 tools; and who gains, by resources and by evaluation regime, with quality outcomes that do not depend on journal queues. This is not Kusumegi et al. on SSRN with another proxy: their design asks what happens to adopters after adoption; ours asks whose output rose when a capability became available, whether or not we can see them use it.

# (I) So What?

**For those who count papers.** If the expected SSRN count of a database-archival scholar rose by X% relative to an experimentalist's, a count threshold set in 2019 is now Y% easier to meet for the former. Promotion committees, schools that manage to ABDC or ABS lists, AACSB accreditation based on counts of intellectual contributions and national assessments (the successor to Australia's ERA; REF 2029) should then benchmark within method or stop counting working papers. H4 says whether elite institutions are losing their edge again (Kim, Morse & Zingales 2009) or count-based regimes produce more of what is counted (Heckman & Moktan 2020).

**For editors.** If Z% of the post-2022 surge traces to a few segments whose marginal papers score lower on slot-free quality measures, targeted screening beats blanket submission fees or AI bans; SSRN's and journals' AI-disclosure policies need the same map.

**For doctoral programs.** Methods whose output rose without a matching rise in quality are being commoditised; training should shift toward primary data, identification and theoretical judgement. Keloharju & Keloharju (2025) argue that humans keep an edge in higher-order reasoning; H2 tests that claim rather than assuming it.

# (J) Contribution

Two literatures and one mechanism. To research on AI and the production of science (Kusumegi et al. 2025; Filimonovic, Rutzer & Wunsch 2025; Arcila 2026; Nee et al. 2026; Hao, Xu, Li & Evans 2026), the first scholar-level estimate built on predetermined exposure rather than observed adoption, with timing by capability wave; the precedent is work on earlier technologies and academic productivity (Agrawal & Goldfarb 2008; Kim, Morse & Zingales 2009; Ding, Levin, Stephan & Winkler 2010). To research on evaluation under quantity incentives and publication congestion (Ellison 2002; Card & DellaVigna 2013; Heckman & Moktan 2020; Gartenberg et al. 2026), evidence on where the surge comes from and what the marginal paper is worth, by evaluation regime. The mechanism comes from finance and accounting methodology: AI as the automation of specification search (Harvey 2017; Novy-Marx & Velikov 2026; Ciconte et al. 2026). For accounting, the AI literature moves from documenting use (Gardner et al. 2026; Barrick et al. 2025; Stratopoulos & Wang 2025) to measuring output and quality.

# (K) Other Considerations

-   **Target outputs.** Lead: *Management Science*, cross-field, led by the event-study figure and the regime heterogeneity. Finance-led alternative: *JFE*, *Review of Finance* or *JFQA*; the *Journal of Finance* only with a credible level design. Accounting companion (posting stage, top-six publication, conference outcomes): *Contemporary Accounting Research* or *Accounting Horizons*. The 2028 publication-outcome paper: *The Accounting Review* or *JFE*.
-   **Risks.** (1) Competition from Walther & Dutordoir, Arcila and Nee et al.: a stage-1 draft by February 2027. (2) Overlapping waves: the labels can be rejected by the event-study timing; only the 2024--25 waves separate reasoning from coding. (3) Method-specific shocks unrelated to AI (AI as a topic, crypto, climate finance): area-by-period effects, the AI-topic share, placebo dates, randomisation inference. (4) Measurement: scholar identity, the OpenAlex series, classification error, each with a validation plan. (5) Posting versus production, including journal pipelines and earlier posting in accounting: the ceiling test, the conference-based propensity, versions per paper.
-   **Limitations stated upfront.** The design identifies differences between methods, not the total effect of AI; the anchored level rests on an assumption. Working papers proxy for research output, and in accounting SSRN is a stage-dependent window on it. The vocabulary measure captures AI-assisted writing only. Finance barely varies in experimental, survey and review methods, so H1 and H3 are largely identified from accounting scholars, and theory cells are small; the power statement says what can be detected.
-   **Feasibility, ethics and timeline.** Metadata come from Crossref and OpenAlex (CC0), never from scraping SSRN; abstracts feed computed measures only. A low-risk application to the Adelaide HREC goes in during the first week of November. Stage 1 (November 2026 to February 2027) delivers draft v1 and an AFA 2028 submission; stage 2 (to June 2027) adds the quality outcomes and heterogeneity; stage 3 the 2027--28 updates. Cash cost about A\$8--10k for stage 1 and A\$18--25k in all (Appendix A6).
-   **What I am looking for.** Two coauthors: an accounting researcher who knows the BYU taxonomy, the AAA and FARS circuit and the accounting journals, to own the accounting classification, the posting-stage analysis and the accounting positioning; and an applied econometrician or data engineer at home with event-study Poisson designs and the OpenAlex and Crossref APIs, to own identification, inference and the replication package. What exists now: the OpenAlex and Crossref tabulations behind (D), the draft design and this pitch. [Division of labour, authorship order and time commitments: to discuss at the first meeting.]

# Appendix A. Protocol notes

**A1. Release calendar and windows.** ChatGPT, 30 November 2022 (text and code); GPT-4, 14 March 2023; Code Interpreter, July 2023 (code execution); Claude 3.5 Sonnet, June 2024; o1-preview, September 2024, o1, December 2024 and DeepSeek-R1, January 2025 (reasoning); Claude Code, February 2025, and OpenAI Codex, May 2025 (agentic coding). GitHub Copilot was generally available from June 2022, before the first window. Windows: W1 2022Q4--2023Q2; W2 2023Q3--2024Q3; W3 2024Q4--2025Q1; W4 2025Q2--2026Q2. Secondary specification: shares interacted with a continuous capability or diffusion index (coding and mathematics benchmark scores; ChatGPT weekly users) in place of the windows.

**A2. Reading the coefficients.** With shares summing to one, $\sum_m \text{Release}(t) \times \text{Share}_{im}$ equals $\text{Release}(t)$ for every scholar, a field-level time dummy absorbed by the field-by-period effects; one method per window must therefore be the reference, and $\beta_{wm}$ is a gain relative to a scholar whose earlier papers all used the reference methods. Summing $\beta_{wm} \times \text{Share}_{im}$ over methods gives a scholar's effect relative to such a scholar, not the AI share of total growth. The anchored level adds the assumption that the reference methods are unaffected, and we report how the level moves if that assumption is off by ±10 or ±25%. Linearity of the shares inside the exponent restricts mixed-method scholars; the paper-level model relaxes it. Career-stage bins are coarse (five years) because career age is collinear with scholar and period effects.

**A3. Sample windows and the fixed-capacity null.** The sample is selected, and shares are measured, on 2014--2018; the pre-trend test runs over 2019Q1--2022Q3, so it is not computed inside the window that conditions the sample, and the COVID quarters are displayed rather than hidden (SSRN output rose sharply in the first weeks of the 2020 lockdowns, Cui, Ding & Zhu 2022, and the pandemic shifted finance productivity unevenly, Barber et al. 2021). Mean reversion after selection would show up in 2019--2022 if it mattered. For quality: if a cohort posts $S_c$ papers and the journals open $K$ slots to it within the window, an unchanged quality distribution still lowers the publication share $K/S_c$ one-for-one with the supply increase; within-cohort method gaps net this out only if slots are not method-specific, which they are, hence the slot-free outcomes and the hazard model with journal turnaround as a covariate.

**A4. Data protocol.** *Posting dates:* Crossref `created` dates, checked by hand against 50 SSRN pages (year-only dates would default to 1 January and corrupt quarterly timing). *Identity:* OpenAlex IDs attached by DOI; an independent within-spine assignment from normalised name, coauthor overlap, topic similarity and ORCID; 150--200 scholars hand-validated, stratified by name frequency and field, pre- and post-2022 attributions checked separately; authorship-level and scholar-level ORCID shares reported; estimates repeated on the ORCID-linked, uncommon-name subsample. *Classification:* LLM labels from title and abstract (title only where no abstract exists, accuracy reported separately); 600 papers stratified by predicted class and field double-coded by two human coders blind to the LLM label; human--human and human--LLM agreement (Cohen's κ), confusion matrix and per-class precision; shares corrected for misclassification; replication with a second model family and a supervised baseline trained on the 600 labels. *Attrition:* an "active" indicator (any work on any platform in a rolling three-year window), exit rates by method, estimates with and without conditioning on activity. *Journal pipelines:* postings whose metadata pattern matches submission-system deposits, and whose journal version appears in a participating journal with posting within days of the received date, flagged and excluded in a robustness specification.

**A5. Inference plan.** Scholar-clustered standard errors alongside exposure-robust standard errors for share designs (Adão, Kolesár & Morales 2019); randomisation inference over placebo release dates in 2015--2021 and over 1,000 permutations of shares across scholars within field and area; four pre-registered primary contrasts (AS versus the reference in W2; T versus AS in W3--W4; R versus all in W1; AH versus AS) with Romano--Wolf adjustment for the remaining cells (Romano & Wolf 2005); power computed from the 2014--2021 panel (scholars per method cell, baseline rates, detectable window effects at 80% power) before estimation; a random 30% of scholars held out for confirmation if the primary contrasts are revised after seeing the data.

**A6. Ethics, timeline and budget.** The panel uses identifiable public information about people, which the National Statement treats as human research, so a low-risk HREC application (no participant contact; scholar-level AI-use measures reported only in aggregate) is submitted in the first week of November 2026 and takes four to eight weeks. Stage 1, November 2026 to February 2027: Crossref spine, OpenAlex enrichment, panel and identity validation, classification with 600 double-coded papers, event studies, placebos, power statement, draft v1, AFA 2028 submission. Stage 2, March to June 2027: conference and citation outcomes, heterogeneity, journal linkage, draft v2 for journal submission. Stage 3, from mid-2027: 36- and 48-month publication updates (September 2027 and 2028), companion papers, replication package. Budget: LLM classification runs about US\$1--1.5k; research-assistant double coding about A\$6--8k; no data fees; about A\$8--10k for stage 1 and A\$18--25k in all.

# Appendix B. Open items before wider circulation

1.  Re-derive abstract coverage by year, separating Crossref from OpenAlex and by deposit type; an independent analysis of the January 2025 Crossref snapshot reports no abstracts in the Crossref metadata of SSRN preprints, which conflicts with the earlier tabulation. Report 2014--2018 coverage, which the classification needs most.
2.  Validate the OpenAlex SSRN series against SSRN's published statistics; explain the 2021--22 doubling of total SSRN postings (indexing or registration change versus production); add the 2023 and 2024 finance and accounting counts to (D).
3.  Test whether the Scopus APIs return SSRN preprints (20 known 2025 DOIs); ICSR Lab closed at the end of 2023 and is no longer a route. Consider a Dimensions no-cost research application as a fallback.
4.  Confirm citation details: the accounting submit-to-accept time in Hurley, Gal-Or, Knechel & Pesch (2025) (an earlier version reported about 23 months to 2019; "about two years" is used in this draft); the current version and sample of Walther & Dutordoir (2025); the figures in the Kusumegi et al. (2026) reply; the SSRN number of Arcila (2026); the article number of Renault et al. (2026); Barrick et al. (2025), now forthcoming in *Accounting Horizons*; the author list of Nee, Zhong & Ni (2026); volume and pages of Hao et al. (2026).
5.  Quantify journal-pipeline postings by quarter from metadata patterns; decide the exclusion rule.
6.  Run the power calculation from the 2014--2021 panel and fix the primary contrasts before estimation; register the analysis plan.

# References

::: {#refs}
Adão, R., Kolesár, M., & Morales, E. (2019). Shift-share designs: Theory and inference. *Quarterly Journal of Economics, 134*(4), 1949--2010.

Agrawal, A., & Goldfarb, A. (2008). Restructuring research: Communication costs and the democratization of university innovation. *American Economic Review, 98*(4), 1578--1590.

American Economic Association. (n.d.). *JEL classification system / EconLit subject descriptors*. <https://www.aeaweb.org/econlit/jelCodes.php>

Arcila, A. (2026). *Causal effects of generative AI adoption on scientific output: Quasi-experimental evidence of heterogeneous impacts across 26 disciplines* (Working paper). SSRN 6385141.

Barber, B. M., Jiang, W., Morse, A., Puri, M., Tookes, H., & Werner, I. M. (2021). What explains differences in finance research productivity during the pandemic? *Journal of Finance, 76*(4), 1655--1697.

Barrick, J. A., Summers, S. L., & Wood, D. A. (2025). *Accounting publication process: Are we making progress? What about GenAI?* (Working paper). SSRN 5546300.

Brodeur, A., Cook, N., & Heyes, A. (2020). Methods matter: p-hacking and publication bias in causal analysis in economics. *American Economic Review, 110*(11), 3634--3660.

Card, D., & DellaVigna, S. (2013). Nine facts about top journals in economics. *Journal of Economic Literature, 51*(1), 144--161.

Ciconte, W. A., Rozario, A. M., & Urcan, O. (2026). Using AI to identify exogenous shocks and conduct archival accounting research. *Review of Accounting Studies, 31*(3), 1638--1676.

Cohn, J. B., Liu, Z., & Wardlaw, M. I. (2022). Count (and count-like) data in finance. *Journal of Financial Economics, 146*(2), 529--551.

Correia, S., Guimarães, P., & Zylkin, T. (2020). Fast Poisson estimation with high-dimensional fixed effects. *Stata Journal, 20*(1), 95--115.

Coyne, J. G., Summers, S. L., Williams, B., & Wood, D. A. (2010). Accounting program research rankings by topical area and methodology. *Issues in Accounting Education, 25*(4), 631--654.

Cui, R., Ding, H., & Zhu, F. (2022). Gender inequality in research productivity during the COVID-19 pandemic. *Manufacturing & Service Operations Management, 24*(2), 707--726.

Ding, W. W., Levin, S. G., Stephan, P. E., & Winkler, A. E. (2010). The impact of information technology on academic scientists' productivity and collaboration patterns. *Management Science, 56*(9), 1439--1461.

Ellison, G. (2002). The slowdown of the economics publishing process. *Journal of Political Economy, 110*(5), 947--993.

Eloundou, T., Manning, S., Mishkin, P., & Rock, D. (2024). GPTs are GPTs: Labor market impact potential of LLMs. *Science, 384*(6702), 1306--1308.

Faff, R. W. (2024). *Pitching Research* (Version 19.0). SSRN 2462059.

Felten, E., Raj, M., & Seamans, R. (2021). Occupational, industry, and geographic exposure to artificial intelligence: A novel dataset and its potential uses. *Strategic Management Journal, 42*(12), 2195--2217.

Filimonovic, D., Rutzer, C., & Wunsch, C. (2025). *Can GenAI improve academic performance? Evidence from the social and behavioral sciences* (Working paper). arXiv 2510.02408.

Gardner, J., Krupa, N. R., & Mammadov, B. (2026). Generative artificial intelligence in the writing process of accounting research. *Accounting Open, 2*, 100010.

Gartenberg, C., Hasan, S., Murray, A., & Pierce, L. (2026). More versus better: Artificial intelligence, incentives, and the emerging crisis in peer review. *Organization Science, 37*(3), 795--812.

Hao, Q., Xu, F., Li, Y., & Evans, J. (2026). Artificial intelligence tools expand scientists' impact but contract science's focus. *Nature*.

Harvey, C. R. (2017). Presidential address: The scientific outlook in financial economics. *Journal of Finance, 72*(4), 1399--1440.

Harvey, C. R., Liu, Y., & Zhu, H. (2016). ... and the cross-section of expected returns. *Review of Financial Studies, 29*(1), 5--68.

Heckman, J. J., & Moktan, S. (2020). Publishing and promotion in economics: The tyranny of the top five. *Journal of Economic Literature, 58*(2), 419--470.

Hurley, P. J., Gal-Or, R., Knechel, W. R., & Pesch, H. L. (2025). Submit-to-accept times in accounting: Determinants and comparisons to other business disciplines. *The Accounting Review, 100*(2), 219--247.

Keloharju, M., & Keloharju, R. (2025). *Accounting research in the age of AI* (IFN Working Paper No. 1528). Research Institute of Industrial Economics.

Kerr, N. L. (1998). HARKing: Hypothesizing after the results are known. *Personality and Social Psychology Review, 2*(3), 196--217.

Kim, E. H., Morse, A., & Zingales, L. (2009). Are elite universities losing their competitive edge? *Journal of Financial Economics, 93*(3), 353--381.

Kobak, D., González-Márquez, R., Horvát, E.-Á., & Lause, J. (2025). Delving into LLM-assisted writing in biomedical publications through excess vocabulary. *Science Advances, 11*(27).

Korinek, A. (2023). Generative AI for economic research: Use cases and implications for economists. *Journal of Economic Literature, 61*(4), 1281--1317.

Kusumegi, K., Yang, X., Ginsparg, P., de Vaan, M., Stuart, T., & Yin, Y. (2025). Scientific production in the era of large language models. *Science, 390*(6779), 1240--1243.

Kusumegi, K., Yang, X., Ginsparg, P., de Vaan, M., Stuart, T., & Yin, Y. (2026). *A robust association between LLM use and scientific productivity: Assessing stopping-time selection* (Working paper). arXiv 2607.28968.

Lu, H., Luo, Y., & Yu, L. (2026). *How well do LLMs perform in peer review? Evidence from finance and accounting* (Working paper). SSRN 7607363.

Mitton, T. (2022). Methodological variation in empirical corporate finance. *Review of Financial Studies, 35*(2), 527--575.

Nee, X., Zhong, H., & Ni, X. (2026). *The generative AI gold rush in theoretical and computational research* (Working paper). arXiv 2609.04872.

Novy-Marx, R., & Velikov, M. (2026). Artificial intelligence--powered (finance) scholarship. *Journal of Economic Literature, 64*(1), 5--37.

Oler, D. K., Oler, M. J., & Skousen, C. J. (2010). Characterizing accounting research. *Accounting Horizons, 24*(4), 635--670.

Priem, J., Piwowar, H., & Orr, R. (2022). *OpenAlex: A fully-open index of scholarly works, authors, venues, institutions, and concepts* (Working paper). arXiv 2205.01833.

Rambachan, A., & Roth, J. (2023). A more credible approach to parallel trends. *Review of Economic Studies, 90*(5), 2555--2591.

Renault, T., Bergeaud, A., & Bosquet, C. (2026). Scientific production in the era of large language models: Outcome-triggered treatment timing and spurious event-study dynamics. *Proceedings of the National Academy of Sciences, 123*(33).

Romano, J. P., & Wolf, M. (2005). Stepwise multiple testing as formalized data snooping. *Econometrica, 73*(4), 1237--1282.

Stratopoulos, T. C., & Wang, V. X. (2025). Artificial intelligence and accounting research: A framework and agenda. *International Journal of Accounting Information Systems, 56*, 100760.

Walther, T., & Dutordoir, M. (2025). *Certainly! Generative AI and its influence on academic writing (in finance)* (Working paper). SSRN 5317993.
:::
