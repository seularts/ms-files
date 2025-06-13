:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Example](#div-example){#example-link .tab-link role="tab"
  aria-selected="false" aria-controls="example"}

# OWASP Secure by Design Framework {#owasp-secure-by-design-framework .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
OWASP Secure by Design Framework provides structured guidance on
embedding security during the architecture and system design phase.
Unlike OWASP Top 10, ASVS, or secure coding guidelines, this project
does not cover secure coding, vulnerabilities, or security assessments.
Instead, it ensures that:

- Architectural patterns enforce least privilege, isolation, and
  resilience.
- Microservice boundaries and API gateways follow strong security
  models.
- Messaging and event-driven security are designed upfront rather than
  patched later.
- Service communication and dependencies are structured to minimize
  risk.
- Data protection, encryption strategies, and compliance considerations
  are built into the architecture.

What this project does not cover:

- No secure coding practices (covered by OWASP ASVS and Top 10).
- No implementation-phase security (focuses only on design-phase
  security decisions).
- No vulnerability assessments (not a vulnerability-focused project).
- No threat modeling (Secure by Design lays the foundation, while threat
  modeling assesses a completed design for risks).

How this complements OWASP Threat Modeling:

- Secure by Design comes first to enforce security at the foundation.
- Threat Modeling follows to assess the architecture for risks before
  development starts.
- Without Secure by Design, Threat Modeling often reveals preventable
  security gaps, leading to costly redesigns.

This project fills a missing gap in OWASP by ensuring security is built
into architecture before development begins, reducing the need for later
security fixes and assessments.

### Road Map

Phase 1: Initial Draft (3-5 Months)

- Define core secure design principles.
- Structure the framework into modules (e.g., service isolation, API
  security, data security, etc.).
- Publish a draft document for early feedback.

Phase 2: Community Contributions (5-10 Months)

- Open the project for public review and contributions.
- Add real-world case studies and best practices.
- Conduct OWASP meetups and discussions to refine guidance.

Phase 3: Formal OWASP Framework Release (10-18 Months)

- Publish Version 1.0 of the OWASP Secure by Design Framework.
- Integrate with other OWASP projects (SAMM, ASVS, Cheat Sheets).
- Develop training materials and workshops.

Phase 4: Continuous Improvement

- Adapt the framework based on new threats and architectural trends.
- Collaborate with OWASP Threat Modeling, SAMM, and ASVS to ensure
  alignment.
:::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

Put whatever you like here: news, screenshots, features, supporters, or
remove this file and don't use tabs at all.
:::
:::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-secure-by-design-framework/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-secure-by-design-framework){.github-button
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

### Secure by Design Framework Information

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

- [Siamak
  Hatami](../cdn-cgi/l/email-protection.html#95e6fcf4f8d5fae2f4e6e5bbfae7f2)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
