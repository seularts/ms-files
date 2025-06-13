:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}

# OWASP Faction {#owasp-faction .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::: {#sec-main .section .page-body}
# OWASP FACTION PenTesting Report Generation and Collaboration Framework

![GitHub last
commit](https://img.shields.io/github/last-commit/factionsecurity/faction)
![GitHub Release Date -
Published_At](https://img.shields.io/github/release-date/factionsecurity/faction)

[![Bluesky](https://img.shields.io/badge/Bluesky-0285FF?logo=bluesky&logoColor=fff)](https://bsky.app/profile/factionsecurity.com)

![image](assets/images/290761747-d9237bed-302f-4e6a-9716-22ae88d0dc36.png)

### Become a Sponsor ❤️ {#become-a-sponsor-️}

If you like the project and would like to see it advance then consider
being a sponser. All sponsers get access to the Faction discord server
and will have bug reports priotirized. Just click the sponsor links at
the top of this repo.

[Sponsor via GitHub
Sponosrs](https://github.com/sponsors/factionsecurity)

## Introduction

FACTION is your entire assessment workflow in a box. With FACTION you
can:

1.  Automate pen testing and security assessment Reports
2.  Peer review and track changes for reports
3.  Create customized DOCX templates for different assessment types and
    retests
4.  Real-time collaboration with assessors via the web app and [Burp
    Suite Extensions](https://github.com/factionsecurity/Faction-Burp)
5.  Customizable vulnerability templates with over 75 prepopulated
6.  Easily manage assessment teams and track progress across your
    organization
7.  Track vulnerability remediation efforts with custom SLA warnings and
    alerts  
8.  Full Rest API to integrate with other tools                     

Other Features:           

1.  LDAP Integration       
2.  OAUTH2.0 Integration
3.  SMTP integration 
4.  Extendable with Custom Plugins similar to Burp Extender.
5.  Custom Report Variables

**Want to see it in action?** -\> [Faction YouTube
Channel](https://www.youtube.com/@factionsecurity/videos)

## Quick Setup

**Requirements**

- Java JDK11
- Maven (for building the project)
- (Optional for VM). Mongo DB requires a CPU with AVX support. You may
  run into this issue if using [Oracle
  Virtual](https://www.mongodb.com/community/forums/t/could-not-start-mongodb-5-0-running-oracle-linux-on-virtualbox/120524/10)
  Box or
  [Kubernetes](https://stackoverflow.com/questions/70818543/mongo-db-deployment-not-working-in-kubernetes-because-processor-doesnt-have-avx)

Run the following commands to build the war file and deploy it to the
docker container.

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
git clone [email protected]:factionsecurity/faction.git
cd faction
docker-compose up --build
```
:::
::::

Once the containers are up you can navigate to http://127.0.0.1:8080 to
access your FACTION instance. On the first boot, it will ask you to
create an admin account.

## Import the Vulnerability Templates

1.  Navigate to Templates -\> Default Vulnerabilities
2.  Click Update from Faction.

## Customize reports

You can find out more information about creating your own custom report
templates here: [Custom Security Report Templates - Faction
Security](https://docs.factionsecurity.com/Custom%20Security%20Report%20Templates/)

## Burp Suite Extension

Faction is in the Burp BApp store but you can also get it from our
github: [Burp Suite
Extensions](https://github.com/factionsecurity/Faction-Burp)

## Manuals and Tutorials

[Manual](https://docs.factionsecurity.com/)

## Screenshots

**Vulnerability Templates** ![image](assets/images/vuln-templates.png)

**Assessment Scheduling** ![image](assets/images/scheduling.png)

**Peer Review and Track Changes** ![image](assets/images/peerreview.png)

**Remediation/Retest Queue** ![image](assets/images/retests.png)

**Schedule Retests** ![image](assets/images/scheduleretests.png)

**Assessor Retest Interface** ![image](assets/images/assessorretest.png)

**Vulnerability Status Tracking** ![image](assets/images/vulnstatus.png)

# Faction App Store

Faction 1.2 introduces the App Store! The Faction App Store will make it
easier for developers to extend faction. Faction Extensions can be used
to trigger custom code when certain events happen in your workflow like
sending all vulnerbilities to Jira when the assessment is complete or
update a tracking system when retests pass or fail. More information can
be found in the [documentation site](https://docs.factionsecurity.com/).

### ⭐️ Jira Integration and AppStore Dashboard {#️-jira-integration-and-appstore-dashboard}

![image](assets/images/appstore.png)

Note you can reorder extensions so that updates for one can affect
updates to the next.

### ⭐️ Extensions for Custom Graphics {#️-extensions-for-custom-graphics}

Extensions will also allow custom bar charts to your reports:
![image](assets/images/appstore2.png)

Generated report with graphics: ![image](assets/images/report.png)

### Current Road Map

- Open sourced the base application on github in dec 2023
- Adding API and plugin features - March 2024
- Streamlined remediation workflows - August 2024
- Update backend and code refactor - October 2025
- Adding 4 more plugins and integrations - December 2025
- Overhaul the UI to be more modern and simple - March 2026
:::::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

Put whatever you like here: news, screenshots, features, supporters, or
remove this file and don't use tabs at all.
:::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-faction/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-faction){.github-button
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

### Faction Information

[ ]{.fa-stack .fa-2x style="margin-top: -30px"}

- [Incubator Project](../other_projects/index.html)
- [Version
  1.4.3](https://github.com/factionsecurity/faction/releases/tag/1.4.3)

### Downloads or Social Links

- [Documentation](https://docs.factionsecurity.com/)
- [BlueSky](https://bsky.app/profile/factionsecurity.com)

### Code Repository

- [Github repo](https://github.com/factionsecurity/faction)

### Releases and Change Log

- [Releases](https://github.com/factionsecurity/faction/releases)

### Leaders

- [Josh
  Summitt](../cdn-cgi/l/email-protection.html#bcf6d3cfd492efc9d1d1d5c8c8848cfcd3cbddcfcc92d3cedb)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::
