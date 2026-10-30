# Review 3 — Significance to the field and to practice ("so what?")

**Pitch reviewed:** "Generative AI and the Productivity of Finance and Accounting Scholars" (Pitching Research template, 23 October 2026). **Lens:** former department editor; promotion committee member; dean; PhD director. Tags: [verified] = web-checked 30 Oct 2026; [memory] = reviewer's knowledge; [unverified] = not checkable here (SSRN and arXiv unreachable).

## 1. Verdict

**Score: 6/10 as pitched; 8–9 reachable with the re-centring below.**

This is a timely project with one genuinely good idea: using each scholar's pre-ChatGPT method mix as a predetermined, task-based exposure measure and letting successive release types (writing, coding, reasoning) time the effects. That idea could make the paper memorable: it re-examines the largest estimate in the Science/PNAS dispute (Kusumegi et al.'s +59.8% on SSRN [verified]; Renault et al.'s timing critique [verified]) with a design immune to the critique. But the pitch is organised around a question section K concedes it cannot answer ("how much does generative AI raise research output"), its "research vs inflation" test treats a fixed-slot tournament outcome as a quality measure, and its So-What names audiences without saying what any of them would do differently or by how much. The most consequential result the design can deliver, who gains and what the marginal paper is worth, is parked as a fourth hypothesis. As written, the modal outcome is a competent paper documenting method-level differences whose direction nobody disputes. Re-centred, it is the paper a dean quotes when reforming count-based evaluation, editors cite when defending targeted screening, and the science-of-science community cites as the clean SSRN number. Fix the framing before recruiting: coauthors will sign up for the headline question and find the limitation in section K.

**Elevator statement:** "Using the research methods finance and accounting scholars practised before ChatGPT as a predetermined measure of exposure to each kind of AI tool, this paper shows which kinds of research generative AI has accelerated, who gained most, and whether the extra working papers clear the bar of peer review, turning a contested aggregate ('AI raises output by 7% to 60%') into a map of where the surge comes from and what it is worth."

**The carrying figure:** a stacked, quarter-by-quarter decomposition of the post-2022 SSRN surge into (i) new entrants with no pre-2022 record, (ii) established scholars' AI-attributable output by method (β_km × Share), (iii) measured posting-rate change, and (iv) the unexplained common component. It answers "where do the extra papers come from?" in one picture and is honest about what is not identified; the method-by-release event study (H1–H3 with the first stage overlaid) is the proof and belongs as Figure 2.

## 2. Major issues, ranked by severity

### M1. The headline question does not match what the design delivers (high)

(a) Section B: "How much does generative AI raise the research output of finance and accounting scholars"; the Summary repeats it. Section K: "The design identifies differences between methods, not the total effect of AI."

(b) Readers, referees and coauthors anchor on the first sentence. A design that puts the common effect into τ_f,t answers "where and when", not "how much". The level question is also crowded terrain (Kusumegi/Renault; Walther & Dutordoir; Arcila [unverified]); entering it with a design not built for it is a losing position. Evaluators and editors actually need the composition question.

(c) Fix. Rewrite B: "Which kinds of finance and accounting research has generative AI accelerated, by research method and type of AI tool; who has gained most; and do the additional working papers clear the bar of peer review?" Then report a *bounded* total effect in one table: (i) lower bound: take the least-exposed group (experimental, survey, field and hand-collected archival) as the reference, show its first stage is flat, and read β for exposed methods as a lower bound, assuming AI did not reduce the reference group's output; (ii) upper bound: the fixed panel's aggregate post-2022 growth relative to its own 2018–21 trend, net of the measured posting-rate change; (iii) optional: country-level ChatGPT availability (not officially offered in mainland China, Hong Kong or Russia [memory]) interacted with release dates, given the large China-affiliated share of SSRN finance posters; imperfect, but a sign check.

### M2. "Research vs inflation", as measured, is a tournament outcome, not a quality measure (high)

(a) Section G: "the share published in an ABDC A*/A or FT50 journal within 24 months of posting ... inflation predicts a larger fall in the methods whose output rose most."

(b) Three problems leave readers unconvinced. Fixed capacity: top-journal slots are roughly fixed in the short run, so if output rises 50% the publication share must fall by about a third even if every paper is as good as before, and the between-method comparison within cohort does not fix this because capacity is itself method-specific. Lifecycle timing: scholars post at different stages; if AI shifts posting earlier, the 24-month share falls mechanically, and with accounting submit-to-accept times around 26 months (Hurley et al. 2025 [citation verified; figure unverified]) the window is nearly uninformative for accounting. Language: "inflation" implies worthlessness; a good paper unpublished at 24 months is not inflation.

