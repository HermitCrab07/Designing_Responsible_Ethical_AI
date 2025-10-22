# How To Use the Structure and Rigor of RCTs (Randomized Clinical Trials) to ship AI better, safer, and faster

## Summary

We ship AI faster when we borrow fundamental habits from RCTs: a single primary question, pre-specifying the evaluation of the models, and monitoring the harms. 


## Overview

This document looks at parallels between randomized controlled trials (RCTs) in drugs (or say interventions) development - something I have spent years doing - and ethical, responsible AI system design. Although these domains may appear very different at first glance, they are not. As I found out while working in AI and product development in AI - they share a deep, structural resemblance, which is why it occurred to me that if we followed a "Checklist" of designing and implementing a great RCT (as we had to do during every clinical trial throughout my career) it would be immensely useful in executing a great AI project as well.

## Background: 

To give a little background, RCTs are conducted in many different areas of research, but I'm mostly familiar with biomedical research, so I'll stick to that. Now while AI is grounded in data and computation, RCTs are grounded in creation of drugs in labs then testing through what is referred to as Phase I/Phase II/Phase III where... 

That said, both have incredible parallels from start to finish. The fundamental truth is that both are high-stakes attempts to intervene and improve human lives, therefore the consequences - if these are not designed and executed well - can impact humans in a extremely negative way. To ensure fairness, efficacy, safety, and transparency, both must contend with more or less the same set of consequences - for example: bias and unintended harm. Finally, and obviously, both must be planned and implemented well. 

RCTs have been under the scrutiny of the FDA for years therefore, the regulatory compliance is well established. Every step we took from the design to randomization or the statistical analysis plan to the final unblinding and results, had to follow SOPs (Standard Operating Procedures). The thing is - whereas RCTs have been executed under a myriad of rules and regulations, AI is only beginning to anticipate problems and design the oversight. 

This is where the difference is. 

Now let's take a preliminary look at the parallels:

## Fundamental Thematic Parallels: Clinical Trial vs. Responsible AI Design 

| Clinical Trial Design               | Responsible AI Design                  |
| ----------------------------------- | -------------------------------------- |
| 1. Define medical hypothesis        | 1. Define task or objective            |
| 2. Identify target population       | 2. Identify user groups                |
| 3. Literature & data review         | 3. Literature & dataset review         |
| 4. Trial design (RCT)               | 4. Model design and pipeline setup     |
| 5. Inclusion/exclusion criteria     | 5. Data collection & sampling          |
| 6. IRB ethics review                | 6. AI ethics review or audit           |
| 7. Trial execution                  | 7. Model training                      |
| 8. Monitor adverse effects          | 8. Monitor algorithmic bias            |
| 9. Analyze outcomes                 | 9. Evaluate model performance          |
| 10. Regulatory approval             | 10. Transparency and explainability    |
| 11. Post-market surveillance        | 11. Post-deployment monitoring         |
| 12. Iteration based on new findings | 12. Retraining and ongoing refinement  |

---

### 1. Defining the Objective/Problem

* **Primary Question:** It's critical to nail down a single primary question that has to be measured on a specific population, in a defined time window, using a specific outcome. For example, does deploying model X reduce problem Y within a certain period of time among adults discharged after a certain procedure Z? We must be specific with respect to what it is, what it answers, why it does not answer, why it is important to be answered, how it is measured, how variable it is, how much missing data there will be, during what time frame it is best collected, and if it best shows the effect we want it to show, and using what outcome. This is often far more complex that it appears.

* **Similarly, in AI Development:** defining the problem clearly — say, predicting readmission within a month after a patient who presented with diabetes at the hospital is discharged from the hospital - is critical. Once the specificity is nailed down with respect to time, measurement, variability, missingness, it makes everything much, much easier. Poor problem definition often leads to downstream ethical and practical failures. 

### 2. Identifying Target Population

* **Clinical Trials** design trials around a population of interest, ensuring appropriate group representation. For example, models predicting risk of a heart disease in US will be different compared to models predicting risk of heart disease in Japan, though both models are predicting the risk of heart disease. Furthermore, if the model is developed on white men in the US, it is not necessarily going to perform well on (say) white women. If the model should predict well on men and women, the model should be developed on  men and women. Do we have proper representation when we're choosing people to test the drug on? In many drug trials, women, older adults, minorities have historically been left out. What then is the accuracy of the models on these unrepresented groups?

* The most important problem in this situation is that when we're using the models, we DO NOT KNOW the data the models were developed on. For instance, were women in the training data? Were different ethnicities? If not, we will get wrong predictions but NOT KNOW they are wrong. Just as pharmacogenomics can affect how individuals metabolize drugs, demographic and social factors influence how drugs and AI systems interact with users. Thus, drugs are tested across subgroups to catch population-specific effects. 

* **Similarly, in AI Development** We must define who the AI system is meant to serve. This tells you what data should be collected and how the model should be evaluated. AI systems must be stress-tested for fairness and performance across demographic slices, i.e., subgroup analysis is essential in either domain. Systematic bias can occur at the design level without careful scrutiny. Therefore, it's critical that the drug and AI model be developed on the data on which the final predictions will be used. In AI, if we're not careful, training datasets will often reflect the dominant group, which needless to say, is a problem. Training data MUST reflect the data on which the model is supposed to predict. Representative data is not a "nice to have" - it’s basic to efficacy and safety. 

