# Review 6: Field norms and editorial judgement (finance and accounting)

**Pitch reviewed:** "Generative AI and the Productivity of Finance and Accounting Scholars" (Faff template, 23 October 2026). **Review date:** 30 October 2026.

**Verification note.** Citations were checked by web search; SSRN, arXiv, AEA, AAA, Wiley, DOI and several university hosts were unreachable, so some checks rest on secondary listings (RePEc, Springer, press releases, faculty pages). Tags: [V] verified; [V-p] partly verified; [M] from memory; [U] could not verify.

## 1. Verdict

**Fit with finance: 6/10. Fit with accounting: 4/10** (5/10 for CAR or Accounting Horizons; 3/10 for JAR).

The pitch is a well-built applied-micro design: a Bartik-style exposure (pre-ChatGPT method shares) interacted with release dates, estimated by Poisson PML with field-by-quarter effects, and it correctly neutralises the Renault et al. critique of outcome-triggered adoption dating. That is its main asset. Its liabilities are field-norm problems rather than econometric ones. SSRN is a near-census of finance working papers but a selected, stage-dependent window on accounting output. The headline question ("how much does AI raise output") is not what the design identifies ("which methods gain relative to others"), a mismatch conceded only in section K. The 24-month ABDC A*/A publication window is not a quality measure either field's editors would accept, and in finance it is contaminated by fast ABDC-A outlets. The "business schools count papers" premise describes ABDC/ABS regimes, not the US top-journal regime the target editors live in. Realistically this is a Management Science (cross-field) paper, or a JFE/Review of Finance/JFQA paper if finance-led; JF and JAR are not credible first targets. Most citations check out; three numbers need correcting.

## 2. The finance editor's view (JF / RFS / Management Science, Finance)

**Desk review.** The editor files this with Barber et al. (2021, JF) and Kim, Morse & Zingales (2009, JFE): "finance about finance" papers that JF/JFE publish occasionally, usually when an AFA-connected team delivers a profession-wide fact. Reaction: competent and timely, but the identified object is a within-field relative effect, the quality test is weak, and the hook ("AI raises finance output by X%") is exactly the number the design cannot produce. At JF, a desk reject with an encouraging note; at Management Science, even odds of reaching referees, with the editor asking whether Accounting or Organizations is the better department.

**First-round referee demands.** (1) Event-study plots by method as the main specification, with flat 2018–2022 coefficients. (2) A method-specific outcome: papers *of* method m, not papers *by* scholars whose past mix was m. (3) Evidence that pre-period method mix is not proxying for subfield fashions (machine-learning asset pricing, climate finance, crypto) that boomed after 2022. (4) A quality measure the field recognises: AFA/WFA/EFA/SFS Cavalcade acceptance, citations, long-window top-3 publication. (5) Quantification of the Elsevier submission-to-SSRN pipeline. (6) Randomisation inference over placebo dates, given only about 15 post quarters of method-level variation.

**Major issues, ranked.**

**F1. The headline promises a total effect that the design identifies away.** Quote: "This project asks how much generative AI raises the output of finance and accounting scholars" (Summary) against "The design identifies differences between methods, not the total effect of AI" (K). Why it matters: the editor reads the summary expecting the total, finds in K that the paper cannot deliver it, and discounts the contribution. Fix: re-headline around "which research methods generative AI speeds up, and when" (the H2 timing test is the genuinely new result), or add a level design using OpenAlex subfields with low measured AI exposure, or SSRN networks outside finance/accounting, as a control for the field-by-quarter effects. Say in the summary which the paper delivers.

