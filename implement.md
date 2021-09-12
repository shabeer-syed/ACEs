---
title: Implemetation and methods
---
### [Go back](https://shabeer-syed.github.io/ACEs/)

## ACE indicators - instructions 
The code lists for ACEs are provided below.
Each ACE indicator represents a variable of grouped codes or measures (self-report recording) for a potential ACE. Indicators are further grouped into six or seven overall ACE domains (depending on sample size, social service involvements can be combined with CM to create 6 domains).

For GP records, we define indicators by combining information recorded in Read codes, prescriptions, referral fields and validated self-report measures (continuous variables needing re-coding) routinely administered by GPs or nurses (e.g. alcohol use).

For hospital and death registration records, we define indicators by combining codes from the International Classification of Diseases 9th/10th edition (ICD-9/10), the Classification of Interventions and Procedures (OPCS-4) and HES-APC discharge/admission fields.

Unless specified, indicators refers to information recorded in both child and maternal records.

Multiple different rule-based algorithms must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions (bone diseases), traumatic birth injuries or maternal-child transmissions during birth (see below).

# [See code list browser](https://shabeer-syed.github.io/ACEs/codelist)

### Code list data dictionary

*  `Code`: Original code as entered into respective system (removed punctuations, adds prefixes: "d_" to prodcodes and "e_" to OPSC-4). Prefixes prevents de-duplication as different systems may use the same code for different descriptions.
*  `Coding term`: Original code description
*  `Indicator 1`: Most specific ACE indicator combining multiple codes or measures
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

## Code lists by ACE domain
*Total number of included ACE codes: 7448 (ACEs) + 8808 (covariates)*

*Total number of excluded/tested codes: 7671*

Right click on link to save as a ".txt" file (i.e. using option "save link as" )

* ### [Child maltreatment (873)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/cm.txt)
* ### [Social service involvement (239)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/SSI.txt)
* ### [Maternal intimate partner violence (292)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/mIPV.txt)
* ### [High-risk presentation of CM (643)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/HRP-CM.txt)

* ### [Adverse family environment (1216)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/AFE.txt)
* ### [Maternal mental health problems (3998)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/mMHPs.txt)
* ### [Maternal substance misuse (2112)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/MSM.txt)

### [Covariates: non-ACEs used to add information to risk prediction models (8808)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Health%20comorbidities.txt)

### Code lists for rule-based exclusions
* ### [Accidents (2017)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Accidents.txt)
* ### [Osteoporosis - Bone disease (406)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Osteoporosis%20Bone%20disease.txt)
* ### [Birth injuries or traumatic complications (238)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Birth%20injury%20or%20complication.txt)
* ### [Mother-to-child-transmissions (15)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Mother-to-child%20transmission.txt)


## Suggested implementation of indicators
Whilst most indicators are ready for use in your dataset (e.g. via merging a code list), some indicators requires rule-based algorithms as listed below. 

### Brief outline
//1. Merge each specific code list or the complete ACEs code list with your data file containing the target population (e.g. correct ages for children/mothers):
![alt text](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/merge%20codelist.png)

//2. Convert continuous measures to binary indicators by applying/"filtering" using the additional "cut-off" variable provided (i.e. data > cut_off)

e.g. Example "one liner" in R or Python with dplyr:

 `e.g. mmhps_alcohol <- merged_data %>% filter(Domain=="mMHPs" & Indicator 1=="Alcohol misuse" & scale=="1" & data1 > cut_off)`

//3. More advanced [control flow methods](https://adv-r.hadley.nz/control-flow.html) are required to apply multiple rule-based algorithims (age critera, accident exclusions etc) and to achieve faster implementation. Control flow (data dependent "if then assumptions") are widley covered by the data science community ([1](https://adv-r.hadley.nz/control-flow.html) [2](https://advanced-r-solutions.rbind.io/control-flow.html)).

