---
title: Definitions and frameworks
---
### [Go back](https://shabeer-syed.github.io/ACEs/)

---------------------------------
This page briefly summarises the theoretical framework and definitions that underpinned the development of the ACE indicators. 

## Background
-------------------------------------------------------

Adverse childhood experiences (ACEs) are potentially traumatic, neglectful or [violent](https://www.who.int/violenceprevention/approach/definition/en/) experiences in childhood. Examples of ACEs range from child maltreatment, and witnessing violence in the home, to growing up with a parent with a mental health problem [(1)](https://www.cdc.gov/violenceprevention/aces/fastfact.html). Studies estimate that approximately 1 in 2 adults in England reports experiencing at least one ACE in childhood [(2)](https://bmcmedicine.biomedcentral.com/articles/10.1186/1741-7015-12-72). ACEs are linked to considerable health burden in adulthood, and can pose a substantial pressure on families, health and social care systems [(3)](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(17)30118-4/fulltext).

The concept of adversity is not new. However, the term "ACEs" was first introduced by a groundbreaking [study published in 1998](https://pubmed.ncbi.nlm.nih.gov/9635069/) conducted by the Centers for Disease Control and the Kaiser Permanente health care organization in USA, California. The concept of ACEs helped bring together and measure a diverse set of preventable adverse childhood experiences that can lead to considerable long-term health problems. The initial ACEs predominately referred to seven domains of adversity in the home environment, including child maltreatment *(1. psychological abuse, 2. physical abuse, 3. sexual abuse)* and household dysfunction *(4. substance abuse in the household, 5. mental illness in the household, 6. mother treated violently, 7. criminal behaviour in the household).* Sometimes the original domains are referred to as the "ten ACEs" when  including *"physical neglect", "emotional neglect", and "parental separation"*.

### Challenges in defining ACEs
Since the late 1990s, the initial "ACE domains" have undergone numerous expansions across studies. Whilst this variation helped innovate and adapt indicators of ACEs to different goals, it also means there is currently little consistency over which experiences should be included as an "ACE", or what mutual critera defines as an "ACE". Previous studies have mainly determined the validity and relevance of ACEs based on their risk association with self-reported health outcomes in adulthood. However, these studies sometimes reveal that ACEs are poor predictors of negative health outcomes relative to other life factors.Poor health outcomes in adult  The World Health Organization also show that traumatic stress symptoms after events like ACEs naturally resolve on average 6-years after the event.[1](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5632781/),[2](https://jamanetwork.com/journals/jamapsychiatry/fullarticle/2595039). The absence of consistent definitions, reference standards and theoretical frameworks, creates multiple challenges to developing new indicators of ACEs for electronic health records (EHRs).

### Establishing a consistent definition and an integrated conceptual model of ACEs
To promote a clearer understanding in developing ACE indicators, we developed a set of criteria to define ACE indicators and we developed a "testable" biopsychosocial conceptual model that can help generate predictions of which ACE indicators might be more relevant than others. We have summarised the developed definition and integrative conceputal modelbelow.

## Definitions and inclusions
-------------------------------------------------------

We defined ACE indicators as any experience within the family environment recorded in the child or the maternal record considered to be:

> * Frightening, violent, traumatic or neglectful [(see WHO violence definition)](https://www.who.int/violence_injury_prevention/violence/world_report/en/summary_en.pdf),  with potential for immediate or longer-term harm to a child's biopsychosocial development (intentionally or unintentionally) [(see UK government definition)](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf), as caused by;

> * A single significant event or through repeated exposure;

> * Caused by external factors and not the child themselves, such as self-harm, and;

> * Amenable to health or social care intervention at a family level (i.e. excluding wider factors such as socioeconomic status, community violence, school bullying etc).

We made several adaptations to previously studied ACEs to allow for feasible ascertainment in electronic health records (EHRs). We defined indicators as variables of grouped codes and measures. We aimed to develop ACE indicators that reflected clinically meaningful risk groups of adversity to identify families that may be eligible for targeted maternal-child care interventions in England (e.g. targeted care pathway of [the Healthy Child Programme by Public Health England](https://www.gov.uk/government/publications/healthy-child-programme-0-to-19-health-visitor-and-school-nurse-commissioning)). See also WHO for [intervention studies](https://www.who.int/teams/social-determinants-of-health/violence-prevention/global-status-report-on-violence-against-children-2020).

We manually grouped indicators into broader ACE domains consistent with the [original study](https://www.ajpmonline.org/article/S0749-3797(98)00017-8/fulltext) by [Kaiser Permanente and CDC](https://www.cdc.gov/violenceprevention/aces/index.html).  Due to the lack of recordings, we collapsed all types of child abuse and neglect into child maltreatment (CM). We collapsed "imprisonment of household members" and "household challenges" into Adverse family environments. We created a separate indicator, "Social service involvement" (SSI), for social care related codes that did not contain descriptions of CM or mIPV. SSI was merged with CM in the final selection process owing to few recordings and high intercorrelations.

Given the substantial under-recording of CM and mIPV (e.g. see [1](https://www.cambridge.org/core/journals/the-british-journal-of-psychiatry/article/barriers-and-facilitators-of-disclosures-of-domestic-violence-by-mental-health-service-users-qualitative-study/7A690CCBC0322D045442549A5FA3C4CF), [2](https://bjgp.org/content/67/659/e437.long)) we also added the domain “high-risk presentations of CM” (HRP-CM). HRP-CM encompassed indicators from the [National Institute for Health and Care Excellence (NICE)](https://www.nice.org.uk/guidance/cg89/chapter/1-Guidance) and [Royal College of General Practitioners (RGCP)](https://www.rcgp.org.uk/clinical-and-research/resources/toolkits/child-safeguarding-toolkit.aspx) that should raise clinical suspicion for CM.

ACEs can be recorded in both mothers' and children's records. ACEs are considered based on each specific child's time from birth. Children are therefore considered unexposed if no relevant recording occurs in the study period, regardless of previous exposure in children within the same family. This approach mirrors changes in stress levels as the family moves through different life stages.

## A an integrated conceptual model to defining and develop ACEs
-------------------------------------------------------

In this model, we use the socio-ecological system theory by [Bronfenbrenner (1977)](https://psycnet.apa.org/record/1978-06857-001) and [Belsky (1980)](https://psycnet.apa.org/record/1980-12117-001) as a base, with predictions of relevant ACE indictaors drawn from the attachment theory (Bowlby, 1969–82; Ainsworth et al., 1978), the [cumulative stress model](https://pubmed.ncbi.nlm.nih.gov/22201156/) (includes the ["allostatic load" model](https://www.nejm.org/doi/10.1056/NEJM199801153380307) and the ["ecobiodevelopmental" framework)](https://www.publications.aap.org/pediatrics/article-split/129/1/e232/31628/The-Lifelong-Effects-of-Early-Childhood-Adversity), and [cognitive behaviorual theories of emotions](https://psycnet.apa.org/record/1989-26231-001).

The figure does not represent an exhaustive list of potential mechanisms behind ACEs.

![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/formulation%20lower%20res%201.png)

[*Download the figure in high resolution*](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/formulation.png). 

In summary, the figure shows child maltreatment and parental intimate partner violence (herein termed "family violence") as a result of cumulating underlying adversity in the context of co-occurring intergenerational risk factors ([5](https://pubmed.ncbi.nlm.nih.gov/33689982/)) and limited protective factors across two ecological levels (society and the family environment).

People cope with stress and perception of threats using different preventative strategies (e.g. avoidance, escape, fight) in an attempt to minimise negative consequences (e.g. see [theories on emotional processing](https://psycnet.apa.org/record/1986-15090-001), [selective attention and overestimation of threat](https://pubmed.ncbi.nlm.nih.gov/10402694/)).

Whilst strategies are perceived as logical at the moment, over time, they can leave families in a cycle that perpetuates stress (e.g. avoidance prevents learning from experience). As underlying stress increases and without mediation, caregivers have fewer resources to cope and regulate responses (e.g. reduced response inhibition/executive functioning) ([6](https://pubmed.ncbi.nlm.nih.gov/12212647/)) increasing the risk of more immediate coping responses to escape or re-gaining control (e.g. shouting, violence, neglect etc.).

Coping responses may vary as a function of the level of need to escape distress and harm, ranging from immediate escape (e.g. violence, substance misuse, abandonment/neglect) to stronger forms of avoidance (e.g. avoiding going out, which reduces social support systems in the longer-term) ([7](https://link.springer.com/article/10.1023/B:JOBA.0000007455.08539.94))

The model, therefore, considers families as resilient and constantly striving to cope using different strategies and resources at hand (e.g. protective factors). The model also helps separate the *adverse experience* from the *adverse stress* response of the child, overcoming previous study limitations of [reverse causality] when looking at long-term outcomes. We consider ACEs recorded at the family level (middle segment) amenable to service level intervention and relevant to electronic health records (see above for all criteria).

### A multistage risk prediction model to determine relevance of indicators (Increased adversity --> Increased risk of family violence)

We assessed the relevance of identified candidate ACE indicators based on their consistent risk association with a reference standard in a multistage prediction model. The reference standard (outcome) was any occurrence of child maltreatment (CM) and maternal intimate partner violence (mIPV) up to 5-years post-birth.

Consistent with our theoretical model, we predicted that indicators would reflect a continuum of clinical relevance, ranging from high need for intervention (i.e. high risk of family violence) to lower relevance.


[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/home%20view%20domains.png)](https://shabeer-syed.github.io/ACEs/domains) | [![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/code%20lists.png)](https://shabeer-syed.github.io/ACEs/codelist)

### [Go back](https://shabeer-syed.github.io/ACEs/)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>