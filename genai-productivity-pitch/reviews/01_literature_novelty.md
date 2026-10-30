# Review 1 — Contribution to the literature and novelty

Pitch: "Generative AI and the Productivity of Finance and Accounting Scholars" (Faff template, 23 October 2026); reviewed 30 October 2026. Tags: [V] verified this week against the paper's abstract or a reliable secondary source; [PV] partly verified; [UV] could not verify; [M] from memory. Direct access to arXiv, SSRN, RePEc, Nature and Zenodo was blocked, so verification relied on indexed abstracts and press summaries (ledger at the end).

## 1. Verdict

**Score on contribution/novelty: 6/10.**

The pitch is unusually well read for a recruiting document: it has absorbed the Renault–Kusumegi exchange, designs around the outcome-triggered-timing problem, and picks a setting (finance and accounting on SSRN) where the largest headline estimate and the clearest demonstrations of end-to-end AI paper production coincide. But "What's New" misallocates the novelty. Two of its three claims — scholar-level effects at the working-paper stage, and method-by-release timing — are respectively Kusumegi et al.'s own design and the territory of Nee, Zhong & Ni (2026), while the element that is genuinely new is never stated in its own terms: an exposure (intention-to-treat) design built from predetermined method shares at the scholar level, which needs no adoption date, isolates the intensive margin of incumbent scholars from the entry that drives field-level counts, and operates where Arcila's 26 OpenAlex fields cannot see finance or accounting at all. The "research versus inflation" framing is the existing conversation (Gartenberg et al.; Novy-Marx & Velikov; Walther & Dutordoir; quality outcomes already appear in Kusumegi, Filimonovic et al. and Hao et al.), so it cannot carry the contribution; a method-specific inflation test anchored in the finance and accounting multiple-testing literature can. Several citation details are inaccurate or unverifiable as written, and the task-based framing is asserted rather than operationalised. With the fixes below the pitch would read as a 7.5–8 on this dimension.

## 2. Major issues (ranked by severity)

### M1. (H) claims the wrong novelty and invites "Kusumegi on SSRN with another proxy"

(a) (H) item 1: "effects for individual scholars at the working-paper stage, identified from method mixes fixed before ChatGPT". Kusumegi et al. (2025) already estimate scholar-level effects on preprints, including SSRN [V]. A referee reads item 1 as a replication with a different adoption proxy.

(b) The defensible novelty is the estimand, not the unit. Kusumegi, and Filimonovic et al. (2025) [V: matched author-level panel, DiD], estimate an effect of adoption on adopters and need an adoption date, which is where Renault et al. bite. The pitch estimates a reduced-form effect of capability availability on scholars who differ in predetermined task exposure, with scholar and field×quarter fixed effects: a shift-share design whose shares are the 2018–2021 method mix and whose shifts are release dates. It (i) never conditions on the scholar's own post-2022 output or text, (ii) recovers the intensive margin for a fixed panel of incumbents, so entry of new authors and AI paper mills — the leading alternative explanation of the field-level surge — is excluded by construction. None of the four studies in (H) does this, and the Kusumegi reply explicitly defends only "the existence and direction of a positive association ... not a specific magnitude" [V, abstract of arXiv 2607.28968]. The magnitude is open; that is the gap.

(c) Fix. Rewrite (H) item 1: "An exposure design rather than an adoption design: the treatment is the interaction of public release dates with each scholar's pre-ChatGPT method mix, so identification never uses the scholar's own output or text, the estimand is the intensive-margin response of incumbent scholars, and the Renault et al. mechanism cannot operate." State the identifying assumption in shift-share terms (shares exogenous conditional on fixed effects; Goldsmith-Pinkham, Sorkin & Swift 2020, AER 110(8), 2586–2624; Borusyak, Hull & Jaravel 2022, REStud 89(1), 181–213 [M]) and add a paragraph headed "Why this is not a replication of Kusumegi et al." Sharpen the Arcila contrast: his 26 "disciplines" are the 26 OpenAlex fields [V: 92M works, 26 fields, 2015–2025], so finance sits inside "Economics, Econometrics and Finance" and accounting inside "Business, Management and Accounting"; he cannot observe either, nor separate entry from incumbents.

