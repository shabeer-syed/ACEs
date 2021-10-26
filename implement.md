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

* ### [All ACEs (8802)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/ALL_ACEs.txt)
* ### [All ACEs + crossmapped SNOMED CT and ICD-11 (9563)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/All_ACEs_with_crossmaped_snomedCT_icd11_non_validated.txt)

### By ACE domain:

* ### [Child maltreatment (1290)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/CM_ACEs.txt)

* ### [Maternal intimate partner violence (450 + 503 for assault algorithm)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/mIPV_ACEs.txt)

* ### [High-risk presentation of CM (802)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/HRP_CM_ACEs.txt)

* ### [Adverse family environment (701)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/AFE_ACEs.txt)
* ### [Maternal mental health problems (3966)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/mMHPs_ACEs.txt)
* ### [Maternal substance misuse (1090)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/MSM_ACEs.txt)

### [Covariates: non-ACEs used to add information to risk prediction models (8808)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Health%20comorbidities.txt)

### Code lists for rule-based exclusions
* ### [Accidents (2017)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Accidents.txt)
* ### [Osteoporosis - Bone disease (406)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Osteoporosis%20Bone%20disease.txt)
* ### [Birth injuries or traumatic complications (238)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Birth%20injury%20or%20complication.txt)
* ### [Mother-to-child-transmissions (15)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Mother-to-child%20transmission.txt)

## Code list data dictionary
 | Command | Description |
 | --- | --- |
 | `git status` | List all *new or modified* files |
 | `git diff` | Show file differences that **haven't been** staged |


## Code list data dictionary
--------------------------------------------

*  `Code`: Original code as entered into respective system (removed punctuations, adds prefixes: "d_" to prodcodes and "e_" to OPSC-4). Prefixes prevents de-duplication as different systems may use the same code for different descriptions.
*  `Coding term`: Original code description
*  `Indicator code`: Indicator code name
*   `Indicator specific`: Most specific indicator
*  `Indicator 1`: Main rACE indicator combining multiple codes or measures as used in  validation paper
*  `Indicator 2`: Broader ACE indicator combining multiple codes or measures
*  `Domain`: ACE domain grouping all indicators together (applicable for the overall code list)

Rule-specific tabs
*  `Severity`: Where applicable, this variable indicates the severity classification of the code description. e.g. For alcohol misuse, "mild", "moderate", "severe".
*  `Scale`: 1= Indicates that the code and severity classifications are dependent on extra clinical information (e.g. frequency of alcohol consumption). By default, this is set to "Mild" for alcohol. See rule-based algorithms.
*  `Reference`: 1=code is part of family violence reference standard, 2=code can be used as a broader measure of family violence 
*  `Individual`: 1=code applies to child only, 2=code applies to mother only, 3=code applies to mother or child (i.e. either),4= code only applicable to female children
*  `Coding systems`: 
    -  GP/primary care: Read, OXMIS, Prodcode (prescriptions or items), CPRD REFERRAL FHSASPEC (field specific), CPRD REFERRAL NHSSPEC (field specific)

    -  HES-APC/secondary care/ONS: ICD-10, OPCS-4, ICD-9 (applies to ONS < year 2000), HES-APC DISDEST OR ADMISORC (field specific)


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

![alt text](https://cdn-coiao.nitrocdn.com/CYHudqJZsSxQpAPzLkHFOkuzFKDpEHGF/assets/static/optimized/wp-content/uploads/2021/03/a670ca8abe87057f7f4867446a2db9f4.r-case_when-multiple-cases-syntax.png "script example")

[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/home%20view%20indicators.png)](https://shabeer-syed.github.io/ACEs/Indicators) | [![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/code%20lists.png)](https://shabeer-syed.github.io/ACEs/codelist)

### [Go back](https://shabeer-syed.github.io/ACEs/)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>