:::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Demonstration](#div-demonstration){#demonstration-link .tab-link
  role="tab" aria-selected="false" aria-controls="demonstration"}
- [Contributing](#div-contributing){#contributing-link .tab-link
  role="tab" aria-selected="false" aria-controls="contributing"}

# OWASP Dragon-GPT {#owasp-dragon-gpt .page-title}

::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![Dragon-GPT Icon](assets/images/icon.png){width="20%" height="20%"
align="left" hspace="15" vspace="45"
style="margin-bottom: 30px; position: relative"}

[![](https://img.shields.io/badge/owasp-incubator-blue)](../other_projects/index.html)
[![GitHub
contributors](https://img.shields.io/github/contributors/LuizBoina/dragon-gpt)](https://github.com/LuizBoina/dragon-gpt/graphs/contributors)
[![GitHub
Pulse](https://img.shields.io/github/commit-activity/m/LuizBoina/dragon-gpt)](https://github.com/badges/shields/pulse)
[![GitHub Workflow Status (with
event)](https://img.shields.io/github/actions/workflow/status/LuizBoina/dragon-gpt/.github%2Fworkflows%2Fdjango-test.yml)](https://github.com/LuizBoina/dragon-gpt/actions)

## Description

Dragon-GPT is an AI-powered tool that automatically performs the threat
modeling analysis on the diagram made using the OWASP Threat Dragon
modeling software. It uses the OpenAI API, so you need to have a valid
account for their tokens to use on each program call, and the JSON file
generated when you save/export an OWASP Threat Dragon project (generally
saved in td.vue folder).

The program itself is pretty simple, it extracts every relevant
information on the JSON file, like the diagram model and components used
on the modeling, and transforms it into a human-readable sentence. After
that, the sentence is send via OpenAI API, and the result of the
analysis is printed. By default, it uses chatgpt-3.5-turbo but you can
change that via parameter to another model like the chatgpt-4.

## Changelog

- \[Update on 27/10/23\] Add Support to Local LLM, the Llama 2, so you
  don't need an OpenAI account. The results using Llama may be inferior
  and slower than ChatGPT but at least it's free.
:::

:::: {#sec-demonstration .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

In the example below we have a very simple architecture where a user
interacts with a web client, the web client sends HTTP requests to the
server and the server makes queries to an SQL database. The Dragon-GPT
creates a list of sentences, describes the diagram based on the JSON
file created by OWASP THreat Dragon, and uses it as input to the LLM,
which can be the ChatGPT or a local LLM.

::: {align="center"}
[![Dragon-GPT
Demonstration](assets/images/yt_preview.jpg){height="480px"}](https://www.youtube.com/watch?v=CUHcyfK1BXM)
:::
::::

::: {#sec-contributing .section .page-body .tab-hidden}

------------------------------------------------------------------------

![Dragon-GPT Logo](assets/images/logo.png){hspace="15" vspace="45"
style="margin-bottom: 30px; position: relative"}

------------------------------------------------------------------------

Contributing in the development and promotion of Dragon-GPT is actively
encouraged! You don't need to be a security nor developer expert in
order to contribute. Some of the ways you can help:

- [Open a pull request](https://github.com/LuizBoina/dragon-gpt/pulls)
- [Give us feedback / suggestions / report
  bugs](https://github.com/LuizBoina/dragon-gpt/issues)
- Contact me via
  [LinkedIn](https://www.linkedin.com/in/luiz-felipe-boina/)
:::
:::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-dragon-gpt/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-dragon-gpt){.github-button
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

### Dragon-GPT Information

-  Incubator Project
-  Tool

### Audience

-  Defender
-  Builder

### License

![MIT license](https://img.shields.io/badge/license-MIT-green)

### Code Repository

- [Github Repo](https://github.com/LuizBoina/dragon-gpt)

### Change Log

- [changes](index.html#changelog)

### Leaders

- [Luiz Felipe
  Boina](../cdn-cgi/l/email-protection.html#c488b1adbeea82a1a8adb4a186abadaaa5f2fc84abb3a5b7b4eaabb6a3)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::
