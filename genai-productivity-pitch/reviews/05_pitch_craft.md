# Review 05 — Pitch craft, clarity and internal consistency

Pitch reviewed: "Generative AI and the Productivity of Finance and Accounting Scholars", research pitch dated 23 October 2026 (Faff template). Review date: 30 October 2026. Lens: a busy potential coauthor with ten minutes.

## 1. Verdict

**Clarity/craft score: 6/10.**

The raw material is strong: a timely wedge (the Renault et al. critique of Kusumegi et al.), a design explainable in one sentence (pre-2022 method mix × AI release dates), and a concrete data and ethics plan. But the document is not yet a pitch. At about 3,750 words of body plus 700 words of references it is three times Faff's two-page norm, and its best selling point, that the treatment "never depends on a scholar's own output", is buried in (H) instead of leading the summary. The sections drift in what they promise: the summary and (B) ask "how much" AI raises output while (K) concedes that only differences between methods are identified, and the motivating puzzle (research or inflation?) is answered only by an analysis that (B) and (K) call secondary. The hypotheses are directional prose rather than statements about the model's parameters, and (C) points to an H1 that does not say what (C) claims it tests. For a file named "pitch_coauthors", it is written in the first person singular and never says what the author needs from a coauthor, what already exists, or how work and credit would be split. One hard editing pass along the list in section 7 would lift this to an 8 or 9.

## 2. Inconsistencies found

1. **"How much" versus "differences only".** (B): "How much does generative AI raise the research output of finance and accounting scholars". (K): "The design identifies differences between methods, not the total effect of AI". *Resolution:* rewrite (B) and the summary as "which methods, by how much relative to the least-exposed methods, and when"; if a total effect is wanted, state the extra assumption (zero AI gain in the reference method).

2. **Table 2 "decomposes" total output, but the coefficients are relative.** Table 2: column "Part of output growth"; β row "Productivity due to AI, by method and release type"; text below: "averaging it within a group ... gives the AI part of that group's output growth". Same table: "relative to a reference method". Because shares sum to one, one β per release must be dropped, so the sum is a gain relative to the omitted method. *Resolution:* retitle the column "What the term absorbs", name the reference method (experimental), and write "gain relative to scholars whose work is entirely experimental".

3. **(C) misdescribes H1.** (C): "standard archival designs are the easiest to automate, a prediction this project tests (H1)". (E) H1: "After the writing-type release, output rises most in review and commentary ...; after coding-type releases, it rises most in archival work". The archival ranking is an end-to-end claim and only half of H1. *Resolution:* make the archival ranking H1 and review/commentary H1b.

4. **"AI cannot have shaped it" misnames the threat.** Summary and Table 2: "The method mix is fixed before ChatGPT, so AI cannot have shaped it". (K) Risk 4: "Method-specific shocks unrelated to AI ... could mimic the pattern"; (F): "an LLM classifies each 2018--2021 paper". Predetermined shares remove reverse causality and the Renault problem, not method-specific trends, and the shares are themselves produced by an LLM. *Resolution:* "measured on 2018–2021 papers, so exposure cannot respond to later output or AI use; the remaining threat is method-specific trends, addressed by pre-trends and placebo dates."

5. **"No common trend predicts this timing" is asserted while the timing is unfixed.** H2: "Theory gains only after reasoning-type releases (late 2024 onward) ... No common trend predicts this timing." Table 2: "reasoning (from late 2024; dates to be confirmed)". Common trends are absorbed by τ_f,t anyway; the threat is a theory-specific trend. If the date is chosen after seeing theory output, the pitch reproduces the outcome-triggered timing it criticises; and Nee et al. date the mathematics surge to 2026, not late 2024. *Resolution:* delete the sentence, fix the dates now (o1-preview 2024Q4, R1/o3 2025Q1) and let the event-study show any lag.

