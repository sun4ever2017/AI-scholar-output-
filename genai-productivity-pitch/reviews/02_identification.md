# Review 02 — Research design, identification and econometrics

**Pitch reviewed:** "Generative AI and the Productivity of Finance and Accounting Scholars" (Faff template, 23 October 2026). **Lens:** applied microeconometrics. [verified] marks claims checked on the web on 30 October 2026; [memory] marks claims not checked.

## 1. Verdict

**Score: 5/10** on design, identification and econometrics.

The pitch makes the right first move: exposure (the pre-ChatGPT method mix) is predetermined and treatment timing is a calendar date, so it genuinely escapes the outcome-triggered-timing problem that Renault, Bergeaud and Bosquet raise against Kusumegi et al. [verified]. But as written the design cannot answer its own headline question: because method shares sum to one, every release step is collinear with the field × quarter effects, so only differences between methods are identified, which Section K admits but Table 2 denies. The writing/coding/reasoning steps are a calendar partition with task labels attached; the labels do not survive the actual release history, and three nested steps in about fifteen post-quarters cannot be attributed to capability types. The sample is selected on activity in the same 2018–2021 window that supplies both the exposure measure and most of the pre-trend period, and that window contains COVID, which hit experimental and archival work asymmetrically. The "first stage/Wald ratio" satisfies no exclusion restriction, and the posting-rate control is a function of the outcome. The fixes below leave a coherent design, but the pitch should be re-framed before coauthors are recruited on the promise of "how much does AI raise output".

## 2. Major issues, ranked by severity

### Issue 1. The headline estimand is not identified; Table 2 contradicts Section K

**(a)** Section B: "How much does generative AI raise the research output…". Table 2 labels β_km "Productivity due to AI" under "Part of output growth", and the next paragraph says that summing β_km × Share_im and averaging within a group "gives the AI part of that group's output growth". Section K concedes the opposite.

**(b)** With Σ_m Share_im = 1, Σ_m Release_k(t) × Share_im = Release_k(t) for every scholar: a field-level time dummy that τ_f(i),t absorbs. One method per release must be dropped; β_km is then relative to the reference method, and Σ_m β_km Share_im is a scholar's effect relative to a hypothetical all-reference-method scholar, not "the AI part" of anything. This is the complete-shares result of Goldsmith-Pinkham, Sorkin & Swift (2020) and Borusyak, Hull & Jaravel (2022): the level is identified only with incomplete shares or an unexposed group [memory], and there is none, since everyone has had ChatGPT since 30 November 2022. With one common shift, the design is a continuous-dose difference-in-differences (dose = share vector), and Callaway, Goodman-Bacon & Sant'Anna (2024) show the TWFE dose × post coefficient has a causal reading only under *strong* parallel trends: scholars at different doses would have followed the same path at any given dose [memory]. That is far stronger than "flat pre-trends", and method-specific topic shocks (Risk 4) violate exactly it.

**(c)** Fix. (i) Re-frame B as "Which research methods does generative AI speed up, and by how much relative to the least-exposed methods?" (ii) If a level is wanted, state an anchor assumption and defend it, e.g. "experimental, field and hand-collected archival work receive no effect through 2024" (consistent with H3), make it the reference, and report the level "relative to the anchor" with sensitivity bands for anchor effects of ±10 and ±25 percent. (iii) Add a one-dimensional dose, Exposure_i = Σ_m Share_im · E_m, with E_m a task-based score from Eloundou et al. (2024), estimated in exposure quartiles × quarter. (iv) Rewrite Table 2's last column so β carries no level interpretation and delete the "AI part" sentence.

### Issue 2. The release calendar is wrong in detail, and nested steps cannot attribute effects to capability types

**(a)** Table 2, Release_k(t): "writing (ChatGPT, November 2022); coding (ChatGPT Code Interpreter, July 2023; agentic tools such as Claude Code, February to May 2025); reasoning (from late 2024; dates to be confirmed)"; Risk 3.

