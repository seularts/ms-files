::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Release Versions](#div-downloads){#downloads-link .tab-link
  role="tab" aria-selected="false" aria-controls="downloads"}
- [FAQ](#div-faq){#faq-link .tab-link role="tab" aria-selected="false"
  aria-controls="faq"}

# OWASP Web Security Testing Guide {#owasp-web-security-testing-guide .page-title}

:::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
[![OWASP
Flagship](https://img.shields.io/badge/owasp-flagship-brightgreen.svg)](../projects/index.html#all-projects)
[![CC BY-SA
4.0](../../licensebuttons.net/l/by-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-sa/4.0/)
[![WSTG Github
Stars](https://img.shields.io/github/stars/OWASP/wstg?label=Stars%20on%20GitHub&style=social)](https://github.com/OWASP/wstg/)
[![Twitter
Follow](https://img.shields.io/twitter/follow/owasp_wstg?style=social)](https://twitter.com/owasp_wstg)

The Web Security Testing Guide (WSTG) Project produces the premier
cybersecurity testing resource for web application developers and
security professionals.

The WSTG is a comprehensive guide to testing the security of web
applications and web services. Created by the collaborative efforts of
cybersecurity professionals and dedicated volunteers, the WSTG provides
a framework of best practices used by penetration testers and
organizations all over the world.

## Contributions

Any contributions to the guide itself should be made via the [guide's
project repo](https://github.com/OWASP/wstg).

![:stop_sign:](../../github.githubassets.com/images/icons/emoji/unicode/1f6d1.png ":stop_sign:"){.emoji
height="20" width="20"} Contributions should only be made in the proper
repo against the latest content. Please don't open PRs here for
versioned or stable content, they represent point-in-time state.

## Stable

View the always-current stable version at [stable](stable/index.html).

## Latest

We are currently developing release version 5.0.

You can [read the latest development documents in our official GitHub
repository](https://github.com/OWASP/wstg/tree/master/document) or view
the bleeding-edge content at [latest](latest/index.html).

## Versioned Releases

[v4.2](v42/index.html) is currently available as a web-hosted release
and PDF. Previous releases are available as PDFs and in some cases web
content via the **Release Versions** tab.

## How To Reference WSTG Scenarios

Each scenario has an identifier in the format
`WSTG-<category>-<number>`{.language-plaintext .highlighter-rouge},
where: 'category' is a 4 character upper case string that identifies the
type of test or weakness, and 'number' is a zero-padded numeric value
from 01 to 99. For example:`WSTG-INFO-02`{.language-plaintext
.highlighter-rouge} is the second Information Gathering test.

The identifiers may change between versions therefore it is preferable
that other documents, reports, or tools use the format:
`WSTG-<version>-<category>-<number>`{.language-plaintext
.highlighter-rouge}, where: 'version' is the version tag with
punctuation removed. For example: `WSTG-v41-INFO-02`{.language-plaintext
.highlighter-rouge} would be understood to mean specifically the second
Information Gathering test from version 4.1.

If identifiers are used without including the
`<version>`{.language-plaintext .highlighter-rouge} element then they
should be assumed to refer to the latest Web Security Testing Guide
content. Obviously as the guide grows and changes this becomes
problematic, which is why writers or developers should include the
version element.

### Linking

Linking to Web Security Testing Guide scenarios should be done using
versioned links not `stable`{.language-plaintext .highlighter-rouge} or
`latest`{.language-plaintext .highlighter-rouge} which will definitely
change with time. However, it is the project team's intention that
versioned links not change. For example:
`https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/01-Information_Gathering/02-Fingerprint_Web_Server`{.language-plaintext
.highlighter-rouge}. Note: the `v42`{.language-plaintext
.highlighter-rouge} element refers to version 4.2.
:::

::: {#sec-downloads .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Stable {#stable}

View the always-current stable version at [stable](stable/index.html).

## \[Unreleased 4.3\] {#unreleased-43}

## \[Version 4.2\] - 2020-12-03 {#version-42---2020-12-03}

[Version 4.2](v42/index.html) introduces new testing scenarios, updates
existing chapters, and offers an improved writing style and chapter
layout.

[Download the v4.2
PDF](https://github.com/OWASP/wstg/releases/download/v4.2/wstg-v4.2.pdf)
here.

## \[Version 4.1\] - 2020-04-21 {#version-41---2020-04-21}

[Version 4.1](v41/index.html) serves as a post-migration stable version
under the new GitHub repository workflow.

[Download the v4.1
PDF](https://github.com/OWASP/wstg/releases/download/v4.1/wstg-v4.1.pdf)
here.

## \[Version 4.0\] - 2014-09-17 {#version-40---2014-09-17}

[Download the v4 PDF](assets/archive/OWASP_Testing_Guide_v4.pdf) here.

A printed book is also made [available for
purchase](https://www.lulu.com/shop/matteo-meucci-and-andrew-muller/testing-guide-40-release/paperback/product-22294314.html).

## \[Version 3.0\] - 2008-12-16 {#version-30---2008-12-16}

[Download the v3 PDF](assets/archive/OWASP_Testing_Guide_v3.pdf) here.

### \[Pre-release 3.0\] - 2008-11-06 {#pre-release-30---2008-11-06}

[View a presentation
(PPT)](assets/archive/OWASP_EU_Summit_2008_OWASP_Testing_Guide_v3.ppt)
previewing the release at the OWASP EU Summit 2008 in Portugal.

## \[Version 2.0\] - 2007-02-10 {#version-20---2007-02-10}

[Download the v2 PDF](assets/archive/OWASP_Testing_Guide_v2.pdf) here.

The guide is also available in [Word Document format in English
(ZIP)](assets/archive/OWASP_Testing_Guide_v2_doc.zip) as well as [Word
Document format translation in Spanish
(ZIP)](assets/archive/OWASP_Testing_Guide_v2_spanish_doc.zip).

## \[Version 1.1\] - 2004-08-14 {#version-11---2004-08-14}

Version 1.1 is released as the *OWASP Web Application Penetration
Checklist*.

[Download the v1.1
PDF](assets/archive/OWASP_Web_Application_Penetration_Checklist_v1_1.pdf)
here.

## \[Version 1.0\] - 2004-12-10 {#version-10---2004-12-10}

[Download the v1 PDF](assets/archive/OWASP_Testing_Guide_v1.pdf) here.

## Archives

Historical [archives of the Mailman owasp-testing mailing
list](https://lists.owasp.org/pipermail/owasp-testing/index) are
available to view or download.
:::

::: {#sec-faq .section .page-body .tab-hidden}

------------------------------------------------------------------------

## How can I help?

We are actively inviting new contributors to help keep the WSTG up to
date! You can get started at [our official GitHub
repository](https://github.com/OWASP/wstg).

## How can I contact you?

To report issues or make suggestions for the WSTG, please use [GitHub
Issues](https://github.com/OWASP/wstg/issues).

For everything else, we're easy to find on Slack:

1.  Join the OWASP Group Slack with this [invitation
    link](https://owasp-slack.herokuapp.com/).
2.  Join this project's [channel,
    #testing-guide](https://app.slack.com/client/T04T40NHX/CJ2QDHLRJ).

You can @ us on Twitter [\@owasp_wstg](https://twitter.com/owasp_wstg).
:::
::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/OWASP/wstg/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/OWASP/wstg){.github-button icon="octicon-star"
data-size="large" show-count="true" aria-label="Star on GitHub"}
:::

:::::: {.sidebar role="complementary"}
::: owasp-sidebar-top
**The OWASP^®^ Foundation** works to improve the security of software
through its community-led open source software projects, hundreds of
chapters worldwide, tens of thousands of members, and by hosting local
and global conferences.
:::

### Project Classification

-  Flagship Project
-  Documentation
-  Breaker
-  Builder

### Project Links

- [Latest](latest/index.html)
- [GitHub Repository](https://github.com/OWASP/wstg)

### Getting Involved

- [Code of
  Conduct](https://github.com/OWASP/wstg/blob/master/CODE_OF_CONDUCT.md)
- [Contribution
  Guide](https://github.com/OWASP/wstg/blob/master/CONTRIBUTING.md)

### Social

- [Join OWASP Slack](../slack/invite.html)
- Channel:
  [#testing-guide](https://app.slack.com/client/T04T40NHX/CJ2QDHLRJ)
- Twitter: [\@owasp_wstg](https://twitter.com/owasp_wstg)
- BlueSky:
  [\@owasp-wstg.bsky.social](https://bsky.app/profile/owasp-wstg.bsky.social)

### License

- [![CC BY-SA
  4.0](../../licensebuttons.net/l/by-sa/4.0/80x15.png)](https://creativecommons.org/licenses/by-sa/4.0/)
  CC BY-SA 4.0

### Leaders

- [Elie
  Saad](../cdn-cgi/l/email-protection.html#bedbd2d7db90cddfdfdafed1c9dfcdce90d1ccd9)
- [Rick
  Mitchell](../cdn-cgi/l/email-protection.html#c2b0aba1a9ecafabb6a1aaa7aeae82adb5a3b1b2ecadb0a5)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::