6. **"Does not assume which methods a release can automate" versus hypotheses that assume exactly that.** (E): "The model does not assume which methods a release can automate"; summary: "without assuming it in advance". H1–H3 say which methods gain, and the reference method is itself such an assumption. *Resolution:* "The model is saturated in release × method, so it can reject the task-based predictions rather than impose them."

7. **The puzzle is "research or inflation", but its test is "secondary".** (D): "The puzzle is to what extent the finance and accounting paper boom is research or inflation". (B): "A secondary question is whether the extra papers are published"; (K) Risk 6: "which is also why the publication analysis is secondary". (G) concedes the 24-month share "measures speed", with the answer arriving in "2027 and 2028", next to Risk 1's "speed matters". *Resolution:* promote quality to co-primary using outcomes available now (conference acceptance, AI referee scores, near-duplicates) and retitle ("More Papers or Better Papers?"), or rewrite (D) so the puzzle is "which methods and when".

8. **Headline numbers do not line up.** Summary: "a decade of flat output". (D): "flat at about 4,400 a year from 2015 to 2022, then reached 7,393 in 2025 and 9,125 by early October 2026"; nothing for finance in 2023–2024, nothing for accounting before 2022, and 9,125 is a partial year. (E): "SSRN postings doubled from 2021 to 2022", before ChatGPT. *Resolution:* one small table of yearly counts 2019–2026 (2026 annualised) and one line saying the 2022 doubling was outside these fields.

9. **Sample descriptions differ.** Summary: "long-term SSRN posters ... pre-ChatGPT papers". (F): "at least two finance or accounting SSRN papers in 2018--2021". Two papers in four years is not "long-term", and "pre-ChatGPT" includes 2022, which the shares exclude. *Resolution:* one definition throughout, with the reason 2022 is excluded.

10. **Three release types or four?** Summary: "(writing, coding and reasoning tools)". Table 2 puts "Code Interpreter, July 2023" and "agentic tools ... February to May 2025" inside one step indicator, while (K) Risk 3 relies on "2025 agentic coding" as separate variation. *Resolution:* k ∈ {writing 2022Q4, coding 2023Q3, reasoning 2024Q4, agentic 2025Q1}, with the quarters that identify each β stated.

11. **The first-stage rule contradicts itself.** (E): "output gains in a method without a matching rise in AI use would point to another cause", then "output can rise after coding releases without more AI-style words". *Resolution:* restrict the rule to the writing release.

12. **(C) and (H) name different "closest" papers; (K) lists a non-competitor.** (C): Kusumegi et al. is "The closest prior work". (H): "Four recent studies are closest to this one" (Walther & Dutordoir, Arcila, Gardner et al., Barrick et al.), none in (C). (K) Risk 1: "Competition from Walther & Dutordoir, Gardner et al. and Arcila", although (H) says Gardner et al. study use "but not its effect on output". *Resolution:* (C) = Kusumegi/Renault, Walther & Dutordoir, Arcila; move Novy-Marx & Velikov and Ciconte et al. to (D); drop Gardner et al. from Risk 1.

13. **Table 2 lists a row "Not in the equation"** in a table titled "Terms of the model". Move it to the first-stage text.

For the methods reviewers: (a) the "flat 2018--2022 pre-trends" check is weakened because 2018–2021 is also the selection and share-measurement window; (b) Table 2's separate "Personal growth" (career stage) and "Common trends" terms are not separately identified in a linear specification with scholar and quarter fixed effects.

## 3. Section-by-section notes (current → target words)

