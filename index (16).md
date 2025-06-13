:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Roadmap](#div-roadmap){#roadmap-link .tab-link role="tab"
  aria-selected="false" aria-controls="roadmap"}

# OWASP VulnerableApp {#owasp-vulnerableapp .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::: {#sec-main .section .page-body}
![VulnerableApp
Logo](../../raw.githubusercontent.com/SasanLabs/VulnerableApp/master/docs/logos/Coloured/iconColoured.png)

![OWASP
Incubator](https://img.shields.io/badge/owasp-incubator-blue.svg)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
![Java CI with
Gradle](https://github.com/SasanLabs/VulnerableApp/workflows/Java%20CI%20with%20Gradle/badge.svg)
[![PRs
Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com/)

As Web Applications are becoming popular these days, there comes a dire
need to secure them. Although there are several Vulnerability Scanning
Tools, however while developing these tools, developers need to test
them. Moreover, they also need to know how well the Vulnerability
Scanning tool is performing. As of now, there are little or no such
vulnerable applications existing for testing such tools. There are
Deliberately Vulnerable Applications existing in the market but they are
not written with such an intent and hence lag extensibility, e.g. adding
new vulnerabilities is quite difficult. Hence, developers resort to
writing their own vulnerable applications, which usually causes
productivity loss and the pain of reworking.

**VulnerableApp** is built keeping these factors in mind. This project
is scalable, extensible, easier to integrate and easier to learn. As
solving the above issue requires addition of various vulnerabilities,
hence it becomes a very good platform to learn various security
vulnerabilities.

### User Interface

![VulnerableApp-facade
UI](../../raw.githubusercontent.com/SasanLabs/VulnerableApp-facade/main/docs/images/gif/VulnerableApp-Facade.gif)

## Technologies used

- Java8
- Spring Boot
- ReactJS
- Javascript/TypeScript

## Currently handled Vulnerability types

1.  [JWT
    Vulnerability](https://github.com/SasanLabs/VulnerableApp/blob/master/src/main/java/org/sasanlabs/service/vulnerability/jwt/)
2.  [Command
    Injection](https://github.com/SasanLabs/VulnerableApp/tree/master/src/main/java/org/sasanlabs/service/vulnerability/commandInjection)
3.  [File Upload
    Vulnerability](https://github.com/SasanLabs/VulnerableApp/tree/master/src/main/java/org/sasanlabs/service/vulnerability/fileupload)
4.  [Path Traversal
    Vulnerability](https://github.com/SasanLabs/VulnerableApp/tree/master/src/main/java/org/sasanlabs/service/vulnerability/pathTraversal)
5.  [SQL
    Injection](https://github.com/SasanLabs/VulnerableApp/tree/master/src/main/java/org/sasanlabs/service/vulnerability/sqlInjection)
    1.  [Error Based
        SQLi](https://github.com/SasanLabs/VulnerableApp/blob/master/src/main/java/org/sasanlabs/service/vulnerability/sqlInjection/ErrorBasedSQLInjectionVulnerability.java)
    2.  [Union Based
        SQLi](https://github.com/SasanLabs/VulnerableApp/blob/master/src/main/java/org/sasanlabs/service/vulnerability/sqlInjection/UnionBasedSQLInjectionVulnerability.java)
    3.  [Blind
        SQLi](https://github.com/SasanLabs/VulnerableApp/blob/master/src/main/java/org/sasanlabs/service/vulnerability/sqlInjection/BlindSQLInjectionVulnerability.java)
6.  [XSS](https://github.com/SasanLabs/VulnerableApp/tree/master/src/main/java/org/sasanlabs/service/vulnerability/xss)
    1.  [Persistent
        XSS](https://github.com/SasanLabs/VulnerableApp/tree/master/src/main/java/org/sasanlabs/service/vulnerability/xss/persistent)
    2.  [Reflected
        XSS](https://github.com/SasanLabs/VulnerableApp/tree/master/src/main/java/org/sasanlabs/service/vulnerability/xss/reflected)
7.  [XXE](https://github.com/SasanLabs/VulnerableApp/tree/master/src/main/java/org/sasanlabs/service/vulnerability/xxe)
8.  [Open
    Redirect](https://github.com/SasanLabs/VulnerableApp/tree/master/src/main/java/org/sasanlabs/service/vulnerability/urlRedirection)
    1.  [Http 3xx Status code
        based](https://github.com/SasanLabs/VulnerableApp/blob/master/src/main/java/org/sasanlabs/service/vulnerability/urlRedirection/Http3xxStatusCodeBasedInjection.java)
9.  [SSRF](https://github.com/SasanLabs/VulnerableApp/tree/master/src/main/java/org/sasanlabs/service/vulnerability/ssrf)

## Contributing to Project

There are multiple ways in which you can contribute to the project:

1.  If you are a developer and trying to start on to the project, then
    the suggestion is to go through the list of
    [issues](https://github.com/SasanLabs/VulnerableApp/issues) which
    contains `good first issue`{.language-plaintext .highlighter-rouge}
    which can be a good starter.
2.  If you are a developer or a security professional looking to add new
    Vulnerability type then you can Generate the Sample Vulnerability by
    running `./gradlew GenerateSampleVulnerability`{.language-plaintext
    .highlighter-rouge}. It will generate the Sample Vulnerability
    template which has placeholders and comments. Modified files can be
    seen in the logs of the command or in the github history. You can
    navigate to those files, fill in the placeholders and then build the
    project to see the effect of the changes.
3.  In case you are looking to contribute to the project by publicising
    it or working on the growth of the project, please feel free to add
    your thoughts to discussions section or issues and we can discuss
    over them.

## Building the project

There are 2 ways in which this project can be built and used:

1.  As a Docker application which will help in running the full-fledged
    VulnerableApplication. For running as Docker application, follow
    following steps:
    1.  Build the docker image by running
        `./gradlew jibDockerBuild`{.language-plaintext
        .highlighter-rouge}
    2.  Download
        [Docker-Compose](https://github.com/SasanLabs/VulnerableApp-facade/blob/main/docker-compose.yml)
        and run in the same directory
        `docker-compose up`{.language-plaintext .highlighter-rouge}
    3.  Navigate to browser and visit
        `http://localhost`{.language-plaintext .highlighter-rouge} and
        this will give the User Interface for VulnerableApp.
2.  As a SpringBoot application which will run with the Legacy UI or
    Rest API but gives the benefit of debugging and solving issues. This
    is the simple way,
    1.  Import the project into your favorite IDE and run it
    2.  Navigate to browser and visit:
        `http://localhost:9090/VulnerableApp`{.language-plaintext
        .highlighter-rouge} and this will give the Legacy User Interface
        for VulnerableApp which you can use to debug and test.

### Connecting to embedded H2 database

For accessing database from browser, visit:
`http://localhost:9090/VulnerableApp/h2`{.language-plaintext
.highlighter-rouge}

Database Connection properties:

:::: {.language-properties .highlighter-rouge}
::: highlight
``` highlight
JDBC Url: jdbc:h2:mem:testdb
User Name: admin
Password: hacker
```
:::
::::

## Contact

In case you are stuck with any of the steps or understanding anything
related to project and its goals, feel free to shoot a mail at
[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
cfemail="d5beb4a7b4bbfba6b4a6b4bb95baa2b4a6a5fbbaa7b2"} or raise an
[issue](https://github.com/SasanLabs/VulnerableApp/issues) and we will
try our best to help you.

## Documentation and References

1.  [Documentation](https://sasanlabs.github.io/VulnerableApp)
2.  [Design
    Documentation](https://sasanlabs.github.io/VulnerableApp/DesignDocumentation.html)
3.  [Owasp VulnerableApp](index.html)
4.  [Overview video for OWASP Spotlight
    series](https://www.youtube.com/watch?v=HRRTrnRgMjs)
5.  [Overview
    Video](https://www.youtube.com/watch?v=AjL4B-WwrrA&ab_channel=OwaspVulnerableApp)

### Blogs

1.  [Overview of Owasp-VulnerableApp - Medium
    article](https://hussaina-begum.medium.com/an-extensible-vulnerable-application-for-testing-the-vulnerability-scanning-tools-cc98f0d94dbc)
2.  [Overview of Owasp-VulnerableApp - Blogspot
    post](https://hussaina-begum.blogspot.com/2020/10/an-extensible-vulnerable-application.html)

### Readme in other languages

1.  [Russian](https://github.com/SasanLabs/VulnerableApp/tree/master/docs/i18n/ru/README.md)
2.  [Chinese](https://github.com/SasanLabs/VulnerableApp/tree/master/docs/i18n/zh-CN/README.md)
3.  [Hindi](https://github.com/SasanLabs/VulnerableApp/tree/master/docs/i18n/hi/README.md)
4.  [Punjabi](https://github.com/SasanLabs/VulnerableApp/tree/master/docs/i18n/pa/README.md)
:::::

::: {#sec-roadmap .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Roadmap

### Vision for the project:

The overall vision for the project is to implement a Platform capability
such that it is easier to write vulnerable code and exposing that
through an API and UI.

### Usage of the project:

This Project mainly targets 4 type of audience:

- Developers of Vulnerability Scanning tools
- New Vulnerability finders (for faster demonstration of the
  vulnerability)
- Security enthusiasts, Students who want to learn more about Security
- CTF organizers (A Platform to Host CTF by choosing vulnerabilities
  present in the project)

### Initial high level plan:

Basic idea for this project is to build an extensible framework which is
driven by the configuration and developers who want to introduce new
vulnerable code into the project need to do minimal boilerplate code and
also the learning curve for configurations is minimum.

Looking at it, the first approach which comes into my mind is to give a
framework similar to Spring i.e. something like annotation driven
framework for including a vulnerability type and also for adding a new
vulnerability to existing vulnerability type and also adding User
Interface for the same.

- Milestone 1: Alpha release - Building extensible backend Platform
- Milestone 2: Beta release - Building extensible User Interface
- Milestone 3: Gamma release - Addition of 50 vulnerabilities using the
  above mentioned Platform
- Milestone 4: Release 1
- Milestone 5: Dev lifecycle integration

### Current State

For know about the current state please go to [Git
Repository](https://github.com/SasanLabs/VulnerableApp) and also visit
issues section for new enhancements,tech-debts and bugs.

### Timeframes

This is hard to estimate as this depends on the number of contributers
but as of now i had already build some of the pieces of Backend platform
and i have started building frontend platform but addition of 50
vulnerabilities can take quite a lot time. So Plan is to release this
Project is near July 31 2020.

### Technology

Technologies used in this project are:

Majorly:

1.  Java-8
2.  SpringBoot
3.  Vanilla Javascript
4.  Vanilla CSS

But we are not limited to above technologies and can extend to new
Horizons. Incase you have any idea on technology and how it can suit us,
please reach out to us on our
[Slack-Channel](https://owasp.slack.com/messages/#owasp-vulnerableapp/).

### Challenges

There are many, please visit
[Issues](https://github.com/SasanLabs/VulnerableApp/issues) for more
information.
:::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-vulnerableapp/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-vulnerableapp){.github-button
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

- ![](assets/images/owasp_level_incubator.svg){width="66"} [Incubator
  Project]{style="font-size: 1.3em;"}
- [Version
  1.11.0](https://github.com/SasanLabs/VulnerableApp/releases/tag/1.11.0)

#### Classification

-  Tool

#### Audience

-  Breaker

### Downloads or Social Links

- [Download](https://github.com/SasanLabs/VulnerableApp/releases)
- [Slack
  Channel](https://owasp.slack.com/messages/#owasp-vulnerableapp/)

### Code Repository

- [Github Repository](https://github.com/SasanLabs/VulnerableApp)

### Change Log

- [changes](https://github.com/SasanLabs/VulnerableApp/releases)

### Leaders

- [Karan Preet Singh
  Sasan](../cdn-cgi/l/email-protection.html#670c0615060949140614060927081006141749081500)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::
