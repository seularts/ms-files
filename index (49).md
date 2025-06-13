:::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Acknowledgments](#div-acknowledgments){#acknowledgments-link
  .tab-link role="tab" aria-selected="false"
  aria-controls="acknowledgments"}
- [Join](#div-join){#join-link .tab-link role="tab"
  aria-selected="false" aria-controls="join"}
- [News](#div-news){#news-link .tab-link role="tab"
  aria-selected="false" aria-controls="news"}
- [Translations](#div-translations){#translations-link .tab-link
  role="tab" aria-selected="false" aria-controls="translations"}
- [Roadmap](#div-roadmap){#roadmap-link .tab-link role="tab"
  aria-selected="false" aria-controls="roadmap"}

# OWASP Serverless Top 10 {#owasp-serverless-top-10 .page-title}

::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
# Main

The [OWASP Top 10: Serverless
Interpretation](https://github.com/OWASP/Serverless-Top-10-Project/raw/master/OWASP-Top-10-Serverless-Interpretation-en.pdf)
is now available.

## Introduction

When adopting serverless technology, we eliminate the need to develop a
server to manage our application. By doing so, we also pass some of the
security threats to the infrastructure provider such as
[AWS](https://aws.amazon.com/serverless),
[Azure](https://azure.microsoft.com/en-us/services/functions/) and
[GCP](https://cloud.google.com/functions/). In addition to the many
advantages of serverless application development, such as cost and
scalability, some security aspects are also handed to our service
provider. Serverless services run code without provisioning or managing
servers and the code is executed only when needed.

However, even if these applications are running without a managed
server, they still execute code. If this code is written in an insecure
manner, it can still be vulnerable to application-level attacks.

The interpretation report examines the differences in attack vectors,
security weaknesses, and the business impact of application attacks on
in the serverless world, and, most importantly, the report will suggest
ways to to prevent them. As we will be able to see in the report, attack
and defense techniques are different from what we used to in the
traditional application world.

After that, an open-call will be established to collect data in the wild
and establishing the official Serverless Top 10 Report.

## Purpose

OWASP Serverless Top 10 aims at educating practitioners and
organizations about the consequences of the most common serverless
application security vulnerabilities, as well as providing basic
techniques to identify and protect against them.

## License

The OWASP Serverless Top 10 is free to use. It is licensed under the
[Creative Commons Attribution-ShareAlike 4.0 license (CC BY-SA
4.0)](http://creativecommons.org/licenses/by-sa/4.0/).
:::

::: {#sec-acknowledgments .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Founder

  ------------------------------------------------------------------------------------------------ ------------------------------------------------------- -----------------------------------------------------
  [Tal Melamed](../cdn-cgi/l/email-protection.html#deaabfb2f0b3bbb2bfb3bbba9eb1a9bfadaef0b1acb9)   [OWASP](https://www.owasp.org/index.php/User:Tal_Mel)   [LinkedIn](https://www.linkedin.com/in/talmelamed/)
  ------------------------------------------------------------------------------------------------ ------------------------------------------------------- -----------------------------------------------------

## Sponsors

![contrast](../../raw.githubusercontent.com/OWASP/www-project-serverless-top-10/master/assets/images/contrast_logo.png)

## Contributors

   
  ----------------------------------
  **Report Reviewers**
  Assaf Hefetz, Snyk
  Erez Metula, AppSec Labs
  Erez Yalon, Checkmarx
  Frank M. Catucci, OWASP
  Guy Bernhart-Magen, Intel
  Hemed Gur Ary, OWASP
  Jeff Williams, Contrast Security
  Jim DelGrosso, Synopsys
  Jochanan Sommerfeld, RDuck
  Kobi Lechner, INFINIDAT
  Limor Sylvie Kessem, IBM
  Marcin Hoppe, Auth0
  Mark Johnston, Google
  Martin Knobloch, OWASP
  Matthew Henderson, Microsoft
  Matteo Meucci, Minded Security
  Owen Pendlebury, OWASP
  Paco Hope, AWS
  Patrick Laverty, Rapid7
  Rupack Ganguly, Serverless Inc.
  Tanya Janca, Microsoft
  Tash Norris, Capital One
  Tom Brennan, IOActive
  Yan Cui, DAZN
  Youssef Elmalty, AWS
:::

::: {#sec-join .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Get Involved

Get involved in **OWASP Serverless Top 10**!

You do not have to be a security expert or a programmer to contribute.
Contact the Project Leader(s) to get involved, we welcome any type of
suggestions and comments.

Possible ways to get contribute:

- We are actively looking for organizations and individuals that will
  provide vulnerability prevalence data.
- Translation efforts (later stages)
- Assisting in the development of related and relevant tools (e.g. DVSA)

## Slack

Join out [Slack
channel](https://join.slack.com/t/owasp/shared_invite/enQtNDI5MzgxMDQ2MTAwLTEyNzIzYWQ2NDZiMGIwNmJhYzYxZDJiNTM0ZmZiZmJlY2EwZmMwYjAyNmJjNzQxNzMyMWY4OTk3ZTQ0MzFhMDY)

## GitHub

The project is maintained in the [OWASP Serverless Top
10](https://github.com/OWASP/Serverless-Top-10-Project/).

Feel free to open or solve an
[issue](https://github.com/OWASP/Serverless-Top-10-Project/issues).

Ready to contribute directly into the repo? Great! Just make sure you
read the [How to Contribute
guide](https://github.com/OWASP/Serverless-Top-10-Project/blob/master/CONTRIBUTING.md).
:::

::: {#sec-news .section .page-body .tab-hidden}

------------------------------------------------------------------------

## News & Events {#news_events}

- \[01 Sep 2018\]: Hello World! Project was donated by [Protego
  Labs](https://protego.io/)
- \[18 Sep 2018\]: Join our
  [Slack-channel](https://join.slack.com/t/owasp/shared_invite/enQtNDI5MzgxMDQ2MTAwLTEyNzIzYWQ2NDZiMGIwNmJhYzYxZDJiNTM0ZmZiZmJlY2EwZmMwYjAyNmJjNzQxNzMyMWY4OTk3ZTQ0MzFhMDY)
  **#project-sls-top-10**.
- \[22 Sep 2018\]: Follow our [Git
  Repo](https://github.com/OWASP/Serverless-Top-10-Project/).
- \[25 Oct 2018\]: [**First
  Release!**](https://ubiquitous-adventure-gnwnz4m.pages.github.io/OWASP-Top-10-Serverless-Interpretation-en.pdf)
- \[30 Oct 2018\]: PureSec joined as sponsor
- \[02 Nov 2018\]: OWASP [Official
  Announcement](https://owasp.blogspot.com/2018/11/serverless-top-10-added-to-project.html)
- \[13 Dec 2018\]: WhiteSource joined as sponsor
:::

::: {#sec-translations .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Translation Efforts

- **Chinese:** [\[OWASP Top 10 - Serverless Interpretation
  中文版（PDF)\](https://github.com/OWASP/Serverless-Top-10-Project/raw/master/2018/cn/OWASP-Top-10-Serverless-Interpretation-cn-v1.0.pdf)]{.underline}

项目牵头人：肖文棣、王颉（[\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
cfemail="196e78777e7359766e786a6937766b7e377a77"}）
项目组成员：刘晓辉、李宇全、明敏、王斌（排名不分先后，按姓氏拼音排列）
:::

::: {#sec-roadmap .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Planned Projects

- Serverless Security Top 10
- [DVSA](https://github.com/OWASP/DVSA) - **D**amn **V**ulnerable
  **S**erverless **A**pplication

## Roadmap

Coming soon!
:::
:::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-serverless-top-10/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-serverless-top-10){.github-button
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

### Serverless Top 10 Information

[![Incubator
Project](https://raw.githubusercontent.com/OWASP/www--site-theme/master/assets/images/common/owasp_level_incubator.svg?sanitize=true){height="66px"}](https://www.owasp.org/index.php/OWASP_Project_Stages#tab=Incubator_Projects)
![Documentation
Project](https://raw.githubusercontent.com/OWASP/www--site-theme/master/assets/images/common/owasp_documentation_project.svg?sanitize=true)

[![Builders](https://raw.githubusercontent.com/OWASP/www--site-theme/master/assets/images/common/owasp_builders.svg?sanitize=true)](https://www.owasp.org/index.php/Builders)
[![Breakers](https://raw.githubusercontent.com/OWASP/www--site-theme/master/assets/images/common/owasp_breakers.svg?sanitize=true)](https://www.owasp.org/index.php/Breakers)
[![Defenders](https://raw.githubusercontent.com/OWASP/www--site-theme/master/assets/images/common/owasp_defenders.svg?sanitize=true)](https://www.owasp.org/index.php/Defenders)

[![CC BY-SA
4.0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by-sa.svg){width="175px"}](http://creativecommons.org/licenses/by-sa/4.0/)

### Downloads or Social Links

- [Top 10 - Serverless Interpretation 2018
  (PDF)](https://github.com/OWASP/Serverless-Top-10-Project/raw/master/OWASP-Top-10-Serverless-Interpretation-en.pdf)
- [Top 10 - Serverless Interpretation 2018 -
  Presentation](https://github.com/OWASP/Serverless-Top-10-Project/raw/master/OWASP_DC_SLS_Top10.pdf)
- [Mailing
  List](https://groups.google.com/a/owasp.org/forum/#!forum/serverless-top-10)

### Code Repository

- [GitHub](https://github.com/OWASP/Serverless-Top-10-Project)

### Leaders

- [Tal
  Melamed](../cdn-cgi/l/email-protection.html#7f0b1e1351121a131e121a1b3f10081e0c0f51100d18)
- [Aruneesh
  Salhotra](../cdn-cgi/l/email-protection.html#c9a8bbbca7acacbaa1e7baa8a5a1a6bdbba889a6bea8bab9e7a6bbae)
- [David
  Melamed](../cdn-cgi/l/email-protection.html#1175706778753f7c747d707c7475517e667062613f7e6376)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::::
