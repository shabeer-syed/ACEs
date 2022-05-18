---
title: Domain - Maternal intimate partner violence (mIPV)
---
### [Go back](https://shabeer-syed.github.io/ACEs/domains) | [View all ACE indicators](https://shabeer-syed.github.io/ACEs/indicatorsfinal) 

--------------------------------
## Definition

Any incident of threatening behaviour, violence or abuse (psychological, physical, sexual, financial or emotional) between adults who are, or have been, intimate partners or family members.51 We restricted mIPV indicators to mothers aged ≥16 and their corresponding children to prevent misclassification of CM in younger mothers.

Includes suspected indicators with coding terms mentioning historic mIPV or maltreatment by an unspecified person. For instance, the “suspected mIPV, NOS” indicator contains codes mentioning “[X]Maltreatment, by acquaintance or friend”,” Risk of non-accidental injury”, “Assault in the home”.

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9802196"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [Maternal intimate partner violence (450 + 519 for assault algorithm)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/mIPV_codelist.txt)

--------------------------------
## Implementation

 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **Susp.mIPV,** Assault NOS (algo); mIPV NOS (Assault and high-risk algo, 30/100 days) | Include as mIPV  if assault recording co-occurs with any “high-risk presentation recording” 30 days before the assault or in 100-days post the assault recording. High-risk recordings are a composite variable of recordings related to parental conflicts, health visitors being sent to the home, nurse partnership referrals, superficial head injuries and bruises. We developed the composite variable using results from our systematic review.51  In the current study the algorithm showed PPVs ranging from 18%-30% of definitive mIPV (derivation cohort). |
 | **mIPV,** Assault NOS (algo), mIPV NOS (Assault and preg. incident and CM algo, 45 days) | Include as mIPV if assault recording co-occurs with any recordings of a safeguarding referral, child protection recording, or definitive CM indicator, or “pregnant state, incidental” (marked in codelist) within 45 days of the assault. UK guidelines state 45 days is the maximum timeframe for an initial outcome following a children’s social care assessment from the date of received safeguarding referral (see point 82, [“working together to safe guard children”](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf)). | 

--------------------------------
## Publications

[*"Adverse Childhood Experiences (ACEs) in English electronic health records of linked mothers and children: validation study using a multistage risk-prediction model, (2021). Shabeer Syed, Arturo Gonzalez-Izquierd, Janice Allister, Gene Feder, Leah Li, Ruth Gilbert."*](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3937569) 

[Syed S, Ashwick R, Schlosser M, Gonzalez-Izquierdo A, Li L, Gilbert R. Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis. Archives of disease in childhood. 2021 Jan 1;106(1):44-53.](https://adc.bmj.com/content/106/1/44.full)

### [Go back](https://shabeer-syed.github.io/ACEs/domains)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>