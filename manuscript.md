---
title: Quantifying the Expectation–Realisation Gap for Agentic AI Systems
keywords:
- agentic systems
- generative AI
- automation
- expectation management
- evaluation
- governance
lang: en-US
date-meta: '2026-02-23'
author-meta:
- Sebastian Lobentanzer
header-includes: |
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta property="og:type" content="article" />
  <meta name="dc.title" content="Quantifying the Expectation–Realisation Gap for Agentic AI Systems" />
  <meta name="citation_title" content="Quantifying the Expectation–Realisation Gap for Agentic AI Systems" />
  <meta property="og:title" content="Quantifying the Expectation–Realisation Gap for Agentic AI Systems" />
  <meta property="twitter:title" content="Quantifying the Expectation–Realisation Gap for Agentic AI Systems" />
  <meta name="dc.date" content="2026-02-23" />
  <meta name="citation_publication_date" content="2026-02-23" />
  <meta property="article:published_time" content="2026-02-23" />
  <meta name="dc.modified" content="2026-02-23T18:37:42+00:00" />
  <meta property="article:modified_time" content="2026-02-23T18:37:42+00:00" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Sebastian Lobentanzer" />
  <meta name="citation_author_institution" content="Institute of Computational Biology, Computational Health Center, Helmholtz Center, Munich, Germany" />
  <meta name="citation_author_institution" content="German Center for Diabetes Research, Munich, Germany" />
  <meta name="citation_author_orcid" content="https://orcid.org/0000-0003-3399-6695" />
  <link rel="canonical" href="https://slolab.github.io/agentic-expectation-realisation-gap/" />
  <meta property="og:url" content="https://slolab.github.io/agentic-expectation-realisation-gap/" />
  <meta property="twitter:url" content="https://slolab.github.io/agentic-expectation-realisation-gap/" />
  <meta name="citation_fulltext_html_url" content="https://slolab.github.io/agentic-expectation-realisation-gap/" />
  <meta name="citation_pdf_url" content="https://slolab.github.io/agentic-expectation-realisation-gap/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://slolab.github.io/agentic-expectation-realisation-gap/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://slolab.github.io/agentic-expectation-realisation-gap/v/7e6077b7f0ee879f62eccf4f916bfd0049ccd1c8/" />
  <meta name="manubot_html_url_versioned" content="https://slolab.github.io/agentic-expectation-realisation-gap/v/7e6077b7f0ee879f62eccf4f916bfd0049ccd1c8/" />
  <meta name="manubot_pdf_url_versioned" content="https://slolab.github.io/agentic-expectation-realisation-gap/v/7e6077b7f0ee879f62eccf4f916bfd0049ccd1c8/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://slolab.github.io/agentic-expectation-realisation-gap/v/7e6077b7f0ee879f62eccf4f916bfd0049ccd1c8/))
