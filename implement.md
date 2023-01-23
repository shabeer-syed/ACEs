---
title: Implementation and downloads
---
### [Go back](https://shabeer-syed.github.io/ACEs/) | [View domains & indicators](https://shabeer-syed.github.io/ACEs/domains)

# How does it work?
--------------------------------------------

![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/implement%20centered1.png)



## Indicators and algorithms
--------------------------------------------
We developed two measures of ACEs for electronic health records (EHRs):
* Domains (ie, grouped indicators) and;
* Indicators (ie, grouped codes or measures)

[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/domains%20and%20indicators%201.png)](https://shabeer-syed.github.io/ACEs/domains)

Most indicators are derived using algorithms that identify and extract information from EHRs using clinically coded healthcare information (for example ICD-10, Read codes, SNOMED-CT). Algorithms are freely available on this webpage.

For GP records, we define indicators by combining information recorded in Read codes, prescriptions, referral fields and validated self-report measures (continuous variables needing re-coding) routinely administered by GPs or nurses (e.g. alcohol use).

For hospital and death registration records, we define indicators by combining codes from the International Classification of Diseases 9th/10th edition (ICD-9/10), the Classification of Interventions and Procedures (OPCS-4) and HES-APC discharge/admission fields. We also provide cross-mapped unvalidated indicators for newer systems (ICD-11/SNOMED CT) for further evaluation. Browse code lists [here](https://acesinehrs.com/codelist).

Unless specified, indicators refers to information recorded in both child and maternal records.

<span style="color:red">Rule-based algorithms must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions (bone diseases), traumatic birth injuries or maternal-child transmissions during birth (see below).</span>

# Download code lists
--------------------------------------------

Right click on link to save as a ".txt" file (i.e. using option "save link as")

*Total number of included ACE codes: 8802 (ACEs) + 8808 (covariates)*

*Total number of excluded/tested codes: 7671*

### Control documentation

* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/ACEs/raw/main/ACEsinEHRs%20v1.2.pdf)

### All ACE indicators:

* [All ACEs (8830)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/ALL_ACEs_codelist.txt)
* [All ACEs + crossmapped SNOMED CT and ICD-11 (10650)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/ACEs_crossmaped_snomedCT_icd11.txt)
* [All ACEs GP/CPRD only: medcodes, prodcodes, measures only (6639)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/ACEs_readcode_gemscript_CPRD_gold_only.txt)
* [All ACEs Hospital only: ICD, OPCS and HES-APC specific fields (2191)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/ACEs_icd_hosp.txt)

### By ACE domain:

* [Child maltreatment (1306)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/CM_codelist.txt)
* [Maternal intimate partner violence (263 + 185 for assault algorithm)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/IPV_codelist.txt)
	* [Maternal intimate partner violence (263 - excluding codes requring algorithms)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/IPV_no_algo_codelist.txt)
* [High-risk presentation of CM (801)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/HRP_CM_codelist.txt)
* [Adverse family environment (972)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/AFE_codelist.txt)
* [Maternal mental health problems (3960)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/mMHPs_codelist.txt)
* [Maternal substance misuse (1090)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/MSM_codelist.txt)

#### [Covariates: non-ACEs used to add information to risk prediction models (8808)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Health%20comorbidities.txt)

### Code lists for rule-based exclusions
* [Accidents (2017)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Accidents.txt)
* [Osteoporosis - Bone disease (406)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Osteoporosis%20Bone%20disease.txt)
* [Birth injuries or traumatic complications (238)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Birth%20injury%20or%20complication.txt)
* [Mother-to-child-transmissions (15)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Mother-to-child%20transmission.txt)

### Need more code lists?
*Visit the HDR UK Phenotype Library:*

[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/hdruk%20small.png)](https://phenotypes.healthdatagateway.org/)

## Code list dictionary

 | Provided variable | Description | 
 | --- | --- | 
 | **Code** | Data ready code. Contains CPRD GOLD medcodes and prodcodes (as used in the data provided by CPRD with added prefixes to prodcode), ICD-9/10 (removed punctuations for ICD), and OPSC-4 codes. Prefixes *`d_`* added to prodcodes and *`p_`* to OPSC-4 codes. Prefixes prevents de-duplication as different systems may use the same code for different descriptions. |
 | **Code original** | Original code as entered into respective system (removed punctuations for ICD) |
 | **Coding term** | Original code description |
 | **Indicator code** | Indicator code name | 
 | **Indicator specific** | Most specific indicator |
 | **Indicator 1** | Main ACE indicator combining multiple codes or measures as used in  validation paper | 
 | **Indicator 2** | Broader ACE indicator combining multiple codes or measures |
 | **Domain** | ACE domain grouping all indicators together (applicable for the overall code list) | 
 | **Severity** | Where applicable, this variable indicates the severity classification of the code description. *e.g. For alcohol misuse, `mild`, `moderate`, `severe`.* |
 | **Scale** | `1`=Indicates that the code and severity classifications are dependent on extra clinical information (e.g. frequency of alcohol consumption). By default, this is set to *`Mild`* for alcohol. See rule-based algorithms. |
 | **Reference** | `1`=code is part of family violence reference standard, `2`=code can be used as a broader measure of family violence |
 | **Individual** | `1`=code applies to child only, `2`=code applies to mother only, `3`=code applies to mother or child (i.e. either), `4`=code only applicable to female children |
 | **Coding systems** | `GP/primary care:` Read, OXMIS, Prodcode (prescriptions or items), CPRD REFERRAL FHSASPEC (field specific), CPRD REFERRAL NHSSPEC (field specific). `HES-APC/secondary care/ONS:` ICD-10, OPCS-4, ICD-9 (applies to ONS < year 2000), HES-APC DISDEST OR ADMISORC (field specific) |

## Example

| Code | Coding  term  | Indicator 1 | Indicator 2 |  domain | severity | scale | reference | individual | coding system |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 912 | [D]Anorexia	Anorexia | Anorexia | Eating disorders | Maternal mental health problem | diagnostic |  |  | 2 | Read | 

# Suggested implementation of indicators
--------------------------------------------

Whilst most indicators are ready to use by merging the correct code list with your data, some indicators requires rule-based algorithms as listed below. 

### 1-2. Merge code lists with the data file containing the target population
e.g. ensure correct ages for children/mothers

![alt text](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/merge%20codelist.png)

### 3.1 Convert continuous measures to binary indicators using the additional "cut-off" variable provided (i.e. data > cut_off)**

e.g. Example "one liner" in R or Python with dplyr:

 `e.g. mmhps_alcohol <- merged_data %>% filter(Domain=="mMHPs" & Indicator 1=="Alcohol misuse" & scale=="1" & data1 > cut_off)`

### 3.2 Apply more advanced [control flow methods](https://adv-r.hadley.nz/control-flow.html)

Apply multiple rule-based algorithims (age critera, accident exclusions etc) using control flow (data dependent "if then assumptions") are widley covered by the data science community ([1](https://adv-r.hadley.nz/control-flow.html) [2](https://advanced-r-solutions.rbind.io/control-flow.html)).

![alt text](![alt text](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/case%20when.jpg)

[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/home%20view%20domains.png)](https://shabeer-syed.github.io/ACEs/domains) | [![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/code%20lists.png)](https://shabeer-syed.github.io/ACEs/codelist)


### [Go back](https://shabeer-syed.github.io/ACEs/)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>