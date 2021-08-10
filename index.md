
### Indicators for indentifying Adverse Childhood Experiences (ACEs) in Electronic Health Records (EHRs)

This repository list all codes and measures retained from the intial validation. 

### Introduction

We made several adaptations to previously studied ACEs to allow for feasible ascertainment in electronic health records (EHRs). We defined ACE indicators (i.e. variables of grouped codes and measures) that reflected clinically meaningful vulnerability and risk groups of adversity used for targeted maternal-child care interventions in England (e.g. targeted care pathway of the Healthy Child Programme by Public Health England) and intervention studies.33-35 36

### Inclusion criteria

We defined ACE indicators as any experience within the family environment recorded in the child or the maternal record considered to be:

* Frightening, violence or neglectful (see WHO violence definition above), or traumatic with potential for immediate or longer-term harm to a child's biopsychosocial development (intentionally or unintentionally),31 37 as caused by;
* A single significant event or through repeated exposure;
* Caused by external factors and not the child themselves such as self-harm, and;
* Amenable to health or social care intervention at a family level (i.e. excluding wider factors such as socioeconomic status, community violence, school bullying etc).

We manually grouped indicators into broader ACE domains consistent with the original study by Kaiser Permanente and CDC.38 39  Due to the lack of recordings, we collapsed all types of child abuse and neglect into CM. We collapsed incarcerated household members and household challenges into Adverse family environments.  We created a separate indicator, "Social service involvement" (SSI), for social care related codes that did not contain descriptions of CM or mIPV. SSI was merged with CM in the final selection process owing to few recordings and high intercorrelations.

Given the substantial under-recording of CM and mIPV,42 43 we also added the domain “high-risk presentations of CM” (HRP-CM). HRP-CM encompassed indicators from the National Institute for Health and Care Excellence (NICE) and Royal College of General Practitioners (RGCP) that should raise clinical suspicion for CM.44 45

ACEs can be recorded in both mothers and children records and based on each specific child's time from birth. Children are therefore considered unexposed if no relevant maternal or child recording occur in the relevant period, regardless of previous exposure in children within the same family to mirror changes in stress levels as the family moves through different life stages.