### M2. Nee, Zhong & Ni (2026) is a closest competitor, not a footnote, and H2 overreads it

(a) (H) item 2 calls the release-type timing pattern one "none of these studies uses"; H2 cites Nee et al. for a surge "once reasoning models could handle verifiable derivations".

(b) Nee et al. is organised around exactly the theory/computation distinction and a capability-threshold timing story: 20 arXiv archives, January 2018–August 2026; mathematics in 2026 is 33.5% above 2025 and 11.9% above a synthetic counterfactual; the authors invoke "delayed diffusion and capability threshold mechanisms" [V, abstract summary]. The abstract does not name reasoning models; that attribution is the pitch's inference. So method-level heterogeneity by capability wave is already in print, and if the theory response is a 2026 phenomenon, roughly 15 months after o1-preview (September 2024 [M]), responses are lagged and diffuse, release-dated step dummies are misspecified, and the theory test rests on three quarters of 2026 data.

(c) Fix. Move Nee et al. into (H) and differentiate on four points: archive-level counts versus a scholar panel; mathematics/physics/CS versus finance and accounting; no publication outcome; no incumbent/entrant split. Reword H2 to "theory responds with a lag after reasoning-type releases and not after the 2023 releases", make the dynamic event study by method the primary object, and state the power limit. Cite Korinek's updated use-case ratings, where usefulness for derivations jumps with reasoning models (Korinek 2023, JEL 61(4), 1281–1317, and the 2025 JEL update [M]).

### M3. "Research versus inflation" is the existing conversation; the new part is the method-specific test, which lacks its theoretical anchor

(a) (D): "The puzzle is to what extent the finance and accounting paper boom is research or inflation."

(b) "More versus better" is the title and message of Gartenberg et al. (2026) [V: Organization Science 37(3), 795–812; submissions +42%; quality down]. Walther & Dutordoir report lower-ranked placement [V]; Kusumegi et al. examine quality with 28,000 peer-review reports and 246 million accesses [V]; Filimonovic et al. report "moderate gains in publication quality" by impact factor [V]; Hao, Xu, Li & Evans (Nature 2026, "Artificial intelligence tools expand scientists' impact but contract science's focus") [V existence; findings M] show impact rising while topical breadth contracts. The pitch cites none of the last three on quality. What is new is a prediction about which methods inflate, and the pitch never says why. The reason lies in its own field: the multiple-testing problem in archival finance and accounting is documented (Harvey, Liu & Zhu 2016, RFS 29(1), 5–68; Harvey 2017, JF 72(4), 1399–1440; Mitton 2022, RFS 35(2), 527–575 [M]), p-hacking varies by method (Brodeur, Cook & Heyes 2020, AER 110(11), 3634–3660 [M]), and Novy-Marx & Velikov show the specification-search production function can be automated. AI lowers the marginal cost of another specification to near zero precisely where data are standardised: a theory of inflation by method.

(c) Fix. Reframe (D) as "This project tests the more-versus-better hypothesis where it has its sharpest prediction", cite the multiple-testing papers, and add outcomes that do not depend on journal queues: topic concentration within scholar (Hao et al.; Doshi & Hauser 2024, Science Advances [M]), within-author near-duplication, and the distribution of reported t-statistics by method.

### M4. Release-type dating and the task framing are asserted, not operationalised

(a) Table 2 dates the coding release to "ChatGPT Code Interpreter, July 2023"; the Summary says the estimates show "which methods each release speeds up without assuming it in advance"; (E) grounds the hypotheses in Felten et al. (2021) and Eloundou et al. (2024).