**F2. The quality test is unusable in finance as specified.** Quote: "I compare the share published in an ABDC A*/A or FT50 journal within 24 months of posting" (G). Why it matters: finance cycles are multi-year. The JF reports a median first-round turnaround of 43 days and a 43% desk-rejection rate for 2023 [V, editor report], but acceptance at JF/JFE/RFS typically takes two to four years over several rounds, often after rejection elsewhere [M]. A 24-month window captures the fast tail, which in finance is dominated by quick ABDC-A outlets (Finance Research Letters is ABDC A and publishes within weeks [M]), so the measure is contaminated by the very outlets that absorb low-quality volume. ABDC carries no weight with US editors. Fix: make conference acceptance (AFA, WFA, EFA, SFS Cavalcade, FIRS programs are public and timely) and 24-month OpenAlex citations the primary timely signals; report top-3 eventual publication with the 36/48-month updates; treat "published in a fast outlet" as a destination outcome, not as quality. Cite the finance AI-referee papers the pitch misses, Newton & Riddiough (2026, SSRN 6446183) and Subrahmanyam (2026, SSRN 6451699) [V, listings].

**F3. The posting-rate control cannot be measured where it matters, and the journal pipeline is bigger than a flag.** Quote: "I measure this posting rate directly, as the share of each field's and method's journal articles that also appear on SSRN, by year" (E). Why it matters: articles published in 2024–2026 were mostly written in 2020–2023; the posting rate for post-period cohorts is unobservable until about 2029, and for recent cohorts it is computed only on papers published fast, which is selection on the outcome. Separately, Elsevier's submission-time preprint posting to SSRN (JBF, JCF, JFM, FRL and others) [M] mechanically adds SSRN papers for exactly the empirical, mid-tier work H1 predicts will grow. Fix: measure posting propensity in real time from conference programs (share of accepted papers with an SSRN version within a quarter) and parallel platforms (NBER, CEPR, arXiv q-fin); quantify journal-pipeline postings by quarter and show results excluding them.

**F4. Release dates are contestable, especially "coding = July 2023".** Quote: "coding (ChatGPT Code Interpreter, July 2023; agentic tools such as Claude Code, February to May 2025)" (Table 2). Why it matters: GitHub Copilot was generally available from June 2022 and ChatGPT wrote Stata and Python from November 2022 [M]; a referee who codes will say the writing/coding distinction collapses in 2023, which Risk 3 half-concedes. Fix: let the quarterly event-study by method date the responses ex post, or build a capability index per task from public benchmarks. Keep the H2 reasoning-model test, the sharpest timing prediction.

**F5. The outcome must be classified by method, not only the scholar.** Quote: "classify each scholar's pre-ChatGPT papers by research area and method" (Summary). Why it matters: as written, the design says which *scholars* (by past mix) post more, not which *papers* (by method) are produced; a theorist who starts posting empirical papers reads as "theory gains". Fix: classify all 2018–2026 papers and estimate a scholar-by-method-by-quarter panel; the own-method versus cross-method split (acceleration versus substitution) is itself a result.

**F6. The method taxonomy omits the finance methods most exposed to AI.** Quote: "Method: analytical (theory); archival, by data source ...; experimental; other" (Table 1). Why it matters: finance's natural split is theory / reduced-form empirical / structural / machine-learning and text methods / experiments; "papers using LLMs as a research method are handled separately" (G) removes a fast-growing category central to the question, and structural or hybrid papers have no home. Fix: add "structural or quantitative theory", "ML or LLM as method" and "methodological/econometric"; report results with LLM-method papers included and excluded.

**F7. Selection on 2018–2021 activity invites mean reversion.** Quote: "Academic authors with at least two finance or accounting SSRN papers in 2018–2021 (selected on pre-period activity only)" (F). Why it matters: conditioning on a high pre-period draws in scholars whose output will regress, and if method mix correlates with pre-period intensity the interaction absorbs it. Fix: eligibility on 2015–2017 as a robustness sample; report the balanced panel.

## 3. The accounting editor's view (JAR / TAR / RAST)