**(b)** ChatGPT wrote Stata, R and Python from launch on 30 November 2022 [memory]; GitHub Copilot was generally available in June 2022, before ChatGPT [memory]; GPT-4 (14 March 2023) was the largest single jump in both writing and coding [memory]; Code Interpreter rolled out from 6 July 2023 [verified] but is a sandboxed execution feature, not the arrival of coding; o1-preview was out by mid-September 2024 (in GitHub Copilot on 19 September 2024 [verified]), o1 in December 2024 and the free DeepSeek-R1 in January 2025 [memory]; Claude Code was announced on 24 February 2025 [verified]. "Writing" and "coding" cannot be separated by date, and "reasoning" (2024Q4) and "agentic coding" (2025Q1) are one or two quarters apart. With nested steps, β_km is simply the change in method m's *relative* output between adjacent windows: W1 = 2022Q4–2023Q2, W2 = 2023Q3–2024Q3, W3 = 2024Q4–2025Q1, W4 = 2025Q2–2026Q3. Given a 6–18-month lag from idea to posting, W1 will show little and W2 will absorb the delayed ChatGPT/GPT-4 effect. Nee, Zhong & Ni (2026) date the mathematics surge to 2026 (33.5 percent above 2025, 11.9 percent above a synthetic counterfactual) and call it "consistent with delayed diffusion and capability threshold mechanisms", not a reasoning-model effect [verified].

**(c)** Fix. Replace the steps with a flexible event study by method and pre-registered reporting windows: δ_{m,s} on 1[t = s] × Share_im for every half-year s relative to 2019, estimated jointly, with W1–W4 averages reported under calendar labels ("2023H1"), not task labels. Secondary: interact shares with a continuous capability or diffusion index (SWE-bench, AIME/FrontierMath, ChatGPT weekly users). Capability labels become hypotheses tested through timing and output composition, not identifying assumptions.

### Issue 3. Selection on 2018–2021 activity contaminates the pre-trend test and the exposure measure; COVID compounds it

**(a)** Section F: "at least two finance or accounting SSRN papers in 2018–2021 (selected on pre-period activity only)"; Section G: "flat 2018–2022 pre-trends as the core check".

**(b)** (i) Conditioning on ≥2 papers in 2018–2021 mechanically elevates output in that window and produces mean reversion afterwards; the reversion is method-specific if methods differ in posting frequency, since an experimentalist who clears the bar is further above her own mean than an archival scholar who clears it. The "flat 2018–2022 pre-trend" is computed inside the selection window, so it is partly an artefact; the only clean pre-quarters are 2022Q1–Q3. (ii) 2020–2021 is COVID. Labs and field sites closed, so experimental shares are under-measured and the delayed papers arrive in 2022–2024 as a rebound that looks like a treatment effect. Barber et al. (2021 JF) is a survey of 1,440 AFA members on self-reported productivity and says nothing about SSRN counts [verified]; Cui, Ding & Zhu (2022 MSOM) show total SSRN output rose about 35 percent in the ten weeks after the US lockdown [verified], a largely archival, topical boom followed by reversion. (iii) Conditioning on a passed, low-power pre-test biases post-period estimates (Roth 2022) [memory].

**(c)** Fix. Separate the three windows: select on activity in 2012–2017 (≥2 SSRN papers), measure shares on 2015–2019 (2018–2021 as robustness) and keep 2018Q1–2022Q3 as a clean pre-period with 2019 as reference and 2020–2021 shown separately by method. Report the power of the pre-test against a trend large enough to overturn H1 (Roth 2022) and Rambachan & Roth (2023) robust confidence sets under relative-magnitude restrictions (M̄ = 0.5, 1, 2).

### Issue 4. Shares are coarse, mis-measured and collinear with research area

**(a)** Threshold "at least two"; "multi-method papers split equally"; LLM classification from title and abstract.