(c) Fix. Reframe the project as a *supply shock to the journal system*: working papers are the supply of claims, tracked through fixed-capacity journals. Replace "inflation" with "quality of the marginal paper" on scales that do not depend on slots: LLM referee scores on full texts (Lu, Luo & Yu 2026; this needs a licensed full-text route), within-author near-duplicate rates, citation accrual at fixed horizons against same-cohort, same-method papers, and top-conference presentation. Keep the publication share as a congestion measure, with the fixed-capacity prediction stated as the null. Make the 36- and 48-month update a separate, pre-registered Paper 2, which one coauthor can own.

### M3. The So-What names audiences but no actions and no magnitudes; key audiences are missing (high)

(a) Section I: "promotion committees end up comparing unlike quantities"; journals "need to know"; doctoral programs "need to know"; SSRN and journal AI policies "need the same evidence".

(b) "Need to know" is not an implication. A committee cannot deflate counts by method; that would penalise archival researchers for using a tool. It can stop counting SSRN postings, cap the works assessed, or benchmark within method. Editors can act on *where* the surge comes from (methods, career stage, institutions, countries) to design targeted screening rather than blanket fees. Missing audiences: AACSB, whose scholarly-academic status rests on five-year counts of intellectual contributions [memory]; ABDC and FT list managers, whose lists create count targets (ABDC is the Australian lever); the ARC's successor to ERA (ERA ceased in 2023 with no finalised successor [verified]) and REF 2029 [memory], both deciding the weight on output volume; funders assessing track records; hiring committees facing AI-assisted job-market papers; and the science-of-science community arguing over the SSRN number.

(c) Fix. Rewrite I as three actor → evidence → action paragraphs with placeholders: "For evaluators: since 2019 the expected SSRN count of an archival scholar using standard data rose X% relative to an experimentalist's, so a count threshold set in 2019 is now Y% easier for the former; evaluators that count (AACSB SA status, ABDC-target schools) should benchmark within method or stop counting working papers. For editors: Z% of the post-2022 surge traces to [segment], whose marginal paper scores W points lower on referee quality; this supports targeted screening over blanket fees. For doctoral programs: methods whose output rose without a matching rise in quality are being commoditised; invest in [primary data, identification, theoretical judgement]."

### M4. Heterogeneity (H4) is the most significant question in the paper and is buried (high)

(a) Section E, H4 is a grab-bag: "career stage and incentives ... resources ... solo authors vs teams ... international collaboration."

(b) The fact people will remember is distributional: does generative AI democratise research production (largest gains where constraints bind: non-native English writers, scholars without RAs, lower-ranked schools) or fuel count-gaming (largest gains where count incentives are strongest and marginal papers are weak)? Kusumegi et al. report larger gains for scholars outside English-speaking institutions [verified, secondary sources]; Gardner et al. report more AI vocabulary among juniors and less research-intensive schools. The pitch already cites Kim, Morse & Zingales (2009); the natural frame is "are elite universities losing their edge, again?". Same design, no extra identification cost, and far more power than theory vs archival.

(c) Fix. Split H4 into two competing hypotheses with distinct signatures (democratisation: gains in constrained groups with unchanged marginal quality; gaming: gains in count-incentivised groups with falling quality). Data: pre-2022 institution rank (UTD/BYU plus a non-US list), country and English-native status from OpenAlex institutions, career age, prior top-journal record, coauthors with no prior record (students), and an incentive proxy (ABDC-list jurisdictions; AACSB-accredited non-research-intensive schools; Chinese institutions before and after the 2020 "break the five onlys" reforms [memory]). Make the 2×2 (who gains × which method) the organising structure and promote it to the title or subtitle.

### M5. SSRN output measures posting, and the pitch undersells the one number everyone will quote (medium-high)

(a) Summary: "the number of ... working papers posted to SSRN has risen sharply"; section K: "Working papers proxy for research output."

(b) SSRN posting is near-universal in finance, not in accounting; the accounting rise (2,683 → 5,653, +110%) exceeding finance (+68%) is as consistent with a posting-norm shift as with AI, and the posting-rate control is observable only with a lag and only for published papers. More importantly, the pitch never plans to *report* the decomposition of the surge into new entrants, established scholars, posting-rate change and residual. Yet "X% of the post-2022 SSRN surge comes from authors with no record before 2022" is the most memorable, dean-ready fact the data can produce, and it rescues the paper if β_km are small: a null then reads "the surge is not established scholars' productivity" rather than "nothing found".

(c) Fix. Add the decomposition as the first descriptive result (the carrying figure); state that the object is working-paper production, the supply side of the journal system; for accounting, triangulate with public AAA and FARS program counts; cross-check the "flat at 4,400 then surge" fact against Crossref SSRN DOI counts, since OpenAlex subfield assignment and SSRN indexing change over time.

### M6. The pitch needs a power statement and a pre-committed reading of each outcome (medium)

