---
title: Domain - Maternal substance misuse (MSM)
---
### [Go back](https://shabeer-syed.github.io/ACEs/domains) | [View all ACE indicators](https://shabeer-syed.github.io/ACEs/indicatorsfinal) 

--------------------------------
## Definition

Any consumption of alcohol/drugs meeting threshold for harmful or addictive levels such as codes mentioning "dependence", "specialist/enhanced treatment", class A through C drugs (e.g. A: heroin, cocaine, ecstasy, LSD), self-report measures (≥35 alcohol units per week higher risk drinking)55 and validated measures with higher cut-off scores (≥20 AUDIT score, SADQ ≥31 scores etc). Indicators for alcohol consumption are also available via the [HDR UK CALIBER phenotype library](https://phenotypes.healthdatagateway.org/).

Indicators are currently restricted to the mother's or child's record (e.g. maternal substance misuse)  due to methodological challenges in accurately linking children to their fathers (a long-standing issue of anonymised secondary and primary care data). However, once reliably linkage of fathers becomes available, the domains "parental mental health problems" and "parental substance misuse" will be updated to include potential fathers.

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9802228"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [Maternal substance misuse (1090)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/MSM_codelist.txt)

* [ACEsinEHRs control documentation / release information](https://github.com/shabeer-syed/ACEs/raw/main/ACEsinEHRs%20v1.2.pdf)

--------------------------------
## Implementation

 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **MSM,** Alcohol misuse Severe | Include if continuous data meets the cut-off assigned to each code (see code list): e.g. AUDIT: ≥20; AUDIT-PC: ≥10; SADQ ≥31; ≥35 alcohol units per week (analogous to higher-risk drinking/harmful drinking/alcohol dependence; [see NICE guidelines](https://www.nice.org.uk/guidance/ph24/chapter/7-Glossary)); >200 mg alcohol per 100 ml blood is classed as potential high-risk offender when driving in England/Wales (see UK gov) (applies to hospital admission codes in this study). | `msm_alcohol <- merged_data %>% filter(Domain=="MSM" & Indicator_1=="Alcohol misuse" & scale=="1" & data1 > cut_off)`|

--------------------------------
## Publications

[Syed, S., Gonzalez-Izquierdo, A., Allister, J., Feder, G., Li, L., & Gilbert, R. (2022). Identifying adverse childhood experiences with electronic health records of linked mothers and children in England: a multistage development and validation study. The Lancet Digital Health.](https://www.sciencedirect.com/science/article/pii/S2589750022000619) 

[Syed S, Ashwick R, Schlosser M, Gonzalez-Izquierdo A, Li L, Gilbert R. Predictive value of indicators for identifying child maltreatment and intimate partner violence in coded electronic health records: a systematic review and meta-analysis. Archives of disease in childhood. 2021 Jan 1;106(1):44-53.](https://adc.bmj.com/content/106/1/44.full)

[Department of Health. Alcohol guidelines review: report from the guidelines development group to the UK chief medical officers. London: Department of Health. January, 2016](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/545739/GDG_report-Jan2016.pdf)"

--------------------------------
### [Go back](https://shabeer-syed.github.io/ACEs/domains)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>