was automatically generated
from [slolab/agentic-expectation-realisation-gap@7e6077b](https://github.com/slolab/agentic-expectation-realisation-gap/tree/7e6077b7f0ee879f62eccf4f916bfd0049ccd1c8)
on February 23, 2026.
</em></small>



## Authors



+ **Sebastian Lobentanzer**
  ^[✉](#correspondence)^<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [https://orcid.org/0000-0003-3399-6695](https://orcid.org/https://orcid.org/0000-0003-3399-6695)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [slobentanzer](https://github.com/slobentanzer)
    <br>
  <small>
     Institute of Computational Biology, Computational Health Center, Helmholtz Center, Munich, Germany; German Center for Diabetes Research, Munich, Germany
  </small>


::: {#correspondence}
✉ — Correspondence possible via [GitHub Issues](https://github.com/slolab/agentic-expectation-realisation-gap/issues)
or email to
Sebastian Lobentanzer \<sebastian.lobentanzer@helmholtz-munich.de\>.


:::


## Abstract {.page_break_before}

Agentic AI systems are deployed with expectations of substantial productivity gains, yet rigorous empirical evidence reveals systematic discrepancies between pre-deployment expectations and post-deployment outcomes.
We review controlled trials and independent validations across software engineering, clinical documentation, and clinical decision support to quantify this expectation--realisation gap.
In software development, experienced developers expected a 24% speedup from AI tools but were slowed by 19%---a 43 percentage-point calibration error.
In clinical documentation, vendor claims of multi-minute time savings contrast with measured reductions of less than one minute per note, and one widely deployed tool showed no statistically significant effect.
In clinical decision support, externally validated performance falls substantially below developer-reported metrics.
These shortfalls are driven by workflow integration friction, verification burden, measurement construct mismatches, and systematic heterogeneity in treatment effects.
The evidence motivates structured planning frameworks that require explicit, quantified benefit expectations with human oversight costs factored in.


## Introduction {.page_break_before}

Agentic AI systems---autonomous software agents that plan, reason, and execute multi-step tasks with limited human oversight---are being adopted across software engineering, clinical medicine, and customer operations with the expectation of transformative productivity gains.
Vendor announcements routinely promise multi-minute time savings per encounter, double-digit percentage speedups, or near-expert-level decision accuracy.
Procurement and investment decisions follow these expectations, committing substantial resources before deployment-grade evidence is available.

Yet a growing body of controlled trials and independent external validations reveals that realised outcomes frequently fall short of pre-deployment expectations---sometimes dramatically so.
This discrepancy, which we term the *expectation--realisation gap*, is not simply a matter of immature technology.
It reflects systematic patterns in how agentic systems interact with human workflows, how performance is measured, and how benefits are distributed across user populations.

Understanding and quantifying this gap is a prerequisite for responsible deployment.
Without structured, quantified expectations that account for real-world integration costs, organisations risk over-investing in systems that deliver marginal gains at best or impose net costs at worst.
This review synthesises the strongest available empirical evidence for the expectation--realisation gap across three domains---software engineering, clinical documentation, and clinical decision support---identifies the mechanistic drivers of shortfalls, and argues that structured planning frameworks with explicit benefit quantification are necessary to close the gap between aspiration and reality.

## Evidence from controlled trials

### Software engineering copilots

The sharpest illustration of the expectation--realisation gap comes from a randomised controlled trial conducted by METR (Model Evaluation & Threat Research) on 16 experienced open-source developers working in their own mature repositories across 246 real tasks [@arxiv:2507.09089].
Before each task, participants forecast that AI assistance would reduce their completion time by 24%.
The measured outcome was a 19% *increase* in completion time---a 43 percentage-point calibration error on the time-change scale, and a complete reversal in direction.
Tasks took approximately 56% longer than developers expected (realised completion time factor 1.19 versus expected 0.76).
Intriguingly, AI-assisted developers also estimated 20% reduction in completion time *after* they had performed the task; the opposite of what had happened.

This result contrasts instructively with a pre-release controlled trial of GitHub Copilot on developers recruited via Upwork, where treated participants completed a standardised, self-contained programming task 55.8% faster (95% CI 21--89%) [@arxiv:2302.06590].
In that experiment, participants' self-estimated productivity gains averaged approximately 35%, meaning they *underestimated* the realised speedup.
Of note, the task here was the same for all participants; the development of an HTTP server in JavaScript.
The divergence between these two trials can be explained by task complexity.
On constrained, well-defined tasks, AI coding tools can exceed expectations, particularly for less experienced professionals; the study notes that the benefit was greater for less experienced developers [@arxiv:2302.06590].
In contrast, in high-context, real-world repositories, the same class of tools can impose net costs that even senior developers fail to anticipate.
These findings are the first instance of heterogeneous treatment effects of agentic AI (see the [section on heterogeneity](#heterogeneity)).

Field experiments at Microsoft and Accenture provide complementary information: developers assigned to Copilot completed 12.9--21.8% more pull requests per week at Microsoft and 7.5--8.7% more at Accenture, though the authors emphasise imprecision and threats to inference including low compliance and organisational confounds [@mit-genai-copilot-field].
However, these throughput metrics do not account for code quality: independent security analyses find that 32.8% of Python and 24.5% of JavaScript snippets generated by Copilot are flagged with security issues [@arxiv:2310.02059], and Copilot can replicate known-vulnerable code patterns at rates around 33%, although it improves on unassisted human developers [@arxiv:2204.04741].
Productivity gains that increase time for human oversight (such as review, remediation, and incident risk) are not net gains.

### Clinical documentation agents

Ambient AI scribes---systems that listen to clinical encounters and generate draft documentation---represent one of the most actively deployed categories of agentic AI in healthcare.
Vendor procurement narratives frequently frame benefits in terms of "minutes saved per encounter"; for instance, Microsoft publicised "5 minutes saved per clinician per encounter on average" for its DAX Copilot product [@microsoft-dax-blog].

Evidence from controlled trials partly contradicts these claims.
A randomised controlled trial at UCLA across 238 physicians in 14 specialties compared two commercial ambient scribe tools (DAX and Nabla) against usual care, with approximately 24 000 encounters per arm [@pmc:PMC12768499].
Nabla reduced time-in-note by 9.5% relative to control (95% CI −17.2 to −1.8; P=0.02), while DAX showed no statistically significant effect (−1.7%, 95% CI −9.4 to +5.9; P=0.66).
Partial adoption was a key contextual factor: the tools were used in only approximately 30--34% of visits, and roughly 15% of treatment-group physicians never used their assigned scribe at all.
Clinicians did not strongly endorse that generated notes were "at least as good as my own"; and "occasional" clinically significant inaccuracies potentially led to a significant loss of time due to oversight activities.

A peer-matched cohort study of DAX in an integrated delivery system (99 providers, 12 specialties) found documentation EHR time fell from 5.3 to 4.54 minutes per patient---a saving of approximately 46 seconds---while after-hours EHR time *worsened* significantly, suggesting time-shifting rather than uniform savings [@pmc:PMC10990544].
A pre/post study of the Abridge ambient listening tool across 332 physicians confirmed sub-minute savings: mean time in notes per note fell from 5.11 to 4.16 minutes (difference 57 seconds, 95% CI 29--85) [@pmc:PMC12657781].
In this study, adoption increased from 15% to 50% of physicians in the study span of 8 weeks; however, the total number of notes created by the scribe only increased from 5% to 15% at the end of the study period.

The perception--reality mismatch that was found in [software engineering studies](#software-engineering-copilots) was replicated in a study of 252 physicians: 86.5% *perceived* that their documentation time had decreased, yet there was no overall association between perceived reductions and objectively measured time changes (OR 0.975, P=0.144) [@pubmed:41592210].
The objective effect was modest: each 10 percentage-point increase in AI scribe usage was associated with approximately 30 seconds lower documentation time per scheduled hour (P<0.001).

### Clinical decision support

Independent external validation of proprietary clinical AI models provides some of the starkest expectation--realisation gaps.
The Epic Sepsis Model, widely implemented across US hospitals, was externally validated in a large academic health system (38 455 hospitalisations) with an area under the receiver operating characteristic curve (AUROC) of 0.63 (95% CI 0.62--0.64), while Epic previously reported AUROC values of 0.76--0.83 [@doi:10.1001/jamainternmed.2021.3333].
At an operational alert threshold, the model achieved only 33% sensitivity (missing two thirds of septic patients), raising questions about clinical utility at scale.

In oncology decision support, IBM publicised concordance rates as high as 96% for Watson for Oncology in lung cancer cases relative to a multidisciplinary tumour board [@ibm-watson-asco-2017].
A subsequent peer-reviewed retrospective study in Korea found strict concordance of 48.9% for colon cancer, with "acceptable" concordance of 65.8% and strong heterogeneity by patient age (concordance dropping to approximately 20% among patients aged 70 and older) [@pubmed:30652564].
This discrepancy reflected both definition dependence---concordance rose substantially when "for consideration" was treated as concordant---and local constraint mismatches in guidelines, reimbursement, and patient demographics that prevent cross-site transferability.

## Why expectations overshoot

The empirical evidence points to three recurrent mechanistic drivers that explain why expectations systematically exceed realised outcomes, consistent with planning fallacies widely reported in the psychology literature [@doi:10.1037/h0034747;@{doi:10.1016/S0065-2601(10)43001-4}].

**Workflow integration friction and partial adoption.**
Agentic AI systems do not operate in isolation; they must integrate into existing workflows, tools, and team practices.
Clinical scribe evaluations repeatedly show partial adoption---tools used in a minority of encounters, with non-trivial drop-off over time [@pmc:PMC12768499;@pmc:PMC10990544].
Even when per-use effects are real, intention-to-treat estimates are attenuated by low compliance, and the practical benefit to an organisation depends on the adoption rate actually achieved, not the rate assumed during procurement.
This is not always a simple, temporary onboarding issue; the UCLA RCT's 30--34% utilisation rate was observed over the full study period [@pmc:PMC12768499].

**Verification and review burden.**
Agentic systems generate outputs that require human verification, and this verification cost is rarely accounted for in pre-deployment projections.
In the METR software engineering trial, the net slowdown occurred because the time spent reviewing, debugging, and integrating AI-generated code exceeded the time saved in initial generation [@arxiv:2507.09089].
In clinical documentation, neutral ratings on note quality and "occasional" clinically significant inaccuracies indicate non-trivial editing and review work that partially or fully offsets time-in-note reductions [@pmc:PMC12768499].
The DAX cohort's simultaneous reduction in documentation time and *increase* in after-hours EHR time concretely shows a shift of effort, as opposed to alleviation [@pmc:PMC10990544].

**Measurement construct mismatch.**
Pre-deployment expectations are often framed in metrics that do not correspond to what deployment-grade evaluations actually measure.
Vendor claims of "minutes saved per encounter" refer to broader workflow impacts, while trial outcomes measure "time-in-note"---one slice of documentation burden [@pmc:PMC12768499].
Developer-reported model performance (AUROC 0.76--0.83 for Epic's sepsis model) reflects evaluation choices that can systematically inflate apparent performance relative to development goals [@doi:10.1001/jamainternmed.2021.3333].
The gap between lab-task performance and field performance in software copilots is a measurement construct problem at its core: bounded tasks estimate *tool capability under low-context load*, while field trials estimate *net productivity under realistic verification and integration costs* [@arxiv:2507.09089;@arxiv:2302.06590].

## Heterogeneity as the default {#heterogeneity}

Across every domain reviewed, treatment effects are not uniform.
They are systematically moderated by baseline user efficiency, task complexity, and local context.
This implies that development of systems useful in practice requires careful planning that respects treatment heterogeneity.

In clinical documentation, objective time savings from AI scribes concentrate among physicians with higher baseline documentation inefficiency; efficient documenters derive minimal benefit [@pubmed:41592210].
In customer support, a field study of 5,172 agents found an average 15% productivity increase from a generative AI assistant, but gains were heavily concentrated among less experienced and lower-skilled workers, while the most experienced agents saw smaller gains and occasional quality declines [@arxiv:2304.11771].
This heterogeneity is not only observed inter-individually but also at the intra-individual level; given a single agent, gains from AI adoption are larger for relatively rare tasks, where human users have less baseline training and experience [@arxiv:2304.11771].
In software engineering, the METR trial specifically selected experienced developers working in familiar repositories---precisely the population most likely to have optimised their workflows already---and this is the population that was slowed [@arxiv:2507.09089].

**In summary, there is currently no stable, globally positive treatment effect for agentic AI.**
Average headline figures (whether from vendors, lab trials, or even well-designed field studies) will systematically misrepresent the benefit realised by any specific user, team, or organisation.
Planning that relies on average expected gains without modelling who benefits and who does not will over-invest in low-yield deployments and under-invest in targeted high-yield ones.

Adjacent experimental evidence reinforces this concern on a longer time horizon.
A randomised controlled trial in higher education found that students who used ChatGPT as a study aid scored significantly lower on a surprise retention test 45 days later (57.5% vs 68.5%; Cohen's d = 0.68) [@chatgpt-retention-rct], suggesting that cognitive offloading can trade immediate task completion for degraded durable learning---a dimension of "benefit" that short-term productivity metrics entirely miss.
A parallel study in software engineering found that AI use impaired conceptual understanding, code reading, and debugging abilities, without delivering significant efficiency gains on average [@doi:10.48550/arXiv.2601.20245].

## Implications for structured planning

The evidence reviewed here converges on a clear conclusion: pre-deployment expectations for agentic AI systems are poorly calibrated, and the resulting *expectation--realisation gap* is large enough to undermine investment decisions, deployment strategies, and trust.
This is not an argument against agentic AI---the evidence also shows that real gains exist in specific contexts and for specific user populations.
It is an argument for *structured planning that takes the gap seriously*.

Several design principles follow directly from the empirical patterns.
First, **benefit expectations must be explicit and quantified**, not framed as vague promises of efficiency.
The contrast between "5 minutes saved per encounter" marketing and sub-minute measured reductions illustrates what happens when expectations lack precision [@pmc:PMC12768499].
Second, **expectations should capture dual perspectives**---what users expect to gain and what developers assess as technically feasible. 
Miscalibration occurs on both sides: developers overshoot in internal validation; users overshoot in self-forecasts.
The estimate--reality mismatch in the METR study, which persisted even after implementation, illustrates the cognitive biases at play [@arxiv:2507.09089].
Third, **human oversight costs must be deducted** from projected benefits.
Every controlled trial reviewed here shows that verification, review, and cleanup absorb a substantial fraction of the gross time savings; ignoring this yields unrealistic net benefit estimates.
Fourth, **outcome metrics must link back to initial expectations** in the same units and at the same level of granularity, enabling direct comparison rather than post hoc rationalisation.
Ideally, plans are formalised early, versioned, and archived, in order to facilitate these later comparisons.
Fifth, **heterogeneity should be modelled explicitly** by specifying which user populations and task types are expected to benefit, rather than assuming uniform effects.

These principles are implemented in the [Agentic Automation Canvas (AAC)](https://aac.slolab.ai), a structured framework for designing, governing, and documenting agentic automation projects that captures user expectations as quantified benefit metrics with baseline values, confidence levels from both user and developer perspectives, and explicit accounting for human oversight [@doi:10.48550/arXiv.2602.15090].
The canvas formalises the bidirectional contract between stakeholders that the evidence reviewed here shows is necessary: without structured mechanisms for surfacing and testing expectations, the gap between aspiration and reality will persist.

## Conclusion

The expectation--realisation gap in agentic AI systems is empirically documented, directionally consistent, and mechanistically explainable.
Across software engineering, clinical documentation, and clinical decision support, pre-deployment expectations systematically overestimate realised benefits in deployment settings, regardless of whether they hail from user forecasts, vendor claims, or developer-reported metrics.
The drivers are complex, but not mysterious: workflow integration friction, verification burden, measurement construct mismatches, and treatment effect heterogeneity are observable, predictable, and addressable in principle.

Closing the expectation--realisation gap requires moving from *ad hoc* expectation-setting to structured, quantified planning that accounts for real-world integration costs, models heterogeneity across user populations, and links outcome measurement directly to initial benefit projections.
It also requires a mature interdisciplinary approach; mismatch from psychological bias cannot be countered by computer science methodology, and building better AI models will not solve all socio-technical problems in deployment and adoption.
The alternative to closing the gap is to continue relying on artificial benchmark results, marketing claims, and intuitive forecasts.
In all likelihood, this will perpetuate a cycle of over-promise and under-delivery that erodes trust in systems that, when properly targeted and governed, can deliver genuine value.


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>

