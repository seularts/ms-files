::::::::::::::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Installation](#div-installation){#installation-link .tab-link
  role="tab" aria-selected="false" aria-controls="installation"}
- [Releases](#div-releases){#releases-link .tab-link role="tab"
  aria-selected="false" aria-controls="releases"}
- [Contributing](#div-contributing){#contributing-link .tab-link
  role="tab" aria-selected="false" aria-controls="contributing"}
- [CodeConduct](#div-codeconduct){#codeconduct-link .tab-link role="tab"
  aria-selected="false" aria-controls="codeconduct"}

# OWASP Cervantes {#owasp-cervantes .page-title}

:::::::::::::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}

------------------------------------------------------------------------

![Cervantes
logo](../../raw.githubusercontent.com/CervantesSecurity/.github/main/profile/logo-horizontal2.png)

[![WEB](https://img.shields.io/badge/website-000000?style=for-the-badge&logo=About.me&logoColor=white)](https://github.com/CervantesSec)
[![GITHUB](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/CervantesSec)
[![TWITTER](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/Cervantes_Sec)
[![DISCORD](https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/BvzNjT3Qzc)
[![DOCS](https://img.shields.io/badge/-DOCS-success?style=for-the-badge&logo=readthedocs&logoColor=white)](https://docs.cervantessec.org/)

Cervantes is an opensource collaborative platform for pentesters or red
teams who want to save time to manage their projects, clients,
vulnerabilities and reports in one place.

## Technologies

![DOTNET](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white)
![CSHARP](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![RIDER](https://img.shields.io/badge/Rider-000000?style=for-the-badge&logo=Rider&logoColor=white)
![JS](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

## Supported

                                                       OWASP Foundation                                                                                                                            Snyk                                                                                                                                              A2SECURE
  -------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------
   [![](../../raw.githubusercontent.com/CervantesSec/.github/main/profile/owasp.png){width="500" height="150"}](index.html)   [![](../../raw.githubusercontent.com/OWASP/www-project-cervantes/main/assets/images/logo-snyk.png){width="500" height="200"}](https://snyk.io/)   [![](../../raw.githubusercontent.com/OWASP/www-project-cervantes/main/assets/images/a2secure.png){width="500" height="75"}](https://a2secure.com/)

## Features

- OpenSource
- Multiplatform
- Multilanguage
- Team Collaboration
- BuiltIn dashbaords and analytics
- Manage your clients and Offensive Security projects
- One click reports creation
- And more

## Contributors

Cervantes has been created, developed and maintained by [Ruben
Mesquida](../cdn-cgi/l/email-protection.html#d8aaadbabdb6f6b5bdaba9adb1bcb998b7afb9aba8f6b7aabf)

![contrib](https://contrib.rocks/image?repo=CervantesSec/cervantes)

## Licensing

![CSS](https://img.shields.io/github/license/CervantesSec/cervantes.svg)

This program is free software: You can modify it under the terms of the
Apache-2.0 License. OWASP Cervantes and any contributions are Copyright
© by Ruben Mesquida
:::

::::::::::::::::: {#sec-installation .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Try Cervantes

There is a live demo running on
[http://demo.cervantessec.org](http://demo.cervantessec.org/).

The demo server has 3 users to show the different permission levels. The
credentials for these users are:

  Username                                                                                                                          Password        Role
  --------------------------------------------------------------------------------------------------------------------------------- --------------- ---------------
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__ cfemail="5e3f3a3337301e3d3b2c283f302a3b2d7032313d3f32"}   Admin123.       Administrator
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__ cfemail="582b2d183b3d2a2e39362c3d2b7634373b3934"}         SuperUser123.   SuperUser
  [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__ cfemail="60151305122003051216010e1405134e0c0f03010c"}     User123.        User

## Runtime requirements

- Docker
- Docker compose

## How to run it locally with Docker compose

1.  First you need to clone this repository

:::: {.language-sh .highlighter-rouge}
::: highlight
``` highlight
git clone https://github.com/CervantesSec/docker.git
```
:::
::::

1.  After that you need to start your docker containers:

:::: {.language-sh .highlighter-rouge}
::: highlight
``` highlight
docker-compose -p cervantes -f docker-compose.yml up -d
```
:::
::::

1.  After this, open your browser at http://localhost

2.  Default User is:

:::: {.language-sh .highlighter-rouge}
::: highlight
``` highlight
[email protected] - Admin123.
```
:::
::::

## How to run it locally from source

1.  Install dotnet sdk from https://dotnet.microsoft.com/en-us/download

2.  Install PostgreSQL https://www.postgresql.org/download/

3.  Clone this repository

:::: {.language-sh .highlighter-rouge}
::: highlight
``` highlight
git clone https://github.com/CervantesSec/cervantes.git
```
:::
::::

1.  In Cervantes.Web -\> appsettings.json edit the DefaultConnection
    with your database parameters

:::: {.language-sh .highlighter-rouge}
::: highlight
``` highlight
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=cervantes;Username=postgres;Password=postgres"
  },
  "Logging": {
    "LogLevel": {
      "Default": "Trace",
      "Microsoft": "Warning",
      "Microsoft.Hosting.Lifetime": "Information",
      "Cervantes.*": "Trace"
    }
  },
  "AllowedHosts": "*",
  "EmailConfiguration": {
    "Enabled": false,
    "Name": "Cervantes",
    "From": "[email protected]",
    "SmtpServer": "localhost",
    "SmtpPort": 1025,
    "SmtpUsername": "[email protected]",
    "SmtpPassword": "cervantes"
  },
  "JiraConfiguration": {
    "Enabled": false,
    "Auth": "Basic",
    "Url": "",
    "Project": "",
    "User": "",
    "Password": "",
    "ConsumerKey": "",
    "ConsumerSecret": "",
    "OAuthAccessToken": "",
    "OAuthTokenSecret": ""
    
  }
}
```
:::
::::

1.  Run the project

:::: {.language-sh .highlighter-rouge}
::: highlight
``` highlight
dotnet run --project /CERVANTES_PATH/Cervantes.Web/
```
:::
::::

1.  After this, open your browser at http://localhost:5001

2.  Default User is:

:::: {.language-sh .highlighter-rouge}
::: highlight
``` highlight
[email protected] - Admin123.
```
:::
::::
:::::::::::::::::

::: {#sec-releases .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Alpha 0.5 {#alpha-05}

**Note**: This is a alpha release. Please file new issues for any bugs
you find in it.

### Changes

- Multilanguage Improvements
- Notifications Improvements
- SMTP Email support
- Minor bug fixes
- Fixed UI Bugs
- Checklists support OWASP MASTG & WSTG
- Report compliance OWASP WSTG & MASTG
- Implemented OWASP Score
- Basic Jira Integration
- Import vulns from CSV
- Data Vault Added
- Vuln Id Autogeneration
- Added Executive Summary Section
- Dark Mode Implemented

And more...

## Alpha 0.4 {#alpha-04}

**Note**: This is a alpha release. Please file new issues for any bugs
you find in it.

### Changes

- Report Generation Reworked
- Nmap Parser
- Import XML nmap scans
- Added Email Service
- Search Module
- Fixed Application Logs
- Project Languages
- Language
- Minor bug fixes
- Fixed UI Bugs
- Security Improvements
- Account Lockout Implementation
- Implemented Anti-XSS
- File Validation

And more...

## Alpha 0.3 {#alpha-03}

**Note**: This is a alpha release. Please file new issues for any bugs
you find in it.

### Changes

- Reformat Data Model
- Added Backup/Resore system
- Added Data Vault on Workspace
- Added feature to assign various targets to one vulnerability
- Added feature to added various targets to one task
- Project/Vuln Templates Improvements
- Fixed Login verification
- User creation improvements
- Fixed Date picker on Project/Task creation
- Fixed ORM problem on duplicate IDs
- Fixed minor UI bugs
- Minor UI Improvements
- Fixed. verification on some forms
:::

::: {#sec-contributing .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Contributing guidelines

- If you are contributing with code, make sure you have fork the
  project, and create a pull requests that contains amongst other things
  a description of your changes.
- Keep your changes small. The smaller the changeset the more likely to
  be merged. This applies to code an documentation.
:::

::: {#sec-codeconduct .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Contributor Covenant Code of Conduct

## Our Pledge

In the interest of fostering an open and welcoming environment, we as
contributors and maintainers pledge to making participation in our
project and our community a harassment-free experience for everyone,
regardless of age, body size, disability, ethnicity, sex
characteristics, gender identity and expression, level of experience,
education, socio-economic status, nationality, personal appearance,
race, religion, or sexual identity and orientation.

## Our Standards

Examples of behavior that contributes to creating a positive environment
include:

- Using welcoming and inclusive language
- Being respectful of differing viewpoints and experiences
- Gracefully accepting constructive criticism
- Focusing on what is best for the community
- Showing empathy towards other community members

Examples of unacceptable behavior by participants include:

- The use of sexualized language or imagery and unwelcome sexual
  attention or advances
- Trolling, insulting/derogatory comments, and personal or political
  attacks
- Public or private harassment
- Publishing others' private information, such as a physical or
  electronic address, without explicit permission
- Other conduct which could reasonably be considered inappropriate in a
  professional setting

## Our Responsibilities

Project maintainers are responsible for clarifying the standards of
acceptable behavior and are expected to take appropriate and fair
corrective action in response to any instances of unacceptable behavior.

Project maintainers have the right and responsibility to remove, edit,
or reject comments, commits, code, wiki edits, issues, and other
contributions that are not aligned to this Code of Conduct, or to ban
temporarily or permanently any contributor for other behaviors that they
deem inappropriate, threatening, offensive, or harmful.

## Scope

This Code of Conduct applies both within project spaces and in public
spaces when an individual is representing the project or its community.
Examples of representing a project or community include using an
official project e-mail address, posting via an official social media
account, or acting as an appointed representative at an online or
offline event. Representation of a project may be further defined and
clarified by project maintainers.

## Enforcement

Instances of abusive, harassing, or otherwise unacceptable behavior may
be reported by contacting the project team lead. All complaints will be
reviewed and investigated and will result in a response that is deemed
necessary and appropriate to the circumstances. The project team is
obligated to maintain confidentiality with regard to the reporter of an
incident. Further details of specific enforcement policies may be posted
separately.

Project maintainers who do not follow or enforce the Code of Conduct in
good faith may face temporary or permanent repercussions as determined
by other members of the project's leadership.

## Attribution

This Code of Conduct is adapted from the [Contributor
Covenant](https://www.contributor-covenant.org/), version 1.4, available
at https://www.contributor-covenant.org/version/1/4/code-of-conduct.html

For answers to common questions about this code of conduct, see
https://www.contributor-covenant.org/faq
:::
::::::::::::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-cervantes/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-cervantes){.github-button
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

### Cervantes Information

- [ ]{.fa-stack .fa-1x} Incubator Project

### Project Links

- [Website](https://www.cervantessec.org/)
- [Demo](http://demo.cervantessec.org/)
- [Docs](https://docs.cervantessec.org/)

#### Classification

-  Tool

#### Audience

-  Builder
-  Breaker
-  Defender

### Code Repository

- [Github](https://github.com/CervantesSec)

### Social Media

- [Website](https://www.cervantessec.org/)
- [Demo](http://demo.cervantessec.org/)
- [Docs](https://docs.cervantessec.org/)
- [Twitter](https://twitter.com/Cervantes_Sec)
- [YouTube](https://www.youtube.com/@cervantessec8047)
- [Discord](https://discord.gg/BvzNjT3Qzc)

### Leaders

- [Ruben
  Mesquida](../cdn-cgi/l/email-protection.html#cbb9bea9aea5e5a6aeb8babea2afaa8ba4bcaab8bbe5a4b9ac)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::::::::::::::
