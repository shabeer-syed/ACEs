---
title: Implemetation and code lists
---

### [Go back](https://shabeer-syed.github.io/ACEs/)

## Code lists and measures of ACEs
--------------------------------------------

For GP records, we define indicators by combining information recorded in Read codes, prescriptions, referral fields and validated self-report measures (continuous variables needing re-coding) routinely administered by GPs or nurses (e.g. alcohol use).

For hospital and death registration records, we define indicators by combining codes from the International Classification of Diseases 9th/10th edition (ICD-9/10), the Classification of Interventions and Procedures (OPCS-4) and HES-APC discharge/admission fields.

Unless specified, indicators refers to information recorded in both child and maternal records.

Multiple different rule-based algorithms must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions (bone diseases), traumatic birth injuries or maternal-child transmissions during birth (see below).

## Download code lists
--------------------------------------------

Right click on link to save as a ".txt" file (i.e. using option "save link as")

*Total number of included ACE codes: 8802 (ACEs) + 8808 (covariates)*

*Total number of excluded/tested codes: 7671*

### All ACE indicators:

* #### [All ACEs (8802)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/ALL_ACEs.txt)
* #### [All ACEs + crossmapped SNOMED CT and ICD-11 (9563)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/All_ACEs_with_crossmaped_snomedCT_icd11_non_validated.txt)
* #### [All ACEs GP/CPRD only: medcodes, prodcodes, measures only (6641)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/ALL_ACEs_medcode_product_only.txt)
* #### [All ACEs Hospital only: ICD, OPCS and HES-APC specific fields (2161)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/ALL_ACEs_ICD_OPCS_only.txt)

### By ACE domain:

* #### [Child maltreatment (1290)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/CM_ACEs.txt)

* #### [Maternal intimate partner violence (450 + 503 for assault algorithm)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/mIPV_ACEs.txt)

* #### [High-risk presentation of CM (802)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/HRP_CM_ACEs.txt)

* #### [Adverse family environment (701)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/AFE_ACEs.txt)
* #### [Maternal mental health problems (3966)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/mMHPs_ACEs.txt)
* #### [Maternal substance misuse (1090)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/MSM_ACEs.txt)

#### [Covariates: non-ACEs used to add information to risk prediction models (8808)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Health%20comorbidities.txt)

### Code lists for rule-based exclusions
* #### [Accidents (2017)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Accidents.txt)
* #### [Osteoporosis - Bone disease (406)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Osteoporosis%20Bone%20disease.txt)
* #### [Birth injuries or traumatic complications (238)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Birth%20injury%20or%20complication.txt)
* #### [Mother-to-child-transmissions (15)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Mother-to-child%20transmission.txt)

## Code list data dictionary

 | Provided variable | Description | 
 | --- | --- | 
 | **Code** | Original code as entered into respective system (removed punctuations, adds prefixes: *"d_"* to prodcodes and *"e_"* to OPSC-4). Prefixes prevents de-duplication as different systems may use the same code for different descriptions. | 
 | **Coding term** | Original code description |
 | **Indicator code** | Indicator code name | 
 | **Indicator specific** | Most specific indicator |
 | **Indicator 1** | Main ACE indicator combining multiple codes or measures as used in  validation paper | 
 | **Indicator 2** | Broader ACE indicator combining multiple codes or measures |
 | **Domain** | ACE domain grouping all indicators together (applicable for the overall code list) | 
 | **Severity** | Where applicable, this variable indicates the severity classification of the code description. *e.g. For alcohol misuse, "mild", "moderate", "severe".* |
 | **Scale** | `1`=Indicates that the code and severity classifications are dependent on extra clinical information (e.g. frequency of alcohol consumption). By default, this is set to *"Mild"* for alcohol. See rule-based algorithms. |
 | **Reference** | `1`=code is part of family violence reference standard, `2`=code can be used as a broader measure of family violence |
 | **Individual** | `1`=code applies to child only, `2`=code applies to mother only, 3=code applies to mother or child (i.e. either), `4`=code only applicable to female children |
 | **Coding systems** | `GP/primary care:` Read, OXMIS, Prodcode (prescriptions or items), CPRD REFERRAL FHSASPEC (field specific), CPRD REFERRAL NHSSPEC (field specific). `HES-APC/secondary care/ONS:` ICD-10, OPCS-4, ICD-9 (applies to ONS < year 2000), HES-APC DISDEST OR ADMISORC (field specific) |

