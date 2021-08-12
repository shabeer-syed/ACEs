
# Indicators of Adverse Childhood Experiences (ACEs) in Electronic Health Records (EHRs)


![alt text](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/Logo%20intro%20disclaimer.png "UCL ICH")

## Introduction
A significant proportion of families present to health care with recorded Adverse Childhood Experiences (ACEs). Children with ACEs face substantially higher risks of poorer health outcomes, with repeated hospital admissions and care costs.

Everyone recognises the  significant challenges of identifying and monitoring ACEs across individual services and nationally.
We know NHS trusts, GPs, clinical teams as well as researchers are at the forefront of this challenge.

We have develeoped indicators for identifying ACEs and at-risk families using routinely collected health care data of mothers and children presenting to GPs and hospitals, from pregnancy up to 10-years post-birth. This repository lists all codes and measures retained from the final validation process and accompanied [systematic reviews](https://adc.bmj.com/content/106/1/44.info).


## Definitions
We made several adaptations to previously studied ACEs to allow for feasible ascertainment in electronic health records (EHRs). We defined indicators as variables of grouped codes and measures. We aimed to develop ACE indicators that reflected clinically meaningful risk groups of adversity to identify families that may be eligible for targeted maternal-child care interventions in England (e.g. targeted care pathway of the Healthy Child Programme by Public Health England). See also WHO for [intervention studies](https://www.who.int/teams/social-determinants-of-health/violence-prevention/global-status-report-on-violence-against-children-2020).

## Inclusion criteria

We defined ACE indicators as any experience within the family environment recorded in the child or the maternal record considered to be:

> * Frightening, violent or neglectful [(see WHO violence definition)](https://www.who.int/violence_injury_prevention/violence/world_report/en/summary_en.pdf), or traumatic with potential for immediate or longer-term harm to a child's biopsychosocial development (intentionally or unintentionally) [(see UK goverment definition)](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf), as caused by;

> * A single significant event or through repeated exposure;

> * Caused by external factors and not the child themselves such as self-harm, and;

> * Amenable to health or social care intervention at a family level (i.e. excluding wider factors such as socioeconomic status, community violence, school bullying etc).

We manually grouped indicators into broader ACE domains consistent with the [original study](https://www.ajpmonline.org/article/S0749-3797(98)00017-8/fulltext) by [Kaiser Permanente and CDC](https://www.cdc.gov/violenceprevention/aces/index.html).  Due to the lack of recordings, we collapsed all types of child abuse and neglect into child maltreatment (CM). We collapsed "imprisonment of household members" and "household challenges" into Adverse family environments. We created a separate indicator, "Social service involvement" (SSI), for social care related codes that did not contain descriptions of CM or mIPV. SSI was merged with CM in the final selection process owing to few recordings and high intercorrelations.

Given the substantial under-recording of CM and mIPV (e.g. see [1](https://www.cambridge.org/core/journals/the-british-journal-of-psychiatry/article/barriers-and-facilitators-of-disclosures-of-domestic-violence-by-mental-health-service-users-qualitative-study/7A690CCBC0322D045442549A5FA3C4CF), [2](https://bjgp.org/content/67/659/e437.long)) we also added the domain “high-risk presentations of CM” (HRP-CM). HRP-CM encompassed indicators from the [National Institute for Health and Care Excellence (NICE)](https://www.nice.org.uk/guidance/cg89/chapter/1-Guidance) and [Royal College of General Practitioners (RGCP)](https://www.rcgp.org.uk/clinical-and-research/resources/toolkits/child-safeguarding-toolkit.aspx) that should raise clinical suspicion for CM.

ACEs can be recorded in both mothers' and children's records and based on each specific child's time from birth. Children are therefore considered unexposed if no relevant maternal or child recording occur in the relevant period, regardless of previous exposure in children within the same family to mirror changes in stress levels as the family moves through different life stages.

# ACEs overview
![alt text](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/domains%20overview.png "Domains")

## ACE indicators - instructions 
The code list for ACEs are provided below.
Each ACE indicator represents a variable of combined codes or measures describing characteristics and health care presentations of mothers and children. Indicators are further grouped into six or seven overall ACE domains (depending on sample size, social service involvements can be combined with CM to create 6 domains).

For GP records, we define indicators by combining information recorded in Read codes, prescriptions, referral fields and validated self-report measures (continous variables needing re-coding) routinely administered by GPs or nurses (e.g. alcohol use).

For hospital and death registration records, we define indicators by combining codes from the International Classification of Diseases 9th/10th edition (ICD-9/10), the Classification of Interventions and Procedures (OPCS-4) and HES-APC discharge/admission fields.

Unless specified, indicators refers to information recorded in both child and maternal records.

Multiple different rule-based algorithms must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions (bone diseases), traumatic birth injuries or maternal-child transmissions during birth (see below).


### Code list data dictionary

*  `Code`: Original code as entered into respective system (removed punctuations, adds prefixes: "d_" to prodcodes and "e_" to OPSC-4). Prefixes prevents de-duplciation as different systems may use the same code for different descriptions.
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
* ### [Osteoporosis - Bone disease (406)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/AFE.txt)
* ### [Birth injuries or traumatic complications (238)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Birth%20injury%20or%20complication.txt)
* ### [Mother-to-child-transmissions (15)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/Mother-to-child%20transmission.txt)

## Contact information


If your require any further information about the development of the ACE indicators, please read the publication here (insert link) or feel free to contact us:

* Shabeer Syed, Researcher in Epidemiology (s.syed.16@ucl.ac.uk) 1,2 
* Dr Arturo Gonzalez-Izquierdo, Senior Research Associate, 1, 3
* Dr Linda Wijlaars, Senior Research Associate, 1, 3
* Dr Janice Allister, General Practitioner, 5
* Dr Leah Li,  Associate Professor in Medical Statistics and Epidemiology 1
* Prof Gene Feder, Professor of Primary Care, 4
* Prof Ruth Gilbert, Professor of Clinical Epidemiology (r.gilbert@ucl.ac.uk) 1,3

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

* [Public Health Wales study on routine screening of ACEs at GP pratices](https://www.wales.nhs.uk/sitesplus/documents/888/Asking%20about%20ACEs%20in%20General%20Practice.pdf)


HM Goverment:

* [Working together to safeguard children: statutory framework](https://www.gov.uk/government/publications/working-together-to-safeguard-children--2)