![alt text](https://cdn-coiao.nitrocdn.com/CYHudqJZsSxQpAPzLkHFOkuzFKDpEHGF/assets/static/optimized/wp-content/uploads/2021/03/a670ca8abe87057f7f4867446a2db9f4.r-case_when-multiple-cases-syntax.png "script example")

## Contact information


If your require any further information about the development of the ACE indicators, please read the publication here (insert link) or feel free to contact us:

* Shabeer Syed, Researcher in Epidemiology (s.syed.16@ucl.ac.uk), 1,2 
* Dr Arturo Gonzalez-Izquierdo, Senior Research Associate, 1, 3
* Dr Linda Wijlaars, Senior Research Associate, 1, 3
* Dr Janice Allister, General Practitioner, 5
* Dr Leah Li,  Associate Professor in Medical Statistics and Epidemiology, 1
* Prof Gene Feder, Professor of Primary Care, 4
* Prof Ruth Gilbert, Professor of Clinical Epidemiology (r.gilbert@ucl.ac.uk), 1,3

*1. UCL Great Ormond Street Institute of Child Health, Population, Policy and Practice, Faculty of Population Health Sciences London WC1N 1EH*

*2. Oxford Institute of Clinical Psychology Training and Research, University of Oxford, Oxford, UK*

*3. Institute of Health Informatics and Health Data Research UK, University College London*

*4. Bristol Medical School, Bristol Population Health Science Institute Centre for Academic Primary Care, University of Bristol*

*5. General Practitioner, NHS*

## More information about ACEs 

For further information about research on ACEs and their uses, please visit:

* [CDC](https://www.cdc.gov/violenceprevention/aces/index.html)

* [British Psychological Society](https://www.bps.org.uk/sites/www.bps.org.uk/files/Policy/Policy%20-%20Files/Briefing%20Paper%20-%20Adverse%20Childhood%20Experiences.pdf)

* [World Health Organization - Prevention of Violence](https://www.who.int/teams/social-determinants-of-health/violence-prevention)

* [University College London reports](https://www.instituteofhealthequity.org/resources-reports/the-impact-of-adverse-experiences-in-the-home-on-children-and-young-people)

* [The BMJ](https://www.bmj.com/content/371/bmj.m3048)

The Lancet research collections:
* [Violence](https://www.thelancet.com/series/violence)
* [Child maltreatment](https://www.thelancet.com/series/child-maltreatment)
* [Violence against women and girls](https://www.thelancet.com/series/violence-against-women-and-girls)
* [Family planning](https://www.thelancet.com/series/family-planning)
* [Women’s and Children’s Health in Conflict Settings](https://www.thelancet.com/series/conflict-health)

JAMA research collections:
* [Violence](https://jamanetwork.com/collections/5957/violence)
* [Child maltreatment](https://jamanetwork.com/collections/5555/child-abuse)
* [Intimate partner violence](https://jamanetwork.com/collections/5711/intimate-partner-violence)

### UK Policy implications related to ACEs:

Public Health England/Wales:

* [Vulnerability in childhood: a public health informed approach](https://www.gov.uk/government/publications/vulnerability-in-childhood-a-public-health-informed-approach)

* [Promoting children and young people’s emotional health and wellbeing](https://www.gov.uk/government/publications/promoting-children-and-young-peoples-emotional-health-and-wellbeing)

* [Public Health Wales](https://phw.nhs.wales/topics/adverse-childhood-experiences/)

* [Public Health Wales study on routine screening of ACEs at GP practices](https://www.wales.nhs.uk/sitesplus/documents/888/Asking%20about%20ACEs%20in%20General%20Practice.pdf)


HM Government:

* [Working together to safeguard children: statutory framework](https://www.gov.uk/government/publications/working-together-to-safeguard-children--2)

# Acknowledgements
This webpage accompanies a study that uses data provided by patients and collected by the NHS as part of their care and support [#DataSavesLives](https://twitter.com/hashtag/DataSavesLives?src=hashtag_click). We are extremely grateful to the generosity of the patients and their families, along with the participating GP practices and NHS staff, for their ongoing contribution to mental health and family violence research.

This study was approved by the MHRA (UK) Independent Scientific Advisory Committee (now called ) [ISAC protocol. 19_162R ], under Section 251 (NHS Social Care Act 2006). This study was carried out as part of the CALIBER© resource. [CALIBER, led by the UCL Institute of Health Informatics](https://academic.oup.com/jamia/article/26/12/1545/5536916), is a research resource providing validated electronic health record phenotyping algorithms and tools for national structured data sources.

This study is based on data from the CPRD obtained under licence from the UK Medicines and Healthcare products Regulatory Agency. The interpretation and conclusions contained in this study are those of the author/s alone HES, and ONS are under copyright © (2020), re-used with the permission of The Health & Social Care Information Centre. All rights reserved.

The research was supported in part by the NIHR Great Ormond Street Hospital Biomedical Research Centre.

This study is based on independent research commissioned from the NIHR Children and Families Policy Research Unit and funded by the National Institute for Health Research Policy Research Programme. The views expressed are those of the author(s) and not necessarily those of the NHS, the National Institute for Health Research, the Department of Health and Social Care or its arm's length bodies, and other Government Departments.