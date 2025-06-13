:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Join](#div-join){#join-link .tab-link role="tab"
  aria-selected="false" aria-controls="join"}
- [Contributors](#div-contributors){#contributors-link .tab-link
  role="tab" aria-selected="false" aria-controls="contributors"}

# OWASP Non-Human Identities Top 10 {#owasp-non-human-identities-top-10 .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
:::: {#sec-main .section .page-body}
::: alert
We\'re thrilled to introduce the [OWASP Non-Human Identities Top 10 for
2025](2025/index.html)!
:::

This comprehensive list highlights the most critical challenges in
integrating Non-Human Identities (NHIs) into the development lifecycle,
ranked based on exploitability, prevalence, detectability, and impact.

## What is Non-Human Identities top 10?

The Non-human identity (NHI) top 10 is a comprehensive list of the most
pressing security risks and vulnerabilities that non-human identities
present to organizations.

Production software environments are composed of a large number of
applications which need to be identified, resulting in "non-human
identities" or NHI. Application identities are often associated with
secrets, which are used as credentials similarly to the way humans
authenticate into computer systems. Application secrets may be used to
authenticate into other applications within the trust domain. They may
also be used to authenticate into 3rd party SaaS applications.

While long-term application secrets behave similarly to human passwords,
short term secrets may be generated on the fly by the run-time
environment, based on application attestation, where the environment
identifies the application and provisions it with credentials.

This project is aimed at helping security professionals thoroughly
understand their non-human identity attack surface, so they can better
protect and manage it. The project spans across thoroughly explaining
the risks and their potential exploits, as well as providing actionable
prevention practices and incident response playbooks.

## NHI Top 10 - 2025 - A sneak peek {#nhi-top-10---2025----a-sneak-peek}

- [NHI1:2025 - Improper
  Offboarding](2025/1-improper-offboarding/index.html)

Improper offboarding refers to the inadequate deactivation or removal of
non-human identities (NHIs) such as service accounts and access keys
when they are no longer needed. Unmonitored and deprecated services may
remain vulnerable, and their associated NHIs can be exploited by
attackers to gain unauthorized access to sensitive systems and data.
[Read More »](2025/1-improper-offboarding/index.html)

- [NHI2:2025 - Secret Leakage](2025/2-secret-leakage/index.html)

Secret Leakage refers to the leakage of sensitive NHIs such as API keys,
tokens, encryption keys, and certificates to unsanctioned data stores
throughout the software development lifecycle When secrets are leaked
---for instance, hard-coded into source code, stored in plain text
configuration files, or sent over public chat applications ---they
become susceptible to exposure. [Read
More »](2025/2-secret-leakage/index.html)

- [NHI3:2025 - Vulnerable Third-Party
  NHI](2025/3-vulnerable-third-party-nhi/index.html)

Third-party non-human identities (NHIs) are extensively integrated into
the development workflow, both through the use of integrated development
environments (IDEs) and their extensions and also through the use of 3rd
party SaaS. If a third-party extension is compromised---whether through
a security vulnerability or a malicious update---it can be exploited to
steal these credentials or misuse the granted permissions. [Read
More »](2025/2-secret-leakage/index.html)

- [NHI4:2025 - Insecure
  Authentication](2025/4-insecure-authentication/index.html)

Developers frequently integrate internal and external (third-party)
services into their applications. These services require access to
resources within these systems, necessitating authentication
credentials. However, some authentication methods are deprecated,
vulnerable to known attacks, or considered weak due to outdated security
practices. Utilizing insecure or obsolete authentication mechanisms can
expose organizations to significant risks. [Read
More »](2025/4-insecure-authentication/index.html)

- [NHI5:2025 - Overprivileged NHI](2025/5-overprivileged-nhi/index.html)

During application development and maintenance, developers or
administrators may assign NHIs with significantly more privileges than
required for their function. When an over-privileged NHI is compromised
--- whether through vulnerabilities in the application, malware, or
other security breaches --- attackers can exploit the excessive
permissions. [Read More »](2025/5-overprivileged-nhi/index.html)

- [NHI6:2025 - Insecure Cloud Deployment
  Configurations](2025/6-insecure-cloud-deployment-configurations/index.html)

Continuous Integration and Continuous Deployment (CI/CD) applications
enable developers to automate the process of building, testing, and
deploying code to production environments. These integrations often
require authentication with cloud services, typically achieved using
static credentials or OpenID Connect (OIDC). Static credentials can be
inadvertently exposed through code repositories, logs, or configuration
files. If compromised, these credentials can provide attackers with
persistent and potentially privileged access to production environments.
While OIDC offers a more secure alternative, if the identity tokens are
not properly validated or there are no strict conditions on token claims
unauthorized users might exploit these weaknesses to gain access. [Read
More »](2025/6-insecure-cloud-deployment-configurations/index.html)