- **Project Summary (214 → ≤180).** Never says why existing evidence is inadequate, what the expected finding is, or what is new; "net of SSRN's own growth in each field" is a specialist aside; one 45-word sentence. Lead with the puzzle, name the Renault problem, end with the expected pattern and who cares.
- **(A) Title (10 → ≤12).** Generic, and "productivity" promises output per input while the outcome is counts. Options: "Which Research Does Generative AI Speed Up? Evidence from Finance and Accounting Working Papers"; "More Papers or Better Papers? Generative AI in Finance and Accounting Research".
- **(B) Research question (48 → 45).** Right length, wrong content (inconsistency 1): primary (which methods, relative to the least exposed, when) and secondary (do the extra papers hold up).
- **(C) Key papers (277 → 130).** Faff wants three papers and one line each on relevance; this has four entries carrying findings, critiques and a hypothesis pointer. Keep the Kusumegi/Renault entry, it is the hook; align with (H).
- **(D) Motivation (424 → 210).** Good argument, wrong order: the puzzle comes last. Structure as fact (one sentence plus the small table), two gaps, puzzle; move the nine numbers and the peer-review-congestion paragraph to the appendix.
- **(E) Idea (1,231 → 420 in the body plus a 500-word appendix).** Doing the work of five sections. Keep the idea in two sentences; classification in three sentences with Table 1 as a one-line list per dimension; the model first in words ("log expected papers = scholar effect + career stage + field×quarter effect + Σ β × [release k available] × [pre-2022 share of method m]"), then the equation with `\exp` in roman and explicit indices, then a four-line legend; the hypotheses (≈120 words). Move Table 2 (362 words), the "SSRN's own growth" paragraph and the first-stage detail to the appendix; gloss "Wald ratio" as "output gain per percentage point of AI-assisted abstracts". Define "inflation" before it is used.
- **(F) Data (433 → 200).** The best-specified section; keep one bullet per source and move coverage percentages and licensing detail to the appendix. Say what "ORCID (on 92% of 2024 SSRN works)" is the share of.
- **(G) Tools (313 → 170).** Estimation and checks are concise; the 170-word "Additional analysis" block should shrink to two sentences here or be promoted (inconsistency 7).
- **(H) What's New (204 → 110).** Replace the prose tour with a four-row comparison (study; unit; outcome; AI measure; what changes here) and three one-line "adds".
- **(I) So What (94 → 90).** The clearest section; keep.
- **(J) Contribution (135 → 70).** Restates (H) items 1–2. Reduce to the two literatures the paper is shelved under and the one conceptual point (task-based exposure applied to research production).
- **(K) Other considerations (308 → 220 plus a 100-word ask).** Seven risks become four (classification error; close release dates; method-specific shocks; SSRN growth); keep "Limitations stated upfront" verbatim, the most honest paragraph in the pitch; ethics in one sentence; add timeline and ask.
- **References (30 → the ~18 cited in the shortened body; full list in the appendix).**

Division of (H)/(I)/(J): (H) answers "new relative to what" (studies); (I) answers "who changes which decision" (audiences); (J) answers "which shelf and which idea" (literatures and concept). Delete every sentence in (J) that repeats (H).

Writing notes. Gloss or drop PPML, Wald ratio, two-way clustering, ICSR Lab and HREC; gather the scattered hedges ("dates to be confirmed", "if licensed", "where possible") into Risks; split sentences over 50 words (the "Second, the only finance evidence" sentence runs 58); break Table 1's seven-category Method cell into lines; remove the duplicated table captions (a pandoc artefact); switch to "we" once coauthors are sought.

## 4. Rewritten Project Summary and hypotheses

**Project Summary (≤180 words):**

Finance and accounting working papers on SSRN have doubled since ChatGPT arrived in late 2022, after years of flat output. Is generative AI making scholars more productive, or mainly multiplying the papers that are easiest to automate? The only scholar-level estimate (Kusumegi et al. 2025, Science) is partly an artefact of how AI adoption was dated; this project avoids that problem. We follow scholars posting on SSRN in 2018–2021, classify their pre-2022 papers by area and method (say, asset pricing theory versus empirical asset pricing), and ask whose output rose after each wave of AI tools: writing assistants (late 2022), coding tools (2023, 2025) and reasoning models (late 2024). Because the method mix is measured before these tools existed, the comparison cannot be driven by who chose to use AI. We expect the largest gains in database-driven archival work, none in experiments and field studies, and gains in theory only after reasoning models. A second analysis asks whether the extra papers reach conferences and ranked journals. It matters to those who count papers: promotion committees, journals and doctoral programs.

