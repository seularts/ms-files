:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}

# OWASP VulnerableApp-Facade {#owasp-vulnerableapp-facade .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
# ![Owasp VulnerableApp-facade](../../raw.githubusercontent.com/SasanLabs/VulnerableApp/master/docs/logos/Coloured/iconColoured.png)

![OWASP
Incubator](https://img.shields.io/badge/owasp-incubator-blue.svg)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![PRs
Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com/)

As we are seeing a lot of technological enhancements in the industry in
the past few years, these technical enhancements are solving one or the
other problem however, with that they also bring few different
vulnerabilities. Vulnerable Applications are generally written in one of
the tech stacks like either Node.js or Java with a SQL or NoSQL database
etc and hence they are not able to expand to a whole new set of
vulnerabilities that are present in other technologies. Also adding more
vulnerabilities in a single vulnerable application makes it heavier and
complex which finally makes it unmaintainable. So VulnerableApp-facade
is built to solve this problem by building a distributed farm of
Vulnerable Applications such that they can be built agnostic to tech
stacks.

## High Level Design Details

![High Level
Design](../../raw.githubusercontent.com/SasanLabs/VulnerableApp-facade/main/docs/images/VulnerableApp-facade.jpg)

**VulnerableApp-facade** is a small component which acts as a webserver
and a gateway. It routes the calls to different Vulnerable Applications
which are registered with it based on a url pattern. It also exposes a
schema/contract (Vulnerability Definition) and if a vulnerable
application adhere to that then it will be able to intract and route the
traffic to that vulnerable application. It also provides the generic
skeleton UI which it builds by reading the provided schema
(Vulnerability Definition) from the vulnerable application and then
loads the UI specific to vulnerable application inside the skeleton
UserInterface.

### Glimpse of the Owasp VulnerableApp-Facade

![Owasp
VulnerableApp-Facade](../../raw.githubusercontent.com/SasanLabs/VulnerableApp-facade/main/docs/images/gif/VulnerableApp-Facade.gif)

## How to run the project

VulnerableApp-facade is a farm of vulnerable applications where each
application runs as a docker container. VulnerableApp-facade has
`docker-compose.yml`{.language-plaintext .highlighter-rouge} file which
contains docker configuration of other vulnerable applications along
with docker configuration of VulnerableApp-facade.

### Simple Start

In order to run entire suit please download and install [Docker
Compose](https://docs.docker.com/compose/install/). After installation,
please copy the
[docker-compose.yml](https://github.com/SasanLabs/VulnerableApp-facade/blob/main/docker-compose.yml)
and run the following command from terminal:
`docker-compose up`{.language-plaintext .highlighter-rouge} Then
navigate to `http://localhost:80`{.language-plaintext
.highlighter-rouge} to play with the application

### Advanced Start

As
[docker-compose.yml](https://github.com/SasanLabs/VulnerableApp-facade/blob/main/docker-compose.yml)
contains all the applications which adhere to the schema of
VulnerableApp-facade so in cause you are looking for specific vulnerable
applications like only Java related vulnerable applications then remove
other vulnerable applications from
[docker-compose.yml](https://github.com/SasanLabs/VulnerableApp-facade/blob/main/docker-compose.yml)
and then run steps as mentioned in the [Simple start
step](#simple-start).

## How to Contribute to the project

VulnerableApp-facade have majorly 2 components:

1.  React UI component
2.  Lua module

React UI component is used to load the skeleton UserInterface and Lua
module is used to merge the Vulnerability Definitions exposed by
different vulnerable applications. In order to do changes in React UI
component,

1.  please navigate to `facade-app`{.language-plaintext
    .highlighter-rouge} folder
2.  add the changes
3.  and run `npm run start`{.language-plaintext .highlighter-rouge}
    which will start the npm server.
4.  navigate to `http://localhost:3000`{.language-plaintext
    .highlighter-rouge} to verify/view the changes

Make sure that the application docker is running such that you can
verify the changes.

In order to make changes in Lua module, the easy way is to add the
changes in the lua files and build the docker image with those changes
by executing command:
`docker build . -t owasp-vulnerableapp-facade`{.language-plaintext
.highlighter-rouge} and then run the project as mentioned at [How to run
the project](#how-to-run-the-project)

Before raising the PR with UI changes please execute
`npm run pretty`{.language-plaintext .highlighter-rouge} command in
`facade-app`{.language-plaintext .highlighter-rouge} folder to auto
handle formatting of javascript/typescript files.

## Integrated Vulnerable Applications

1.  [Owasp VulnerableApp](https://github.com/SasanLabs/VulnerableApp)
2.  [VulnerableApp-jsp](https://github.com/SasanLabs/VulnerableApp-jsp)
3.  [VulnerableApp-php](https://github.com/SasanLabs/VulnerableApp-php)

## Contact

Please raise a github issue for enhancement/issues in
VulnerableApp-facade or send email to
[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
cfemail="abc0cad9cac585d8cad8cac5ebc4dccad8db85c4d9cc"} regarding
queries we will try to resolve issues asap.

## Other links

1.  [Owasp Project link](index.html)
2.  [Github pages](https://sasanlabs.github.io/VulnerableApp-facade/)
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
[Watch](https://github.com/owasp/www-project-vulnerableapp-facade/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-vulnerableapp-facade){.github-button
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
  1.1.0](https://github.com/SasanLabs/VulnerableApp-facade/releases/tag/1.1.0)

#### Classification

-  Tool

#### Audience

-  Breaker

### Downloads or Social Links

- [Download](https://github.com/SasanLabs/VulnerableApp-facade/releases)
- [Slack
  Channel](https://owasp.slack.com/messages/#owasp-vulnerableapp/)

### Code Repository

- [Github Repository](https://github.com/SasanLabs/VulnerableApp-facade)

### Change Log

- [changes](https://github.com/SasanLabs/VulnerableApp-facade/releases)

### Leaders

- [Karan Preet Singh
  Sasan](../cdn-cgi/l/email-protection.html#3d565c4f5c50134e5c4e5c537d524a5c4e4d13524f5a)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
