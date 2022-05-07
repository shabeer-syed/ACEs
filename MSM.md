---
title: Domain - Maternal substance misuse (MSM)
---
### [Go back](https://shabeer-syed.github.io/ACEs/domains) | [View all ACE indicators](https://shabeer-syed.github.io/ACEs/indicatorsfinal) 
--------------------------------
## Definition

Any consumption of alcohol/drugs meeting threshold for harmful or addictive levels such as codes mentioning "dependence", "specialist/enhanced treatment", class A through C drugs (e.g. A: heroin, cocaine, ecstasy, LSD), self-report measures (≥35 alcohol units per week higher risk drinking)55 and validated measures with higher cut-off scores (≥20 AUDIT score, SADQ ≥31 scores etc). Indicators for alcohol consumption are also provided by CALIBER.

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9802228"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Implementation

## Rule-based algorithms

![alt text](https://cdn-coiao.nitrocdn.com/CYHudqJZsSxQpAPzLkHFOkuzFKDpEHGF/assets/static/optimized/rev-4d1b478/wp-content/uploads/2021/03/r-case_when-multiple-cases-syntax.png)

 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **MSM,** Alcohol misuse Severe | Include if continuous data meets the cut-off assigned to each code (see code list): e.g. AUDIT: ≥20; AUDIT-PC: ≥10; SADQ ≥31; ≥35 alcohol units per week (analogous to higher-risk drinking/harmful drinking/alcohol dependence; [see NICE guidelines](https://www.nice.org.uk/guidance/ph24/chapter/7-Glossary)); >200 mg alcohol per 100 ml blood is classed as potential high-risk offender when driving in England/Wales (see UK gov) (applies to hospital admission codes in this study). | `msm_alcohol <- merged_data %>% filter(Domain=="MSM" & Indicator_1=="Alcohol misuse" & scale=="1" & data1 > cut_off)`|

--------------------------------
## Publications

[*"Adverse Childhood Experiences (ACEs) in English electronic health records of linked mothers and children: validation study using a multistage risk-prediction model, (2021). Shabeer Syed, Arturo Gonzalez-Izquierd, Janice Allister, Gene Feder, Leah Li, Ruth Gilbert."*](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3937569)

[Department of Health. Alcohol guidelines review: report from the guidelines development group to the UK chief medical officers. London: Department of Health. January, 2016](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/545739/GDG_report-Jan2016.pdf)"

--------------------------------
## Code list

#### [Maternal substance misuse (1090)](https://raw.githubusercontent.com/shabeer-syed/ACEs/main/MSM_ACEs.txt)

### [Go back](https://shabeer-syed.github.io/ACEs/domains)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>