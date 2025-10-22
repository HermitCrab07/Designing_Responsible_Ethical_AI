# Compilation of Case Studies: Historical Bias in Drug Development and Modern AI

## Introduction

Bias in decision-making systems—whether pharmacological or algorithmic—has led to significant harm, especially for marginalized groups. This document outlines several well-documented failures in drug development and AI deployment, illustrating how inadequate representation, flawed data, and lack of oversight have shaped ethical concerns across both domains.

---

## Part I: Drug Development Disasters Due to Bias

### 1. **Thalidomide (1950s–1960s)** 

* The Lancet in 1961 published a letter to the editor that mentioned an increased incidence of congenital abnormalities in babies delivered by women who took thalidomide during pregnancy as an antiemetic - i.e., to stop from themselves from throwing up. It is an understatement to say that the children had 'abnormalities'. The horrific harm can only be understood by seeing images of these poor children. Thalidomide worked in general but failed in a subgroup of women with terrible harm. Amazingly enough, a woman in the US stopped Thalidomide from being prescribed because she said there wasn't enough data that it was safe. Thus began the FDA.

* In AI too, a model can look perfect overall yet harm a specific subgroup (say age, pregnancy, comorbidities, language, device type). Pregnant women were effectively an untested population. In AI, missing data for certain groups (rare diseases, low-resource languages) creates blind spots. The evaluation set must reflect the **deployment** population, not just the development data. For AI, defining “high-risk cohorts” is just as critical as in drugs. Drug safety is tracked by ongoing pharmacovigilance. For AI - we can use drift detection, fairness & safety dashboards, fallbacks, rollback pathways, and scheduled re-evaluations with fresh data. There should also be safety-critical contexts - i.e., human-in-the-loop overrides, and an off-switch tied to pre-agreed triggers. 

* **Mistake**: Prescribed to pregnant women without testing for teratogenic effects.
* **Bias**: Lack of safety evaluation in pregnant populations.
* **Impact**: 10,000+ children born with limb malformations globally.
* **Citation**: McBride, W. G. (1961). *The Lancet, 278(7216), 1358.*

### 2. **Tuskegee Syphilis Study (1932–1972)**

* From 1932–1972, the U.S. Public Health Service ran the Tuskegee Study in Macon County, Alabama, observing Black men with syphilis without informed consent and withholding effective treatment — even AFTER penicillin became the standard of care in the mid-1940s. Participants were misled, enticed with meals and burial insurance, and monitored for autopsies. The study ended only after whistleblower (Peter Buxtun’s) concerns reached the press in 1972 (AP’s Jean Heller broke the story), triggering public outrage, a federal investigation, a settlement, and reforms including informed-consent rules, IRBs, and the Belmont Report.

* Parallels to AI aren’t about an algorithm “going wrong” so much as **systems going wrong**: deception or non-consent, unequal burden on a vulnerable group, withholding benefits, and weak oversight. The lesson for AI is clear—**no deployment without informed consent (where applicable), independent ethics review, community oversight, transparent risks/benefits, and stop rules**. These are precisely the kind of failures that AI projects must design against.


* **Mistake**: Denial of treatment to African American men.
* **Bias**: Racially exploitative study design.
* **Impact**: Long-term health consequences and widespread mistrust in medical institutions.
* **Citation**: Jones, J. H. (1981). *Bad Blood: The Tuskegee Syphilis Experiment.*

### 3. **Exclusion of Women in Clinical Trials**

* **Mistake**: Systematic exclusion of women, especially of childbearing age.
* **Bias**: Male-centric efficacy and dosage baselines.
* **Impact**: Miscalibrated treatment outcomes and increased adverse events in women.
* **Citation**: Pinnow et al. (2009). *Journal of Women's Health, 18(6), 1043–1050.*

### 4. **BiDil (2005)**

* **Mistake**: Approved exclusively for African Americans without comparative trials.
* **Bias**: Oversimplified racial categories.
* **Impact**: Reinforced race-based medicine debates.
* **Citation**: Kahn, J. (2004). *Yale Journal of Health Policy, Law, and Ethics, 4(1), 1–46.*

### 5. **ACE Inhibitors and African Americans**

* **Mistake**: Overgeneralized efficacy across populations.
* **Bias**: Limited inclusion of Black patients in hypertension trials.
* **Impact**: Poorer cardiovascular outcomes and inadequate treatment adjustments.
* **Citation**: Ferdinand, K. C. (2006). *Cardiovascular Drugs and Therapy, 20(2), 139–146.*

### 6. **Tamoxifen**

* **Mistake**: Overlooked pharmacogenomic variability.
* **Bias**: CYP2D6 enzyme variability across ethnicities.
* **Impact**: Reduced efficacy in Asian women.
* **Citation**: Kiyotani et al. (2012). *Drug Metabolism and Pharmacokinetics, 27(1), 122–131.*

### 7. **Statins and Asians**

* **Mistake**: Underestimated dose sensitivity.
* **Bias**: Poor inclusion of Asian populations in trials.
* **Impact**: Higher side effects; later led to revised dosing.
* **Citation**: Zhou et al. (2017). *Australian Prescriber, 40(3), 90–92.*

### 8. **Gleevec (Imatinib)**

* **Mistake**: Ignored mutation variability across populations.
* **Bias**: Trials focused on Western cohorts.
* **Impact**: Reduced efficacy in underrepresented groups.
* **Citation**: Druker et al. (2006). *NEJM, 355(23), 2408–2417.*

---

## Part II: Major AI Bias Cases and Their Parallels

### 1. **COMPAS Algorithm in Criminal Justice**

* **Issue**: Overestimated risk for Black defendants.
* **Parallel**: Misuse of race as a categorical variable.
* **Citation**: Angwin et al. (2016). *ProPublica.*

### 2. **Amazon’s AI Hiring Tool**

* **Issue**: Penalized resumes with women-related keywords.
* **Parallel**: Exclusion of women in clinical trials.
* **Citation**: Dastin, J. (2018). *Reuters.*

### 3. **Apple Card Gender Disparity**

* **Issue**: Women received lower credit limits despite similar profiles.
* **Parallel**: Mirrors ACE inhibitor issue—neglect of demographic-specific analysis.
* **Citation**: Zaveri & Guynn (2019). *USA Today.*

### 4. **Facial Recognition Bias**

* **Issue**: Misidentification of darker-skinned faces.
* **Parallel**: Thalidomide—testing failures led to population-specific harm.
* **Citation**: Buolamwini & Gebru (2018). *Gender Shades.*

### 5. **Healthcare Risk Scoring Bias**

* **Issue**: Used cost as a proxy for need, disadvantaging Black patients.
* **Parallel**: Like statins—failure to adjust for group-level difference.
* **Citation**: Obermeyer et al. (2019). *Science.*

---

## Key Takeaways

### 1. Flawed Data and Representation

Both fields have been shaped by biased data collection—whether through homogeneous clinical trials or skewed AI training data.

### 2. Harm to Vulnerable Populations

Underrepresented groups—women, minorities, or low-income populations—suffer most when systems fail to account for diversity.

### 3. Ethical Oversight and Regulation

Robust frameworks like the FDA’s clinical trial rules and AI ethics guidelines (e.g. OECD, GDPR) are essential to prevent repeat harms.

## Conclusion

The parallels between biased drug development and biased AI are real and as dangerous. Both fields require a shared commitment to inclusion, transparency, testing across groups, and responsible regulation. Past failures tell us we must build fairer and safer systems.