Home run: staggered, method-specific jumps at the release dates (commentary and archival-text at November 2022; archival-standard-data at mid-2023 and 2025; theory flat in 2023, rising after late 2024; experiments flat), the first stage moving in the same cells, flat pre-trends, lower marginal quality in archival work and democratised gains elsewhere; probability 25–35%. Nothing to see: imprecise, overlapping β_km because method shares are concentrated (most finance posters are archival-standard-data), the two 2023 releases are two quarters apart, pure theorists are few, and quarterly counts for scholars posting about one paper a year are noisy; 2023 effects contaminated by a method-specific COVID rebound (experimental and field work was suppressed in 2020–21 and recovered in 2022–23, which field-by-quarter effects do not absorb) and by GitHub Copilot's availability from June 2022 [memory]; probability 40–50%. Fix: (i) make archival-standard-data × coding release the headline test (the modal method, where the Novy-Marx & Velikov warning bites) and demote review/commentary, a tiny category contaminated by non-research items; (ii) report a power calculation from the 2018–21 panel (scholars per method cell, baseline rates, detectable β at 80% power); (iii) add method-specific 2020–21 controls; (iv) pre-register H1–H3 and the interpretation of a null.

### M7. Venue strategy is one line; it should be a plan (medium)

*Management Science*: plausible lead; needs the bounded total effect, an absolute quality measure and the power statement. *JF/JFE*: precedent exists for the profession studying itself (Barber et al. 2021 JF; Kim, Morse & Zingales 2009 JFE), but it needs a finance-only focus, one clean fact and an economic lesson (fixed-capacity tournament); a JFE short paper could rest on the decomposition plus H2. *JAR/TAR*: TAR published Hurley et al. (2025); an accounting version with journal-system consequences fits, but combining fields dilutes. *Science/PNAS/Nature Human Behaviour*: requires cross-field generality (a generic theory / secondary-data / primary-data / review taxonomy across SSRN's other networks), one striking figure, pre-registration and open data, which SSRN's terms and abstract copyright constrain. *Critical Finance Review*: a companion replication of the Kusumegi SSRN estimate. Recommendation: MS for Paper 1, a PNAS Brief Report if the cross-field extension is cheap, Paper 2 (publication outcomes, 2028) to TAR/JAR or JFE.

## 3. Minor issues

- Title: generic, and "productivity" promises a level. Alternatives: (1) "Which Research Does Generative AI Speed Up? Evidence from the Methods Finance and Accounting Scholars Used Before ChatGPT"; (2) "More Papers or More Research? Generative AI as a Supply Shock to Finance and Accounting Journals"; (3) if H4 is elevated, "Are Elite Universities Losing Their Edge, Again? Generative AI and the Production of Finance and Accounting Research".
- Arcila (2026, SSRN 6385141) could not be located [unverified]; "finance and accounting below the threshold at which gains appear" is load-bearing. Include a link and the estimate; if Arcila finds no field-level gain, that supports M1.
- Other numbers: Kusumegi +59.8% [verified]; Gartenberg et al. +42%, Org. Sci. 37(3) [verified]; Renault et al. (PNAS) and the Kusumegi reply [exist, verified]; the "7–20%" surviving association [unverified]; Nee, Zhong & Ni [exists; mathematics-surge finding unverified].
- "AI cannot have shaped it" overclaims: GPT-3 (2020) and Copilot (2022) predate ChatGPT; say "ChatGPT cannot have shaped it".
- The Wald ratio is computed for the writing release only; say in I what the per-unit number is for, or drop it.
- The doctoral-program implication leans on Keloharju & Keloharju's claim that humans keep an edge in higher-order reasoning; H2 makes that testable rather than assumed. Say so.
- No timeline (give a first-draft date, since competitors are named as a risk) and no data-sharing plan (OpenAlex CC0 identifiers and derived measures are shareable; abstracts are not).

## 4. What works and should be kept

- Predetermined method-mix exposure interacted with release timing: genuinely new, and immune to the outcome-triggered-timing critique.
- H2's timing prediction (theory flat in 2023, rising only after reasoning models) is the pitch's best identification argument.
- Treating AI vocabulary as a first stage rather than as treatment; the fixed panel of pre-2022 posters; the explicit posting-rate control.
- Current, well-chosen Key Papers; Novy-Marx & Velikov and Ciconte et al. give H1 a sharp prior.
- Table 2's plain-language reading of the model, the honest limitations paragraph, the no-scraping stance and the HREC awareness.

## 5. Must fix before circulating to coauthors vs fix later

**Must fix now:** M1 (re-centre B and the Summary; add the bounded total effect); M3 (rewrite I with actors, actions and numbers); M4 (split H4 into democratisation vs gaming and make it the organising structure); the M2 reframing (supply shock, marginal quality, two-paper plan); the Arcila citation; a power statement; the title.

**Fix later:** the COVID-rebound control, Copilot dating, country-access variation, licensed full-text route for referee scores, cross-field extension for a Science-family version, and AAA/FARS triangulation for accounting.