**(b)** For two-paper scholars shares take values {0, 0.5, 1}; the observed share is a binomial draw around a true propensity, so error is non-classical, attenuates β and adds spurious cross-sectional variation; classifier error compounds it. Within field × quarter, method shares co-move with area (accounting is predominantly archival, experimental work sits in auditing and managerial, analytical work in G1/G3 and financial accounting), so β_km loads any area-specific post-2022 shock (AI as a topic, crypto, banking stress). Risk 4 names this, but "pre-trends and placebo dates" cannot catch shocks that begin after 2022.

**(c)** Fix. (i) Main sample ≥4 papers in the share window, robustness at ≥2 and ≥6. (ii) Split-sample IV for measurement error: instrument shares from 2015–2017 papers with shares from 2018–2019 papers. (iii) Area × quarter fixed effects (JEL G1–G5; BYU accounting areas) plus the scholar's pre-period AI/ML-topic share × quarter. (iv) Report the classifier's confusion matrix on the 300 hand-coded papers and an errors-in-variables correction using it.

### Issue 5. The "first stage/Wald ratio" is not a valid IV, and the posting-rate control is a function of the outcome

**(a)** Section E: "dividing a release's output effect by the rise in AI use it brings (a Wald ratio) gives the output gain per unit of AI use." Sections E/F: the SSRN posting-rate control.

**(b)** A Wald ratio is an IV estimate whose exclusion restriction requires Release × Share to affect output only through the vocabulary share. The pitch itself says the vocabulary captures only AI-assisted writing, so the restriction fails by construction, including in 2023H1 (ChatGPT also coded). The vocabulary share is computed on posted abstracts, a selected sample of the outcome with the outcome in its denominator. The posting-rate control is unobservable for recent cohorts until their papers are published, stale when measured by publication year, and has SSRN postings in its numerator: a post-treatment function of the outcome, a textbook bad control (Angrist & Pischke 2009, §3.2.3) [memory].