(b) GitHub Copilot was generally available in June 2022 (Peng et al. 2023 measure a 55% speed-up [M]); ChatGPT wrote Stata, R and Python from November 2022; GPT-4 (March 2023) did so well [M]. Writing and coding capability arrived together; only the 2025 agentic tools are a clean coding shock. Risk (3) in (K) half-admits this but the model does not. Labelling releases "writing/coding/reasoning" and methods by dominant task is the assumption; the βs then test it, so "without assuming it in advance" overclaims. And Felten and Eloundou are occupation-level indices; nothing in the pitch applies their logic to research tasks.

(c) Fix. Build an ex ante index Exposure_mk by hand-coding each method's task bundle (literature search, derivation, data cleaning, estimation, writing, experiment administration) and rating each task by release type with an Eloundou-style rubric, pre-registered; Share_im × Exposure_mk becomes the regressor and step dummies a robustness check. Anchor the mapping in Korinek (2023, 2025) [M], whose taxonomy was written for economic research, and in the micro task evidence behind H1: Noy & Zhang 2023 (Science 381, 187–192) for writing; Peng et al. 2023 and Cui et al. 2024 for coding; Dell'Acqua et al. 2023 (HBS WP 24-013) for the jagged frontier that explains why theory lags [all M]. Re-date the coding shock to 2025 and treat 2023 as a joint writing-plus-coding wave.

### M5. Key-paper and closest-study lists do not match, and obvious references are missing

(a) (C) lists Kusumegi, the Renault exchange, Novy-Marx & Velikov and Ciconte et al.; (H) names Walther & Dutordoir, Arcila, Gardner et al. and Barrick et al. as the "four closest studies", none of which is in (C).

(b) Novy-Marx & Velikov and Ciconte et al. are demonstrations that motivate the inflation hypothesis, not studies of scholar productivity.

(c) Fix. (C) = Kusumegi 2025 with the exchange as one entry; Arcila 2026; Walther & Dutordoir 2025; one quantity-versus-quality anchor (Gartenberg 2026 or Novy-Marx & Velikov 2026). Move Ciconte to (D). Add: Hao et al. (2026, Nature); Liang et al. (2024, "Mapping the increasing use of LLMs in scientific papers"; 2025, Nature Human Behaviour) [M], the standard estimator of LLM-modified text; Hamermesh & Oster (2002, Economic Inquiry 40(4), 539–555), "Tools or toys?" [M]; Agrawal & Goldfarb (2008, AER 98(4), 1578–1590) on BITNET and who gains, the anchor for H4 [M]; Ellison (2002, JPE 110(5), 947–993 and 994–1034) and Card & DellaVigna (2013, JEL 51(1), 144–161) for the congestion baseline [M]; Heckman & Moktan (2020, JEL 58(2), 419–470) for "counting papers" in (I) [M].

### M6. Several cited claims are mis-stated or unverifiable as written

- "(Kusumegi et al.) reply that an association of about 7–20% more papers survives ... but concede that none of their estimates is causal." The reply's abstract says the artifact is real but small and that "our claim concerns the existence and direction of a positive association ... not a specific magnitude" [V]; I found no 7–20% [UV]. "Concede" misdescribes authors who framed the result as an association from the start. Quote the abstract instead.
- "Neither side re-examines SSRN" [UV]. Check both papers; if the reply's alternative designs include SSRN, (H) must say how yours differs from them.
- Kusumegi's "+59.8%" for SSRN [PV]: AAAS reports 23.7–89.3% across groups; repository figures I could confirm are 36.2% (arXiv) and 52.9% (bioRxiv); every source cut off before the SSRN number. Confirm against Science 390(6779), 1240–1243 [V].
- Walther & Dutordoir: the indexed version has 41,489 articles, 34 journals, 2000–April 2025, title "...Impact on Academic Writing (in Finance)", and reports falling readability and rising LLM vocabulary, more pronounced for authors from non-English-speaking countries and in lower-ranked journals [V via secondary sources]. The pitch's 55,964 articles and "publish more papers, but in lower-ranked journals" [UV] may be a later version; cite its date and quote exactly.
- Arcila: the outcome is OpenAlex works, not only "published output" [V]; "finance and accounting below the threshold" should read "the two OpenAlex fields containing finance and accounting".