**Hypotheses, tied to the model.** Methods m: T theory; AS archival with standard databases; AT archival text; AH archival hand-collected; X experimental (reference, β_kX ≡ 0); S survey/interview/field; R review/commentary. Releases k, dated before estimation: W writing 2022Q4; C coding 2023Q3; Z reasoning 2024Q4; A agentic coding 2025Q1.

- **H1 (coding tools speed up data-driven archival work).** β_C,AS and β_C,AT exceed β_C,m for every other m, and the cumulative effect Σ_k β_k,AS through 2026Q3 is the largest of any method. Rejected if the archival coefficients are not the largest or are indistinguishable from zero.
- **H1b (writing tools speed up review and commentary).** β_W,R > β_W,m for all m ≠ R.
- **H2 (theory responds only to reasoning models).** β_W,T = β_C,T = 0 and β_Z,T > 0; the theory event-study path is flat through 2024Q3. Rejected if theory output rises in 2023.
- **H3 (primary-data and hand-collected work are least exposed).** Cumulative Σ_k β_km through 2026Q3 is lowest for S and AH and not distinguishable from zero. Rejected if either exceeds AS.
- **H4 (who gains).** The H1–H2 effects are larger for scholars with career age ≤ 6 years in 2022Q4, at schools outside the UTD top 50, and for solo or two-author teams; tested as Release × Share × Group interactions. Rejected by zero or opposite-signed interactions.
- **First-stage check (not a hypothesis).** The share of AI-style abstracts rises after W most in R and least in X and S.

## 5. Draft "ask to coauthors" (≤120 words)

**What I am looking for.** Two coauthors. First, an accounting researcher who knows the BYU/Coyne classification and the AAA journals, to own the accounting classification, the hand-coded validation and the Journal of Accounting Research positioning. Second, an applied econometrician at home with event-study Poisson designs and OpenAlex/Crossref pipelines, to own identification (release dating, placebo and pre-trend design) and the replication package. I bring the data pipeline already built (OpenAlex and Crossref extracts, 2018–2026 counts, the LLM classifier and validation sample), the draft design and the finance positioning. Authorship alphabetical; I draft, coauthors lead their sections. Timeline: classification validated by December 2026, first estimates February 2027, SSRN draft and AFA/AAA submissions by mid-2027; HREC application in November.

## 6. Reference check results

