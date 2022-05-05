---
title: Definitions and frameworks
---
### [Go back](https://shabeer-syed.github.io/ACEs/)

---------------------------------
This page briefly summarises the theoretical framework and definitions that underpinned the development of the ACE indicators. 

### Background
Adverse childhood experiences (ACEs) are potentially traumatic, neglectful or [violent](https://www.who.int/violenceprevention/approach/definition/en/) experiences in childhood. Examples of ACEs range from child maltreatment, and witnessing violence in the home, to growing up with a parent with a mental health problem [(1)](https://www.cdc.gov/violenceprevention/aces/fastfact.html). Studies estimate that approximately 1 in 2 adults in England reports experiencing at least one ACE in childhood [(2)](https://bmcmedicine.biomedcentral.com/articles/10.1186/1741-7015-12-72). ACEs are linked to considerable health burden in adulthood, and can pose a substantial pressure on families, health and social care systems [(3)](https://www.thelancet.com/journals/lanpub/article/PIIS2468-2667(17)30118-4/fulltext).

The concept of adversity is not new, but the term "ACEs" was first introduced by a groundbreaking [study published in 1998](https://pubmed.ncbi.nlm.nih.gov/9635069/) conducted by the Centers for Disease Control and the Kaiser Permanente health care organization in USA, California. The concept of ACEs helped bring together and measure a diverse set of preventable childhood experiences that can lead to considerable long-term health problems. The initial ACEs predominately referred to seven domains of adversity in the home environment, including child maltreatment *(1. psychological abuse, 2. physical abuse, 3. sexual abuse)* and household dysfunction *(4. substance abuse in the household, 5. mental illness in the household, 6. mother treated violently, 7. criminal behaviour in the household).*

### Challenges in defining ACEs
Since the late 1990s, the initial "ACE domains" have undergone numerous expansions across studies. Whilst this variation helped innovate and adapt indicators of ACEs to different goals, it also means there is currently little consistency over which experiences should be included as an "ACE", or what critera defines as an "ACE". Previous studies have mainly determined the validity and relevance of ACEs based on self-reported health outcomes in adulthood, which sometimes reveal that ACEs are poor predictors of negative health outcomes relative to other life factors. The World Health Organization also show that traumatic stress symptoms after events like ACEs naturally resolve on average 6-years after the event.[1](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5632781/),[2](https://jamanetwork.com/journals/jamapsychiatry/fullarticle/2595039). The absence of consistent definitions, reference standards and theoretical frameworks, creates multiple challenges to developing new indicators of ACEs for electronic health records (EHRs).

### A an integrated conceptual framework to defining and develop ACEs
To overcome previous limitations in developing ACE indicators, we combined previously established theories to develop a "testable" biopsychosocial framework that can help generate predictions of which ACE indicators might be more relevant than others. We have diagrammatically summarised the developed integrative conceputal model in the figure below. In this model, we use the socio-ecological system theory by [Bronfenbrenner (1977)](https://psycnet.apa.org/record/1978-06857-001) and [Belsky (1980)](https://psycnet.apa.org/record/1980-12117-001) as base, with predictions of relevant ACE indictaors drawn from attachment theory (Bowlby, 1969–82; Ainsworth et al., 1978), the [cumulative stress model](https://pubmed.ncbi.nlm.nih.gov/22201156/)(includes the ["allostatic load" model](https://www.nejm.org/doi/10.1056/NEJM199801153380307) and the ["ecobiodevelopmental" framework](https://www.publications.aap.org/pediatrics/article-split/129/1/e232/31628/The-Lifelong-Effects-of-Early-Childhood-Adversity) and cognitive behaviorual theories of emotions(https://psycnet.apa.org/record/1989-26231-001)). 

The figure does not represent an exhaustive list of mechanisms behind ACEs.

![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/formulation%20lower%20res%201.png)

[*Download the figure in high resolution*](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/formulation.png). 


In summary, the figure shows family violence (CM/mIPV) as an outcome from a cumulation of underlying adversity in the context of co-occurring intergenerational risk factors, ([5](https://pubmed.ncbi.nlm.nih.gov/33689982/)) and limited resources across two levels (society/family).

People cope with stress and perception of threat using different preventative strategies (e.g. avoidance, escape, fight) in an attempt to minimise negative consequences (e.g. see [theories on emotional processing](https://psycnet.apa.org/record/1986-15090-001), [selective attention and overestimation of threat](https://pubmed.ncbi.nlm.nih.gov/10402694/)).

Whilst strategies are perceived as logical at the moment, over time, they can leave families in a cycle that perpetuates stress (e.g. avoidance prevents learning from experience). As underlying stress increases and without mediation, caregivers have fewer resources to cope and regulate responses (e.g. reduced response inhibition/executive functioning) ([6](https://pubmed.ncbi.nlm.nih.gov/12212647/)) increasing the risk of more immediate coping responses to escape or re-gaining control (e.g. shouting, violence, neglect etc).

Coping responses may vary as a function of the level of need to escape distress and harm, ranging from immediate escape (e.g. violence, substance misuse, abandonment/neglect), to stronger forms of avoidance (e.g. avoiding going out, which reduce social support systems in the longer-term) ([7](https://link.springer.com/article/10.1023/B:JOBA.0000007455.08539.94))

The model, therefore, considers families as resilient and constantly striving to cope using different strategies and resources at hand (e.g. protective factors). We consider ACEs recorded at the family level (middle segment) amenable to service level intervention and relevant to electronic health records (see above for all criteria).


### ACEs and family violence as a function of cumulative adversity
Here, the reference standard (outcome) was any occurrence of child maltreatment (CM) and maternal intimate partner violence (mIPV) up to 5-years post-birth. CM and mIPV are clinically important. They reflect a need for intervention and are likely outcomes based on the cumulation of adversity. CM and mIPV also separate the *adverse experience* from the *adverse stress* response of the child, overcoming previous study limitations of [reverse causality] when looking at long-term outcomes. Overall, we used a clinically important and theoretically informed outcome to validate the relevance of the selected ACEs. 

## Definitions of the final ACE domains 
---------------------------------

### Reference standard used for validation

**Outcome/reference standard: Definitive child maltreatment (CM) and maternal intimate partner violence (mIPV) 2-years pre-birth up to 5-years post birth**

A composite variable of the definite CM and mIPV domains, containing indicators such as neglect (pre-post birth), child protection recordings or out-of-home placements by social care services (see [code list browser](https://acesinehrs.com/codelist)). CM and mIPV often co-occur as forms of family violence. We selected this reference standard to encapsulate consistent core ACEs (CM/mIPV), clinically meaningful outcomes, and to represent a cumulation of underlying adversity.[4](https://psycnet.apa.org/record/1989-26231-001),[9](https://www.science.org/doi/abs/10.1126/science.2704995) We also aimed to use a reference standard that separates adverse experiences from the adverse stress response of the child.54  Indicators included in the reference standard were excluded from the development/validation. We list all included and excluded indicators by domains [here](https://acesinehrs.com/Indicators).

**Definitive or probable CM (reference standard; birth up to 5-years post-birth)**

Any recorded act of commission or omission by a parent or caregiver resulting in harm, the potential for harm or threat of child harm, including neglect, psychological, physical, sexual and emotional abuse. Harm does not need to be intended.[45](https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(08)61706-7/fulltext) In the UK, [statutory guidelines of CM](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf) include child exposure to IPV, and maternal evidence for omission or commission during pregnancy such as NAS and FAS.

**Definitive or probable mIPV (reference standard; 2-years pre-birth up to 5-years post-birth)**

Any incident of threatening behaviour, violence or abuse (psychological, physical, sexual, financial or emotional) between adults who are, or have been, intimate partners or family members.51 We restricted mIPV indicators to mothers aged ≥16 and their corresponding children to prevent misclassification of CM in younger mothers.

### ACE domains
---------------------------------
**1. Suspected CM**

This domain excludes any indicator of CM/mIPV described above. Suspected CM included any maltreatment-related indicator with codes or measures describing presentations likely to refer to CM but without mentioning the underlying cause (e.g. harm caused by a non-specified person), safeguarding procedures or child social service interventions.48 For instance, the “suspected CM, NOS” indicator contains codes mentioning “Victim of sexual abuse”, “Multi-professional risk assessment done”, “Assault in the home”.

**2. Suspected maternal intimate partner violence (mIPV; excluding reference standard)**

As in suspected CM, excludes any “definitive” indicator of mIPV but may include indicators with coding terms mentioning historic mIPV or maltreatment by an unspecified person. For instance, the “suspected mIPV, NOS” indicator contains codes mentioning “[X]Maltreatment, by acquaintance or friend”,” Risk of non-accidental injury”, “Assault in the home”. 

**3. High-risk presentations of CM (HRP-CM)**

Indicators consistent with NICE Clinical guidelines [CG89] recommended high-risk child presentations that should raise clinical suspicions for CM. To be interpreted as warning signs of maltreatment in the face of uncertainty and the absence of evidence for CM. All indicators are recorded in the child, except for non-attendance of child appointments which uses both maternal and child records.

**4. Maternal substance misuse (MSM)**

Any consumption of alcohol/drugs meeting threshold for harmful or addictive levels such as codes mentioning "dependence", "specialist/enhanced treatment", class A through C drugs (e.g. A: heroin, cocaine, ecstasy, LSD), self-report measures (≥35 alcohol units per week higher risk drinking)55 and validated measures with higher cut-off scores (≥20 AUDIT score, SADQ ≥31 scores etc). Indicators for alcohol consumption are also provided by CALIBER.

**5. Adverse family environments (AFE)**

Any experiences in the child's family environment (not included above) meeting the above inclusion criteria. Incorporates Royal College of General Practitioners recommended indicators for children/families who are a cause for concern.39 52 

**6. Maternal mental health problems (mMHPs)**

Contains indicators of mutually exclusive symptom clusters aligning with disorder classifications laid out by DSM-5/ICD-10 excluding substance misuse. Some codes for self-harm (e.g. overdose) may be represented across both mMHPs and MSM domains. mMHPs indicators are ascertained using read codes, prescriptions, ICD-10 codes or by meeting the higher cut-off score on a validated self-report instrument or validated algorithms with prescriptions.56
Validated codes for mMHPs, MSM and covariates are also available via the [CALIBER platform](https://portal.caliberresearch.org/), with the mapping process described by [Kuan et al.](https://www.thelancet.com/journals/landig/article/PIIS2589-7500(19)30012-3/fulltext)

[![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/home%20view%20indicators.png)](https://shabeer-syed.github.io/ACEs/Indicators) | [![](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/code%20lists.png)](https://shabeer-syed.github.io/ACEs/codelist)

### [Go back](https://shabeer-syed.github.io/ACEs/)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>