::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Releases](#div-releases){#releases-link .tab-link role="tab"
  aria-selected="false" aria-controls="releases"}
- [FAQs](#div-faqs){#faqs-link .tab-link role="tab"
  aria-selected="false" aria-controls="faqs"}
- [Roadmap](#div-roadmap){#roadmap-link .tab-link role="tab"
  aria-selected="false" aria-controls="roadmap"}
- [TMF](#div-tmf){#tmf-link .tab-link role="tab" aria-selected="false"
  aria-controls="tmf"}

# OWASP Threat Dragon {#owasp-threat-dragon .page-title}

:::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![cupcake logo](assets/images/cupcake-256x256.png){.image-right}

## What is Threat Dragon?

OWASP Threat Dragon is a modeling tool used to create threat model
diagrams as part of a secure development lifecycle. Threat Dragon
follows the values and principles of the [threat modeling
manifesto](https://www.threatmodelingmanifesto.org/). It can be used to
record possible threats and decide on their mitigations, as well as
giving a visual indication of the threat model components and threat
surfaces. Threat Dragon runs either as a web application or as a desktop
application.

Threat Dragon supports STRIDE / [LINDDUN](https://www.linddun.org/) /
CIA / DIE / [PLOT4ai](https://plot4.ai/), provides modeling diagrams and
implements a rule engine to auto-generate threats and their mitigations.

### Resources

Use the [version 1](https://threatdragon.github.io/) or [version
2](https://www.threatdragon.com/docs/) documentation to get started,
along with the recording of Mike Goodwin giving a [lightning
demo](https://youtu.be/n6JGcZGFq5o) during the OWASP Open Security
Summit in June 2020.

An [introduction](https://www.youtube.com/watch?v=hUOAoc6QGJo) to Threat
Dragon is provided by the [OWASP
Spotlight](https://www.youtube.com/playlist?list=PLUKo5k_oSrfOTl27gUmk2o-NBKvkTGw0T)
series, and the [Threat Modeling
Gamification](https://www.youtube.com/watch?v=u2tmLrwv-nc) seminar by
Vlad Styran shows how using Threat Dragon can make threat modeling fun.

There are a couple of OWASP community pages that give overviews on
Threat Modeling and how to get started: [Threat
Modeling](../www-community/Threat_Modeling.html) and [Threat Modeling
Process](../www-community/Threat_Modeling_Process.html).

The easiest way to get in contact with the Threat Dragon community is
via the OWASP Slack
[#project-threat-dragon](https://owasp.slack.com/messages/CURE8PQ68)
project channel, you may need to [subscribe](../slack/invite.html)
first.

### Related Projects

- [OWASP pytm (Pythonic Threat
  Modeling)](../www-project-pytm/index.html)
- [Threat Modeling OWASP Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html)
- [Threagile - Agile Threat Modeling](https://threagile.io/), an
  (non-OWASP) open source project

------------------------------------------------------------------------

Threat Dragon: *making threat modeling less threatening*
:::

::: {#sec-releases .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Releases

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Release           Date              Location                                                                                     Comments
  ----------------- ----------------- -------------------------------------------------------------------------------------------- -----------------------------------------------------
  v2.4.1            Mar 2025          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.4.1)                         Bug fix for diagram labels, TBA renamed TBD

  v2.4              Mar 2025          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.4.0)                         Additional threat priorities, TLS credentials, export
                                                                                                                                   model diagrams, create new repo branches

  v2.3              Dec 2024          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.3.0)                         suggest threats by element and threats by context,
                                                                                                                                   builds for ARM64 platforms and google sign-in feature

  v2.2              Feb 2024          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.2.0)                         add GitLab support and user prompt to save model when
                                                                                                                                   quitting

  v2.1.3            Jan 2024          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.1.3)                         bug fix for desktop menu discarding diagram edits,
                                                                                                                                   add schema for Open Threat Modeling (OTM)

  v2.1.2            Nov 2023          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.1.2)                         add Bitbucket access, PLOT4ai threats and bug-fix for
                                                                                                                                   data-flows overwriting properties

  v2.1.1            Oct 2023          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.1.1)                         desktop version provides guard advising of
                                                                                                                                   overwriting threats changes

  v2.1              Oct 2023          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.1.0)                         desktop version provides guard advising of
                                                                                                                                   overwriting diagram changes

  v2.0.9            Oct 2023          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.0.9)                         names for diagram data flow and trust boundary curves
                                                                                                                                   preserved when unselected

  v2.0.8            Oct 2023          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.0.8)                         diagram component properties correctly displayed when
                                                                                                                                   selecting new component

  v2.0.7            Sep 2023          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.0.7)                         fix bug when selecting trust boundary curves

  v2.0.6            Sep 2023          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.0.6)                         ability to filter Github repos; translation for
                                                                                                                                   Finnish; improve data flow selection and handling

  v2.0.4            Aug 2023          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.0.4)                         various bug fixes;

  v2.0.2            Apr 2023          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.0.2)                         collection of bug fixes; PDF report button, threat
                                                                                                                                   IDs fixed, reporting expanded

  v2.0              Feb 2023          [github](https://github.com/OWASP/threat-dragon/releases/tag/v2.0.0)                         substantial rewrite for new drawing library
                                                                                                                                   [\@antv/g6](https://www.npmjs.com/package/@antv/g6)

  v1.6.1            Mar 2022          [github](https://github.com/OWASP/threat-dragon/releases/tag/v1.6.1)                         Docs now moved to the new site\
                                                                                                                                   Last release of 1.x before version 2.0

  v1.6              Dec 2021          [github](https://github.com/OWASP/threat-dragon/releases/tag/v1.6.0)                         Automated threat and context threat generation

  v1.5.8            Sep 2021          [github](https://github.com/OWASP/threat-dragon/releases/tag/v1.5.8)                         Shows 'NA' threats as completed/ mitigated\
                                                                                                                                   Fixes bug in threat engine (web app only)\
                                                                                                                                   Signed binaries for Windows

  v1.5.5            Sep 2021          [github](https://github.com/OWASP/threat-dragon/releases/tag/v1.5.5)                         MacOS images are signed and notarized\
                                                                                                                                   Linux Snap image available as [snapcraft
                                                                                                                                   distribution](https://snapcraft.io/threat-dragon)

  v1.4              5 May 2021        [github](https://github.com/OWASP/threat-dragon/releases/tag/v1.4.0)                         Provides dotenv for environment variables\
                                                                                                                                   updates to docker image\
                                                                                                                                   substantial code reorganisation

  v1.3.1            26 Oct 2020       [Web app](https://github.com/OWASP/threat-dragon/releases/tag/v1.3.1)\                       update documentation link to point to new docs page
                                      [Desktop](https://github.com/OWASP/threat-dragon-desktop/releases/tag/v1.3.1)                

  v1.3              3 Sep 2020        [Web app](https://github.com/OWASP/threat-dragon/releases/tag/v1.3)\                         support for LINDDUN and CIA as well as STRIDE\
                                      [Desktop](https://github.com/OWASP/threat-dragon-desktop/releases/tag/v1.3)                  and desktop command line interface

  v1.2              14 Apr 2020       [Web app](https://github.com/mike-goodwin/owasp-threat-dragon/releases/tag/v1.2)\            description for diagram elements\
                                      [Desktop](https://github.com/mike-goodwin/owasp-threat-dragon-desktop/releases/tag/v1.2)     label applied to boundaries\
                                                                                                                                   save button always enabled\
                                                                                                                                   zoom functionality disabled\
                                                                                                                                   hot key copy and paste for diagram elements

  v1.1              15 Mar 2020       [Web app](https://github.com/mike-goodwin/owasp-threat-dragon/releases/tag/v1.1)             Duplicate element/diagram feature

  v1.1              10 Mar 2020       [Desktop](https://github.com/mike-goodwin/owasp-threat-dragon-desktop/releases/tag/v1.1)     Bug fix for blank screen on new model,\
                                                                                                                                   and duplicate element/diagram feature

  v1.0              22 Feb 2020       [Desktop](https://github.com/mike-goodwin/owasp-threat-dragon-desktop/releases/tag/v1.0)     First full desktop release for Windows, MacOS and
                                                                                                                                   Linux

  v0.1.27-alpha     28 Jul 2019       [Desktop](https://github.com/mike-goodwin/owasp-threat-dragon-desktop/releases/tag/0.1.27)   Windows desktop only

  v0.1.26           16 May 2017       [Desktop](https://github.com/mike-goodwin/owasp-threat-dragon-desktop/releases/tag/0.1.26)   MacOS and Windows desktop only

  0.3.0             14 Mar 2017       [Web app](https://github.com/mike-goodwin/owasp-threat-dragon/releases/tag/0.3.0)            alpha release

  v0.1.1-alpha      14 Mar 2016       [Web app](https://github.com/mike-goodwin/owasp-threat-dragon/releases/tag/v0.1.1-alpha)     alpha release
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

Threat Dragon: *making threat modeling less threatening*
:::

::: {#sec-faqs .section .page-body .tab-hidden}

------------------------------------------------------------------------

## FAQs

- [Where are the arrows that allow me to create data
  flows?](https://github.com/OWASP/threat-dragon/wiki/FAQs#where-are-the-arrows-that-allow-me-to-create-dataflows)

- [Why do the earlier releases come from Mike Goodwin's repo, not the
  OWASP
  repo?](https://github.com/OWASP/threat-dragon/wiki/FAQs#why-do-the-earlier-releases-come-from-mike-goodwins-repo-not-the-owasp-repo)

- [I get failures when installing from source
  code](https://github.com/OWASP/threat-dragon/wiki/FAQs#i-get-failures-when-installing-from-source-code)

- [I get a failure when printing a
  report](https://github.com/OWASP/threat-dragon/wiki/FAQs#i-get-a-failure-when-printing-a-report)

- [Why do I get 'OWASP-Threat-Dragon-Setup isn't commonly downloaded'
  warnings after downloading on
  Windows?](https://github.com/OWASP/threat-dragon/wiki/FAQs#why-do-i-get-owasp-threat-dragon-setup-isnt-commonly-downloaded-warnings-after-downloading-on-windows)

- [Why do I get 'Apple cannot check it for malicious software' errors
  after installing on
  MacOS?](https://github.com/OWASP/threat-dragon/wiki/FAQs#why-do-i-get-developer-can-not-be-verified-errors-after-installing-on-macos)

- [Why do I get 'Permissions failure opening Mac desktop app' when
  installing from the zip
  file?](https://github.com/OWASP/threat-dragon/wiki/FAQs#why-do-i-get-permissions-failure-opening-mac-desktop-app-when-installing-from-the-zip-file)

- [Why do I get 'developer can not be verified' errors after installing
  on
  MacOS?](https://github.com/OWASP/threat-dragon/wiki/FAQs#why-do-i-get-developer-can-not-be-verified-errors-after-installing-on-macos)

- [Can I run Threat Dragon Desktop from a command
  line?](https://github.com/OWASP/threat-dragon/wiki/FAQs#can-i-run-threat-dragon-desktop-from-a-command-line)

- [Is there a command line interface for Threat Dragon
  Desktop?](https://github.com/OWASP/threat-dragon/wiki/FAQs#is-there-a-command-line-interface-for-threat-dragon-desktop)

- [What browsers can be used for Threat
  Dragon?](https://github.com/OWASP/threat-dragon/wiki/FAQs#what-browsers-can-be-used-for-threat-dragon)

- [Hold on...isn't this the same as Mozilla's
  SeaSponge?](https://github.com/OWASP/threat-dragon/wiki/FAQs#hold-onisnt-this-the-same-as-mozillas-seasponge)

- [When is Threat Dragon's birthday? And does Threat Dragon have a theme
  tune?](https://github.com/OWASP/threat-dragon/wiki/FAQs#when-is-threat-dragons-birthday-and-does-threat-dragon-have-a-theme-tune)

------------------------------------------------------------------------

Threat Dragon: *making threat modeling less threatening*
:::

::: {#sec-roadmap .section .page-body .tab-hidden}

------------------------------------------------------------------------

### Version 2.5: in progress {#version-25-in-progress}

- [ ] provide an API for CI/CD pipelines
- [ ] provide a CLI for scripting based on TD's existing [use of
  yargs](https://github.com/yargs/yargs)

### Version 2.3: released December 2024 {#version-23-released-december-2024}

- [x] automated threats (both by element and by OATS)

### Version 2.2: released February 2024 {#version-22-released-february-2024}

Threat model access for web app:

- [x] load models from various repos :
  - [x] github enterprise
  - [x] gitlab
  - [x] github enterprise
  - [x] BitBucket

### Version 2.1: released October 2023 {#version-21-released-october-2023}

Stable version of 2.x.x with bug fixes and usable diagram tools. Still
not feature complete:

- missing CLI for scripting based
- missing automated threats (both by element and by OATS)

### Version 2.0: released February 2023 {#version-20-released-february-2023}

**migrate to a combined application for both desktop and webapp**:

- [x] be strictly open source
- [x] use
  [Vue](https://v3.vuejs.org/guide/introduction.html#what-is-vue-js) for
  frontend application
- [x] use [\@antv/g6](https://www.npmjs.com/package/@antv/g6) for the
  drawing library
- [x] frontend logging using
  [bunyan](https://github.com/trentm/node-bunyan) and optional logging
  to the console during development
- [x] use [electron](https://www.electronjs.org/) to wrap webapp for
  desktop
- [x] provide auto-update using [electron](https://www.electronjs.org/)
- [x] expand electron unit tests using [WDIO Electron
  Service](https://github.com/webdriverio-community/wdio-electron-service)
- [x] webapp unit test framework [Jest](https://jestjs.io/)
- [x] component test [Vue testing
  library](https://github.com/testing-library/vue-testing-library)
- [x] end-to-end test [cypress](https://github.com/cypress-io/cypress)
- [x] set up ZAP to provide security testing on commit
- [x] design files are to be backwardly compatible to Threat Dragon json

**demonstration pages**:

- [x] an online demonstration to be provided on [threat dragon's
  site](https://www.threatdragon.com/)
- [x] demo should either be a snapshot or a release version

### Version 1.4: released May 2021 {#version-14-released-may-2021}

- [x] written in javascript ES6 / ECMAScript 2015 or compatible
- [x] run on [node.js](https://nodejs.org/en/) server
- [x] use [express](http://expressjs.com/en/starter/installing.html) for
  backend application
- [x] provide a dockerfile for running in docker, similar to [existing
  TD](https://github.com/OWASP/threat-dragon/blob/main/Dockerfile)
- [x] static code analysis using [ESLint](https://eslint.org/)
- [x] webapp test runner
  [Karma](http://karma-runner.github.io/6.3/intro/installation.html)
  with [Jasmine](https://jasmine.github.io/) for [Vue Test
  Utils](https://vue-test-utils.vuejs.org/installation/#using-other-test-runners)
- [x] backend unit test framework [MochaJS](https://mochajs.org/) and
  assertions from [chai](https://github.com/chaijs/chai)
- [x] bundle the application and api for production using
  [webpack](https://webpack.js.org/)
- [x] be strictly open source, avoiding using languages or frameworks
  maintained outside the open source community

**documentation**:

- [x] documentation should be updated at the [threat dragon github
  pages](https://threatdragon.github.io/)
- [x] version 1.x docs are preserved and migrated to version 2.0
- [x] docs should be static pages based on
  [Jekyll](https://jekyllrb.com/) and markdown

### Previous versions

Mike Goodwin's initial roadmap for the project is [archived
here](https://github.com/OWASP/www-project-threat-dragon/wiki/Original-Roadmap).
The original roadmap had various milestones, most of which were achieved
by late 2020.

**Milestone 4**: Dev lifecycle integration

- Some CLI interface available mid 2020

**Milestone 3**: Release 1.0

- production version released February 2020
- version 1.3.1 released October 2020

**Milestone 2**: Beta release: Threat/mitigation rule engine

- achieved May 2017 with version 0.1.26

**Milestone 1**: Alpha release - Basic threat modelling experience

- achieved October 2015

------------------------------------------------------------------------

Threat Dragon: *making threat modeling less threatening*
:::

::: {#sec-tmf .section .page-body .tab-hidden}

------------------------------------------------------------------------

### Threat Model File (TMF) format

Threat Dragon version 1.x and Threat Dragon version 2.x use closely
related but incompatible JSON file formats. In addition both these file
formats are arranged around diagram elements used by the graph editing
engines: JointJS for version 1.x and AntV/X6 for version2.x. The data
model use in the Threat Dragon file format would be better centred round
threat model information rather than the data used for the graph
editing.

Both Threat Dragon file formats are incompatible with other open source
Threat Modeling files such as pytm, Threagile and Open Threat Model.

The intention is to change the model file format in Threat Dragon
version 3.x onwards. The goal will be to define a schema that is
flexible enough to easily convert from the existing:

- OWASP Threat Dragon versions 1.x and 2.x
- [OWASP pytm](../www-project-pytm/index.html) pythonic threat modeling
- [Threagile](https://threagile.io/) open-source toolkit for agile
  threat modeling
- [Open Threat Model](https://github.com/iriusrisk/OpenThreatModel)
  (OTM) file format

There is an [open
discussion](https://github.com/OWASP/threat-dragon/discussions/1152) for
suggestions and debate on this subject.
:::
::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-threat-dragon/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-threat-dragon){.github-button
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

### Classification

-  Lab Project
-  Tool

### Audience

-  Builder
-  Defender

### Documentation

- [Version 1.6.x](https://threatdragon.github.io/)
- [Version 2.x](https://www.threatdragon.com/docs/)
- [Demonstration](https://www.threatdragon.com/)

### Downloads

- Single page [web
  application](https://github.com/OWASP/threat-dragon/releases/tag/v2.4.1)
- Docker
  [image](https://hub.docker.com/r/owasp/threat-dragon/tags?page=1&ordering=name)
- Desktop installers for:
- [Linux / MacOS /
  Windows](https://github.com/OWASP/threat-dragon/releases/tag/v2.4.1)

### Source

- Threat Dragon [github repo](https://github.com/OWASP/threat-dragon)

### Licensing

- [Apache 2 License](https://www.apache.org/licenses/LICENSE-2.0)

### Leaders

- [Mike
  Goodwin](../cdn-cgi/l/email-protection.html#f5989c9e90db929a9a91829c9bb59a82948685db9a8792)
- [Jon
  Gadsden](../cdn-cgi/l/email-protection.html#abc1c4c585cccacfd8cfcec5ebc4dccad8db85c4d9cc)
- [Leo
  Reading](../cdn-cgi/l/email-protection.html#620e070d4c100703060b0c05220d150311124c0d1005)

### Main Contributors

- [Mohamed El-Bohy](https://github.com/mohamedselbohy)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::
