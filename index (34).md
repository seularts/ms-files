:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Contributors](#div-contributors){#contributors-link .tab-link
  role="tab" aria-selected="false" aria-controls="contributors"}
- [Join](#div-join){#join-link .tab-link role="tab"
  aria-selected="false" aria-controls="join"}
- [Roadmap](#div-roadmap){#roadmap-link .tab-link role="tab"
  aria-selected="false" aria-controls="roadmap"}

# OWASP Top 10 CI/CD Security Risks {#owasp-top-10-cicd-security-risks .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![alt_text](assets/images/risks.png)

# Introduction

CI/CD environments, processes, and systems are the beating heart of any
modern software organization. They deliver code from an engineer's
workstation to production. Combined with the rise of the DevOps
discipline and microservice architectures, CI/CD systems and processes
have reshaped the engineering ecosystem:

- The technical stack is more diverse, both in relation to coding
  languages as well as to technologies and frameworks adopted further
  down the pipeline (e.g. GitOps, K8s).
- Adoption of new languages and frameworks is increasingly quicker,
  without significant technical barriers.
- There is an increased use of automation and Infrastructure as Code
  (IaC) practices.
- 3rd parties, both in the shape of external providers as well as
  dependencies in code, have become a major part of any CI/CD ecosystem,
  with the integration of a new service typically requiring no more than
  adding 1-2 lines of code.

These characteristics allow faster, more flexible and diverse software
delivery. However, they have also reshaped the attack surface with a
multitude of new avenues and opportunities for attackers.

Adversaries of all levels of sophistication are shifting their attention
to CI/CD, realizing CI/CD services provide an efficient path to reaching
an organization's crown jewels. The industry is witnessing a significant
rise in the amount, frequency and magnitude of incidents and attack
vectors focusing on abusing flaws in the CI/CD ecosystem, including -

- The compromise of the **SolarWinds** build system, used to spread
  malware through to 18,000 customers.
- The **Codecov** breach, that led to exfiltration of secrets stored
  within environment variables in thousands of build pipelines across
  numerous enterprises.
- The **PHP breach**, resulting in publication of a malicious version of
  PHP containing a backdoor.
- The **Dependency Confusion** flaw, which affected dozens of giant
  enterprises, and abuses flaws in the way external dependencies are
  fetched to run malicious code on developer workstations and build
  environments.
- The compromises of the ***ua-parser-js*, *coa* and *rc* NPM
  packages**, with millions of weekly downloads each, resulting in
  malicious code running on millions of build environments and developer
  workstations.

While attackers have adapted their techniques to the new realities of
CI/CD, most defenders are still early on in their efforts to find the
right ways to detect, understand, and manage the risks associated with
these environments. Seeking the right balance between optimal security
and engineering velocity, security teams are in search for the most
effective security controls that will allow engineering to remain agile
without compromising on security.

# The "Top 10 CI/CD Security Risks" initiative

This document helps defenders identify focus areas for securing their
CI/CD ecosystem. It is the result of extensive research into attack
vectors associated with CI/CD, and the analysis of high profile breaches
and security flaws.

Numerous industry experts across multiple verticals and disciplines came
together to collaborate on this document to ensure its relevance to
today's threat landscape, risk surface, and the challenges that
defenders face in dealing with these risks.

We would like to thank and acknowledge all experts which took part in
reviewing and validating this document.

## Authors

- [Daniel Krivelevich](https://twitter.com/Dkrivelev) (CTO @ Cider
  Security)
- [Omer Gil](https://twitter.com/omer_gil) (Director of Research @ Cider
  Security)

## Reviewers