**Desk review.** JAR would desk-reject: it rarely publishes research on the research process, and half the paper is finance. TAR and RAST would hesitate over the output measure. Accounting editors do not regard SSRN as a census of accounting production: posting is uneven across subfields and career stages, often tied to conference acceptance or the R&R stage, and historically more common in financial accounting (Brown 2003, Review of Quantitative Finance and Accounting 20(3) [V, RePEc listing]). The pitch's own number, OpenAlex links "only 15–72% of articles in six top journals to their SSRN versions", reads as evidence that the posting margin is large and heterogeneous. Whether any top accounting journal ever formally discouraged prior circulation I could not confirm (TAR's current policy bars only manuscripts under review elsewhere [V-p]; JAR's page was unreachable; the rest is folklore [M]); document the policies in a data appendix rather than assert either way. The editor would also note that the accounting literature cited is thin and recent, and that "inflation" is not the field's vocabulary.

**First-round referee demands.** (1) Direct evidence on posting selection: share of TAR/JAR/JAE/CAR/RAST/AOS articles with a prior SSRN version, by year and method, back to 2010. (2) Posting-stage measurement: is the first SSRN version an early draft or a conference/R&R-stage paper? (3) Quality against the top-6 and FARS/AAA/JAR-conference programs, not ABDC. (4) A rule separating "archival text" from "LLM as method". (5) Aggregated reporting of scholar-level AI-use measures, for identifiability as much as HREC.

**Major issues, ranked.**

**A1. SSRN is a stage-dependent window on accounting output, and AI may move the stage.** Quote: "Expected number of new SSRN working papers posted by scholar i in quarter t" (Table 2). Why it matters: if accounting scholars post later in a paper's life than finance scholars [M; consistent with the 15–72% range], SSRN counts lag production by a year or more, blurring release timing; and if cheaper drafting leads scholars to post earlier drafts, SSRN output rises with no change in production while the posting-to-publication gap lengthens mechanically, which the quality test would read as inflation. Fix: use Crossref/OpenAlex version metadata to measure versions per paper and the gap between first posting and conference appearance; test whether that gap shifts after 2022 by method; show main estimates on first versions and conference-dated papers.

**A2. The review-time number is unverified, and the 24-month window fails in the other direction.** Quote: "Accounting journals already averaged about 26 months from submission to acceptance (Hurley et al. 2025), so this share measures speed" (G). Why it matters: Hurley, Gal-Or, Knechel & Pesch (2025, TAR 100(2), 219–247) is real and the author order is right [V]; the earlier working paper reported accounting submit-to-accept rising from about 18 to about 23 months after 2008 (data to 2019) [V-p]; the published version runs to 2021 and I could not confirm "about 26 months" [U]. Whatever the figure, if submit-to-accept alone is about two years, "published in a top-6 journal within 24 months of SSRN posting" is near zero for early-posted papers and positive mainly for papers posted at R&R stage, so the measure captures posting stage, not quality; the within-cohort method gap does not rescue it. Fix: cite the exact table; drop the 24-month share for accounting; use FARS/AAA/JAR/RAST/CAR conference acceptance, citations and the 48-month top-6 outcome; add the companion paper on tenure consequences of submit-to-accept delays (Accounting Horizons, 2026 [V, listing]) to the "So what".

**A3. The taxonomy is recognisable but the extension is not Coyne et al.'s.** Quote: "archival, by data source (standard databases, text, hand-collected records) ... Source: Coyne et al. (2010); Oler et al. (2010)" (Table 1). Why it matters: BYU's methods are analytical, archival, experimental and other; the data-source split is the author's, and referees will object to the attribution. More substantively, text-based archival work is where LLMs are both tool and method; without a coding rule, "archival with text" in H1 and the excluded "LLM-as-method" papers overlap. Fix: label the split as the project's extension; publish the rule (an LLM used to build a variable is archival-text; a paper whose contribution is the pipeline is LLM-method) and report inter-coder agreement on that boundary. Experimentalists will also ask that "experimental" distinguish lab, online-panel and field experiments, since online panels are cheap and not insulated from AI (H3).

**A4. The "business schools count papers" premise is an ABDC/ABS premise.** Quote: "Business schools count papers, often against journal lists" (I). Why it matters: US top-school accounting and finance departments count top-6/top-3 publications, not papers [M; cf. Heckman & Moktan 2020 for economics]; a JAR or JF editor finds the premise foreign, while Australian, UK, European and Asian readers recognise it at once. Fix: make it the paper's best heterogeneity test rather than its premise: classify institutions by evaluation regime (list-counting versus top-journal) and show whether the output response and the quality gap concentrate under count-based regimes. That result travels to both audiences and speaks to the incentives mechanism in Gartenberg et al.