Direct fetches of arxiv.org, papers.ssrn.com, zenodo.org and pnas.org are blocked from this session; confirmations rest on search-engine records (PNAS, RePEc, Springer and arXiv listings, Rozario's CV).

| Item in pitch | Status | Notes |
|---|---|---|
| Renault, Bergeaud & Bosquet (2026), PNAS 123(33) | Confirmed | Vol. 123 no. 33 (18 Aug 2026), DOI 10.1073/pnas.2618638123; arXiv 2605.17979. Add the DOI/article number. |
| Kusumegi et al. (2026), arXiv 2607.28968 | Confirmed | Title and ID match. The "7--20%" figure in (C) was not checked. |
| Nee, Zhong & Ni (2026), arXiv 2609.04872 | Confirmed | Xiaoshn Nee, Haobo Zhong, Xiaomin Ni; submitted 4 Sep 2026. Caution: it reports a 2026 mathematics anomaly (+33.5% on 2025) with capability thresholds as one interpretation; "verifiable derivations" is the pitch's gloss, and the surge is 2026, not late 2024. |
| Lu, Luo & Yu (2026), SSRN 7607363 | Confirmed | Hai Lu, Yichen Luo, Luping Yu; posted 13 Oct 2026; also arXiv 2610.18435. The pitch's description matches. |
| Ciconte, Rozario & Urcan (2026), RAST 31(3), 1638–1676 | Confirmed; verify pages | RePEc gives 31(3), 1638–1676, DOI 10.1007/s11142-026-09967-y; a Springer issue page shows 1970–2010. |
| Novy-Marx & Velikov (2026), JEL 64(1), 5–37 | Confirmed | DOI 10.1257/jel.20251821. NBER version titled "AI-Powered (Finance) Scholarship". |
| Gartenberg et al. (2026), Org. Sci. 37(3), 795–812 | Confirmed | Online 27 Apr 2026; the 42% figure matches the abstract. |
| Arcila (2026), SSRN 6385141 | Paper confirmed; SSRN ID not confirmed | Zenodo replication package (Andres Arcila, 19 Oct 2026, DOI 10.5281/zenodo.23478840) carries the exact title; no SSRN record surfaced. Check "published output": OpenAlex works include preprints. |
| Kusumegi et al. (2025), Science 390(6779) (bonus) | Confirmed | DOI 10.1126/science.adw3000; starts p. 1240; end page not verified. |

Formatting: consistent APA style, but add missing article numbers (Renault et al.; Kobak et al. 2025, Science Advances 11(27)), use one locator style for working papers, and add years to "Kobak et al." and "Barrick et al." in the text. Nothing checked looks fabricated.

## 7. Prioritised edit list (one revision pass)

1. Cut the body to about 1,700 words; move Table 2, the SSRN-growth paragraph, first-stage detail, coverage percentages and the publication-analysis design to a one-page technical appendix.
2. Replace every "how much"/"AI part of output growth" claim with "relative to the least-exposed methods", name the reference method, retitle Table 2's third column (inconsistencies 1–2).
3. Decide whether the quality/inflation analysis is co-primary or secondary, then align the summary, (B), (D), (G), (K) and the title (inconsistency 7).
4. Rewrite H1–H4 as parameter statements with fixed release dates and an explicit reference group; make (C)'s pointer match (inconsistencies 3, 5, 10).
5. Delete "AI cannot have shaped it", "without assuming it in advance" and "No common trend predicts this timing"; state what the design actually buys (inconsistencies 4–6).
6. Add the coauthor ask: roles sought, what exists, division of labour, authorship norm, timeline.
7. Make (C) and (H) name the same three closest papers; move Novy-Marx & Velikov and Ciconte et al. to (D); drop Gardner et al. from Risk 1 (inconsistency 12).
8. State the model in words before the equation; fix `exp` to `\exp`, add summation indices, replace Table 2 with a five-line legend, remove the "Not in the equation" row.
9. Add one small table of yearly finance and accounting SSRN counts 2019–2026 (annualised); drop "a decade of flat output" unless supported (inconsistencies 8–9).
10. Clean the references (DOIs and article numbers, Ciconte pagination, Arcila SSRN ID, arXiv ID for Lu et al., years in text) and remove the duplicated table captions.

## 8. What works and should be kept

- The opening wedge: using the Renault et al. critique to motivate an exposure measure that cannot depend on a scholar's own output. Promote it to the summary; it is the sentence a coauthor will repeat.
- The design: pre-2022 method shares × dated release types is explainable in one breath and yields distinct, time-stamped predictions, especially the theory/reasoning timing test.
- The task-based framing (Felten et al.; Eloundou et al.), which gives the heterogeneity a theory rather than a fishing licence.
- The SSRN posting-rate control measured from journal articles, a fix for a confound most readers would miss.
- The data section's specificity: OpenAlex/Crossref routes, licensed abstracts, no scraping, HREC awareness.
- The honesty of "Limitations stated upfront" and of the 24/36/48-month publication updates.
- (I) So What: three named audiences with a decision each.
- An up-to-date literature (Lu et al. posted ten days before the pitch).
