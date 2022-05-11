---
title: Domain - Maternal mental health problems (mMHPs)
---
### [Go back](https://shabeer-syed.github.io/ACEs/domains) | [View all ACE indicators](https://shabeer-syed.github.io/ACEs/indicatorsfinal) 

--------------------------------
## Definition

This domain contains indicators of mutually exclusive symptom clusters aligning with disorder classifications laid out by DSM-5/ICD-10 excluding substance misuse. Some codes for self-harm (e.g. overdose) may be represented across both maternal mental health problems (mMHPs) and maternal substance misuse (MSM) domains. mMHPs indicators are ascertained using read codes, prescriptions, ICD-10 codes or by meeting the higher cut-off score on a validated self-report instrument or validated algorithms with prescriptions.[1](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-016-0274-7). Validated codes for mMHPs and MSM are also available via the [HDR UK CALIBER phenotype library](https://phenotypes.healthdatagateway.org/), with the mapping process described by [Kuan et al.](https://www.thelancet.com/journals/landig/article/PIIS2589-7500(19)30012-3/fulltext)

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9802273"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [Maternal mental health problems (3966)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/mMHPs_ACEs.txt)

--------------------------------
## Implementation

 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **mMHPs,** Depression | Include if continuous data meets the cut-off assigned to each code (see code list): e.g. DASS-21 (sub-scales): ≥14; EDPS: ≥13; HADS (sub-scale): ≥11; HDRS (sub-scale): ≥ 14; PHQ-9: ≥10; SDS (Zungs's): ≥50 | `mmhps_depres_anx <- merged_data %>% filter(Domain=="mMHPs" & scale=="1" & data1 > cut_off)` | 
 | **mMHPs,** Anxiety | Include if continuous data meets the cut-off assigned to each code (see code list): e.g DASS-21: ≥10; HADS (sub-scale): ≥11; HDRS (sub-scale): ≥18; SAS (Zungs's):  ≥45 score; GAD-7: ≥8 | `as above.` | 
 | **mMHPs,** Anxiety or depressive symptoms, antidepressants or anxiolytics and mental health service referral/interventions received | Codes referring to anxiety symptoms (e.g., worrying) or depression (e.g. “feeling low”) are only considered a case of depression or an anxiety disorder when the patient was also given antidepressants and/or anxiolytic medication within 3-months or initiated psychological treatment  within 2-years. Comparison estimates for mothers in CPRD-MBL with and without this algorithm are provided by [Abel et al.](https://www.thelancet.com/cms/10.1016/S2468-2667(19)30059-3/attachment/2df04b45-aaff-40de-8118-79df6a9ef5ca/mmc1.pdf) Rule: Include symptoms/medications as an anxiety or depression indicator, if a previous diagnostic code or tier 3 intervention code exists (within 2-years), or if there is a co-occurrence of a prescription consistent with a symptom within 3-months (e.g. anxiolytics &  anxiety symptoms). e.g. Use the `Indicator (specific)==INSERT Antidepressant or Anxiolytic` to separate medication from other mMHPs  | `mmhps_depres_anx <- merged_data %>% filter(Domain=="mMHPs" & scale=="1" & data1 > cut_off)` | 

--------------------------------
## Publications

[*"Adverse Childhood Experiences (ACEs) in English electronic health records of linked mothers and children: validation study using a multistage risk-prediction model, (2021). Shabeer Syed, Arturo Gonzalez-Izquierd, Janice Allister, Gene Feder, Leah Li, Ruth Gilbert."*](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3937569)

[John A, McGregor J, Fone D, Dunstan F, Cornish R, Lyons RA, Lloyd KR. Case-finding for common mental disorders of anxiety and depression in primary care: an external validation of routinely collected data. BMC medical informatics and decision making. 2016 Dec;16(1):1-0.](https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-016-0274-7)

[Syed S, Ashwick R, Schlosser M, Gonzalez-Izquierdo A, Li L, Gilbert R. Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis. Archives of disease in childhood. 2021 Jan 1;106(1):44-53.](https://adc.bmj.com/content/106/1/44.full)

### [Go back](https://shabeer-syed.github.io/ACEs/domains)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>