::::::::::: main-wrapper
# OWASP Dependency-Check {#owasp-dependency-check .page-title}

:::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
Dependency-Check is a Software Composition Analysis (SCA) tool that
attempts to detect publicly disclosed vulnerabilities contained within a
project's dependencies. It does this by determining if there is a Common
Platform Enumeration (CPE) identifier for a given dependency. If found,
it will generate a report linking to the associated CVE entries.

## Introduction

The OWASP Top 10 2013 contains a new entry: A9-Using Components with
Known Vulnerabilities. Dependency Check can currently be used to scan
applications (and their dependent libraries) to identify any known
vulnerable components.

The problem with using known vulnerable components was described very
well in a paper by Jeff Williams and Arshan Dabirsiaghi titled,
"[Unfortunate Reality of Insecure
Libraries](https://cdn2.hubspot.net/hub/203759/file-1100864196-pdf/docs/Contrast_-_Insecure_Libraries_2014.pdf)".
The gist of the paper is that we as a development community include
third party libraries in our applications that contain well known
published vulnerabilities (such as those at the [National Vulnerability
Database](https://nvd.nist.gov/vuln/search)).

Dependency-check has a command line interface, a Maven plugin, an Ant
task, and a Jenkins plugin. The core engine contains a series of
analyzers that inspect the project dependencies, collect pieces of
information about the dependencies (referred to as evidence within the
tool). The evidence is then used to identify the [Common Platform
Enumeration (CPE)](https://nvd.nist.gov/products/cpe) for the given
dependency. If a CPE is identified, a listing of associated [Common
Vulnerability and Exposure (CVE)](https://cve.mitre.org/) entries are
listed in a report. Other 3rd party services and data sources such as
the NPM Audit API, the OSS Index, RetireJS, and Bundler Audit are
utilized for specific technologies.

Dependency-check automatically updates itself using the [NVD Data
Feeds](https://nvd.nist.gov/vuln/data-feeds) hosted by NIST.
'\''IMPORTANT NOTE:''' The initial download of the data may take ten
minutes or more. If you run the tool at least once every seven days,
only a small JSON file needs to be downloaded to keep the local copy of
the data current.
:::
::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/dependency-check/DependencyCheck/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/dependency-check/DependencyCheck){.github-button
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

### Project Classification

![Flagship
Project](../assets/images/common/owasp_level_flagship.svg "Flagship Project")

![Builders](../assets/images/common/owasp_builders.svg)
![Defenders](assets/images/common/owasp_defenders.svg)

![Tool Project](../assets/images/common/owasp_tool_project.svg)

### Downloads

Version 12.1.0

- [Command
  Line](https://github.com/dependency-check/DependencyCheck/releases/download/v12.1.0/dependency-check-12.1.0-release.zip)
- [Ant
  Task](https://github.com/dependency-check/DependencyCheck/releases/download/v12.1.0/dependency-check-ant-12.1.0-release.zip)
- [Maven
  Plugin](https://search.maven.org/#artifactdetails%7Corg.owasp%7Cdependency-check-maven%7C12.1.0%7Cmaven-plugin)
- [Gradle
  Plugin](https://search.maven.org/#artifactdetails%7Corg.owasp%7Cdependency-check-gradle%7C12.1.0%7Cgradle-plugin)
- [Mac Homebrew](https://brew.sh/):\
  `brew update && brew install dependency-check`

Other Plugins

- [Jenkins
  Plugin](https://plugins.jenkins.io/dependency-check-jenkins-plugin)
- [SBT
  Plugin](https://search.maven.org/#search%7Cga%7C1%7Cg%3A%22net.vonbuchholtz%22%20a%3A%22sbt-dependency-check%22)
- [lein-dependency-check](https://github.com/livingsocial/lein-dependency-check)

### Integrations

- [SonarQube
  Plugin](https://github.com/SonarSecurityCommunity/dependency-check-sonar-plugin)
- [Circle CI Orb](https://github.com/entur/owasp-orb)

### External Resources

- [GitHub](https://github.com/dependency-check/DependencyCheck)
- [Gradle
  Source](https://github.com/dependency-check/dependency-check-gradle)
- [SBT Source](https://github.com/albuch/sbt-dependency-check)
- [Jenkins Source](https://github.com/jenkinsci/dependency-check-plugin)
- [Ohloh](https://www.ohloh.net/p/dependencycheck)
- [Bintray](https://bintray.com/jeremy-long/owasp)

### Documentation

- [Documentation (on
  GitHub)](https://dependency-check.github.io/DependencyCheck/)

### Support

- [GitHub
  Issues](https://github.com/dependency-check/DependencyCheck/issues)

### Presentation

- [dependency-check
  (PDF)](https://dependency-check.github.io/DependencyCheck/general/dependency-check.pdf)
- [dependency-check
  (PPTX)](https://dependency-check.github.io/DependencyCheck/general/dependency-check.pptx)

### Licensing

[Apache 2 License](https://www.apache.org/licenses/LICENSE-2.0)

### Leaders

- [Jeremy
  Long](../cdn-cgi/l/email-protection.html#654a4a0f001700081c4b090a0b02250a120416154b0a1702)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::