- [NHI7:2025 - Long-Lived Secrets](2025/7-long-lived-secrets/index.html)

Long-lived Secrets refers to the use of sensitive NHIs such as API keys,
tokens, encryption keys, and certificates with expiration dates that are
too far in the future or that don't expire at all. If a breached secret
is long-lived, it provides attackers with access to sensitive services
without any time constraints. [Read
More »](2025/7-long-lived-secrets/index.html)

- [NHI8:2025 - Environment
  Isolation](2025/8-environment-isolation/index.html)

Environment isolation is a fundamental security practice in cloud
application deployment, where separate environments are used for
development, testing, staging, and production. NHIs are often utilized
during the deployment process and throughout an application's lifecycle.
However, reusing the same NHIs across multiple environments---especially
between testing and production---can introduce significant security
vulnerabilities. [Read More »](2025/8-environment-isolation/index.html)

- [NHI9:2025 - NHI Reuse](2025/9-nhi-reuse/index.html)

Reusing the same NHI across different applications, services, or
components --- even if they are deployed together --- introduces
significant security risks. If an NHI is compromised in one area, an
attacker can exploit it to gain unauthorized access to other parts of
the system that use the same credentials. [Read
More »](2025/9-nhi-reuse/index.html)

- [NHI10:2025 - Human Use of NHI](2025/10-human-use-of-nhi/index.html)

During application development and maintenance, developers or
administrators may misuse NHIs for manual tasks that should be performed
using individual human identities with appropriate privileges. This
practice introduces significant security risks such as elevated
privileges for NHIs, lack of auditing and accountability due to
indistinguishable activity between humans and automation. [Read
More »](2025/10-human-use-of-nhi/index.html)
::::

