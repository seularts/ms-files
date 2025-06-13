:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Roadmap](#div-roadmap){#roadmap-link .tab-link role="tab"
  aria-selected="false" aria-controls="roadmap"}
- [Start-Contributing](#div-contributing){#contributing-link .tab-link
  role="tab" aria-selected="false" aria-controls="contributing"}

# OWASP AI Testing Guide {#owasp-ai-testing-guide .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
:::: {#sec-main .section .page-body}
::: {align="center"}
![Alt text](assets/images/OWASP_AI_Testing_Guide.png){width="400"}
:::

As organizations increasingly adopt artificial intelligence (AI)
solutions, the need for a robust framework to rigorously test AI systems
for security, ethics, reliability, and compliance becomes essential.
Although numerous application security testing guides exist, such as the
OWASP Web Security Testing Guide (WSTG) and Mobile Security Testing
Guide (MSTG), the unique risks and challenges of AI systems require
specialized guidance.

The OWASP AI Testing Guide aims to become the reference for identifying
security, privacy, ethical, and compliance vulnerabilities inherent in
AI applications. Inspired by established OWASP methodologies, the AI
Testing Guide will deliver structured and practical guidance for
security professionals, testers, and AI developers. This guide will be
technology and industry agnostic, emphasizing applicability across
various AI implementation scenarios.

## Importance of AI Testing

AI testing is vital because AI now underpins critical decision-making
and daily operations across industries, from healthcare and finance to
automotive and cybersecurity. To ensure an AI system is truly reliable,
secure, accurate, and ethical, testing must go well beyond basic
functionality. It needs to validate bias and fairness controls to
prevent discrimination, conduct adversarial robustness checks against
crafted inputs designed to fool or hijack models, and perform security
and privacy assessments, such as model-extraction, data-leakage, and
poisoning attack simulations. Incorporating techniques like differential
privacy ensures compliance with data-protection laws while safeguarding
individual records. This guide's comprehensive approach to AI testing
aims to uncover hidden risks and maintain trust in AI-driven solutions.

## Why AI Testing is Unique

Testing AI systems presents unique challenges compared to traditional
software testing. AI models, especially those based on machine learning
(ML), exhibit non-deterministic behavior; since many AI algorithms
involve randomness, during training or inference making outputs
probabilistic rather than repeatable. This demands specialized
regression and stability tests that account for acceptable variance. AI
models learn from and depend on the quality and distribution of their
training data. Unlike traditional code, changing inputs (data drift) can
silently degrade performance, so tests must validate both data quality
and model output over time.

Because AI systems depend so heavily on the quality and integrity of
their training and input data, data-centric testing methodologies become
indispensable to ensure reliable, fair, and accurate model performance.
Unintended biases hidden in training data can lead to discriminatory
outcomes. AI testing must include fairness assessments and mitigation
strategies, which are not part of conventional software QA. The
complexity and "black-box" nature of certain AI systems, such as deep
learning neural networks, can obscure internal decision-making
processes, complicating verification and validation. Adversarial or
offensive security testing isn't just recommended, it's indispensable
for AI technologies.

Because AI models can be fooled or manipulated by carefully crafted
inputs (adversarial examples), organizations must employ dedicated
adversarial robustness testing methodologies that extend well beyond
standard functional tests. Without these specialized security
assessments, AI systems remain vulnerable to subtle attacks that can
compromise their integrity, reliability, and overall trustworthiness.

Finally all AI models live in ever-changing environments hence ongoing
monitoring and automated re-validation of both data and model
performance are essential to catch drift, emerging biases, or new
vulnerabilities.

## Purpose and Scope of the OWASP AI Testing Guide

The OWASP AI Testing Guide is designed to serve as a comprehensive
reference for software developers, architects, data analysts,
researchers, and risk officers, ensuring that AI risks are
systematically addressed throughout the product development lifecycle.
It outlines a robust suite of tests, ranging from data‐centric
validation and fairness assessments to adversarial robustness and
continuous performance monitoring, that collectively provide documented
evidence of risk validation and control. By following this guidance,
teams can establish the level of trust required to confidently deploy AI
systems into production, with verifiable assurances that potential
biases, vulnerabilities, and performance degradations have been
proactively identified and mitigated.

### Start contributing [DRAFT](https://github.com/OWASP/www-project-ai-testing-guide)
::::

::: {#sec-roadmap .section .page-body .tab-hidden}

------------------------------------------------------------------------

### Road Map

### Road Map

We wrote a first draft
[here](https://github.com/MatOwasp/AI-Testing-Guide)

Phase 1: Initial Draft and Community Formation (JUNE 2025) Publish an
initial project outline clearly defining the scope, mission, and testing
categories. Establish an OWASP GitHub repository and set up a dedicated
community team. Conduct initial outreach to invite contributions from
the OWASP and AI communities.

Phase 2: Framework Development and First Release (SEPTEMBER 2025)
Develop detailed testing guidelines covering key AI-specific risks
including model security, data poisoning, adversarial robustness, prompt
injection, privacy, and ethics validation. Publish a draft version for
public review and community feedback. Begin pilot testing the guide's
methodologies in collaboration with industry partners to gather
practical insights and validate effectiveness.

Phase 3: Refinement, Release, and Promotion (DECEMBER 2025) Incorporate
community and industry feedback to finalize the first official release
of the OWASP AI Testing Guide. Present the guide at global OWASP
conferences, including hosting workshops and interactive sessions to
encourage broader adoption and continuous improvement. Establish a
structured update cycle to ensure ongoing relevance with advancements in
AI.
:::

::: {#sec-contributing .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Start Contributing

The OWASP projects are an open source effort, and we enthusiastically
welcome all forms of contributions and feedback.

- 📥 Send your suggestion, propose your concepts to the [project
  leader](../cdn-cgi/l/email-protection.html#acc1cdd8d8c9c382c1c9d9cfcfc5ecc3dbcddfdc82c3decb).
- 👋 Join OWASP in our [Slack](#) workspace.
- Start contributing
  [Here](https://github.com/OWASP/www-project-ai-testing-guide/blob/master/DRAFT/README.md)

### Project Lead

- [Matteo Meucci (Synapsed.ai)](https://www.linkedin.com/in/meucci/) -
  [[\[email protected\]]{.__cf_email__
  cfemail="3d505c49495852135058485e5e547d524a5c4e4d13524f5a"}](../cdn-cgi/l/email-protection.html#462b2732322329682b233325252f06293127353668293421)
- [Marco Morana (Avocado Systems)](https://www.linkedin.com/in/go4it/) -
  [[\[email protected\]]{.__cf_email__
  cfemail="4a272b3829256427642725382b242b0a2d272b232664292527"}](../cdn-cgi/l/email-protection.html#4825293a2b2766256625273a292629082f25292124662b2725)
:::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-ai-testing-guide/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-ai-testing-guide){.github-button
icon="octicon-star" data-size="large" show-count="true"
aria-label="Star on GitHub"}
:::

:::::: {.sidebar role="complementary"}
::: owasp-sidebar-top
**The OWASP^®^ Foundation** works to improve the security of software
through its community-led open source software projects, hundreds of
chapters worldwide, tens of thousands of members, and by hosting local
and global conferences.
:::

### AI Testing Guide Information

- [Incubator Project](#)
- [Type of Project](#)
- [Version 0.0.0](#)
- [Builder](#)
- [Breaker](#)

### Downloads or Social Links

- [Download](#)
- [Meetup](#)

### Code Repository

- [repo](#)

### Change Log

- [changes](#)

### Leaders

- [Matteo
  Meucci](../cdn-cgi/l/email-protection.html#4c012d38382923622129392f2f250c233b2d3f3c62233e2b)
- [Marco
  Morana](../cdn-cgi/l/email-protection.html#5c313d2e3f3372317231332e3d323d1c3b313d3530723f3331)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::