## Example

| Code | Coding  term  | Indicator 1 | Indicator 2 |  domain | severity | scale | reference | individual | coding system |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 912 | [D]Anorexia	Anorexia | Anorexia | Eating disorders | Maternal mental health problem | diagnostic |  |  | 2 | Read | 

## Suggested implementation of indicators
--------------------------------------------

Whilst most indicators are ready for use in your dataset (e.g. via merging a code list), some indicators requires rule-based algorithms as listed below. 

### Brief outline
//1. Merge each specific code list or the complete ACEs code list with your data file containing the target population (e.g. correct ages for children/mothers):
![alt text](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/merge%20codelist.png)

//2. Convert continuous measures to binary indicators by applying/"filtering" using the additional "cut-off" variable provided (i.e. data > cut_off)

e.g. Example "one liner" in R or Python with dplyr:

 `e.g. mmhps_alcohol <- merged_data %>% filter(Domain=="mMHPs" & Indicator 1=="Alcohol misuse" & scale=="1" & data1 > cut_off)`

//3. More advanced [control flow methods](https://adv-r.hadley.nz/control-flow.html) are required to apply multiple rule-based algorithims (age critera, accident exclusions etc) and to achieve faster implementation. Control flow (data dependent "if then assumptions") are widley covered by the data science community ([1](https://adv-r.hadley.nz/control-flow.html) [2](https://advanced-r-solutions.rbind.io/control-flow.html)).

* ## [Download introductory tutorial here](https://github.com/shabeer-syed/ACEs/raw/main/ACEs%20implementation%20tutorial.pdf)

## Rule-based algorithms