### 3. Reviewing Existing Literature and Data

* **Clinical Trials:** This is self-explanatory. Literature reviews are critical while setting up hypotheses to avoid redundant or harmful trials and experimentation. This is the time to understand all previous trials that have been done, on what populations, what results were obtained, and what the flaws and gaps existed in these trials. 

* **Similarly, in AI Development** Avoid reintroducing bias by understanding existing data limitations, past failures, and known methodological critiques.

### 4. Study Design vs. AI Model Design

* **Clinical Trials**: Randomization, control arms, and blinding reduce bias.
* **AI Development**: Model design choices (e.g., supervised vs. causal inference approaches) play a similar role. Thoughtful train-test splits, synthetic controls, or counterfactual models are tools to minimize bias and overfitting.

### 5. Inclusion Criteria vs. Data Collection

* **Clinical Trials**: Inclusion/exclusion criteria define who participates. In Phase I trials we establish safety and tolerability to find the Maximum Tolerated Dose. When the drug moves to Phase II, the goal is to show preliminary efficacy and estimate an effect size to justify a Phase III (which is much larger and far more expensive). Efficacy-oriented Phase II trials use narrow inclusion and stricter exclusions (in other words, homogeneous patient groups, low and/or controlled comorbidities and concomitant meds) to maximize internal validity and detect a clean treatment signal. Phase III trials are Effectiveness and pragmatic trials and these use broad inclusion with minimal exclusions (diverse patients, usual care, flexible workflows) to maximize external validity and estimate real-world impact.
  
* **AI Development**: Efficacy vs. effectiveness is an important question when evaluating AI models as well. Though we may develop AI models on narrow inclusion and strict exclusion, at some point, the AI model might be evaluated on the broad inclusion with minimal exclusion criteria. It's the only way to assess and estimate real world impact. It's one thing to do maximize internal validity and quite another to check for external validity. 

### 6. Ethics Review

* **Clinical Trials**: Self-explanatory. Require IRB approval to ensure patient safety, consent, and scientific validity.
* **AI Development**: Similarly, an analogous process should include ethical review boards, impact assessments, and pre-launch audits.

### 7. Trial Execution vs. AI Training

* **Clinical Trials**: Self-explanatory. Data collection follows strict protocol.
* **AI Development**: Training must be conducted under rigorous, replicable conditions, with safeguards against data leakage or biased loss functions.

### 8. Adverse Effects vs. Bias Monitoring

* **Clinical Trials**: Self-explanatory. Trials pause if harms are detected.
* **AI Development**: Models must be monitored for discriminatory or harmful outputs, both during development and after deployment.

### 9. Data Analysis and Outcome Assessment

* **Clinical Trials**: Self-explanatory. Outcomes evaluated with predefined metrics, often stratified by subgroups.
* **AI Development**: Models must be evaluated using disaggregated metrics (e.g., fairness across race, gender, age).

### 10. Regulatory Approval vs. Transparency

* **Clinical Trials**: No drug is released without approval by regulatory bodies. Drug development is tightly regulated. AI is moving slowly toward similar scrutiny through emerging standards, ethics boards, and government frameworks.

**Parallel**: Oversight ensures accountability. Without it, safety, fairness, and trust erode.
* **AI Development**: Increasingly, AI systems are expected to be auditable, interpretable, and transparent before deployment.

### 11. Post-Market Surveillance

* **Clinical Trials**: Monitor for long-term effects in the real world. 

Clear communication is required in drug trials (methodology, side effects, outcomes). Similarly, AI models must be interpretable—especially in healthcare, finance, and criminal justice. Drug developers must balance benefit vs. risk. AI developers face a similar responsibility, especially when systems can deny access to healthcare, employment, or justice.

**Parallel**: Both must design with vulnerable populations in mind and prioritize harm reduction. Without transparency and explainability, trust collapses—whether in doctors, patients, users, or regulators. 
* **AI Development**: Track model drift, unfair outcomes, or new failure modes in production environments.

### 12. Iteration and Retraining

* **Clinical Trials:** New findings often lead to revised trials - post-Deployment Monitoring and Feedback. Neither a drug nor an algorithm is ever "done." Both require surveillance, feedback loops, and the willingness to adjust when harm emerges. Ongoing refinement is not optional — it's core to ethical practice.

* **Similarly, in AI Development:** Continuous feedback and retraining ensure AI systems remain fair and effective as real-world data evolves.

---

## Conclusion

The similarities between randomized clinical trial design and AI development are not metaphorical — they are structural. Each step in one domain has a parallel in the other, grounded in the need to deliver safe, fair, and effective interventions that changes to human lives. Thus, both demand careful planning, ethical oversight, and rigorous testing, and continuous refinement, both require awareness of bias and a deep commitment to justice. Finally, both, ultimately, are systems of trust: trust that the product - whether it is a pill or a model — has been built with care, tested with rigor, and deployed with responsibility. 

We would do well to apply the rigors of RCTs to AI model development and deployment. 



References:
- ICH E9(R1) on estimands & handling intercurrent events.
- CONSORT 2010 statement (trial reporting discipline).
- CONSORT-AI extension (AI-specific considerations).
- RECOVERY trial write-up (clean primary endpoint & pragmatic design).
- ISPOR/HTA basics on outcomes and decision rules.

