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

* From 1932–1972, the U.S. Public Health Service ran the Tuskegee Study in Macon County, Alabama, observing Black men with syphilis without informed consent and withholding effective treatment — even AFTER penicillin became the standard of care in the mid-1940s. Participants were misled, enticed with meals and burial insurance, and monitored for autopsies. The study ended  after whistleblower (Peter Buxtun) expressed concerns to the press (AP’s Jean Heller), triggering public outrage, a federal investigation, a settlement, and reforms including informed-consent, IRBs, and the Belmont Report. In other words - oversight. 

* Parallels to AI aren’t about an algorithm “going wrong” so much as **systems going wrong**: deception or non-consent, unequal burden on a vulnerable group, withholding benefits, and weak oversight. The lesson for AI is clear—**no deployment without informed consent (where applicable), independent ethics review, community oversight, transparent risks/benefits, and stop rules**. These are precisely the kind of failures that AI projects must design against.

* **Mistake**: Denial of treatment to African American men.
* **Bias**: Racially exploitative study design.
* **Impact**: Long-term health consequences and widespread mistrust in medical institutions.
* **Citation**: Jones, J. H. (1981). *Bad Blood: The Tuskegee Syphilis Experiment.*

### 3. **Statins and Asians**

* There was a history of “one-size-fits-all” dosing built on largely non-Asian trial data, later corrected by PK/genetic evidence. Many lipid-lowering RCTs historically had limited Asian enrollment, so early dosing guidance mostly extrapolated from Western cohorts. Asians show ~2× higher exposure to rosuvastatin on average; the FDA label now recommends a **5 mg starting dose** for Asian patients. Reviews and trials reported that **lower statin doses** often achieve comparable LDL-C reductions in Asians vs. higher doses in Whites—evidence that earlier uniform dosing likely overdosed some Asian patients. 

* **Mistake**: Underestimated dose sensitivity.
* **Bias**: Poor inclusion of Asian populations in trials.
* **Impact**: Higher side effects; later led to revised dosing.
* **Citation**: Zhou et al. (2017). *Australian Prescriber, 40(3), 90–92.*

---

## Part II: Major AI Bias Cases and Their Parallels

### 1. **COMPAS Algorithm in Criminal Justice**

* **Issue**: Black defendants were more likely to be labeled high-risk and not reoffend, revealing disparate false-positive rates. Overestimated risk for Black defendants.
* **Parallel**: Misuse of race as a categorical variable.
* **Citation**: Angwin et al. (2016). *ProPublica.*

### 2. **Facial Recognition Bias**

* **Issue**: Error rates were much higher for darker-skinned women than for lighter-skinned men, showing stark intersectional disparities. Misidentification of darker-skinned faces.
* **Parallel**: Thalidomide—testing failures led to population-specific harm.
* **Citation**: Buolamwini & Gebru (2018). *Gender Shades.*

### 3. **Healthcare Risk Scoring Bias**

* **Issue**: Using spend as a proxy for illness under-referred Black patients with equal disease burden; fixing the target variable dramatically reduced bias. Parallel: statins lesson—train on the right signal/population. Used cost as a proxy for need, disadvantaging Black patients.
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

