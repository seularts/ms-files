:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Sponsors](#div-sponsors){#sponsors-link .tab-link role="tab"
  aria-selected="false" aria-controls="sponsors"}

# OWASP Cloud-Native Application Security Top 10 {#owasp-cloud-native-application-security-top-10 .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
[![Follow on
Twitter](https://img.shields.io/twitter/follow/owaspcloudnati1?label=Follow%20%40owaspcloudnati1&style=social)](https://twitter.com/owaspcloudnati1)

## Overview

**Important Note:** This project is **very much alive**, and was last
updates in April 2022. We are currently looking for contributors willing
to draft the different categories, so please feel free to drop us an
email if you would like to assist.

Cloud native technologies empower organizations to build and run
scalable applications in modern, dynamic environments such as public,
private, and hybrid clouds. Containers, service meshes, microservices,
immutable infrastructure, and declarative APIs exemplify this approach.
Cloud-Native applications are a fundamentally new and exciting approach
to designing and building software. However, it also raises a completely
new set of security challenges. For example, when you move to a
microservice model, end-to-end visibility, monitoring and detection
become more complex and difficult to execute.\
\
The primary goal of the OWASP Cloud-Native Application Security Top 10
document is to provide assistance and education for organizations
looking to adopt Cloud-Native applications securely. The guide provides
information about what are the most prominent security risks for
cloud-native applications, the challenges involved, and how to overcome
them.

## Interim List of Risks - Currently Under Review!

The OWASP Cloud-Native Top 10 list is currently under development (July
2021). As part of our effort to collect feedback, we are presenting an
interim list below. Please feel free to contact the project leaders if
you have any feedback.

#### [CNAS-1: Insecure cloud, container or orchestration configuration](https://github.com/OWASP/www-project-cloud-native-application-security-top-10/blob/master/2022/en/src/0x01_insecure_cco_config.md)

Examples:

- Publicly open cloud storage buckets
- Imrpoper permissions set on cloud storage buckets
- Container runs as root
- Container shares resources with the host (network interface, etc.)
- Insecure Infrastructure-as-Code (IaC) configuration
- ...

#### [CNAS-2: Injection flaws (app layer, cloud events, cloud services)](https://github.com/OWASP/www-project-cloud-native-application-security-top-10/blob/master/2022/en/src/0x02_inj_flaws.md)

Examples:

- SQL injection
- XXE
- NoSQL injection
- OS command injection
- Serverless event data injection
- ...

#### [CNAS-3: Improper authentication & authorization](https://github.com/OWASP/www-project-cloud-native-application-security-top-10/blob/master/2022/en/src/0x03_improper_auth.md) {#cnas-3-improper-authentication--authorization}

Examples:

- Unauthenticated API access on a microservice
- Over-permissive cloud IAM role
- Lack of orchestrator node trust rules (e.g. unauthorized hosts joining
  the cluster)
- Unauthenticated orchestrator console access
- Unauthrized or overly-permissive orchestrator access

#### [CNAS-4: CI/CD pipeline & software supply chain flaws](https://github.com/OWASP/www-project-cloud-native-application-security-top-10/blob/master/2022/en/src/0x04_cicd_ssc_flaws.md) {#cnas-4-cicd-pipeline--software-supply-chain-flaws}

Examples:

- Insufficient authentication on CI/CD pipeline systems
- Use of untrusted images
- Use of stale images
- Insecure communication channels to registries
- Overly-permissive registry access
- Using a single environment to run CI/CD tasks for projects requiring
  different levels of security
- ...

#### [CNAS-5: Insecure secrets storage](https://github.com/OWASP/www-project-cloud-native-application-security-top-10/blob/master/2022/en/src/0x05_insecure_secrets.md)

Examples:

- Orchestrator secrets stored unencrypted
- API keys or passwords stored unencrypted inside containers
- Hardcoded application secrets
- Poorly encrypted secrets (e.g. use of obsolete encryption methods, use
  of encoding instead of encryption, etc.)
- Mounting of storage containing sensitive information
- ...

#### [CNAS-6: Over-permissive or insecure network policies](https://github.com/OWASP/www-project-cloud-native-application-security-top-10/blob/master/2022/en/src/0x06_over_permissive_network.md)

Examples:

- Over-permissive pod to pod communication allowed
- Internal microservices exposed to the public Internet
- No network segmentation defined
- End-to-end communications not encrypted
- Network traffic to unknown or potentially malicious domains not
  monitored and blocked
- ...

#### [CNAS-7: Using components with known vulnerabilities](https://github.com/OWASP/www-project-cloud-native-application-security-top-10/blob/master/2022/en/src/0x07_vuln_components.md)

Examples:

- Vulnerable 3rd party open source packages
- Vulnerable versions of application components
- Use of known vulnerable container images
- ...

#### [CNAS-8: Improper assets management](https://github.com/OWASP/www-project-cloud-native-application-security-top-10/blob/master/2022/en/src/0x08_asset_mgmt.md)

Examples:

- Undocumented microservices & APIs
- Obsolete & unmanaged cloud resources
- ...

#### [CNAS-9: Inadequate 'compute' resource quota limits](https://github.com/OWASP/www-project-cloud-native-application-security-top-10/blob/master/2022/en/src/0x09_compute_resources.md)

Examples:

- Resource-unbound containers
- Over-permissive request quota set on APIs
- ...

#### [CNAS-10: Ineffective logging & monitoring (e.g. runtime activity)](https://github.com/OWASP/www-project-cloud-native-application-security-top-10/blob/master/2022/en/src/0x0A_logging.md) {#cnas-10-ineffective-logging--monitoring-eg-runtime-activity}

Examples:

- No container or host process activity monitoring
- No network communications monitoring among microservices
- No resource consumption monitoring to ensure availability of critical
  resources
- Lack of monitoring on orchestration configuration propagation and
  stale configs
- ...

## Getting Involved

You do not have to be a security expert or a programmer to contribute.
Contact the project leader(s) to get involved, we welcome any type of
suggestion and comments. Possible ways to contribute:

- We are actively looking for organizations and individuals that will
  provide vulnerability prevalence data
- Translation efforts (later stages)
- Individuals and organizations that will contribute to the project will
  be listed on the acknowledgments page.
:::

::: {#sec-sponsors .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Project Sponsors
:::
:::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-cloud-native-application-security-top-10/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-cloud-native-application-security-top-10){.github-button
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

## Cloud Native Application Security Top 10 Information

![Documentation
Project](https://raw.githubusercontent.com/OWASP/www--site-theme/master/assets/images/common/owasp_documentation_project.svg?sanitize=true)

[![Builders](https://raw.githubusercontent.com/OWASP/www--site-theme/master/assets/images/common/owasp_builders.svg?sanitize=true)](https://www.owasp.org/index.php/Builders)
[![Breakers](https://raw.githubusercontent.com/OWASP/www--site-theme/master/assets/images/common/owasp_breakers.svg?sanitize=true)](https://www.owasp.org/index.php/Breakers)
[![Defenders](https://raw.githubusercontent.com/OWASP/www--site-theme/master/assets/images/common/owasp_defenders.svg?sanitize=true)](https://www.owasp.org/index.php/Defenders)

### Slack

[#cloud-native-app-sec-top-10](https://owasp.slack.com/archives/C024XB3408P)

### Leaders

- [Ory
  Segal](../cdn-cgi/l/email-protection.html#99f6ebe0eafcfef8f5d9fef4f8f0f5b7faf6f4)
- [Elad
  Shuster](../cdn-cgi/l/email-protection.html#7a1f161b1e5409120f090e1f083a150d1b090a5415081d)
- [Dean
  Agron](../cdn-cgi/l/email-protection.html#fc98999d92bc9384998599d29593)
- [Ron
  Vider](../cdn-cgi/l/email-protection.html#50223f3e103f283529357e393f)
- [Daniel
  Abeles](../cdn-cgi/l/email-protection.html#a1c5c0cfc8c4cd8fc0c3c4cdc4d2e1ced6c0d2d18fced3c6)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
