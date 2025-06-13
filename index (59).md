::::::::::: main-wrapper
# OWASP secureCodeBox {#owasp-securecodebox .page-title}

:::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![logo](assets/images/logo.png "Logo secureCodeBox")

[![License
Apache-2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![GitHub release (latest
SemVer)](https://img.shields.io/github/v/release/secureCodeBox/secureCodeBox?sort=semver)](https://github.com/secureCodeBox/secureCodeBox/releases/latest)
[![OWASP Lab
Project](https://img.shields.io/badge/owasp-lab%20project-yellow)](index.html)
[![Artifact
HUB](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/secureCodeBox)](https://artifacthub.io/packages/search?repo=securecodebox)
[![Twitter
Follower](https://img.shields.io/twitter/follow/securecodebox?style=flat&color=blue&logo=twitter)](https://twitter.com/securecodebox)

[![Build](https://github.com/secureCodeBox/secureCodeBox/workflows/CI/badge.svg)](https://github.com/secureCodeBox/secureCodeBox/actions?query=workflow%3ACI)
[![Known
Vulnerabilities](https://snyk.io/test/github/secureCodeBox/secureCodeBox/badge.svg)](https://snyk.io/test/github/secureCodeBox/secureCodeBox/)

> The OWASP secureCodeBox Project is a **kubernetes based, modularized
> toolchain** for *continuous security scans of your software project*.
> Its goal is to *orchestrate* and easily *automate* a bunch of
> *security-testing tools* out of the box. With secureCodeBox we provide
> a toolchain for continuous scanning of applications to find the
> low-hanging fruit issues early in the development process and free the
> resources of the penetration tester to concentrate on the major
> security issues.

## Description

The purpose of secureCodeBox is not to replace the penetration testers
or make them obsolete. We strongly recommend to run extensive tests by
experienced penetration testers on all your applications. For more
information about this project, please have look at our [GitHub Repo
secureCodeBox](https://github.com/secureCodeBox/secureCodeBox) or
[online documentation](https://docs.securecodebox.io/).

Our *main goal* is to implement a major security testing platform and
framework which enables developers and teams to integrate a bunch of
security testing tools in their CI/CD environment or kubernetes
environment as easy as possible. The flexibility and scalability of the
platform architecture leads to features like *multi tenancy support*,
*large scale (multi-) project testing*, support of distributed and
private networks, customizable security test flows, which enables
projects to test complex environments without implementing the complete
security testing infrastructure on their own.

Secondly we try to foster a broad range of security tools to be easily
integrated. Also we will try to integrate existing OWASP Projects as
building blocks in our platform.

### Architecture

![SCBv2 Architecture
Overview](assets/images/scbv2-architecture.svg "SCBv2 Architecture Overview")

The secureCodeBox architecture is based on Kubernetes Custom Ressource
Definitions (CRDs) and follows a function as a service (FaaS) principle.
Therefore we implemented a Kubernetes operator which schedules *security
scans* as *kubernetes jobs*. This architecture is much more resource
efficient. Instead of long running microservices (SCB v1 Architecture),
scans only consume cluster resources for a short amount of time.

## Roadmap

Our [project
roadmap](https://docs.securecodebox.io/docs/architecture/#road-map) is
documented on our [documentation site](https://docs.securecodebox.io/)
in the [architecture
section](https://docs.securecodebox.io/docs/architecture/)

## Quickstart secureCodeBox

For a quickstart see our [installation
documentation](https://docs.securecodebox.io/docs/getting-started/installation)
and the [starting your first scan
documentation](https://docs.securecodebox.io/docs/getting-started/first-scans)
on our comprehensive [documentation
site](https://docs.securecodebox.io/).

## Community

You are welcome, please join us on... 👋

- [GitHub](https://github.com/secureCodeBox/secureCodeBox)
- [Slack](https://join.slack.com/t/securecodebox/shared_invite/enQtNDU3MTUyOTM0NTMwLTBjOWRjNjVkNGEyMjQ0ZGMyNDdlYTQxYWQ4MzNiNGY3MDMxNThkZjJmMzY2NDRhMTk3ZWM3OWFkYmY1YzUxNTU)
- [Twitter](https://twitter.com/secureCodeBox)

### Contributors

[![GitHub
contributors](https://img.shields.io/github/contributors/secureCodeBox/secureCodeBox.svg)](https://github.com/secureCodeBox/secureCodeBox/graphs/contributors)

## Licensing

This Project is free software: you can redistribute it and/or modify it
under the terms of the [Apache License
2.0](https://github.com/secureCodeBox/secureCodeBox/blob/master/LICENSE).
OWASP secureCodeBox Project and any contributions are Copyright by the
secureCodeBox authors.
:::
::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-securecodebox/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-securecodebox){.github-button
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

- Lab Project

#### Classification

-  Tool

  #### Audience

-  Builder

-  Breaker

-  Defender

### Project About

- [GitHub Project](https://github.com/secureCodeBox/secureCodeBox/)
- [Documentation](https://docs.securecodebox.io/)
- [Issue Tracker](https://github.com/secureCodeBox/secureCodeBox/issues)
- [Website](https://www.securecodebox.io/)
- [Slack](https://join.slack.com/t/securecodebox/shared_invite/enQtNDU3MTUyOTM0NTMwLTBjOWRjNjVkNGEyMjQ0ZGMyNDdlYTQxYWQ4MzNiNGY3MDMxNThkZjJmMzY2NDRhMTk3ZWM3OWFkYmY1YzUxNTU)
- [Twitter](https://twitter.com/secureCodeBox)

### Integrated Projects

- [OWASP AMASS](../www-project-amass/index.html)
- [OWASP JuiceShop Project](../www-project-juice-shop/index.html)
- [ZAP Project](https://zaproxy.org/)
- [OWASP DefectDojo Project](../www-project-defectdojo/index.html)

### Related Projects

- [OWASP DevSlop Project](../www-project-devslop/index.html)
- [OWASP Glue Tool Project](../www-project-glue-tool/index.html)

### Leaders

- [Robert Felber](robert.seedorff%40owasp.html)
- [Jannik Hollenbach](jannik.hollenbach%40owasp.html)
- [Sven Strittmatter](sven.strittmatter%40owasp.html)

### Maintainers

- [Jannik Hollenbach](https://github.com/J12934)
- [Sven Strittmatter](https://github.com/Weltraumschaf)
- [Yannik Fuhrmeister](https://github.com/fuhrmeistery)

### Contributers

- [Timo Pagel](https://github.com/wurstbrot)
- [Benjamin Pfänder](https://github.com/bpfaender)
- [Jorge Estigarribia](https://github.com/jorgestiga)
- [Sebastian Franz](https://github.com/SebieF)
- [Daniel Patanin](https://github.com/dpatanin)
- [Paul Schmelzer](https://github.com/paulschmelzer)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::