::: {#sec-join .section .page-body .tab-hidden}

------------------------------------------------------------------------

## How to contribute

Involvement in the development and promotion of OWASP Non-Human
Identities Top 10 is actively encouraged! You do not have to be a
security expert in order to contribute.

Here are some ways you can help:

- We are looking for organizations and individuals that will provide
  vulnerability prevalence data
- Translate the top 10 to non-English languages
- Review, critique and suggest improvements to the Top 10 list
- Star the [GitHub
  Project](https://github.com/OWASP/www-project-non-human-identities-top-10)
- Contribute real world examples to categories in the Top 10 list
- Add your Success Story - [tell
  us](../cdn-cgi/l/email-protection.html#94e6fbfafdbaf8fdf7fce0f9f5fad4fbe3f5e7e4bafbe6f3)
  and the world how you're using the Top 10 list
- Feel free to also add a note for the next periodic "OWASP Non-Human
  Identities Top 10" meeting
  [here](https://docs.google.com/document/d/1lJE0AwgWc4PHUX5Y0-s3TPhi6Lh8_dqWgsiEeJopkKY/edit?pli=1#heading=h.29vste2an1z).

Individuals and organizations that provide a significant contribution to
the project will be listed on the Contributors page.

## How to reach out:

- Give us feedback / suggestions / report bugs on
  [GitHub](https://github.com/OWASP/www-project-non-human-identities-top-10)
- Join our [email
  group](https://groups.google.com/g/owasp-non-human-identities)
- Contact the [project
  leads](../cdn-cgi/l/email-protection.html#d4a6bbbabdfab8bdb7bca0b9b5ba94bba3b5a7a4fabba6b3)
- Talk to us on [Slack](https://owasp.slack.com/archives/C02C6RU6G10)
  (#non-human-identities-top-10)

## Got an idea?

Got any ideas on how to make this project better? These guidelines will
help with how to get involved:

1.  Join the conversation on
    [email](https://groups.google.com/g/owasp-non-human-identities) or
    [Slack](https://owasp.slack.com/archives/C02C6RU6G10) to find
    collaborators or see if others have a similar interest.
2.  Search the project's [GitHub
    issues](https://github.com/OWASP/www-project-non-human-identities-top-10/issues)
    for related proposals. Found one? Join it!
3.  If you haven't found a relevant issue, create one! Clearly specify
    why your proposal is important and which changes are proposed.
    Advertise your proposal to others to find collaborators.

## Getting Started with your first Pull Request

A Pull Request (PR) can be created by [following these
steps](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork).

Remember to:

1.  Fork the repository.
2.  Create an initial draft implementing your proposal and submit it for
    review as a PR. Don't let perfect be the enemy of good.
3.  Advertise your proposal to others and ask for reviews.
4.  Once your PR is merged, continue to submit PRs to fine-tune and
    improve on previous versions.
5.  Congrats and thank you!
:::

::: {#sec-contributors .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Contributors

Individuals that provided a significant contribution to the project:

  Name              Affiliation       Contact
  ----------------- ----------------- ------------------------------------------------------------------------------------------------
  Roni Lichtman     Torch Security    [Twitter](https://x.com/roni_lichtman_) [LinkedIn](https://www.linkedin.com/in/roni-lichtman/)
  Tal Skverer       Astrix Security   [LinkedIn](https://www.linkedin.com/in/reverser/)
  Or Cohen          \-                [LinkedIn](https://www.linkedin.com/in/or-cohen-51a32b131/)
  Idan Basre        \-                [LinkedIn](https://www.linkedin.com/in/idan-basre/)
  Amir Benvenisti   \-                [LinkedIn](https://www.linkedin.com/in/amir-benvenisti/)
  Dor Dali          Cyolo             [LinkedIn](https://www.linkedin.com/in/dordali/)
  Jack Schofield    Snyk              [LinkedIn](https://www.linkedin.com/in/jackschofield85/)
  Tomer Yahalom     Astrix Security   [LinkedIn](https://www.linkedin.com/in/tomer-yahalom-4622b0178/)
  Danielle Guetta   Astrix Security   [LinkedIn](https://www.linkedin.com/in/danielle-guetta-94108310/)
  Bar Kaduri        Orca Security     [LinkedIn](https://www.linkedin.com/in/bar-kaduri)
  Yonatan Yosef     Orca Security     [LinkedIn](https://www.linkedin.com/in/yonatan-yosef-93a028188/)
  Adam Ochayon      Oasis Security    [LinkedIn](https://www.linkedin.com/in/adamochayon/)
  Yaron Sheffer     Intuit            [LinkedIn](https://www.linkedin.com/in/yaronf/)
  Ben Kim           Cremit            [LinkedIn](https://www.linkedin.com/in/ben-dh-kim/)

## Sponsors

The OWASP Non-Human Identities Top 10 project is sponsored by
[Astrix](https://astrix.security/)

\

[![astrix.security](assets/images/sponsor-logo-1.png){height="75"
width="334"}](https://astrix.security/)
:::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-non-human-identities-top-10/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-non-human-identities-top-10){.github-button
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

### Non-Human Identities Top 10 Information

[Incubator Project]{style="font-size: 1.3em;"} ![Documentation
Project](https://raw.githubusercontent.com/OWASP/www--site-theme/master/assets/images/common/owasp_documentation_project.svg?sanitize=true)

[Builders](https://www.owasp.org/index.php/Builders)
[Breakers](https://www.owasp.org/index.php/Breakers)
[Defenders](https://www.owasp.org/index.php/Defenders)

### License

[![CC BY-SA
4.0](assets/images/by-sa.svg){width="175px"}](http://creativecommons.org/licenses/by-sa/4.0/)

### Social and Community

[Slack](https://owasp.slack.com/archives/C02C6RU6G10)

[Email group](email-group.html)

### Code Repository

- [repo](https://github.com/OWASP/www-project-non-human-identities-top-10)

### Change Log

- [Top 10 2025 Release Notes](2025/release-notes/index.html)

### Leaders

- [Tal
  Skverer](../cdn-cgi/l/email-protection.html#a7d3c6cb89d4ccd1c2d5c2d5e7c8d0c6d4d789c8d5c0)
- [Roni
  Lichtman](../cdn-cgi/l/email-protection.html#493b2627206725202a213d24282709263e283a3967263b2e)
- [Or
  Cohen](../cdn-cgi/l/email-protection.html#b9d6cbdad6d1dcd7f9c9d8d5d6d8d5cdd6d7dccdced6cbd2ca97dad6d4)
- [Idan
  Basre](../cdn-cgi/l/email-protection.html#c2aba6a3aca0a3b1b0a782a5afa3abaeeca1adaf)
- [Amir
  Benvenisti](../cdn-cgi/l/email-protection.html#8eefe3e7fca0ecebe0f8ebe0e7fdfae7cee9e3efe7e2a0ede1e3)
- [Dor
  Dali](../cdn-cgi/l/email-protection.html#43272c3127222f2a03242e222a2f6d202c2e)
- [Jack
  Schofield](../cdn-cgi/l/email-protection.html#7c161d1f17520f1f14131a151910183c0f120517521513)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::
