::::::::::::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Features](#div-features){#features-link .tab-link role="tab"
  aria-selected="false" aria-controls="features"}
- [Integrations](#div-integrations){#integrations-link .tab-link
  role="tab" aria-selected="false" aria-controls="integrations"}
- [Installation](#div-installation){#installation-link .tab-link
  role="tab" aria-selected="false" aria-controls="installation"}
- [News](#div-news){#news-link .tab-link role="tab"
  aria-selected="false" aria-controls="news"}
- [Our Supporters](#div-supporters){#supporters-link .tab-link
  role="tab" aria-selected="false" aria-controls="supporters"}
- [Executive Order
  14028](#div-executive-order-14028){#executive-order-14028-link
  .tab-link role="tab" aria-selected="false"
  aria-controls="executive-order-14028"}

# OWASP Dependency-Track {#owasp-dependency-track .page-title}

:::::::::::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::::::: {#sec-main .section .page-body}
For more details about Dependency-Track see the projects website at
[dependencytrack.org](https://dependencytrack.org/)

Dependency-Track is an intelligent [Component
Analysis](../www-community/Component_Analysis.html) platform that allows
organizations to identify and reduce risk in the software supply chain.
Dependency-Track takes a unique and highly beneficial approach by
leveraging the capabilities of [Software Bill of
Materials](../www-community/Component_Analysis.html#software-bill-of-materials-sbom)
(SBOM). This approach provides capabilities that traditional Software
Composition Analysis (SCA) solutions cannot achieve.

<div>

::::::: {style="position:relative;padding-top:56.25%;"}
:::::: iframe
::: {#player}
:::

:::: player-unavailable
# A apărut o eroare. {#a-apărut-o-eroare. .message}

::: submessage
[Încearcă să vizionezi acest videoclip pe
www.youtube.com](https://www.youtube.com/watch?v=cQuk6jKTrTs){target="_blank"}
sau activează JavaScript (dacă este dezactivat în browser).
:::
::::
::::::
:::::::

</div>

Dependency-Track monitors component usage across all versions of every
application in its portfolio in order to proactively identify risk
across an organization. The platform has an API-first design and is
ideal for use in CI/CD environments.

![Screenshot](../../raw.githubusercontent.com/DependencyTrack/dependency-track/master/docs/images/screenshots/dashboard.png)
:::::::::

::: {#sec-features .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Features

- Consumes and produces [CycloneDX](https://cyclonedx.org/) Software
  Bill of Materials (SBOM)
- Consumes and produces CycloneDX Vulnerability Exploitability Exchange
  (VEX)
- Full-stack component support for:
  - Applications
  - Libraries
  - Frameworks
  - Operating systems
  - Containers
  - Firmware
  - Files
  - Hardware
  - Services
- Tracks component usage across every application in an organizations
  portfolio
- Quickly identify what is affected, and where
- Identifies multiple forms of risk including
  - Components with known vulnerabilities
  - Out-of-date components
  - Modified components
  - License risk
  - More coming soon...
- Integrates with multiple sources of vulnerability intelligence
  including:
  - [National Vulnerability Database](https://nvd.nist.gov/) (NVD)
  - [GitHub Advisories](https://www.github.com/advisories)
  - [Sonatype OSS Index](https://ossindex.sonatype.org/)
  - [VulnDB](https://vulndb.cyberriskanalytics.com/) from [Risk Based
    Security](https://www.riskbasedsecurity.com/)
  - More coming soon.
- Helps to prioritize mitigation by incorporating support for the
  [Exploit Prediction Scoring System
  (EPSS)](https://www.first.org/epss/)
- Maintain a private vulnerability database of vulnerability components
- Robust policy engine with support for global and per-project policies
  - Security risk and compliance
  - License risk and compliance
  - Operational risk and compliance
- Ecosystem agnostic with built-in repository support for:
  - Cargo (Rust)
  - Composer (PHP)
  - Gems (Ruby)
  - Hex (Erlang/Elixir)
  - Maven (Java)
  - NPM (Javascript)
  - NuGet (.NET)
  - Pypi (Python)
  - More coming soon.
- Identifies APIs and external service components including:
  - Service provider
  - Endpoint URIs
  - Data classification
  - Directional flow of data
  - Trust boundary traversal
  - Authentication requirements
- Includes a comprehensive auditing workflow for triaging results
- Configurable notifications supporting Slack, Microsoft Teams, WebEx,
  Webhooks, and Email
- Supports standardized SPDX license ID's and tracks license use by
  component
- Easy to read metrics for components, projects, and portfolio
- Native support for Kenna Security, Fortify SSC, ThreadFix, and
  DefectDojo
- API-first design facilitates easy integration with other systems
- API documentation available in OpenAPI format
- OAuth 2.0 + OpenID Connect (OIDC) support for single sign-on
  (authN/authZ)
- Supports internally managed users, Active Directory/LDAP, and API Keys
- Simple to install and configure. Get up and running in just a few
  minutes
:::

::: {#sec-integrations .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Integrations

![Integrations](../../raw.githubusercontent.com/DependencyTrack/dependency-track/master/docs/images/integrations.png)
:::

::::::: {#sec-installation .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Installation

Dependency-Track is distributed as Docker containers.

### Docker Compose

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
curl -LO https://dependencytrack.org/docker-compose.yml
docker-compose up -d
```
:::
::::

### Docker Swarm

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
curl -LO https://dependencytrack.org/docker-compose.yml
docker swarm init
docker stack deploy -c docker-compose.yml dtrack
```
:::
::::
:::::::

::: {#sec-news .section .page-body .tab-hidden}

------------------------------------------------------------------------

## News

- 2022/05/18
  [v4.5.0](https://docs.dependencytrack.org/2022/05/18/v4.5.0/) Released
- 2022/02/18
  [v4.4.1](https://docs.dependencytrack.org/2022/02/18/v4.4.1/) Released
- 2022/02/17
  [v4.4.0](https://docs.dependencytrack.org/2022/02/17/v4.4.0/) Released
- 2021/09/20
  [v4.3.6](https://docs.dependencytrack.org/2021/09/20/v4.3.6/) Released
- 2021/09/20
  [v4.3.5](https://docs.dependencytrack.org/2021/09/20/v4.3.5/) Released
- 2021/08/31
  [v4.3.4](https://docs.dependencytrack.org/2021/08/31/v4.3.4/) Released
- 2021/08/20
  [v4.3.3](https://docs.dependencytrack.org/2021/08/20/v4.3.3/) Released
- 2021/08/07
  [v4.3.2](https://docs.dependencytrack.org/2021/08/07/v4.3.2/) Released
- 2021/08/03
  [v4.3.1](https://docs.dependencytrack.org/2021/08/03/v4.3.1/) Released
- 2021/08/02
  [v4.3.0](https://docs.dependencytrack.org/2021/08/02/v4.3.0/) Released
- 2021/05/07
  [v4.2.2](https://docs.dependencytrack.org/2021/05/07/v4.2.2/) Released
- 2021/03/20
  [v4.2.1](https://docs.dependencytrack.org/2021/03/20/v4.2.1/) Released
- 2021/03/17
  [v4.2.0](https://docs.dependencytrack.org/2021/03/17/v4.2.0/) Released
- 2021/02/09
  [v4.1.0](https://docs.dependencytrack.org/2021/02/09/v4.1.0/) Released
- 2021/01/12
  [v4.0.1](https://docs.dependencytrack.org/2021/01/12/v4.0.1/) Released
- 2021/01/03
  [v4.0.0](https://docs.dependencytrack.org/2021/01/03/v4.0.0/) Released
- 2020/03/22
  [v3.8.0](https://docs.dependencytrack.org/2020/03/22/v3.8.0/) Released
- 2020/01/07
  [v3.7.1](https://docs.dependencytrack.org/2020/01/07/v3.7.1/) Released
- 2019/12/16
  [v3.7.0](https://docs.dependencytrack.org/2019/12/16/v3.7.0/) Released
- 2019/10/01
  [v3.6.1](https://docs.dependencytrack.org/2019/10/01/v3.6.1/) Released
- 2019/09/28
  [v3.6.0](https://docs.dependencytrack.org/2019/09/28/v3.6.0/) Released
- 2019/07/17
  [v3.5.1](https://docs.dependencytrack.org/2019/07/17/v3.5.1/) Released
- 2019/06/07
  [v3.5.0](https://docs.dependencytrack.org/2019/06/07/v3.5.0/) Released
- 2019/04/16
  [v3.4.1](https://docs.dependencytrack.org/2019/04/16/v3.4.1/) Released
- 2018/12/22
  [v3.4.0](https://docs.dependencytrack.org/2018/12/22/v3.4.0/) Released
- 2018/11/13
  [v3.3.1](https://docs.dependencytrack.org/2018/11/13/v3.3.1/) Released
- 2018/10/25
  [v3.3.0](https://docs.dependencytrack.org/2018/10/25/v3.3.0/) Released
- 2018/10/02
  [v3.2.2](https://docs.dependencytrack.org/2018/10/02/v3.2.2/) Released
- 2018/09/21
  [v3.2.1](https://docs.dependencytrack.org/2018/09/21/v3.2.1/) Released
- 2018/09/06
  [v3.2.0](https://docs.dependencytrack.org/2018/09/06/v3.2.0/) Released
- 2018/06/19
  [v3.1.0](https://docs.dependencytrack.org/2018/06/19/v3.1.0/) Released
- 2018/05/02
  [v3.0.4](https://docs.dependencytrack.org/2018/05/02/v3.0.4/) Released
- 2018/04/13
  [v3.0.3](https://docs.dependencytrack.org/2018/04/13/v3.0.3/) Released
- 2018/03/30
  [v3.0.2](https://docs.dependencytrack.org/2018/03/30/v3.0.2/) Released
- 2018/03/29
  [v3.0.1](https://docs.dependencytrack.org/2018/03/29/v3.0.1/) Released
- 2018/03/27
  [v3.0.0](https://docs.dependencytrack.org/2018/03/27/v3.0.0/) Released
- 2017/10/08 [v3.0 Updates to
  community](https://groups.google.com/forum/#!topic/dependency-track/0PUJI5rNgzI)
- 2017/06/16 [Presentation at OWASP Summit
  2017](https://www.youtube.com/watch?v=88YAlzuDH04&t=50s)
:::

::: {#sec-supporters .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Supporters

Dependency-Track is developed by a worldwide team of volunteers.

But we have also been helped by many organizations, either financially
or by encouraging their employees to work on Dependency-Track:

[![Risk Based
Security](assets/images/risk-based-security.png){width="250"}](https://www.riskbasedsecurity.com/){style="float:left; padding:2rem;"}

[![KPMG](assets/images/KPMG.svg){width="250"}](https://www.kpmg.com/){style="float:left; padding:2rem;"}
:::

::: {#sec-executive-order-14028 .section .page-body .tab-hidden}

------------------------------------------------------------------------

## U.S. Executive Order 14028 {#us-executive-order-14028}

Since its inception in 2013, OWASP Dependency-Track has been at the
forefront of analyzing bill of materials for cybersecurity risk
identification and reduction. Dependency-Track allows organizations and
governments to operationalize SBOM in conformance with [U.S. Executive
Order
14028](https://www.whitehouse.gov/briefing-room/presidential-actions/2021/05/12/executive-order-on-improving-the-nations-cybersecurity/).

- Supports the OWASP CycloneDX BOM format specifically defined in the
  [NTIA Minimum Elements For a Software Bill of
  Materials(SBOM)](https://www.ntia.gov/files/ntia/publications/sbom_minimum_elements_report.pdf)
- Consumes and analyzes SBOMs for known security, operational, and
  license risk
- Ideal for use in
  [procurement](https://docs.dependencytrack.org/usage/procurement/) and
  [continuous integration and
  delivery](https://docs.dependencytrack.org/usage/cicd/) environments
- Supports the OWASP CycloneDX VEX format exceeding the [Vulnerability
  Exploitability Exchange requirements defined by
  CISA](https://www.cisa.gov/sites/default/files/publications/VEX_Use_Cases_Document_508c.pdf)

### For software consumers

- Tracks all systems and applications that have SBOMs
- Upload SBOMs through the user interface or via automation
- Components defined in SBOMs will be analyzed for known vulnerabilities
  using multiple sources of vulnerability intelligence, including the
  [NVD](https://nvd.nist.gov/)
- Displays all identified vulnerabilities and vulnerable components for
  every SBOM analyzed
- Upload CycloneDX VEX obtained from suppliers to gain insight into the
  vulnerable components that pose risk, and the ones that don't
- Quickly identify all systems and applications that have a specific
  component or are affected by a specific vulnerability
- Helps to prioritize mitigation by incorporating support for the
  [Exploit Prediction Scoring System
  (EPSS)](https://www.first.org/epss/)
- Evaluate the portfolio of systems and applications against
  user-configurable security, operational, and license policies

### For software producers

- Create and consume CycloneDX SBOMs in development pipelines
- SBOMs will be analyzed for known security, operational, and license
  risk
- Evaluates the portfolio of applications against user-configurable
  security, operational, and license policies
- Inspect security findings and make audit decisions about the relevance
  and exploitability of each vulnerability
- CycloneDX BOMs can be dynamically generated from current inventory for
  any application
- CycloneDX VEX is dynamically generated from audit decisions for each
  application
- An API-first design allows software producers to extract SBOMs for
  released products, produce VEX whenever updated audit decisions are
  made, and make data available to internal systems responsible for SBOM
  and VEX distribution.

### Other considerations

- Both CycloneDX and Dependency-Track are full-stack solutions
  supporting software, hardware, and services. The CycloneDX standard
  and use with Dependency-Track is not limited to SBOM use cases.
- Software consumers may optionally audit security findings from vendor
  SBOMs. If consumers discover discrepancies in vendor supplied VEX,
  consumers can share their own auto-generated VEX with suppliers,
  completing a bi-directional exchange of vulnerability and
  exploitability information.
:::
::::::::::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/DependencyTrack/dependency-track/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/DependencyTrack/dependency-track){.github-button
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

### Project Information

-  [Flagship Project]{style="font-size: 1.3em;"}

#### Classification

-  Tool

#### Audience

-  Builder
-  Defender

### External Resources

- [Documentation](https://docs.dependencytrack.org/)
- [GitHub](https://github.com/DependencyTrack)
- [Slack](https://dependencytrack.org/slack) -
  [invite](https://dependencytrack.org/slack/invite)
- [Twitter](https://twitter.com/dependencytrack)
- [Website](https://dependencytrack.org/)
- [YouTube](https://www.youtube.com/channel/UC8xdttysl3gNAQYvk1J9Efg)

### Licensing

[Apache 2 License](https://www.apache.org/licenses/LICENSE-2.0)

### Leaders

- [Steve
  Springett](../cdn-cgi/l/email-protection.html#6b181f0e1d0e45181b1902050c0e1f1f2b041c0a181b4504190c)
- [Niklas
  Düster](../cdn-cgi/l/email-protection.html#2f414644434e5c014b5a4a5c5b4a5d6f40584e5c5f01405d48)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::::::::::::