## 4. Shared issues

**Classification.** JEL G1–G5 omit G0 and all non-G finance (E4/E5 macro-finance, C58 financial econometrics, K22, Q54 climate, O33 fintech); G4 and G5 are real headings [V] but overlap heavily with G1/G3; fintech and crypto straddle G1, G2 and O3. The area dimension is secondary, so this is "fix later", but report a "G0/other/non-G" bucket. The accounting method taxonomy works for finance's theory-versus-empirical split but loses finance-specific methods (F6); and because finance barely varies on experimental, survey and review methods, H1 and H3 are in practice accounting-identified. Say so.

**Measurement.** The OpenAlex series needs external validation: "SSRN postings doubled from 2021 to 2022" (E) is a pre-ChatGPT jump that looks like an indexing or Crossref-registration change, not production; compare with SSRN's own statistics before any figure uses the series. OpenAlex "Finance" and "Accounting" are algorithmic topic labels, not SSRN network membership [M]. The 2025 abstract gap (17–34%) sits exactly on the reasoning and agentic releases, so the Scopus/ICSR route is necessary. SSRN's AI-disclosure policy update of August 2026 [V, Elsevier support page] is a screening change inside the sample window.

**Framing.** "Inflation" reads as monetary to finance editors and as pejorative to accounting editors; "more versus better" (Gartenberg et al.) is the available neutral phrase. Pair causal language ("the estimates show which methods each release speeds up") with the identifying assumption: parallel trends across pre-period method mixes within field.

**Citation check.**

| Citation in pitch | Status |
|---|---|
| Novy-Marx & Velikov 2026, JEL 64(1), 5–37 | [V] correct; description accurate |
| Kusumegi et al. 2025, Science 390(6779) | [V] correct; SSRN +59.8% confirmed (arXiv 36.2%, bioRxiv 52.9%) |
| Renault et al. 2026; Kusumegi et al. 2026 reply | [V-p] arXiv 2605.17979 and 2607.28968 exist; PNAS 123(33) unconfirmed; the reply's "no estimate is causal" confirmed, its "7–20%" [U] |
| Gartenberg et al. 2026, Org. Sci. 37(3), 795–812 | [V] correct; +42%; Pangram |
| Walther & Dutordoir 2025, SSRN 5317993 | [V-p] authors and findings correct; earlier versions report 41,489 articles and title "Impact"; 55,964 unconfirmed |
| Lu, Luo & Yu 2026, SSRN 7607363 | [V] posted 13 Oct 2026; one-SD higher LLM score raises publication probability 44%, net of author reputation |
| Nee, Zhong & Ni 2026, arXiv 2609.04872 | [V-p] paper and mathematics surge (+33.5% on 2025) confirmed; authors unconfirmed; reasoning-model attribution is the pitch's reading |
| Hurley et al. 2025, TAR 100(2), 219–247 | [V] venue and author order; "about 26 months" [U] (earlier version: about 23 months by 2019) |
| Ciconte, Rozario & Urcan 2026, RAST 31(3), 1638–1676 | [V] correct; description accurate |
| Barrick, Summers & Wood 2025, SSRN 5546300 | [V] correct (>1,100 respondents; "nearly two-thirds"); now forthcoming in Accounting Horizons as "Back to the Future ..." |
| Gardner, Krupa & Mammadov 2026, Accounting Open | [V] exists; 13-word list and junior-author finding [U] |
| Keloharju & Keloharju 2025, IFN WP 1528 | [V] correct; accurately used |
| Arcila 2026, SSRN 6385141 | [U] not locatable by title, author or number |

## 5. Desk-reject risk and positioning