![alt text](https://cdn-coiao.nitrocdn.com/CYHudqJZsSxQpAPzLkHFOkuzFKDpEHGF/assets/static/optimized/rev-46bfc56/wp-content/uploads/2021/03/r-case_when-multiple-cases-syntax.png)

 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **MSM, Alcohol misuse Severe** | Include if continuous data meets the cut-off assigned to each code (see code list): e.g. AUDIT: ≥20; AUDIT-PC: ≥10; SADQ ≥31; ≥35 alcohol units per week (analogous to higher-risk drinking/harmful drinking/alcohol dependence; see NICE guidelines); >200 mg alcohol per 100 ml blood is classed as potential high-risk offender when driving in England/Wales (see UK gov) (applies to hospital admission codes in this study). | `mmhps_alcohol <- merged_data %>% filter(Domain=="mMHPs" & Indicator_1=="Alcohol misuse" & scale=="1" & data1 > cut_off)`| 
 | **mMHPs, Depression** | Include if continuous data meets the cut-off assigned to each code (see code list): e.g. DASS-21 (sub-scales): ≥14; EDPS: ≥13; HADS (sub-scale): ≥11; HDRS (sub-scale): ≥ 14; PHQ-9: ≥10; SDS (Zungs's): ≥50 | `mmhps_depres_anx <- merged_data %>% filter(Domain=="mMHPs" & scale=="1" & data1 > cut_off)` | 
 | **mMHPs, Anxiety** | Include if continuous data meets the cut-off assigned to each code (see code list): e.g DASS-21: ≥10; HADS (sub-scale): ≥11; HDRS (sub-scale): ≥18; SAS (Zungs's):  ≥45 score; GAD-7: ≥8 | `as above.` | 
 | **Anxiety or depressive symptoms, antidepressants or anxiolytics and mental health service referral/interventions received** | Codes referring to anxiety symptoms (e.g., worrying) or depression (e.g. “feeling low”) were only considered a case of depression or an anxiety disorder when the patient was also given antidepressants and/or anxiolytic medication within 3-months or initiated psychological treatment  within 2-years. Comparison estimates for mothers in CPRD-MBL with and without this algorithm are provided by Abel et al.61
 Rule: Include symptoms/medications as an anxiety or depression indicator, if a previous diagnostic code or tier 3 intervention code exists (within 2-years), or if there is a co-occurrence of a prescription consistent with a symptom within 3-months (e.g. anxiolytics &  anxiety symptoms).62 | `mmhps_depres_anx <- merged_data %>% filter(Domain=="mMHPs" & scale=="1" & data1 > cut_off) | 
 | **CM, FGM** | Apply codes mentioning circumcision to female children only (e.g. "54314 - routine or ritual circumcision"). Code list includes markers for rule inclusion. | 
 | **Susp.mIPV, Assault NOS (algo); mIPV NOS (Assault and high-risk algo, 30/100 days)** | Include as mIPV  if assault recording co-occurs with any “high-risk presentation recording” 30 days before the assault or in 100-days post the assault recording. High-risk recordings are a composite variable of recordings related to parental conflicts, health visitors being sent to the home, nurse partnership referrals, superficial head injuries and bruises. We developed the composite variable using results from our systematic review.51  In the current study the algorithm showed PPVs ranging from 18%-30% of definitive mIPV (derivation cohort). |
 | **mIPV, Assault NOS (algo), mIPV NOS (Assault and preg. incident and CM algo, 45 days)** | Include as mIPV if assault recording co-occurs with any recordings of a safeguarding referral, child protection recording, or definitive CM indicator, or “pregnant state, incidental” (marked in codelist) within 45 days of the assault. UK guidelines state 45 days is the maximum timeframe for an initial outcome following a children’s social care assessment from the date of received safeguarding referral (see point 82, “working together to safe guard children”).49 | 
 | **HRP-CM, Child harm by undetermined intent; Lacerations, scars and abrasions; Thermal injuries; Unknown and unspecified causes of morbidity in child;Other and unspecified abdominal pain; Unspecified event in child, Obs for other suspected diseases and conditions in child** | Include as HRP-CM when excluded co-occurring accident-related injuries recorded within +/-15 days of the event. Time frame selected based on the median time difference between data sources for some accidental injuries.  NICE Clinical guideline [CG89]: 1.1.1-1.1.8; 1.1.15; 1.2.4, 1.2.5;  1.2.13 | 
 |**HRP-CM, Eye trauma, NOS;Subarachnoid haemorrhage other; Subdural haematoma/retinal haemorrhage; Fractures, Intra-abdominal injuries, spinal injuries,  intracranial** | Include as HRP-CM when excluded co-occurring accident-related injuries recorded within +/-15 days of the event, and when excluded birth-related injuries recorded <2 days post birth. NICE Clinical guideline [CG89]: 1.1.11; 1.1.10 |
 |**HRP-CM, Fractures, Intra-abdominal injuries, spinal injuries,  intracranial** | Include as HRP-CM when excluded co-occurring accident-related injuries recorded within +/-15 days of the event, and when excluded birth-related injuries recorded <2 days post birth, and when excluded children with fragile bone disease (Osteoporosis), unless definitive CM is recorded within +/-30 days . NICE Clinical guideline [CG89]: 1.1.9; 1.1.12;  1.1.13 |


[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/home%20view%20indicators.png)](https://shabeer-syed.github.io/ACEs/Indicators) | [![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/code%20lists.png)](https://shabeer-syed.github.io/ACEs/codelist)

### [Go back](https://shabeer-syed.github.io/ACEs/)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>