- [Iftach Ian Amit](https://twitter.com/iiamit) (Advisory CSO @ Rapid7)
- [Jonathan Claudius](https://twitter.com/claudijd) (CISO @ Jump Crypto)
- [Michael Coates](https://twitter.com/_mwc) (CEO & Co-Founder @
  Altitude Networks, Former CISO @ Twitter)
- Jonathan Jaffe (CISO @ Lemonade Insurance)
- Adrian Ludwig (Chief Trust Officer @ Atlassian)
- [Travis McPeak](https://twitter.com/travismcpeak) (Head of Product
  Security @ Databricks)
- Ron Peled (Founder & CEO @ ProtectOps, Former CISO @ LivePerson)
- [Ty Sbano](https://twitter.com/tysbano) (CISO @ Vercel)
- [Astha Singhal](https://twitter.com/astha_singhal) (Director of
  Application Security @ Netflix)
- [Hiroki Suezawa](https://twitter.com/rung) (Security Engineer @
  Mercari, inc.)
- Tyler Welton (Principal Security Engineer @ Built Technologies, Owner
  @ Untamed Theory)
- Tyler Young (Head of Security at Relativity)
- [Ory Segal](https://twitter.com/orysegal) (Senior Director, Product
  Management @ Palo Alto Networks)
- Noa Ginzbursky (DevOps Engineer @ Cider Security)
- [Asi Greenholts](https://twitter.com/TupleType) (Security Researcher @
  Cider Security)

# Top 10 risks

Presented below are the top 10 CI/CD security risks. All risks follow a
consistent structure -

- **Definition** - Concise definition of the nature of the risk.
- **Description** - Detailed explanation of the context and the
  adversary motivation.
- **Impact** - Detail around the potential impact the realization of the
  risk can have on an organization.
- **Recommendations** - A set of measures and controls recommended for
  optimizing an organization's CI/CD posture in relation to the risk in
  question.
- **References** - A list of real world examples and precedents in which
  the risk in question was exploited.

The list was compiled on the basis of extensive research and analysis
based on the following sources:

- Analysis of the architecture, design and security posture of hundreds
  of CI/CD environments across multiple verticals and industries.
- Profound discussions with industry experts.
- Publications detailing incidents and security flaws within the CI/CD
  security domain. Examples are provided where relevant.

[List of the top 10 CI/CD security
risks:]{style="text-decoration:underline;"}

[CICD-SEC-1](CICD-SEC-01-Insufficient-Flow-Control-Mechanisms.html):
Insufficient Flow Control Mechanisms

[CICD-SEC-2](CICD-SEC-02-Inadequate-Identity-And-Access-Management.html):
Inadequate Identity and Access Management

[CICD-SEC-3](CICD-SEC-03-Dependency-Chain-Abuse.html): Dependency Chain
Abuse

[CICD-SEC-4](CICD-SEC-04-Poisoned-Pipeline-Execution.html): Poisoned
Pipeline Execution (PPE)

[CICD-SEC-5](CICD-SEC-05-Insufficient-PBAC.html): Insufficient PBAC
(Pipeline-Based Access Controls)

[CICD-SEC-6](CICD-SEC-06-Insufficient-Credential-Hygiene.html):
Insufficient Credential Hygiene

[CICD-SEC-7](CICD-SEC-07-Insecure-System-Configuration.html): Insecure
System Configuration

[CICD-SEC-8](CICD-SEC-08-Ungoverned-Usage-of-3rd-Party-Services.html):
Ungoverned Usage of 3rd Party Services

[CICD-SEC-9](CICD-SEC-09-Improper-Artifact-Integrity-Validation.html):
Improper Artifact Integrity Validation

[CICD-SEC-10](CICD-SEC-10-Insufficient-Logging-And-Visibility.html):
Insufficient Logging and Visibility
:::

::: {#sec-contributors .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Founders

  ---------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------ -------------------------------------------------------------
  [Daniel Krivelevich](../cdn-cgi/l/email-protection.html#5e3a3f30373b321e3d373a3b2c2d3b3d2b2c372a27703731) (Co-Founder & CTO, Cider Security)   [Twitter](https://twitter.com/Dkrivelev)   [LinkedIn](https://www.linkedin.com/in/daniel-krivelevich/)
  [Omer Gil](../cdn-cgi/l/email-protection.html#8de2e0e8ffcdeee4e9e8fffee8eef8ffe4f9f4a3e4e2) (Director Of Research, Cider Security)             [Twitter](https://twitter.com/omer_gil)    [LinkedIn](https://www.linkedin.com/in/omer-gil/)
  ---------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------ -------------------------------------------------------------

## Sponsors

[![Cider
Security](assets/images/cider_logo.png)](https://www.cidersecurity.io/)

## Contributors

   
  ----------------------------------------------------------------------------------------------------------
  **Project Reviewers**
  [Iftach Ian Amit](https://twitter.com/iiamit) (Advisory CSO @ Rapid7)
  [Jonathan Claudius](https://twitter.com/claudijd) (CISO @ Jump Crypto)
  [Michael Coates](https://twitter.com/_mwc) (CEO & Co-Founder @ Altitude Networks, Former CISO @ Twitter)
  Jonathan Jaffe (CISO @ Lemonade Insurance)
  Adrian Ludwig (Chief Trust Officer @ Atlassian)
  [Travis McPeak](https://twitter.com/travismcpeak) (Head of Product Security @ Databricks)
  Ron Peled (Founder & CEO @ ProtectOps, Former CISO @ LivePerson)
  [Ty Sbano](https://twitter.com/tysbano) (CISO @ Vercel)
  [Astha Singhal](https://twitter.com/astha_singhal) (Director of Application Security @ Netflix)
  [Hiroki Suezawa](https://twitter.com/rung) (Security Engineer @ Mercari, inc.)
  Tyler Welton (Principal Security Engineer @ Built Technologies, Owner @ Untamed Theory)
  Tyler Young (Head of Security at Relativity)
  [Ory Segal](https://twitter.com/orysegal) (Senior Director, Product Management @ Palo Alto Networks)
  Noa Ginzbursky (DevOps Engineer @ Cider Security)
  [Asi Greenholts](https://twitter.com/TupleType) (Security Researcher @ Cider Security)
:::

::: {#sec-join .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Get Involved

Get involved in **OWASP Top 10 CI/CD Security Risks**!

We encourage the community - security experts, devops engineers,
programmers, and anyone who's interested - to join and contribute.
Contact the Project Leaders to get involved, we welcome any type of
suggestions and comments.

## GitHub

The project is maintained in the [Top 10 CI/CD Security
Risks](https://github.com/cider-security-research/top-10-cicd-security-risks)
GitHub repository.

Feel free to open or solve an issue.
:::

::: {#sec-roadmap .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Project Roadmap

- Initial release: v1.0, September 2022
- Project promotion, additional reviews: October, 2022
- Stable release: v1.0, October 2022
:::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-top-10-ci-cd-security-risks/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-top-10-ci-cd-security-risks){.github-button
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

### Top 10 CI-CD Security Risks Information

-  [Lab Project]{style="font-size: 1.3em;"}

#### Classification

-  Documentation

#### Audience

-  Builder
-  Breaker
-  Defender

### Downloads or Social Links

- [Download](https://github.com/OWASP/www-project-top-10-ci-cd-security-risks/raw/3204d6d181e2a5517ffdcbe208fb536b9cc6c50b/assets/OWASP_Top_10_CICD_Risks.pdf)

### Code Repository

- [GitHub](https://github.com/cider-security-research/top-10-cicd-security-risks)

### Top 10 CI/CD Security Risks

- [Return to homepage](index.html)
- [CICD-SEC-1: Insufficient Flow Control
  Mechanisms](CICD-SEC-01-Insufficient-Flow-Control-Mechanisms.html)
- [CICD-SEC-2: Inadequate Identity and Access
  Management](CICD-SEC-02-Inadequate-Identity-And-Access-Management.html)
- [CICD-SEC-3: Dependency Chain
  Abuse](CICD-SEC-03-Dependency-Chain-Abuse.html)
- [CICD-SEC-4: Poisoned Pipeline
  Execution](CICD-SEC-04-Poisoned-Pipeline-Execution.html)
- [CICD-SEC-5: Insufficient PBAC](CICD-SEC-05-Insufficient-PBAC.html)
- [CICD-SEC-6: Insufficient Credential
  Hygiene](CICD-SEC-06-Insufficient-Credential-Hygiene.html)
- [CICD-SEC-7: Insecure System
  Configuration](CICD-SEC-07-Insecure-System-Configuration.html)
- [CICD-SEC-8: Ungoverned Usage of 3rd Party
  Services](CICD-SEC-08-Ungoverned-Usage-of-3rd-Party-Services.html)
- [CICD-SEC-9: Improper Artifact Integrity
  Validation](CICD-SEC-09-Improper-Artifact-Integrity-Validation.html)
- [CICD-SEC-10: Insufficient Logging and
  Visibility](CICD-SEC-10-Insufficient-Logging-And-Visibility.html)

### Leaders

- [Daniel
  Krivelevich](../cdn-cgi/l/email-protection.html#096d6867606c65496a606d6c7b7a6c6a7c7b607d70276066)
- [Omer
  Gil](../cdn-cgi/l/email-protection.html#bad5d7dfc894ddd3d6fad5cddbc9ca94d5c8dd)
- [Ory
  Segal](../cdn-cgi/l/email-protection.html#610e13184f120406000d210e160012114f0e1306)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::
