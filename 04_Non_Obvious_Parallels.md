Here are 7 non-obvious parallels between the RCT ideas → the AI translation → what to do. But just the way, we plan for these events in RCTs 
especially in the SAPs - i.e., the Statistical Analysis Plans), we should plan for them during an AI model development and deployment.

1. Estimands ≠ Metrics

* **RCT**: ICH E9 forces us to declare the population, treatment, endpoint, and events handling. Which is hard, but necessary.
* **AI**: This is a good practice: Replace “accuracy only using AUC” with a decision-centric questions: for whom, under what use, what payoff/costs, what happens when users don’t comply.
* **Do**: Write a one-liner for your AI (population, decision, why and at what cost/benefit, and what events like overrides/dropouts/alerts ignored) and ensure eval + deployment logs match it.

2. Events ↔ Real Frictions - 
 Events that might suddenly happen that we MUST prepare for and deal with at both patient level/analysis level during RCTs - some examples:

* **RCTs**:
  - Discontinuation/interruption of assigned treatment (toxicity, intolerance, patient preference).
  - Non-adherence (missed doses, partial compliance - happens all the time).
  - Events that preclude outcome measurement.
  - Data capture failure (say, EHR field missing).
  - Loss to follow-up/withdrawal of consent (no endpoint obtained).
  - Missed visits/late assessments (endpoint timing off the window).
  
* **AI**: Every event listed above can happen during AI product implementation and these change what your performance means.
* **Do**: Pre-specify how you’ll handle each event and show it (and consquences) in the offline evaluation and post-deployment dashboards.

3. Analysis sets (ITT / per-protocol) ↔ Use-based evaluation

* **RCT**: ITT (as randomized) vs per-protocol (compliers only) tell different stories and usually show very different results.
* **AI**: Evaluate as-exposed (all cases where the model COULD have acted) vs as-used (where users actually engaged) vs per-protocol (correctly followed recommendations).
* **Do**: Report all three. Expect “as-used” to be not so good and this is our implementation gap and a target for UX/process changes—not just model tuning.

4. Minimal Clinically Important Difference (MCID) ↔ Decision thresholds

* **RCT**: Power is set on an effect size that clinically matters, not just significance (which is an empty measure if not use with consideration).
* **AI**: Pick yardsticks that maximize net benefits given false-positive/negative costs and not just max AUROC (i.e. do not go by power and AUC metric but supplement with something more meaningful. 

5. Multiplicity control ↔ Hyperparameter/search/metric discipline

* **RCT**: Multiple endpoints/subgroups inflate Type I error; we should pre-specify primary vs exploratory.
* **AI**: You run tons of experiments (features, models, metrics, segments). Without discipline it’s a garden-of-different-paths.
* **Do**: Pre-register a primary metric & segment; shortlist secondaries; separate exploratory from confirmatory; control false discovery (imp).

6. External validity & transportability ↔ Data coverage + shift management 

* **RCT**: Eligibility criteria, site mix determine generalizability.
* **AI**: Detecting Dataset shift (critical to keep track of else predictions will be wrong with no one the wiser).
* **Do**: Report who/where/when the data come from (as mentioned in another article - if we don't know the mix of the data, we don't know whether the model has a chance)
* set triggers for revalidation (say) and/or calibration of sites to ensure that it remains same (or triggers if it changes drastically).

7. Safety monitoring, stopping rules, & DMC ↔ Guardrails + change control

* **RCT**: Data Monitoring Committee, predefined stopping for benefit/futility/harm. RCTs take these very seriously and with good reason. If a treatment is bad and it's known immediately, it's unethical to continue, obviously.
* **AI**: Live systems need harm dashboards (over-alerting, workload spikes, equity gaps), rollback plans, and a change-advisory process for model updates (not sure if it is possible to anticipate all possible issues, but a plan is a good idea).
* **Do**: Define leading indicators (e.g., false-positive workload per shift, treatment delays), auto-alerts for drift/harm, and pre-approved rollback (previous model, safe default policy). Treat model updates like **protocol amendments** with impact notes.