| Target | Desk-reject risk | Why | What it would need |
|---|---|---|---|
| Management Science (Finance) | about 55% | MS does publish research on the academy (cf. "Institutional Ties and Publications in Top Accounting Journals", 10.1287/mnsc.2024.04553 [V, title]); Finance is the wrong department | Submit cross-field; lead with the event-study figure and regime heterogeneity; fix F1–F3, A1–A2 |
| Journal of Finance | 85–90% | No profession-wide causal number; relative effects by method are not general-interest; the Barber et al. precedent was AFA-commissioned | A level design (F1) plus conference-based quality evidence; even then JFE, Review of Finance or JFQA are the realistic homes |
| Journal of Accounting Research | above 90% | Meta-research is outside JAR's remit; SSRN measurement in accounting is contested; half the paper is finance | An accounting-only companion with posting-selection modelling and top-6/conference outcomes, for CAR, Accounting Horizons, European Accounting Review or Accounting Open |

**Positioning: finance-led, with accounting as the method-heterogeneity comparison; cross-field only for Management Science.** SSRN is the finance profession's working-paper medium, so output is measured where it is credible; finance has the cleanest theory-versus-empirical split with enough scholars in each cell, timely public quality signals (conference programs) and an annual editor-report series; accounting contributes the experimental/survey contrast (H3) and the evaluation-regime test (A4) but carries the posting-selection liability. Path: Management Science first; then JFE or Review of Finance, with a parallel accounting paper for CAR or Accounting Horizons. For an Australian audience, Accounting & Finance or the Australian Journal of Management would take the ABDC-regime heterogeneity as a stand-alone contribution [M].

## 6. What works and should be kept

- Treatment defined from pre-ChatGPT method shares, which neutralises the Renault critique, and AI-word measures treated as a first stage, not the treatment.
- Poisson PML with scholar, career-stage and field-by-quarter effects; Table 2 is unusually clear for a pitch.
- H2 as a sharp, falsifiable timing prediction. The figure that would carry the paper for a finance editor: quarterly event-study coefficients with flat pre-trends, empirical-method divergence in 2023 and a theory jump only from late 2024/2025, overlaid with the first-stage AI-word share. For an accounting editor: archival-standard-database output rising against flat experimental output, split by evaluation regime, with FARS/AAA acceptance rates of the marginal papers.
- The HARKing framing from Novy-Marx & Velikov and Ciconte et al., which gives H1 a mechanism.
- Data ethics and feasibility: no scraping, OpenAlex/Crossref routes, licensed abstracts, HREC awareness, conference matching, the 2027/2028 updates.
- Candid risks and limitations (Risks 3–6 and "Limitations stated upfront").

## 7. Must fix before circulating to coauthors vs fix later

**Must fix now**
1. Re-align the headline with what is identified, or add a level design (F1).
2. Replace the 24-month ABDC A*/A test with conference acceptance, citations and long-window top-3/top-6 publication; treat fast-outlet publication as a destination outcome (F2, A2).
3. Redesign the posting-rate control around conference programs and parallel platforms, quantify journal-pipeline postings (F3), and add the posting-stage analysis for accounting (A1).
4. Classify all 2018–2026 papers by method and estimate scholar-by-method-by-quarter (F5).
5. Correct or confirm: Hurley et al. "26 months"; Walther & Dutordoir sample and title; the Arcila handle; Renault et al. PNAS details; Barrick et al. as Accounting Horizons 2026; Nee et al. authorship and attribution.
6. Validate the OpenAlex SSRN series against SSRN's own counts before any figure uses it.
7. Add the finance AI-referee literature and fix the Coyne et al. attribution (A3).

**Fix later**
- Extend finance areas (G0, non-G, fintech, climate) and methods (structural, ML/LLM-as-method, econometric) (F6).
- Convert release dummies to capability indices or ex-post event-study timing (F4).
- Eligibility on 2015–2017 output; randomisation inference over placebo dates (F7).
- Evaluation-regime heterogeneity as a headline test (A4).
- Replace "inflation" with "more versus better"; aggregate scholar-level AI-use reporting; document journals' prior-circulation policies; split "experimental" into lab, online and field; coauthor-network exposure.
