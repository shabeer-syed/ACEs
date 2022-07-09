---
title: Definitions and frameworks
---
### [Go back](https://shabeer-syed.github.io/ACEs/)

---------------------------------
This page provides summaries of the theoretical frameworks and definitions that underpinned the development of the ACE indicators. 

## Background
-------------------------------------------------------

Adverse childhood experiences (ACEs) are potentially traumatic, neglectful or [violent](https://www.who.int/violenceprevention/approach/definition/en/) experiences in childhood. Examples of ACEs range from child maltreatment and witnessing violence in the home, to growing up with a parent with a mental health problem [(1)](https://www.cdc.gov/violenceprevention/aces/fastfact.html). Studies estimate that approximately 1 in 2 adults in England reports experiencing at least one ACE in childhood [(2)](https://bmcmedicine.biomedcentral.com/articles/10.1186/1741-7015-12-72). ACEs are linked to considerable health burden in adulthood, and can substantially pressure families, health and social care systems [(3)](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(17)30118-4/fulltext).

The concept of adversity is not new. However, the term "ACEs" was first introduced by a groundbreaking [study published in 1998](https://pubmed.ncbi.nlm.nih.gov/9635069/) by the Centers for Disease Control and the Kaiser Permanente health care organization in USA, California. The concept of ACEs helped bring together and measure a diverse set of preventable adverse childhood experiences that can lead to considerable long-term health problems. The initial ACEs predominately referred to seven domains of adversity in the home environment, including child maltreatment *(1. psychological abuse, 2. physical abuse, 3. sexual abuse)* and household dysfunction *(4. substance abuse in the household, 5. mental illness in the household, 6. mother treated violently, 7. criminal behaviour in the household).* Sometimes the original domains are referred to as the "ten ACEs" when  including *"physical neglect", "emotional neglect", and "parental separation"*.

### Challenges in defining ACEs
Since the late 1990s, the initial "ACE domains" have undergone numerous expansions across studies. Whilst this variation helped innovate and adapt indicators of ACEs to different goals, there is currently little consistency in the definition and inclusion of ACEs. The large variation of measured ACEs also means there is no agreed reference standard for developing new measures of ACEs. Previous studies have mainly assessed the validity and relevance of ACEs based on their risk association with poorer health outcomes in adulthood. However, most studies reporting on the negative health effects of ACEs are based on cross-sectional samples of adults asked to recall experiences from childhood [(1)](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(17)30118-4/fulltext). Recent birth cohort studies, however, reveal that ACEs are relatively poor predictors of negative health outcomes in adulthood relative to other socioeconomic factors [(2)](https://jamanetwork.com/journals/jamapediatrics/article-abstract/2775420). Global studies by the World Health Organization show that traumatic stress symptoms naturally resolve on average six years after a linked traumatic event (e.g., an ACE),[(3)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5632781/),[(4)](https://jamanetwork.com/journals/jamapsychiatry/fullarticle/2595039). These gaps create multiple challenges when attempting to develop new indicators of ACEs for electronic health records (EHRs).

### Establishing a consistent definition and an integrated conceptual model of ACEs
To promote a clearer understanding of developing ACE indicators, we developed a set of criteria to define ACE indicators. We developed a "testable" conceptual biopsychosocial model to help generate theoretically informed predictions of which ACE indicators might be more relevant than others. We have summarised this integrative conceptual model below, along with the pre-specified definition of ACEs.

## Definitions and inclusions
-------------------------------------------------------

We defined ACE indicators as any experience within the family environment recorded in the child or the maternal record considered to be:

> * Frightening, violent, traumatic or neglectful [(see WHO violence definition)](https://apps.who.int/iris/bitstream/handle/10665/42495/9241545615_eng.pdf), with potential for immediate or longer-term harm to a child's biopsychosocial development (intentionally or unintentionally) [(see UK government definition)](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf), as caused by;

> * A single significant event or through repeated exposure;

> * Caused by external factors and not the child themselves, such as self-harm, and;

> * Amenable to health or social care intervention at a family level (i.e. excluding wider factors such as socioeconomic status, community violence, school bullying etc; see [1](https://jamanetwork.com/journals/jama/fullarticle/2783975), [2](https://www.gov.uk/government/publications/supporting-families-programme-guidance-2022-to-2025/chapter-4-identifying-and-working-with-families), [3](https://www.sciencedirect.com/science/article/abs/pii/S0749379719300315))

We made several adaptations to previously studied ACEs to allow for feasible ascertainment in electronic health records (EHRs). We defined indicators as variables of grouped codes and measures. We aimed to develop ACE indicators that reflected clinically meaningful risk groups of adversity to identify families that may be eligible for targeted maternal-child care interventions in England (e.g. [Supporting Families programme](https://www.gov.uk/government/publications/supporting-families-programme-guidance-2021-to-2022), or previously "targeted care pathway" of [the Healthy Child Programme by Public Health England](https://www.gov.uk/government/publications/healthy-child-programme-0-to-19-health-visitor-and-school-nurse-commissioning). See also WHO for [intervention studies](https://www.who.int/teams/social-determinants-of-health/violence-prevention/global-status-report-on-violence-against-children-2020).

We manually grouped indicators into broader ACE domains consistent with the [original study](https://www.ajpmonline.org/article/S0749-3797(98)00017-8/fulltext) by [Kaiser Permanente and CDC](https://www.cdc.gov/violenceprevention/aces/index.html).  Due to the lack of recordings, we collapsed all types of child abuse and neglect into child maltreatment (CM). We collapsed "imprisonment of household members" and "household challenges" into Adverse family environments. We created a separate indicator, "Social service involvement" (SSI), for social care-related codes that did not contain descriptions of CM or mIPV. SSI was merged with CM in the final selection process owing to few recordings and high intercorrelations.

Given the substantial under-recording of CM and mIPV (e.g. see [1](https://www.cambridge.org/core/journals/the-british-journal-of-psychiatry/article/barriers-and-facilitators-of-disclosures-of-domestic-violence-by-mental-health-service-users-qualitative-study/7A690CCBC0322D045442549A5FA3C4CF), [2](https://bjgp.org/content/67/659/e437.long)), we also added the domain “high-risk presentations of CM” (HRP-CM). HRP-CM encompassed indicators from the [National Institute for Health and Care Excellence (NICE)](https://www.nice.org.uk/guidance/cg89/chapter/1-Guidance) and [Royal College of General Practitioners (RGCP)](https://www.rcgp.org.uk/clinical-and-research/resources/toolkits/child-safeguarding-toolkit.aspx) that should raise clinical suspicion for CM.

ACEs can be recorded in both mothers' and children's records. ACEs are considered based on each specific child's time from birth. Children are therefore considered unexposed if no relevant recording occurs in the study period, regardless of previous exposure in children within the same family. This approach mirrors changes in stress levels as the family moves through different life stages.

## A biopsychosocial conceptual model for defining and developing ACEs
-------------------------------------------------------
To make theoretically informed categorisations and predictions of relevant ACEs, we use the socio-ecological system theory by [Bronfenbrenner (1977)](https://psycnet.apa.org/record/1978-06857-001) and [Belsky (1980)](https://psycnet.apa.org/record/1980-12117-001) as a platform or map to specific predictions of ACEs within two ecological levels (the individual and the family environment). By focusing on the first two ecological levels, we restricted ACEs to clinically measurable and intervenable indicators at a family level.

Across these two "ecological levels we make predictions of relevant ACEs based on attachment theory (Bowlby, 1969–82; Ainsworth et al., 1978), the [cumulative stress model](https://pubmed.ncbi.nlm.nih.gov/22201156/) (includes the ["allostatic load" model](https://www.nejm.org/doi/10.1056/NEJM199801153380307) and the ["ecobiodevelopmental" framework)](https://www.publications.aap.org/pediatrics/article-split/129/1/e232/31628/The-Lifelong-Effects-of-Early-Childhood-Adversity), and [cognitive behaviorual theories of emotions](https://psycnet.apa.org/record/1989-26231-001).

In summary, this integrative biopsychosocial conceptual model predicts cumulating adversity in the context of co-occurring intergenerational risk factors ([5](https://pubmed.ncbi.nlm.nih.gov/33689982/)) and limited protective factors lead to potential child maltreatment and parental intimate partner violence (herein termed "family violence"). 

We summarise different key theories and mechanisms hypothesised to play a role in ACEs below. It does not represent an exhaustive list.

![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/formulation%20lower%20res%201.png)

[*Download the figure in high resolution*](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/formulation.png). 

*The figure does not represent an exhaustive list of potential mechanisms behind ACEs.*

### Society & community level
Social determinants of health encompass socioeconomic conditions that shape health outcomes for individuals, families and communities. Children with ACEs are more likely to grow up in environments where it is harder to raise a family and cope with everyday challenges. Families may live in communities with high unemployment and a lack of local resources for families, with parents having to travel long distances to work, or family members may be more likely to suffer from health problems that make it difficult to work.

### Individual & family level
*Attachment and learning theory.* Social risk factors can negatively influence carers' ability to respond, such as being available and responsive to a child's attachment cues. Children with ACEs may be more likely to develop insecure attachments from reduced caregiving responses of emotional validation (e.g., "my pain matters") and reduced experiences of healthy parental modelling of emotion regulation. This can also mean a child loses friends and the support of adults and so misses out on opportunities to grow social support networks.

*Cognitive and behavioural theories.* People cope with stress and perceived threats using different preventative strategies (e.g. avoidance, escape, fight) to minimise negative consequences. Children who grew up in environments with increased levels of stress and unpredictability can be more likely to perceive the world as less safe and feel less confident they can manage. To cope, children may develop cognitive biases toward threats, learn to suppress emotions, and avoid situations they fear will cause further distress (e.g. see [theories on emotional processing](https://psycnet.apa.org/record/1986-15090-001), [selective attention and overestimation of threat](https://pubmed.ncbi.nlm.nih.gov/10402694/)). Over time, however, this interaction of biopsychosocial factors prevents new learning of balanced threat appraisals (e.g. "I can cope"), creating a maintenance cycle of stress.

For some families, these social risk factors and coping responses are carried over across generations as children become parents themselves. Whilst strategies are perceived as logical at the moment, over time, they can leave families in a cycle that perpetuates stress (e.g. avoidance prevents learning from experience). As underlying stress increases, caregivers and children have fewer resources to cope and regulate responses (e.g. reduced response inhibition/executive functioning)([6](https://pubmed.ncbi.nlm.nih.gov/12212647/)), increasing the risk of more immediate coping responses to escape or re-gaining control (e.g. shouting, violence, neglect etc.).

Coping responses may vary as a function of the level of need to escape distress and harm, ranging from immediate escape (e.g. violence, substance misuse, abandonment/neglect) to stronger forms of avoidance (e.g. avoiding going out, which reduces social support systems in the longer-term) ([7](https://link.springer.com/article/10.1023/B:JOBA.0000007455.08539.94))

*Life course approach.* Taken together, the model views ACEs as a complex social phenomena and considers families as resilient and constantly striving to cope using different strategies and resources at hand (e.g. protective factors). The model also helps separate the *adverse experience* from the *adverse stress* response of the child, overcoming previous study limitations of [reverse causality] when looking at long-term outcomes. We consider ACEs recorded at the family level (middle segment) amenable to service level intervention and relevant to electronic health records (see above for all criteria).

### A multistage risk prediction model to determine relevance of candidate ACEs (increased adversity --> increased risk of family violence)

We assessed the relevance of identified candidate ACE indicators based on their consistent risk association with a reference standard of family violence in a multistage prediction model. The reference standard (outcome) was any occurrence of child maltreatment (CM) and maternal intimate partner violence (mIPV) up to 5-years post-birth.

Consistent with our theoretical model, we predicted that the final ACE indicators would reflect a continuum of clinical relevance, ranging from high need for intervention (i.e. high risk of family violence) to lower relevance, consistent with previous studied ACEs domains.

[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/home%20view%20domains.png)](https://shabeer-syed.github.io/ACEs/domains) | [![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/code%20lists.png)](https://shabeer-syed.github.io/ACEs/codelist)

### [Go back](https://shabeer-syed.github.io/ACEs/)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>