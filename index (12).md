:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Example](#div-example){#example-link .tab-link role="tab"
  aria-selected="false" aria-controls="example"}

# OWASP WAF Advanced Ruleset Management {#owasp-waf-advanced-ruleset-management .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::: {#sec-main .section .page-body}
# OWASP WARM -- WAF Advanced Ruleset Management {#owasp-warm--waf-advanced-ruleset-management}

![OWASP WARM
Logo](assets/images/logos/png/ColorLogo_noBackground.png){width="600"}

⸻

**OWASP WARM** tackles a critical challenge: improving the effectiveness
of the rulesets used by Web Application Firewalls (WAFs) to protect web
applications and APIs from attacks.

WAF rulesets---typically made up of regular expressions---are applied
generically, without taking into account how the protected application
is built or what types of input it expects. Furthermore, each rule is
often assigned a score that reflects the severity of the attack it
detects. This score is usually based on the experience of the ruleset
author and not on the specific context of the application in which the
ruleset is deployed.

Before going live, a tuning phase is necessary to reduce false positives
by:

- disabling overly sensitive rules,
- adjusting detection thresholds,
- reweighting rule scores.

This process is mostly manual, time-consuming, and error-prone. While it
reduces false positives, it can also severely undermine detection
capabilities---resulting in a suboptimal tradeoff between accuracy and
security.

*The Solution: Machine Learning for Smarter Tuning*

**OWASP WARM** introduces an innovative, machine learning--driven
approach to automate and improve this tuning process. By training a
simple linear model on real-world data, the system can:

- systematically explore all rule combinations,
- adjust rule scores based on actual traffic and attack patterns,
- identify an optimal balance between false positives and detection
  accuracy.

The project will focus on applying this method in real deployment
environments, starting with the widely adopted OWASP Core Rule Set
(CRS). The techniques developed will be generalizable and can be adapted
to other rulesets as well.

⸻

### Research

The following two scientific papers provide the foundational background
for the **OWASP WARM** project:

- **[ModSec-Learn: Boosting ModSecurity with Machine
  Learning](https://arxiv.org/abs/2406.13547)**\
  This paper introduces a machine learning-based approach to improve the
  effectiveness of ModSecurity, the most widely adopted open-source Web
  Application Firewall (WAF).

- **[Adversarial ModSecurity: Countering Adversarial SQL Injections with
  Robust Machine Learning](https://arxiv.org/abs/2308.04964)**\
  This study explores how adversarial examples can bypass WAF
  protections and presents a robust machine learning strategy to enhance
  SQL injection detection.

⸻

### Roadmap

Within the first 12 months, the project aims to deliver:

- Documentation explaining the problem and proposed approach
- Public datasets to reproduce experiments from the referenced study
  *"ModSec-Learn: Boosting ModSecurity with Machine Learning"*
- A first dataset of legitimate traffic
- A dataset of malicious traffic focused on SQL injection (SQLi) attacks
- Code and scripts to run the optimization process and update the scores
  of SQLi rules in production CRS-based environments

In the long term, the project will expand to include:

- Support for other attack categories (beyond SQLi)
- Production-ready tools to apply optimization on live traffic and
  deploy the resulting ruleset easily
- Performance evaluations on benchmark environments using the provided
  datasets
- Continuously updated documentation to track project progress

**OWASP WARM** empowers security teams to replace trial-and-error tuning
with data-driven optimization, turning WAF rule management into a
continuous and intelligent security enhancement process.

⸻

***Acknowledgments***

**OWASP WARM** is supported by the *APPtake* project
([www.apptake.eu](https://www.apptake.eu/)). *APPtake* is funded under
Grant Agreement No. ​101128082​ by the *European Cybersecurity Competence
Centre*.

::: {style="display: flex; align-items: center; gap: 20px;"}
![APPTake
Logo](assets/images/EU_projects_logos/APPTAKE_Logo.png){width="400"}
![ECCC Logo](assets/images/EU_projects_logos/ECCC_Logo.png){width="300"}
:::

**OWASP WARM** is supported by the *KINAITICS* project
([kinaitics.eu](http://kinaitics.eu/)). *KINAITICS* has received funding
from *Horizon Europe* under Grant Agreement No. 101070176.

::: {style="display: flex; align-items: center; gap: 20px;"}
![KINAITICS
Logo](assets/images/EU_projects_logos/KINAITICS_Logo.jpg){width="300"}
![ECCC
Logo](assets/images/EU_projects_logos/HORIZON2020_Logo.png){width="300"}
:::
:::::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

Put whatever you like here: news, screenshots, features, supporters, or
remove this file and don't use tabs at all.
:::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-waf-advanced-ruleset-management/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-waf-advanced-ruleset-management){.github-button
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

### WAF Advanced Ruleset Management Information

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

- [Davide
  Ariu](../cdn-cgi/l/email-protection.html#80e4e1f6e9e4e5aee1f2e9f5c0eff7e1f3f0aeeff2e7)
- [Luca
  Piras](../cdn-cgi/l/email-protection.html#d0bca5b3b1fea0b9a2b1a390bfa7b1a3a0febfa2b7)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::