### M7. (J)'s three-literature structure is weaker than the paper

(a) Literature 2 pairs Kim, Morse & Zingales and Ding et al. (technology) with Brogaard, Engelberg & Parsons (editor networks) and Barber et al. (pandemic), which are not technology papers; literature 3 ("from documenting use to measuring productivity") is thin.

(b) The natural homes are two: AI and the production of science (Kusumegi; Arcila; Nee; Hao; Filimonovic) and research evaluation under quantity incentives (Gartenberg; Heckman & Moktan; Card & DellaVigna; Ellison), with finance and accounting methodology (Harvey; Novy-Marx & Velikov) supplying the mechanism. The older technology-and-academia work is precedent inside the first, not a separate contribution.

(c) Fix. Rewrite (J) around those two literatures plus the mechanism, with one falsifiable sentence of contribution to each.

## 3. Minor issues

- AI referee scores (Lu, Luo & Yu 2026) as a quality metric for possibly LLM-written papers invite the self-preference objection (Panickssery, Bowman & Feng 2024, NeurIPS [M]); say how you handle it or drop it.
- Agarwal (2026, SSRN 7236301), "Recovery, then acceleration", reports growth concentrated in computer science and business/management [V, abstract summary]; it contradicts Arcila on business and belongs in (D).
- The first stage measures writing use only; the Summary's "which release speeds up" should not imply the coding and reasoning channels are measured.
- "a breakdown by use that Arcila leaves for future work" [UV]; quote or cut.
- Walther & Dutordoir's AI measure "comes from the authors' own papers" is listed as a weakness; your first stage shares it, which (E) handles well; say so in (H).

## 4. What works and should be kept

- Making the Renault critique the organising constraint, and keeping AI vocabulary out of the treatment, is correct and well explained.
- The fixed 2018–2021 panel, field×quarter effects and measured SSRN posting rate are the right answers to platform growth; promote the incumbent/entrant distinction to a headline (M1).
- The JEL × BYU-method taxonomy gives cells (empirical asset pricing, experimental auditing) that referees in both fields will accept.
- The congestion-aware publication test, with within-cohort comparisons and 2027/2028 updates, is more careful than anything in the closest studies.
- The (K) limitation that the common effect is unidentified is honest; keep it, as is the concrete policy audience in (I).

## 5. Must fix before circulating to coauthors vs fix later

**Must fix now:** M1 (restate the novelty as an exposure design; add the "not a replication" paragraph and the OpenAlex-fields point); M2 (bring Nee et al. into (H); reword H2 and its power limit); M4 (re-date the coding shock; drop "without assuming it in advance" or build the exposure index); M6 (every citation detail); M5's (C)/(H) alignment.

**Fix later (before the first full draft):** M3's additional outcomes and multiple-testing anchor; M7's reorganisation of (J); the missing older references; the minor items.

## Verification ledger

Verified via indexed abstracts/press summaries: Kusumegi et al. 2025 bibliographic details, sample sizes, the 23.7–89.3% range and the arXiv/bioRxiv figures; Renault et al. (arXiv 2605.17979; PNAS publication corroborated by a lab page, volume/issue unchecked); the Kusumegi reply's abstract (arXiv 2607.28968, 31 July 2026); Arcila's abstract (SSRN 6385141, March 2026); Gartenberg et al. 2026; Nee et al. (arXiv 2609.04872, 4 September 2026); Filimonovic et al. (arXiv 2510.02408); Walther & Dutordoir's indexed version; Hao et al. 2026 (Nature) existence. From memory: all [M] items and the Copilot, GPT-4 and o1-preview dates.
