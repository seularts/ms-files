:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Example](#div-example){#example-link .tab-link role="tab"
  aria-selected="false" aria-controls="example"}

# OWASP Top 10 for Large Language Model Applications {#owasp-top-10-for-large-language-model-applications .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
The OWASP Top 10 for Large Language Model Applications Project aims to
educate developers, designers, architects, managers, and organizations
about the potential security risks when deploying and managing Large
Language Models (LLMs) and Generative AI applications. The project
provides a range of resources. Most notably the OWASP Top 10 list for
LLM applications listing the top 10 most critical vulnerabilities often
seen in LLM applications, highlighting their potential impact, ease of
exploitation, and prevalence in real-world applications.

Examples of vulnerabilities include prompt injections, data leakage,
inadequate sandboxing, and unauthorized code execution, among others.
The goal is to raise awareness of these vulnerabilities, suggest
remediation strategies, and ultimately improve the security posture of
LLM applications.

## 📢 The 2025 List is Available: {#-the-2025-list-is-available}

Download OWASP Top 10 for LLM Applications List for 2025 [Full
Version](https://genai.owasp.org/resource/owasp-top-10-for-llm-applications-2025/).

## Download Additional Resources from our [Website](https://genai.owasp.org/) including:

- [Security & Governance Checklist
  v1.0](https://genai.owasp.org/resource/llm-applications-cybersecurity-and-governance-checklist-english/)
  Essential guidance for CISOs managing the rollout of Gen AI
  technology.
- [Guide for Preparing and Responding to
  DeepFakes](https://genai.owasp.org/resource/guide-for-preparing-and-responding-to-deepfake-events/)
- [2025 AI Security Solutions Directory and
  Guide](https://genai.owasp.org/ai-security-solutions-landscape/)

## Localized versions are also available. {#localized-versions-are-also-available}

- Security & Governance Checklist v1.0 - also now [available in
  French](llm-top-10-governance-doc/LLM_AI_Security_and_Governance_Checklist-v1_FR.html)
  and
  [Japanese](llm-top-10-governance-doc/LLM_AI_Security_and_Governance_Checklist-v1_1_JP.html)

## Want to Contribute your Expertise? Join us. {#want-to-contribute-your-expertise-join-us}

- We have a working group channel on the [OWASP
  Slack](../slack/invite.html), so please sign up and then join us on
  the #project-top10-for-llm channel.
- The working group is collaborating on our
  [wiki](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications/wiki)
- Want to stay updated on periodic progress? [Subscribe to our
  newsletter](https://llmtop10.beehiiv.com/subscribe) or [Follow our
  project LinkedIn
  page](https://www.linkedin.com/company/owasp-top-10-for-large-language-model-applications/)

## Just Want to Learn About LLM Security

New to LLM Application security? Check out our [resources
page](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications/wiki/Educational-Resources)
to learn more.

## Become a Project Supporter or Sponsor Sponsorship

We are a not for profit open source community driven project. If you are
interested in supporting the project with reasources or become a sponsor
to help us ensure we can continue to sustain the community efforts,
offsetting operational, and outreach costs. Visit the [Sponsor
Section](https://genai.owasp.org/sponsorship) on our website.

## Thank you to our Current [Sponsors and Supporters](https://genai.owasp.org/supporters/)
:::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

# OWASP Top 10 for Large Language Model Applications version 1.1 {#owasp-top-10-for-large-language-model-applications-version-11}

## LLM01: Prompt Injection

Manipulating LLMs via crafted inputs can lead to unauthorized access,
data breaches, and compromised decision-making.

## LLM02: Insecure Output Handling

Neglecting to validate LLM outputs may lead to downstream security
exploits, including code execution that compromises systems and exposes
data.

## LLM03: Training Data Poisoning

Tampered training data can impair LLM models leading to responses that
may compromise security, accuracy, or ethical behavior.

## LLM04: Model Denial of Service

Overloading LLMs with resource-heavy operations can cause service
disruptions and increased costs.

## LLM05: Supply Chain Vulnerabilities

Depending upon compromised components, services or datasets undermine
system integrity, causing data breaches and system failures.

## LLM06: Sensitive Information Disclosure

Failure to protect against disclosure of sensitive information in LLM
outputs can result in legal consequences or a loss of competitive
advantage.

## LLM07: Insecure Plugin Design

LLM plugins processing untrusted inputs and having insufficient access
control risk severe exploits like remote code execution.

## LLM08: Excessive Agency

Granting LLMs unchecked autonomy to take action can lead to unintended
consequences, jeopardizing reliability, privacy, and trust.

## LLM09: Overreliance

Failing to critically assess LLM outputs can lead to compromised
decision making, security vulnerabilities, and legal liabilities.

## LLM10: Model Theft

Unauthorized access to proprietary large language models risks theft,
competitive advantage, and dissemination of sensitive information.
:::
:::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-top-10-for-large-language-model-applications/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-top-10-for-large-language-model-applications){.github-button
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

### Top 10 for Large Language Model Applications Information

- [Lab Status Project](../projects/index.html)
- [Version
  2025](https://genai.owasp.org/resource/owasp-top-10-for-llm-applications-2025/)
- [Version 1.1.0
  Translations](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications/tree/main/assets/translations)
  (archived)
- [Version 1.1.0](assets/PDF/OWASP-Top-10-for-LLMs-2023-v1_1.pdf)
  (archived)
- [Version 1.0.1](assets/PDF/OWASP-Top-10-for-LLMs-2023-v1_0_1.pdf)
  (archived)
- [Version 1.0.0](assets/PDF/OWASP-Top-10-for-LLMs-2023-v1_0.pdf)
  (archived)
- [Version 0.9.0](assets/PDF/OWASP-Top-10-for-LLMs-2023-v09.pdf)
  (archived)
- [Version 0.5.0](assets/PDF/OWASP-Top-10-for-LLMs-2023-v05.pdf)
  (archived)
- [Version 0.1.0](Archive/0_1_vulns/index.html) (archived)

### Social Links

- [Subscribe to our Newsletter](https://llmtop10.beehiiv.com/subscribe)
- [v1.1
  Announcement](https://www.linkedin.com/pulse/new-release-owasp-top-10-llm-apps-steve-wilson?trk=public_post_feed-article-content)
- [v1
  Announcement](https://www.linkedin.com/pulse/official-release-owasp-top-10-large-language-model-v10-steve-wilson/)
- [Project
  Announcement](https://www.linkedin.com/pulse/announcing-owasp-top-10-large-language-models-ai-project-steve-wilson/)
- [Share on
  Twitter](https://twitter.com/intent/tweet?url=https://owasp.org/www-project-top-10-for-large-language-model-applications/&text=Check%20out%20the%20OWASP%20Top%2010%20for%20Large%20Language%20Model%20Applications%20project:%20)
- [Share on
  LinkedIn](https://www.linkedin.com/sharing/share-offsite/?url=https://owasp.org/www-project-top-10-for-large-language-model-applications/)

### Code Repository

- [repo](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications)
- [wiki](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications/wiki)

### Change Log

- [changes](changes.html)

### Leaders

- Lead [Steve
  Wilson](../cdn-cgi/l/email-protection.html#0477706172612a736d68776b6a446b736577742a6b7663) -
  [LinkedIn](https://www.linkedin.com/in/wilsonsd/)
  [Twitter](https://twitter.com/virtualsteve)
- Co-lead [Ads
  Dawson](../cdn-cgi/l/email-protection.html#e7868394c9838690948889a78890869497c9889580) -
  [LinkedIn](https://www.linkedin.com/in/adamdawson0/)
  [GitHub](https://github.com/GangGreenTemperTatum)
- Co-lead [John
  Sotiropoulos](../cdn-cgi/l/email-protection.html#12787d7a7c3c617d667b607d627d677e7d61527d657361623c7d6075) -
  [LinkedIn](https://www.linkedin.com/in/jsotiropoulos/)
- Co-lead [Scott
  Clinton](../cdn-cgi/l/email-protection.html#afdcccc0dbdb81ccc3c6c1dbc0c1efc0d8cedcdf81c0ddc8) -
  [LinkedIn](https://www.linkedin.com/in/scottjclinton/)

### Core Leadership vTeam

- Full Core Team [Team
  Page](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications/wiki/Core-Team)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
