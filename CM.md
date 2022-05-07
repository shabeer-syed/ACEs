---
title: Domain - Child maltreatment
---
### [Go back](https://shabeer-syed.github.io/ACEs/domains) | [View all ACE indicators](https://shabeer-syed.github.io/ACEs/indicatorsfinal) 
--------------------------------
## Definition

Any recorded act of commission or omission by a parent or caregiver resulting in harm, the potential for harm or threat of child harm, including neglect, psychological, physical, sexual and emotional abuse. Harm does not need to be intended.[45](https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(08)61706-7/fulltext) In the UK, [statutory guidelines of CM](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/942454/Working_together_to_safeguard_children_inter_agency_guidance.pdf) include child exposure to IPV, and maternal evidence for omission or commission during pregnancy such as NAS and FAS.

Includes indicators such as neglect (pre-post birth), child protection recordings or out-of-home placements by social care services (see [code list browser](https://acesinehrs.com/codelist)).

Suspected CM included any maltreatment-related indicator with codes or measures describing presentations likely to refer to CM but without mentioning the underlying cause (e.g. harm caused by non-specified person), safeguarding procedures or child social service interventions.48 For instance, the “suspected CM, NOS” indicator contains codes mentioning “Victim of sexual abuse”, “Multi-professional risk assessment done”, “Assault in the home”

--------------------------------
## Indicator list
 
<div class="flourish-embed flourish-table" data-src="visualisation/9799589"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

--------------------------------
## Code list

#### [Child maltreatment (1290)](https://raw.githubusercontent.com/shabeer-syed/ACEs/code-lists/CM_ACEs.txt)

--------------------------------
## Implementation
 | ACE domain, Indicator(s) |  Rule-based algorithms | Scrip/code* |
 | --- | --- | --- | 
 | **CM,** FGM | Apply codes mentioning circumcision to female children only (e.g. "54314 - routine or ritual circumcision"). Code list includes markers for rule inclusion. | `cm_fgm <- merged_data %>% filter(Domain=="CM" & individual=="4" & gender=="female"` | 

--------------------------------
## Publications

[*"Adverse Childhood Experiences (ACEs) in English electronic health records of linked mothers and children: validation study using a multistage risk-prediction model, (2021). Shabeer Syed, Arturo Gonzalez-Izquierd, Janice Allister, Gene Feder, Leah Li, Ruth Gilbert."*](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3937569) 

[Gilbert R, Fluke J, O'Donnell M, Gonzalez-Izquierdo A, Brownell M, Gulliver P, Janson S, Sidebotham P. Child maltreatment: variation in trends and policies in six developed countries. The Lancet. 2012 Feb 25;379(9817):758-72.](https://www.sciencedirect.com/science/article/pii/S0140673611610878) Code list can be found [here](https://ars.els-cdn.com/content/image/1-s2.0-S0140673611610878-mmc1.pdf).

[Simkiss DE, Spencer NJ, Stallard N, Thorogood M. Health service use in families where children enter public care: a nested case control study using the General Practice Research Database. BMC health services research. 2012 Dec;12(1):1-2.](https://link.springer.com/article/10.1186/1472-6963-12-65)

[Royal College of General Practitioners. Child safeguarding toolkit.](https://elearning.rcgp.org.uk/mod/book/view.php?id=12531)



### [Go back](https://shabeer-syed.github.io/ACEs/domains)

<script src="http://code.jquery.com/jquery-1.4.2.min.js"></script> <script> var x = document.getElementsByClassName("site-footer-credits"); setTimeout(() => { x[0].remove(); }, 10); </script>