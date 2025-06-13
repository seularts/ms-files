:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}

# OWASP SEDATED® {#owasp-sedated .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![SEDATED_logo_full](../../raw.githubusercontent.com/OWASP/www-project-sedated/master/assets/images/SEDATED_logo_full.png)

The **SEDATED®** Project (Sensitive Enterprise Data Analyzer To
Eliminate Disclosure) focuses in on preventing sensitive data such as
user credentials and tokens from being pushed to Git. Developers are
constantly pushing changes to GitHub and will most likely eventually try
pushing a commit that contains sensitive information and we want to help
catch and prevent that. The **SEDATED®** application will run on the Git
server and review all incoming code changes. If it identifies sensitive
data it will reject the push otherwise it will allow it.

## Purpose

With the myriad of code changes required in today's CICD environment
developers are constantly pushing code that could unintentionally
contain sensitive information. This potential sensitive data exposure
represents a huge risk to organizations ([2021 OWASP Top Ten #2 -
Cryptographic
Failures](../Top10/A02_2021-Cryptographic_Failures/index.html)).
**SEDATED®** addresses this issue by automatically reviewing all
incoming code changes and providing instant feedback to the developer.
If it identifies sensitive data it will prevent the commit(s) from being
pushed to the Git server.

## Latest Version

[Version 1.2.0](https://github.com/OWASP/SEDATED/releases/tag/v1.2.0) is
the latest version!

## Getting Involved

We are looking for community support with this project as there is a lot
more we can do! Feel free to checkout the
**[OWASP/SEDATED®](https://github.com/owasp/sedated)** repository and
contribute any ideas you may have to make **SEDATED®** even better!
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
[Watch](https://github.com/owasp/www-project-sedated/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-sedated){.github-button
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

### Leaders

- [Simeon
  Cloutier](https://www.linkedin.com/in/simeon-cloutier-7956a856/)
- [Dennis Kennedy](https://www.linkedin.com/in/denniskennedy113/)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
