The following checklist is a good list to follow when developing AI models. Quite a few of them are not applicable to AI models.
But the rest are excellent points to think about and every AI model could benefit from a discussion. 

## A. CONSORT 2010 (report all)

| #   | Item (succinct)                                             | RCT  | DONE? | IN AI |
| --- | ----------------------------------------------------------- | ---: | :---- | :---- |
| 1a  | Title states randomized trial                               |  YES |       |   NA  |
| 1b  | Structured abstract (design, methods, results, conclusions) |  YES |       |       |
| 2a  | Background & scientific rationale                           |  YES |       |       |
| 2b  | Objectives/hypotheses                                       |  YES |       |       |
| 3a  | Trial design (parallel/factorial) & allocation ratio        |  YES |       |       |
| 3b  | Important post-start changes (with reasons)                 |  YES |       |       |       
| 4a  | Participant eligibility criteria                            |  YES |       |       |
| 4b  | Settings & locations                                        |  YES |       |       |
| 5   | Interventions (detail sufficient for replication)           |  YES |       |       |
| 6a  | Prespecified outcomes & how/when assessed                   |  YES |       |       |
| 6b  | Outcome changes after start (reasons)                       |  YES |       |       |
| 7a  | Sample size determination                                   |  YES |       |       |
| 8b  | Type of randomization; restrictions (blocking)              |  YES |       |   NA  |
| 9   | Allocation concealment mechanism                            |  YES |       |   NA  |       
| 11a | Blinding: who, how                                          |  YES |       |   NA  |       
| 11b | Similarity of interventions (if relevant)                   |  YES |       |   NA  |       
| 12a | Statistical methods for primary/secondary outcomes          |  YES |       |       |
| 12b | Methods for additional analyses (subgroups/adjusted)        |  YES |       |       |
| 13a | Numbers randomized/treated/analyzed per group               |  YES |       |       |
| 13b | Losses/exclusions after randomization (reasons)             |  YES |       |       |
| 14a | Recruitment & follow-up dates                               |  YES |       |   NA  |
| 14b | Why trial ended/was stopped                                 |  YES |       |   NA  |
| 15  | Baseline characteristics table                              |  YES |       |       |
| 16  | Numbers analyzed per group; analysis set (e.g., ITT)        |  YES |       |       |
| 17a | Outcome results with effect size & 95% CI                   |  YES |       |       |
| 17b | For binary outcomes: absolute **and** relative effects      |  YES |       |       |
| 18  | Ancillary analyses (pre-specified vs exploratory)           |  YES |       |       |
| 19  | Harms/unintended effects                                    |  YES |       |       |
| 20  | Limitations: bias, imprecision, multiplicity                |  YES |       |       |
| 21  | Generalizability (external validity)                        |  YES |       |       |
| 22  | Interpretation balancing benefits/harms/other evidence      |  YES |       |       |
| 23  | Trial registration (registry + number)                      |  YES |       |   NA  |
| 24  | Full protocol access                                        |  YES |       |       |
| 25  | Funding sources & role of funders                           |  YES |       |       |

---

## B. CONSORT-AI Extension (report **in addition** to CONSORT 2010) - SPECIFIC to AI models:

| # (AI)   | AI-specific consideration                            | Done | Where | Notes |
| -------- | ---------------------------------------------------- | ---: | :---- | :---- |
| 1a/b(i)  | Title/abstract: say it’s AI/ML; specify model type   |  [ ] |       |       |
| 1a/b(ii) | Title/abstract: state intended clinical task/use     |  [ ] |       |       |
| 2a(i)    | Intended use in clinical pathway; intended users     |  [ ] |       |       |
| 4a(i)    | Participant-level inclusion/exclusion                |  [ ] |       |       |
| 4a(ii)   | **Input-data** inclusion/exclusion                   |  [ ] |       |       |
| 4b       | Site integration (hardware/software/IT dependencies) |  [ ] |       |       |
| 5(i)     | Algorithm **version** used (changes, if any)         |  [ ] |       |       |
| 5(ii)    | Input acquisition/selection/**pre-processing**       |  [ ] |       |       |
| 5(iii)   | Handling **poor-quality/missing** inputs             |  [ ] |       |       |
| 5(iv)    | Human–AI input workflow; training/expertise          |  [ ] |       |       |
| 5(v)     | AI **output** type (probability/class/alert/action)  |  [ ] |       |       |
| 5(vi)    | How outputs inform decisions; thresholds/rules       |  [ ] |       |       |
| 19       | Error/performance-failure analysis (or justify none) |  [ ] |       |       |
| 25       | Access to system/code; reuse restrictions            |  [ ] |       |       |

---

### Tips

* For AI trials, document data flow, human oversight, and any site-specific constraints that affect deployment or external validity.