**(c)** Fix. Present AI vocabulary as a descriptive mechanism check, and delete "first stage" and "Wald ratio". If an instrument is wanted, use access shocks external to the scholar: country-level ChatGPT availability (mainland China, Russia, Iran; Italy's four-week ban in April 2023 as a placebo) [memory], interacted with shares. For posting propensity, use the conference programs already in the data plan (AFA, WFA, EFA, SFS Cavalcade, AAA) as a non-SSRN sampling frame: the share of program papers with an SSRN version is observable in real time and independent of SSRN counts.

### Issue 6. Inference is clustered at the wrong level; many cells; no pre-registration plan

**(a)** Section G: "standard errors clustered by scholar (two-way by scholar and institution as robustness)"; k × m cells; H1–H4.

**(b)** Treatment varies at method-share × calendar time, and the shocks are three or four common dates. Adão, Kolesár & Morales (2019) show that in share-based designs residuals are correlated across units with similar shares and unit-level clustering can understate standard errors severalfold [memory]. With about seven method groups, cluster-at-method asymptotics are unavailable, and 20–28 β_km plus H4 interactions multiply false positives.

**(c)** Fix. (i) Exposure-robust (AKM) standard errors alongside scholar clusters. (ii) Randomisation inference: re-estimate each window coefficient at every placebo release quarter in 2015–2021 and under 1,000 permutations of shares across scholars within field × area. (iii) Pre-register four or five primary contrasts (standard-database archival vs anchor in W2; analytical vs archival in W3/W4; review vs all in W1) with Romano–Wolf step-down for the rest. (iv) Hold out a random 30 percent of scholars for confirmation, since the data are in hand.

### Issue 7. The publication ("inflation") test has little power and a circular quality proxy

**(a)** Section G: "share published in an ABDC A*/A or FT50 journal within 24 months"; "AI referee scores (validated against later top-three publication by Lu, Luo & Yu 2026)".

**(b)** Hurley et al. (2025 TAR) show accounting submit-to-accept times lengthened significantly over 1993–2021 [verified; the 26-month figure could not be checked because both host sites are outside this session's network]. If the mean is about two years, publication within 24 months of *posting* in an A*/A or FT50 journal is a low base rate dominated by fast journals (JFE, RFS, Management Science): it measures speed and destination, not quality. Within-cohort method gaps are confounded by journal-specific congestion because journals are method-specific. An LLM referee scoring LLM-assisted papers inherits self-preference bias (Panickssery, Bowman & Feng 2024) [memory].

**(c)** Fix. A discrete-time hazard of publication with right-censoring, stratified by destination journal, with journal turnaround from editor reports as a time-varying covariate. Make conference acceptance (6–12-month horizon) and 24-month citations the primary near-term quality outcomes. Keep AI referee scores only after testing on pre-2022 papers whether the score correlates with AI-style vocabulary.

### Issue 8. Panel mechanics: disambiguation, attrition, age–period–cohort, zero-heavy quarters

**(a)** Section F: "OpenAlex … author identifiers, ORCID (on 92% of 2024 SSRN works)"; Table 2: λ_a(i,t); "scholar-quarter panel".

**(b)** OpenAlex author IDs split and merge, especially for common surnames, and the 2023 re-disambiguation changed IDs [memory]; ORCID coverage on 2018–2021 SSRN works is far below 92 percent; errors correlate with name origin and hence with area and method. A balanced 2018–2026 panel contains retirees and PhD students who left for industry; their zeros bias β by method. Career age equals calendar time minus entry year, so λ_a is collinear with α_i + τ_t unless coarsely binned, and the pitch does not say how. Quarterly counts are mostly zeros; PPML copes (Correia, Guimarães & Zylkin 2020) [memory], but quarterly event-study coefficients will be noisy.

**(c)** Fix. Build the author key from Crossref SSRN records plus ORCID and name–institution matching, validate on 200 hand-checked authors, and re-run on the ORCID-linked subsample. Define an "active" indicator (any work on any platform in a rolling three-year window), report exit rates by method, and estimate unconditional and active-conditional effects. Use five-year career-age bins and a half-year event study.

### Proposed specification and first-draft figures

E[Y_it] = exp( α_i + τ_{f(i),t} + θ_{a(i),t} + λ_{c(i,t)} + Σ_{m≠m0} Σ_{s≠2019} δ_{m,s} · 1[t = s] · Share_im )

where f is field, a is area (JEL G1–G5 or BYU accounting area), c is a five-year career-age bin, Share_im is measured on 2015–2019 for scholars selected on 2012–2017 activity with ≥4 papers, and m0 is the stated anchor (experimental/field/hand-collected). Report W1–W4 window averages, exposure-robust SEs, randomisation p-values and Rambachan–Roth sets. Companion: a paper-level model Y_imt with scholar × quarter fixed effects and method × window effects, with the caveat that post-2022 method is endogenous.

Figure 1. Raw mean quarterly SSRN papers per scholar by pre-period method group (pure standard-database archival, pure analytical, pure experimental/field, review/commentary, mixed), 2015Q1–2026Q3, normalised to 2019 = 1 on a log scale, with vertical lines at 2022Q4, 2023Q1, 2024Q3 and 2025Q1.

Figure 2. Event-study δ_{m,s} by method, one panel per method, half-yearly, relative to m0 and 2019, with exposure-robust intervals and Rambachan–Roth bands for M̄ = 1, pre-period 2015–2022H1 displayed.

Figure 3. Randomisation inference: the distribution of the W2 archival-vs-anchor and W4 analytical-vs-anchor coefficients under 1,000 share permutations and at every placebo release quarter 2015–2021, actual estimates marked.

## 3. Minor issues

- Renault, Bergeaud & Bosquet is cited as PNAS 123(33); the version I could verify is arXiv comment 2605.17979 (May 2026) [verified].
- Kusumegi et al.'s SSRN-specific +59.8% could not be confirmed; the published range is 23.7–89.3% [verified].
- "each coefficient reads approximately as a percentage change" holds only for small β; report exp(β) − 1.
- Linearity in shares inside the exponent imposes a geometric-mean restriction on mixed-method scholars; the paper-level model relaxes it.
- Crossref abstract coverage of 17–34 percent in 2025 falls exactly in the reasoning/agentic windows; show coverage by method.
- Specify whether AI-topic and LLM-method papers are excluded from the outcome or a separate outcome; they are the most obvious method-correlated topic shock.

## 4. What works and should be kept

- Predetermined exposure plus calendar-dated treatment sidesteps outcome-triggered timing, and the pitch explains why a scholar's own AI words would reintroduce it.
- A fixed panel of pre-existing posters neutralises SSRN's extensive-margin growth; the pitch is candid about SSRN's 2021–2022 doubling.
- PPML with high-dimensional fixed effects for a count outcome (Cohn, Liu & Wardlaw 2022) [verified].
- Field × quarter effects, placebo dates, any-platform outcome, fractional counts.
- H2 is a sharp, falsifiable timing prediction; keep it as a primary contrast.
- "Limitations stated upfront" is honest; it just needs to govern Table 2 and Section B.

## 5. Must fix before circulating to coauthors vs fix later

**Must fix before circulating**

1. Re-frame Section B and Table 2 to the relative (method-gradient) estimand; delete the "AI part of total growth" claim or state and defend an anchor (Issue 1).
2. Replace the three labelled steps with a method-specific event study and pre-specified calendar windows; correct the release calendar (Issue 2).
3. Decouple the selection window, the share window and the pre-period; move share measurement before COVID (Issue 3).
4. Remove the "first stage/Wald ratio" framing; redefine posting propensity from conference programs (Issue 5).
5. State the inference plan (exposure-robust SEs, randomisation inference) and the pre-registered primary contrasts (Issue 6).

**Fix later**

- Share-threshold robustness, split-sample IV, area × quarter effects (Issue 4).
- Hazard-model publication analysis and AI-referee-score de-biasing (Issue 7).
- Disambiguation validation, attrition handling, career-age bins (Issue 8).
- The continuous capability/dose index as a secondary specification.

## Fact-check log

Verified (web, 30 Oct 2026): Code Interpreter 6 July 2023; Claude Code 24 February 2025; o1-preview in Copilot by 19 September 2024; Renault–Bergeaud–Bosquet (arXiv 2605.17979) and its placebos; Kusumegi et al. 23.7–89.3%; Hurley et al. and Barber et al. (scope, findings); Cui, Ding & Zhu +35%; Cohn, Liu & Wardlaw; Nee, Zhong & Ni. From memory: other release dates, Italy's ban, OpenAlex disambiguation, and the econometric results cited.

## References proposed for the revision

Adão, R., Kolesár, M., & Morales, E. (2019). Shift-share designs: Theory and inference. *Quarterly Journal of Economics, 134*(4), 1949–2010.
Borusyak, K., Hull, P., & Jaravel, X. (2022). Quasi-experimental shift-share research designs. *Review of Economic Studies, 89*(1), 181–213.
Callaway, B., Goodman-Bacon, A., & Sant'Anna, P. H. C. (2024). Difference-in-differences with a continuous treatment. NBER Working Paper 32117.
Goldsmith-Pinkham, P., Sorkin, I., & Swift, H. (2020). Bartik instruments: What, when, why, and how. *American Economic Review, 110*(8), 2586–2624.
Rambachan, A., & Roth, J. (2023). A more credible approach to parallel trends. *Review of Economic Studies, 90*(5), 2555–2591.
Roth, J. (2022). Pretest with caution: Event-study estimates after testing for parallel trends. *American Economic Review: Insights, 4*(3), 305–322.
