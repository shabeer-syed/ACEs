---
title: ACEs introduction and overview
---
### [Go back](https://shabeer-syed.github.io/ACEs/)

## Introduction
<img style="float: right;" src="https://raw.githubusercontent.com/shabeer-syed/ACEs/main/overview%20aces%20home.png">
Adverse childhood experiences (ACEs) are potentially traumatic or [violent](https://www.who.int/violenceprevention/approach/definition/en/) events that happen in childhood. Examples range from child maltreatment, and witnessing violence in the home, to growing up with a parent with a mental health problem [(1)](https://www.cdc.gov/violenceprevention/aces/fastfact.html). Studies estimate that approximatley 1 in 2 adults in England reports experiencing at least one ACE in childhood [(2)](https://bmcmedicine.biomedcentral.com/articles/10.1186/1741-7015-12-72). ACEs are linked to considerable health burden in adulthood, and can pose a substantial pressure on families, health and social care systems [(3)](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(17)30118-4/fulltext).

ACEs are preventable. However, many ACEs are very difficult to identify in childhood. Most studies rely on self-reports of adults many years after the event happened, when its more difficult to prevent the negative effects of ACEs.

## How can routinely collected non-identifiable patient data help?
Everyone recognises the  significant challenges of identifying and monitoring ACEs across individual services and nationally.
We know NHS trusts, GPs, clinical teams as well as researchers are at the forefront of this challenge.

Electronic health records (EHRs) are routinely collected data from hospitals, GPs and other health systems. Data is often recorded as events happens and part of routine care. The data is available shorlty  after a health care presentation and pose little burden to patients. All data is made non-identifiable and stored securely (watch the video below to find out more). 

In the UK, mothers and children's data can be linked across services. The ability to link mother’s and children’s records provides an opportunity to measure ACEs before pregnancy, throughout childhood and intergenerationally.

![alt text](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/overall%20logo%20flow.png "workflow")


## Find out more about linked EHRs and how they can benefit us all.
<iframe width="600" height="380" src="https://mediacentral.ucl.ac.uk//Player?autostart=n&fullscreen=y&width=0&height=0&videoId=CFGDc8DB&quality=hi&captions=y&chapterId=0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## What are ACE indicators?
We have developed indicators for identifying ACEs and at-risk families using routinely collected health care data of mothers and children presenting to GPs and hospitals, from pregnancy up to 5-years post-birth. This page provides more information on definitions and brief methods used to develop the indicators. 

Each ACE indicator represents a variable of grouped codes or measures for a potential recorded ACE in mothers or children. Indicators are further grouped into six or seven overall ACE domains.

<div class="flourish-embed flourish-hierarchy" data-src="visualisation/7242701"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

## Definitions and inclusions

We defined ACE indicators as any experience within the family environment recorded in the child or the maternal record considered to be:

> * Frightening, violent, traumatic or neglectful [(see WHO violence definition)](https://www.who.int/violence_injury_prevention/violence/world_report/en/summary_en.pdf),  with potential for immediate or longer-term harm to a child's biopsychosocial development (intentionally or unintentionally) [(see UK government definition)](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf), as caused by;

> * A single significant event or through repeated exposure;

> * Caused by external factors and not the child themselves such as self-harm, and;

> * Amenable to health or social care intervention at a family level (i.e. excluding wider factors such as socioeconomic status, community violence, school bullying etc).


We made several adaptations to previously studied ACEs to allow for feasible ascertainment in electronic health records (EHRs). We defined indicators as variables of grouped codes and measures. We aimed to develop ACE indicators that reflected clinically meaningful risk groups of adversity to identify families that may be eligible for targeted maternal-child care interventions in England (e.g. targeted care pathway of [the Healthy Child Programme by Public Health England](https://www.gov.uk/government/publications/healthy-child-programme-0-to-19-health-visitor-and-school-nurse-commissioning)). See also WHO for [intervention studies](https://www.who.int/teams/social-determinants-of-health/violence-prevention/global-status-report-on-violence-against-children-2020).

We manually grouped indicators into broader ACE domains consistent with the [original study](https://www.ajpmonline.org/article/S0749-3797(98)00017-8/fulltext) by [Kaiser Permanente and CDC](https://www.cdc.gov/violenceprevention/aces/index.html).  Due to the lack of recordings, we collapsed all types of child abuse and neglect into child maltreatment (CM). We collapsed "imprisonment of household members" and "household challenges" into Adverse family environments. We created a separate indicator, "Social service involvement" (SSI), for social care related codes that did not contain descriptions of CM or mIPV. SSI was merged with CM in the final selection process owing to few recordings and high intercorrelations.

Given the substantial under-recording of CM and mIPV (e.g. see [1](https://www.cambridge.org/core/journals/the-british-journal-of-psychiatry/article/barriers-and-facilitators-of-disclosures-of-domestic-violence-by-mental-health-service-users-qualitative-study/7A690CCBC0322D045442549A5FA3C4CF), [2](https://bjgp.org/content/67/659/e437.long)) we also added the domain “high-risk presentations of CM” (HRP-CM). HRP-CM encompassed indicators from the [National Institute for Health and Care Excellence (NICE)](https://www.nice.org.uk/guidance/cg89/chapter/1-Guidance) and [Royal College of General Practitioners (RGCP)](https://www.rcgp.org.uk/clinical-and-research/resources/toolkits/child-safeguarding-toolkit.aspx) that should raise clinical suspicion for CM.

ACEs can be recorded in both mothers' and children's records. ACEs are considered based on each specific child's time from birth. Children are therefore considered unexposed if no relevant recording occur in the study period, regardless of previous exposure in children within the same family. This approach mirrors changes in stress levels as the family moves through different life stages.

# Indicator rankings
*The figure shows included and excluded indicators of ACEs and their median ranking from different variable selection models predicting family violence (highest value ranked 1st, lowest ranked 178th place)* 

<div class="flourish-embed flourish-scatter" data-src="visualisation/7015151"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

###  [See all indicators & selection results](https://shabeer-syed.github.io/ACEs/Indicators) 
Click on the header to see a table overview of median rankings of selected and excluded ACE indicators from the selection process.

# Conceptual model of ACEs and family violence as function of cumulative adversity
![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/formulation%20lower%20res%201.png)

The above figure is an illustrative example of an integration of the socio-ecological system theory ([1](https://psycnet.apa.org/record/1992-98662-005),[2](https://pubmed.ncbi.nlm.nih.gov/7386966/)), and the biopsychosocial cumulative stress model ([3](https://pubmed.ncbi.nlm.nih.gov/22201156/),[4](https://psycnet.apa.org/record/1989-26231-001)) that informed the selection of relevant ACEs in this study.

It does not represent an exhaustive list of factors or mechanisms of ACEs or outcomes.

In summary, the figure shows family violence (CM/mIPV) as outcomes from a cumulation of underlying adversity in the context of co-occurring intergenerational risk factors, ([5](https://pubmed.ncbi.nlm.nih.gov/33689982/)) and limited resources across two levels (society/family).

People cope with stress and perception of threat using different preventative strategies (e.g. avoidance, escape, fight) in an attempt to minimise negative consequences (e.g. see [theories on emotional processing](https://psycnet.apa.org/record/1986-15090-001), [selective attention and overestimation of threat](https://pubmed.ncbi.nlm.nih.gov/10402694/)).

Whilst strategies are perceived as logical in the moment, over time, they can leave families in a cycle that perpetuates stress (e.g. avoidance prevents learning from experience). As underlying stress increases and without mediation, caregivers have fewer resources to cope and regulate responses (e.g. reduced response inhibition/executive functioning) ([6](https://pubmed.ncbi.nlm.nih.gov/12212647/)) increasing the risk of more immediate coping responses to escape or re-gaining control (e.g. shouting, violence, neglect etc).

Coping responses may vary as a function of the level of need to escape distress and harm, ranging from immediate escape (e.g. violence, substance misuse, abandonment/neglect), to stronger forms of avoidance (e.g. avoiding going out which reduce social support systems in the longer-term) ([7](https://link.springer.com/article/10.1023/B:JOBA.0000007455.08539.94)) 

The model, therefore, considers families as resilient and constantly striving to cope using different strategies and resources at hand (e.g. protective factors). We consider ACEs recorded at the family level (middle segment) as amenable to service level intervention and relevant to electronic health records (see above for all criteria).

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

This research benefits from and contributes to the [NIHR Children and Families Policy Research Unit](https://www.ucl.ac.uk/children-policy-research/), but was not commissioned by the National Institute for Health Research (NIHR) Policy Research Programme. The views expressed are those of the author(s) and not necessarily those of the NHS, the National Institute for Health Research, the Department of Health and Social Care or its arm's length bodies, and other Government Departments.

[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/logo%20affil.png)](https://www.ucl.ac.uk/children-policy-research/research)

### [Go back](https://shabeer-syed.github.io/ACEs/)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>