
# Indicators for indentifying Adverse Childhood Experiences (ACEs) in Electronic Health Records (EHRs)

This repository lists all codes and measures retained from our [systematic reviews](https://adc.bmj.com/content/106/1/44.info) and validation in primary and seconary care.

## Introduction

We made several adaptations to previously studied ACEs to allow for feasible ascertainment in electronic health records (EHRs). We defined ACE indicators (i.e. variables of grouped codes and measures) that reflected clinically meaningful vulnerability and risk groups of adversity used for targeted maternal-child care interventions in England (e.g. targeted care pathway of the Healthy Child Programme by Public Health England) and [intervention studies](https://www.who.int/teams/social-determinants-of-health/violence-prevention/global-status-report-on-violence-against-children-2020).

## Inclusion criteria

We defined ACE indicators as any experience within the family environment recorded in the child or the maternal record considered to be:

* Frightening, violence or neglectful [(see WHO violence definition)](https://www.who.int/violence_injury_prevention/violence/world_report/en/summary_en.pdf), or traumatic with potential for immediate or longer-term harm to a child's biopsychosocial development (intentionally or unintentionally) [(see UK goverment definition)](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf), as caused by;
* A single significant event or through repeated exposure;
* Caused by external factors and not the child themselves such as self-harm, and;
* Amenable to health or social care intervention at a family level (i.e. excluding wider factors such as socioeconomic status, community violence, school bullying etc).

We manually grouped indicators into broader ACE domains consistent with the [original study](https://www.ajpmonline.org/article/S0749-3797(98)00017-8/fulltext) by [Kaiser Permanente and CDC](https://www.cdc.gov/violenceprevention/aces/index.html).  Due to the lack of recordings, we collapsed all types of child abuse and neglect into CM. We collapsed incarcerated household members and household challenges into Adverse family environments.  We created a separate indicator, "Social service involvement" (SSI), for social care related codes that did not contain descriptions of CM or mIPV. SSI was merged with CM in the final selection process owing to few recordings and high intercorrelations.

Given the substantial under-recording of CM and mIPV (e.g. see [1](https://www.cambridge.org/core/journals/the-british-journal-of-psychiatry/article/barriers-and-facilitators-of-disclosures-of-domestic-violence-by-mental-health-service-users-qualitative-study/7A690CCBC0322D045442549A5FA3C4CF), [2](https://bjgp.org/content/67/659/e437.long)) we also added the domain “high-risk presentations of CM” (HRP-CM). HRP-CM encompassed indicators from the [National Institute for Health and Care Excellence (NICE)](https://www.nice.org.uk/guidance/cg89/chapter/1-Guidance) and [Royal College of General Practitioners (RGCP)](https://www.rcgp.org.uk/clinical-and-research/resources/toolkits/child-safeguarding-toolkit.aspx) that should raise clinical suspicion for CM.

ACEs can be recorded in both mothers and children records and based on each specific child's time from birth. Children are therefore considered unexposed if no relevant maternal or child recording occur in the relevant period, regardless of previous exposure in children within the same family to mirror changes in stress levels as the family moves through different life stages.

## ACE indicators - instructions 
The code list for ACEs are provided below.
Each ACE indicator represents a variable of combined codes or measures describing characteristics and health care presentations of mothers and children. Indicators are further grouped into six or seven overall ACE domains (Depending on sample size, social service involvements may need to be combined with CM, which creates 6 domains).

For GP records, we define indicators by combining information recorded in Read codes, prescriptions, referral fields and validated self-report measures (continous variables needing re-coding) routinely administered by GPs or nurses (e.g. alcohol use).

For hospital and death registration records, we define indicators by combining codes from the International Classification of Diseases 9th/10th edition (ICD-9/10), the Classification of Interventions and Procedures (OPCS-4) and HES-APC discharge/admission fields.

Unless specified, indicators refers to information recorded in both child and maternal records.

Multiple different rule-based algorithms must be applied to specific indicators (mainly HRP-CM) to prevent misclassification including age-restrictions, exclusions of accidental injuries, genetic predispositions (bone diseases), traumatic birth injuries or maternal-child transmissions during birth (see below).

## Code lists of ACEs by domain

Right click on link to save as a ".txt" file (i.e. using option "save link as" )

### [Child maltreatment (873)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/cm.txt)
### [Social service involvement (239)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/SSI.txt)
### [Maternal intimate partner violence (292)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/mIPV.txt)
### [High-risk presentation of CM (6413)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/HRP-CM.txt)

### [Adverse family environment (1216)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/AFE.txt)
### [Maternal mental health problems (3998)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/mMHPs.txt)
### [Maternal substance misuse (2112)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/MSM.txt)

### [Covariates: non-ACEs used to add information to risk prediction models]
