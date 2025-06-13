::::::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}

# OWASP Noir {#owasp-noir .page-title}

:::::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
:::: {#sec-main .section .page-body}
::: {align="center"}
![](assets/images/logo619b.png?noir){width="500px;"}

Attack surface detector that identifies endpoints by static analysis.
:::

[![](https://img.shields.io/badge/CONTRIBUTIONS-WELCOME-000000?style=for-the-badge&labelColor=black)](https://github.com/owasp-noir/noir/blob/main/CONTRIBUTING.md)
[![](https://img.shields.io/github/v/release/owasp-noir/noir?style=for-the-badge&color=black&labelColor=black&logo=web)](https://github.com/owasp-noir/noir/releases)
[![](https://img.shields.io/badge/Crystal-000000?style=for-the-badge&logo=crystal&logoColor=white)](https://crystal-lang.org/)
[![](https://img.shields.io/badge/OWASP-000000?style=for-the-badge&logo=owasp&logoColor=white)](index.html)

------------------------------------------------------------------------

Noir is an open-source project specializing in identifying attack
surfaces for enhanced whitebox security testing and security pipeline.
This includes the capability to discover API endpoints, web endpoints,
and other potential entry points within source code for thorough
security analysis and DAST. For more information, please visit our
[documentation page](https://owasp-noir.github.io/noir/).

![](assets/images/preview.jpg)

## Key Features

- Extract API endpoints and parameters from source code.
- Support multiple languages and frameworks.
- Uncover security issues with detailed analysis and rule-based passive
  scanning.
- Integrate seamlessly with DevOps pipelines and tools like curl, ZAP,
  and Caido.
- Deliver clear, actionable results in formats like JSON, YAML, and OAS.
- Enhance endpoint discovery with AI for unfamiliar frameworks and
  hidden APIs.

## Road Map

We plan to expand the range of supported programming languages and
frameworks, and to continuously increase accuracy. Furthermore, we will
leverage AI and Large Language Models (LLMs) to significantly broaden
our analysis capabilities.

Initially conceived as a tool to assist with WhiteBox testing, our
immediate goal remains to extract and provide endpoints from the source
code within the DevSecOps Pipeline. This enables Dynamic Application
Security Testing (DAST) tools to conduct more accurate and stable scans.

Looking ahead, our ambition is for our tool to evolve into a crucial
bridge, seamlessly connecting source code with DAST and other security
testing tools, thereby facilitating a more integrated and effective
security posture.
::::

::::::::::: {#sec-installation .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Installation

### Homebrew

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
brew install noir

# https://formulae.brew.sh/formula/noir
```
:::
::::

### Snapcraft

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
sudo snap install noir

# https://snapcraft.io/noir
```
:::
::::

### From Sources

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
# Install Crystal-lang
# https://crystal-lang.org/install/

# Clone this repo
git clone https://github.com/owasp-noir/noir
cd noir

# Install Dependencies
shards install

# Build
shards build --release --no-debug

# Copy binary
cp ./bin/noir /usr/bin/
```
:::
::::

### Docker (GHCR)

:::: {.language-bash .highlighter-rouge}
::: highlight
``` highlight
docker pull ghcr.io/owasp-noir/noir:main
```
:::
::::
:::::::::::
::::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp-noir/noir/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp-noir/noir){.github-button
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

-  Code
-  Builder
-  Breaker

### Downloads or Social Links

- [Releases](https://github.com/owasp-noir/noir/releases)
- [Homebrew](https://formulae.brew.sh/formula/noir)
- [Snapcraft](https://snapcraft.io/noir)
- [Docker
  (GHCR)](https://github.com/owasp-noir/noir/pkgs/container/noir)

### Code Repository

- [Code Repository](https://github.com/owasp-noir/noir)
- [Discussions](https://github.com/orgs/owasp-noir/discussions)
- [Documentation](https://owasp-noir.github.io/noir/)

### Recent Releases

- [v0.21.1](https://github.com/owasp-noir/noir/releases/tag/v0.21.1){target="_blank"}
- [v0.21.0](https://github.com/owasp-noir/noir/releases/tag/v0.21.0){target="_blank"}
- [v0.20.1](https://github.com/owasp-noir/noir/releases/tag/v0.20.1){target="_blank"}
- [v0.20.0](https://github.com/owasp-noir/noir/releases/tag/v0.20.0){target="_blank"}
- [v0.19.1](https://github.com/owasp-noir/noir/releases/tag/v0.19.1){target="_blank"}
- [v0.19.0](https://github.com/owasp-noir/noir/releases/tag/v0.19.0){target="_blank"}

### Leaders

- [HAHWUL](../cdn-cgi/l/email-protection.html#0c64226069694c637b6d7f7c22637e6b)
- [KSG](../cdn-cgi/l/email-protection.html#7506101a1b12121c5b1e1c18351a021406055b1a0712)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::::::
