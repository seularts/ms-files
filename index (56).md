::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Ecosystem](#div-ecosystem){#ecosystem-link .tab-link role="tab"
  aria-selected="false" aria-controls="ecosystem"}
- [Setup](#div-setup){#setup-link .tab-link role="tab"
  aria-selected="false" aria-controls="setup"}
- [Contributing](#div-contributing){#contributing-link .tab-link
  role="tab" aria-selected="false" aria-controls="contributing"}
- [Roadmap](#div-roadmap){#roadmap-link .tab-link role="tab"
  aria-selected="false" aria-controls="roadmap"}

# OWASP Security-C4PO {#owasp-security-c4po .page-title}

:::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
[![OWASP
Incubator](https://img.shields.io/badge/owasp-incubator%20project-3267fe.svg)](../other_projects/index.html)
![workflow_badge](https://github.com/Marcel-Haag/security-c4po/actions/workflows/c4po-ci.yml/badge.svg?branch=main)
![workflow_badge](https://github.com/Marcel-Haag/security-c4po/actions/workflows/c4po-release.yml/badge.svg?branch=main)
[![GitHub
stars](https://img.shields.io/github/stars/marcel-haag/security-c4po.svg?label=GitHub%20%E2%98%85&style=flat)](https://github.com/marcel-haag/security-c4po/stargazers)

Welcome to the OWASP page for Security-C4PO, an open-source pentest
reporting tool. Security-C4PO is an open-source web-application for
managing and documenting penetration tests. It aims to streamline and
automate the often time-consuming task of creating comprehensive reports
by providing an intuitive web-based interface that facilitates the
content of the [OWASP TESTING
GUIDE](../www-project-web-security-testing-guide/v42/index.html).

![C4PO Logo](assets/images/repository-owasp-guide-c4po.png)

## Description

C4PO provides pentesters the perfect solution when it comes to reporting
security vulnerabilities and other risk-related findings. It makes the
pain of copy and paste a thing of the past. The interface is designed to
guide you through your pentests in the style of the OWASP Testing Guide.
Before creating your report we show you a summary through visualizing
findings and their statuses.

Interested? Checkout our [Official Release
Trailer](https://www.youtube.com/watch?v=DXVx4BFckmY)!

### What can it do for you?

- Great starting point for beginners
- Easy way to do pentests without prior knowledge of hacking
- Designed to avoid "Analysis Paralysis"
- Central overview and organisation of pentests
- Saves money compared to hiring third-party pentesters or tools
- Completely open-source under the Apache-2.0 license
- Accelerate your pentest delivery to better serve clients
- Boost margins by slashing report creation time
- Automatically build actionable reports

![Slideshow](assets/images/C4PO_Overview.gif)

## Licensing

[![license](https://img.shields.io/github/license/marcel-haag/security-c4po.svg)](https://github.com/marcel-haag/security-c4po/blob/master/LICENSE)

Security C4PO is licensed under the [Apache License
2.0](https://www.apache.org/licenses/LICENSE-2.0) License. Please see
the
[LICENSE](https://github.com/marcel-haag/security-c4po/blob/main/LICENSE.md)
file for more information.

We hope you find Security C4PO useful for managing and generating
pentest reports. If you encounter any issues or have suggestions for
improvement, please feel free to create an issue on the [issue
tracker](https://github.com/Marcel-Haag/security-c4po/issues).
:::

::: {#sec-ecosystem .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Techstack

[![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/repository/docker/cellecram/security-c4po/general)
![Angular](https://img.shields.io/badge/angular-%23DD0031.svg?style=for-the-badge&logo=angular&logoColor=white)
![RxJS](https://img.shields.io/badge/rxjs-%23B7178C.svg?style=for-the-badge&logo=reactivex&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![Gradle](https://img.shields.io/badge/Gradle-02303A.svg?style=for-the-badge&logo=Gradle&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)

### Development server

Execute `c4po-dev.sh`{.language-plaintext .highlighter-rouge} and all
services will run on a dev server. You can reach the application by
entering http://localhost:4200 in you browser.

### Testuser Credentials

- Username: c4po
- Password: Test1234!

## Application Architecture

![alt architecture](assets/images/C4PO-Architecture.png)

## Data Structure

![alt datastructure](assets/images/C4PO-Datastructure.png)
:::

::: {#sec-setup .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Docker Hub Setup

[![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/repository/docker/cellecram/security-c4po/general)

- Pull all images:
  - `docker image pull --all-tags cellecram/security-c4po`{.language-plaintext
    .highlighter-rouge}
- Create network:
  - `docker network create -d bridge c4po`{.language-plaintext
    .highlighter-rouge}
- Start images:
  - `docker run --network=c4po --name c4po-keycloak -d -p 8080:8080 cellecram/security-c4po:keycloak`{.language-plaintext
    .highlighter-rouge}
  - `docker run --network=c4po --name c4po-db -d -p 27017:27017 cellecram/security-c4po:mongo`{.language-plaintext
    .highlighter-rouge}
  - `docker run --network=c4po --name c4po-angular -d -p 4200:4200 cellecram/security-c4po:angular`{.language-plaintext
    .highlighter-rouge}
  - `docker run --network=c4po -e "SPRING_PROFILES_ACTIVE=COMPOSE" --name c4po-api -d -p 8443:8443 cellecram/security-c4po:api`{.language-plaintext
    .highlighter-rouge}
  - `docker run --network=c4po -e "SPRING_PROFILES_ACTIVE=COMPOSE" --name c4po-reporting -d -p 8444:8444 cellecram/security-c4po:reporting`{.language-plaintext
    .highlighter-rouge}

### OR: Run Script (Docker Hub)

Execute `c4po-prod.sh`{.language-plaintext .highlighter-rouge} and all
services will be pulled from Docker Hub and started. You can reach the
application by entering `http://localhost:4200`{.language-plaintext
.highlighter-rouge} in you browser.
:::

::: {#sec-contributing .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Contributing to Security-C4PO

First off, thanks for taking the time to contribute! 👍

The following is a set of guidelines for contributing to this project
and its packages, which are hosted on GitHub. These are mostly
guidelines, not rules. Use your best judgment, and feel free to propose
changes to this document in a pull request.

### Issue Board

[C4PO Board](https://github.com/Marcel-Haag/security-c4po/projects/1)

## How Can I Contribute?

### Reporting Bugs

This section guides you through submitting a bug report. Following these
guidelines helps maintainers and the community understand your report.

Explain the problem and include additional details to help maintainers
reproduce the problem:

- **Use a clear and descriptive title** for the issue to identify the
  problem.
- **Describe the exact steps which reproduce the problem** in as many
  details as possible. For example, start by explaining how you started
  the application, e.g. which command exactly you used in the terminal,
  or how you started the application otherwise. When listing steps,
  **don't just say what you did, but explain how you did it**.
- **Describe the behavior you observed after following the steps** and
  point out what exactly is the problem with that behavior.
- **Explain which behavior you expected to see instead and why.**
- **Include screenshots and animated GIFs** which show you following the
  described steps and clearly demonstrate the problem.
- **If the problem wasn't triggered by a specific action**, describe
  what you were doing before the problem happened.

### Suggesting Enhancements

This section guides you through submitting an enhancement suggestion,
including completely new features and minor improvements to existing
functionality. Following these guidelines helps maintainers and the
community understand your suggestion :pencil: and find related
suggestions :mag_right:.

- **Use a clear and descriptive title** for the issue to identify the
  suggestion.
- **Provide a step-by-step description of the suggested enhancement** in
  as many details as possible.
- **Include screenshots, mock-ups or animated GIFs** which help you
  demonstrate the steps or point out the part which the suggestion is
  related to.
- **Explain why this enhancement would be useful**

## Code of Conduct

Use the following conventions:

- Branch: `<initial>_c4po_<issuenumber>`{.language-plaintext
  .highlighter-rouge}
- Commit: `feat: <What was implemented?>`{.language-plaintext
  .highlighter-rouge} or `fix: <What got fixed?>`{.language-plaintext
  .highlighter-rouge} By participating, you are expected to uphold this
  code.

## Local development

Security-C4PO and all it's included micorservices can be developed
locally. Execute `c4po-dev.sh`{.language-plaintext .highlighter-rouge}
and all services will run on a dev server.

#### Testuser Credentials: {#testuser-credentials}

- Username: c4po
- Password: Test1234!

#### Technical Environment Requirements

- Docker / Docker-compose
- OpenJDK 11
- Node 14.15.1 / npm 6.14.8

#### Helpfull Tools

- mongoDB Compass
- Postman
:::

::: {#sec-roadmap .section .page-body .tab-hidden}

------------------------------------------------------------------------

## C4PO Roadmap

![alt roadmap](assets/images/C4PO-Roadmap.png)

### Issue Board {#issue-board}

[C4PO Board](https://github.com/Marcel-Haag/security-c4po/projects/1)
:::
::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-security-c4po/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-security-c4po){.github-button
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

### Security-C4PO Information

-  [Incubator Project]{style="font-size: 1.3em;"}
-  Alpha Release Version

### Classification

-  Tool

#### Audience

-  Breaker
-  Defender

### Installation

- [From
  Source](https://github.com/marcel-haag/security-c4po#docker-hub-setup)
- [Docker Hub](https://hub.docker.com/r/cellecram/security-c4po)

### Code Repository

- [C4PO Repo](https://github.com/marcel-haag/security-c4po)

### Social Links

- [Website](https://security.c4po.dev/)
- [Youtube](https://www.youtube.com/@SecurityC4PO/featured)

### Leaders

- [Marcel
  Haag](../cdn-cgi/l/email-protection.html#026f637061676e2c6a636365426d756371722c6d7065)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::