```markdown
### Child maltreatment (873)
Assault NOS (CM)
Child maltreatment NOS
Child protection/safeguarding
NAS/FASD
Neglect incl. emotional/psychological abuse
Physical or sexual abuse

### Social service involvement (239)
Child in care
Social service involved

### Maternal intimate partner violence (292) 
Assault NOS (IV)
FGM (IV)
Parental domestic violence NOS
Physical abuse (IV)
Sexual abuse (IV)

#### High-risk presentation of CM (6413)
Anogenital symptoms - Anal fissure
Anogenital symptoms - Dysuria
Anogenital symptoms - NOS
Anogenital symptoms - Pain in penis
Anogenital symptoms - Vaginal discharge
Anogenital symptoms - Genital injuries (bruises, bleedings, wounds etc)
Child harm by undetermined intent - Exposure to unspecified factor
Child harm by undetermined intent - Falling, jumping, pushing or crash by others or object
Child harm by undetermined intent - NOS or rarer events (incl. by firearm, drownings, SID)
Child harm by undetermined intent - Poisoning
Child harm by undetermined intent - Drug overdose in child (GP recording)
Child harm by undetermined intent - Suffocation or strangulation
Cold injuries - cold extremities NOS
Cold injuries - frostbite, hypothermia or excessive exposure to natural cold
Cold injuries - hypothermia of newborn
Signs of sexual activity - Contraception usage
Signs of sexual activity - Abortion
Signs of sexual activity - Pregnant child
Sexual disease (Gonorrhoea, chlamydia, syphilis, genital herpes, hepatitis C/B, HIV or trichomonas infection)
Elimination symptoms
Emotional and behavioural states
Self-harm or suicide in child (incl. harm by undetermined intent)
PTS symptoms (nightmares, dissociations etc)
School problems
Eye trauma
Subarachnoid haemorrhage other
Subdural haematoma/retinal haemorrhage
Fracture - clavicle
Fracture - lower limbs
Fracture - ribs
Fracture - upper limbs
Fracture or crush injury - skull or intracranial
Fracture or crush injury NOS
Other intracranial injuries
Intra-abdominal injuries or spinal fractures
Lacerations, scars and abrasions - body NOS
Lacerations, scars and abrasions - Bruising and contusions
Lacerations, scars and abrasions - Open wound to upper body incl. head
Lacerations, scars and abrasions - Superficial head injuries
Potential failure of provision - Excessive thirst in child
Potential failure of provision - Non-attendance
Potential failure of provision - Failure to thrive (lack of physiological development, malnutrition)
Potential failure of provision - Abnormal weight loss in child
Potential failure of provision - Poor personal hygiene in child - appearance (incl. smell, clothes, dental)
111 call by child
Seen out of hours/emergency appointment (child/mother)
Thermal injuries - body NOS
Thermal injuries - dressing of burn NOS
Thermal injuries - head, face or neck
Thermal injuries - limbs
Thermal injuries - trunk, back or trachea
Unknown and unspecified causes of morbidity in child, hospital admission recording
Other and unspecified abdominal pain
Observation for other suspected diseases and conditions in child
Unspecified event in child
Discussion about presentation in child

### Adverse family environment (1216)
Adversity-related admission special care baby maternity care unit
Advice about child safety
Assault NOS IV GP
Bereavement
Confidential patient data
CPA
Domestic stress
Family disruption NOS
Family health problem NOS
Family is cause for concern
Family substance misuse
Family/parental support
Health supervision and care of other healthy infant and child
Health visitor increasing concern
High-risk antenatal presentation
High-risk antenatal presentation (social risk specific)
High-risk pregnancy
Supervision of very young primigravida
Other specified pregnancy-related conditions
Recurrent aborter
Emergency contraception, before/during pregnancy
Pregnant state, incidental
Termination of pregnancy NEC
Threatened abortion by mother
Unprotected intercourse
Unwanted/concealed pregnancy
Homelessness
Housing problems incl. refugees
Natural disaster and war exposure
Legal execution
Outreach support
Parental conflict/relationship problems
Parental criminal activity/Imprisonment
Parental death
Parental financial concerns
Parental incapacity increased concerns
Parental legal problems
Parental life crisis
Parental problems with daily living/Limited capacity to work
Parental separation
Parental work problems/stress
Parental unemployment
Problem situation in child or mother
Problems related to negative childhood events
Problems related to psychosocial circumstances
Psychosocial health problem with low-level intervention
Seen by/referral to health visitor
Severe signs of deprivation or potential malnutrition (incl. lack of food/water)
Victim of crime
Vulnerable family

### Maternal mental health problems (3998)
Anorexia
Anorexia (hosp. adm)
Antidepressant
Antipsychotic medication NOS
Antipsychotics (first generation)
Antipsychotics (second generation)
Anxiety disorder
Anxiety disorder (hosp. adm)
Anxiolytic
Bipolar
Bipolar (hosp. adm)
Bulimia
Depression
Depression (hosp. adm)
Eating disorder
GAD
Learning/Intellectual disability
Learning/Intellectual disability (hosp. adm)
Mental health problem NOS
Mental health problem NOS (hosp. adm)
Neurodevelopmental and conduct disorders
Obsessive-compulsive disorders
Obsessive-compulsive disorders (hosp. adm)
Panic disorder (incl. agoraphobia, health anx
Paraphilic disorder
Personality disorder
Personality disorder (hosp. adm)
Psychosis incl. sections
PTSD/Acute stress
Puerperal mental disorder NOS
Seen by/referral to mental health professional
Self-harm or suicide
Self-harm or suicide (hosp. adm)
Sleep-wake disorder
Sleep-wake disorder (hosp. adm)
Somatic symptom and related disorders
Suicidal ideation

### Maternal substance misuse (2112)
Alcohol misuse Moderate
Alcohol misuse Severe
Drug misuse Moderate
Drug misuse Severe
Drugs used for alcohol dependence, multipurpose (incl. anxiety, insomnia) 
Drugs used for alcohol dependence, multipurpose (incl. epilepsy, psychosis, diabetic nephropathy, neuropathy) 
Drugs used for alcohol dependence, specific
Drugs used for opioid dependence, multipurpose (incl. severe pain) 
Maternal poisoning by addictive drugs incl. benzodiazepines
Mental and behavioural disorders due to use of tobacco (dependence syndrome)
Mental behavioural disorders due to tobacco use (harmful use), hospital admission recording 
Opioid analgesics (prescription only, abuse potential), multipurpose (incl. very broad purpose range)
Personal history of psychoactive substance abuse

### Covariates: non-ACEs used to add information to risk prediction models
Physically disabled child
Teenage mother (age <20 years; PHE definition)
Maternal index of multiple deprivation (IMD) - Most deprived
Parity >=4 (25.9% imputed values)
Low birthweight  <2.5kg (11.4% imputed values)
Early term birth, gestational age <37 weeks (15.4% imputed values)
Congenital anomaly (composite variable)
Chronic respiratory diseases (GBD classification)
Cardiovascular and circulatory diseases (GBD classification)
Maternal disorders (GBD classification)
Diabetes urogenital blood and endocrine diseases (GBD classification)
Musculoskeletal disorders (GBD classification)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/shabeer-syed/ACEs/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
