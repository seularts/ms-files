:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Risks](#div-risks){#risks-link .tab-link role="tab"
  aria-selected="false" aria-controls="risks"}

# OWASP Top 10 Risks for Open Source Software {#owasp-top-10-risks-for-open-source-software .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![top 10 oss risks](assets/images/top10.png)

## Introduction

Despite the heavy reliance on OSS in the software supply chain, the
industry lacks a consistent way to understand and measure risk for OSS.
Risk management in OSS started with license management, and then evolved
to CVEs, but we still lack a holistic approach to OSS risk management
that encompasses security, legal, and operational aspects. With this
document, we're excited to collaborate with industry experts and leaders
to create just that.

Over the last decade of reliance on OSS, known vulnerabilities, captured
as CVEs, have emerged as the key metric of security. Known
vulnerabilities, while an important signal, typically capture mistakes
made by well-intentioned developers. These mistakes could be exploited
by attackers and should be fixed, but they hardly encompass the full
spectrum of risks that a reliance on OSS includes.

Operational risks, like ones introduced by outdated or unmaintained
software, or next-generation supply chain attacks like name confusion
attacks, cannot be captured by CVEs. These risks are significant, as
highlighted by the recent [Open Source Security and Risk Analysis
report](https://www.synopsys.com/content/dam/synopsys/sig-assets/reports/rep-ossra-2023.pdf)
by Synopsys:

- 89% of codebases contain OSS that is more than 4 years out of date
- 91% of codebases contain components that have had no new development
  in over two years

On [The State of Dependency
Management](https://endorlabs.webflow.io/learn/state-of-dependency-management),
the Station 9 research team from Endor Labs uncovered that 95% of
vulnerabilities exist in transitive dependencies (the software packages
automatically brought in by the OSS selected by developers). And out of
those, many are not actually reachable, or will cause a devastating
ripple effect of incompatibility if they were updated. With this list,
which was peer-reviewed and contributed to by over 20 CISOs and CTOs,
the team sought to find the top risks security and development teams
should be ready for, both operational and security.

The top 10 OSS risks are:

- [OSS-RISK-1](0-1-risks/OSS1-Known-Vulnerabilities.html) Known
  Vulnerabilities: A component version may contain vulnerable code,
  accidentally introduced by its developers. Vulnerability details are
  publicly disclosed, e.g, through CVE, GitHub Security Advisories or
  other, more informal communication channels. Exploits and patches may
  or may not be available.
- [OSS-RISK-2](0-1-risks/OSS2-Compromise-Legitimate-Package.html)
  Compromise of Legitimate Package: Attackers may compromise resources
  that are part of an existing legitimate project or of the distribution
  infrastructure in order to inject malicious code into a component,
  e.g, through hijacking the accounts of legitimate project maintainers
  or exploiting vulnerabilities in package repositories.
- [OSS-RISK-3](0-1-risks/OSS3-Name-Confusion-Attack.html) Name Confusion
  Attacks: Attackers may create components whose names resemble names of
  legitimate open-source or system components (typo-squatting), suggest
  trustworthy authors (brand-jacking) or play with common naming
  patterns in different languages or ecosystems (combo-squatting).
- [OSS-RISK-4](0-1-risks/OSS4-Unmaintained-Software.html) Unmaintained
  Software: A component or component version may not be actively
  developed any more, thus, patches for functional and non-functional
  bugs may not be provided in a timely fashion (or not at all) by the
  original open source project.
- [OSS-RISK-5](0-1-risks/OSS5-Outdated-Software.html) Outdated Software:
  A project may use an old, outdated version of the component (though
  newer versions exist).
- [OSS-RISK-6](0-1-risks/OSS6-Untracked-Dependencies.html) Untracked
  Dependencies: Project developers may not be aware of a dependency on a
  component at all, e.g., because it is not part of an upstream
  component's SBOM, because SCA tools are not run or do not detect it,
  or because the dependency is not established using a package manager.
- [OSS-RISK-7](0-1-risks/OSS7-License-Regulatory-Risks.html) License
  Risk: A component or project may not have a license at all, or one
  that is incompatible with the intended use or whose requirements are
  not or cannot be met.
- [OSS-RISK-8](0-1-risks/OSS8-Immature-Software.html) Immature Software:
  An open source project may not apply development best-practices, e.g.,
  not use a standard versioning scheme, have no regression test suite,
  review guidelines or documentation. As a result, a component may not
  work reliably or securely.
- [OSS-RISK-9](0-1-risks/OSS9-Unapproved-Change.html) Unapproved Change:
  A component may change without developers being able to notice, review
  or approve such changes, e.g., because the download link points to an
  unversioned resource, because a versioned resource has been modified
  or tampered with or due to an insecure data transfer.
- [OSS-RISK-10](0-1-risks/OSS10-UnderOversized-Dependency.html)
  Under/over-sized Dependency: A component may provide very little
  functionality (e.g. npm micro packages) or a lot of functionality (of
  which only a fraction may be used).

## Authors and Contributors

![Authors](assets/images/authors.png)

## Dependency Management 101

To better understand how these risks may affect us, let us quickly
review some basic concepts of dependency management using a simple
example. Just skip this section if you're familiar with dependency
management.

The root node of the dependency graph displayed below represents the
example project. The child nodes of the root represent 9 open source
components the project "directly" depends on. Those components, however,
depend on other components as well, all of which become "transitive" or
"indirect" dependencies from the perspective of the top-level project.

Direct dependencies are consciously selected by the project developers,
e.g., through the declaration in a manifest file such as package.json
(Node.js/npm) or pom.xml (Java/Maven) file. Package managers take care
of downloading and installing those direct dependencies from 3rd party
package repositories to the developers workstation or a CI/CD system.
When doing so, package managers also identify transitive dependencies,
resolve potential version conflicts and install them locally. In other
words, plenty of components are downloaded in an automated fashion in
order to make sure all code required by the example project (and more)
is present on the developer machine.

![Dependency Graph for Graph Maven Plugin](assets/images/deptree.png)

This high degree of automation boosted the reuse of open source
components in today's software development. As a result, large portions
of modern software have not been specifically developed for an
application at hand, but come from generic open source projects. Looking
again at the dependency graph, it is not surprising that the ratio of
code written for the project itself (the root node) to the code of open
source components is 1:4 or less. And we haven't even touched upon IDEs,
build tools etc.
:::

::: {#sec-risks .section .page-body .tab-hidden}

------------------------------------------------------------------------

## OSS-RISK-1 : Known vulnerabilities in dependencies {#oss-risk-1--known-vulnerabilities-in-dependencies}

**Description:**

A component version may contain vulnerable code, accidentally introduced
by its developers. Vulnerability details are publicly disclosed, e.g,
through CVE, GitHub Security Advisories or other, more informal
communication channels. Exploits and patches may or may not be
available.

The vulnerability may be exploitable in the context of the downstream
software, which could compromise the confidentiality, integrity or
availability of the respective system or its data, allow lateral
movements in the target environment or have other negative effects.

**Examples:**

1.  [CVE-2017-5638](https://cwiki.apache.org/confluence/display/WW/S2-045)
    in Apache Struts, which caused the [Equifax data
    breach](https://en.wikipedia.org/wiki/2017_Equifax_data_breach)
2.  [CVE-2021-44228](https://logging.apache.org/log4j/2.x/security.html#CVE-2021-44228)
    in Apache Log4j, also called
    [Log4Shell](https://en.wikipedia.org/wiki/Log4Shell)

**Actions:**

1.  Monitor applications, containers and systems for the presence of
    (direct and transitive) open source dependencies with known
    vulnerabilities
2.  Prioritize the analysis and mitigation on the basis of, for instance
    - Scores and metrics like [CVSS](https://www.first.org/cvss/) and
      [EPSS](https://www.first.org/epss/)
    - Threat intelligence like the availability and maturity of exploit
      code, or information on attacks observed in the wild such as
      provided by the CISA [KEV
      catalog](https://www.cisa.gov/known-exploited-vulnerabilities-catalog)
    - DAST and SAST tools, which determine if vulnerable code can be
      executed in the context of the dependent software

**References:**

1.  OWASP Top 10:2021 [A06:2021 - Vulnerable and Outdated
    Components](../Top10/A06_2021-Vulnerable_and_Outdated_Components/index.html)

------------------------------------------------------------------------

## OSS-RISK-2 : Compromise of Legitimate Package {#oss-risk-2--compromise-of-legitimate-package}

**Description:**

Attackers may compromise resources that are part of an existing
legitimate project or of the distribution infrastructure in order to
inject malicious code into a component, e.g, through hijacking the
accounts of legitimate project maintainers or exploiting vulnerabilities
in package repositories.

Malicious code can be executed on end-user systems or on systems
belonging to the organization that develops and/or operates the
dependent software (e.g., build systems or developer workstations). The
confidentiality, integrity and availability of systems and the data
processed/stored thereon is at risk.

**Examples:**

1.  [Event-stream](https://blog.npmjs.org/post/180565383195/details-about-the-event-stream-incident):
    This attack on a legitimate component targeted users of Copay
    Bitcoin wallets.
2.  [The SolarWinds Cyber-Attack](https://www.cisecurity.org/solarwinds)

**Actions:**

There's no single action to detect and prevent the ingestion of
compromised packages. Organizations should consult emerging standards
and frameworks like the Secure Supply Chain Consumption Framework
(S2C2F) to inform themselves about possible safeguards, which should be
selected and prioritized according to individual security requirements
and risk appetite.

Example actions comprise:

1.  Verify component provenance according to SLSA
2.  Build component from the sources (yourself or a trusted 3rd-party)
3.  Review code manually and/or automatically
4.  Retrieve all components from a secured internal store (such binary
    repositories host home-made binaries and mirror external components)

**References:**

1.  [Secure Supply Chain Consumption
    Framework](https://www.microsoft.com/en-us/securityengineering/opensource)
    (S2C2F)
2.  [Risk Explorer for Software Supply
    Chains](https://riskexplorer.endorlabs.com/) Subvert Legitimate
    Package (AV-001)
3.  [Supply chain Levels for Software Artifacts](https://slsa.dev/)
    (SLSA)
4.  MITRE ATT&CK [T1195.001 Compromise Software Dependencies and
    Development Tools](https://attack.mitre.org/techniques/T1195/001/)
5.  OWASP Top 10 CI-CD Security Risks [CICD-SEC-3: Dependency Chain
    Abuse](../www-project-top-10-ci-cd-security-risks/CICD-SEC-03-Dependency-Chain-Abuse.html)
6.  OWASP Software Component Versification Standard (SCVS) [V6 Pedigree
    and
    Provenance](https://owasp-scvs.gitbook.io/scvs/v6-pedigree-and-provenance)

------------------------------------------------------------------------

## OSS-RISK-3 : Name Confusion Attacks {#oss-risk-3--name-confusion-attacks}

**Description:**

Attackers may create components whose names resemble names of legitimate
open-source or system components (typo-squatting), suggest trustworthy
authors (brand-jacking) or play with common naming patterns in different
languages or ecosystems.

Malicious code can be executed on end-user systems or on systems
belonging to the organization that develops and/or operates the
dependent software (e.g., build systems or developer workstations). The
confidentiality, integrity and availability of systems and the data
processed/stored thereon is at risk.

**Examples:**

1.  [Colourama](https://bertusk.medium.com/cryptocurrency-clipboard-hijacker-discovered-in-pypi-repository-b66b8a534a8)
    (PyPI, 2018): Typo-squatting attack on the legitimate Python package
    "colorama", redirecting Bitcoin transfers to an attacker-controlled
    wallet.

**Actions:**

Prior to installing/using a component:

1.  Check code characteristics (pre/post installation hooks, encoded
    payloads, etc.) and project characteristics (source code repository,
    maintainer accounts, release frequency, number of downstream users,
    etc.) for leading risk indicators.

    Note that some component metadata is not verified by package
    repositories, thus, can easily be forged by attackers.

2.  Verify that the component carries a signature from a trusted party
    (for ecosystems that support/require signatures)

**References:**

1.  [Secure Supply Chain Consumption
    Framework](https://www.microsoft.com/en-us/securityengineering/opensource)
    (S2C2F)
2.  [Risk Explorer for Software Supply
    Chains](https://riskexplorer.endorlabs.com/) Create Name Confusion
    with Legitimate Package (AV-200)
3.  [Supply chain Levels for Software Artifacts](https://slsa.dev/)
    (SLSA)
4.  MITRE ATT&CK [T1195.001 Compromise Software Dependencies and
    Development Tools](https://attack.mitre.org/techniques/T1195/001/)

------------------------------------------------------------------------

## OSS-RISK-4 : Unmaintained software {#oss-risk-4--unmaintained-software}

**Description:**

A component or component version may not be actively developed or
supported any more, i.e. patches for new functional and security bugs
may not be developed.

Patch development may therefore need to be done by downstream developers
with potentially less experience and knowledge regarding the affected
component.

This can result in increased efforts and longer resolution times. During
that time, system access or functionality may need to be restricted to
avoid continued exposure.

**Examples:**

1.  [core-js](https://www.theregister.com/2020/03/26/corejs_maintainer_jailed_code_release)
    (npm, 2020)
2.  [Gorilla Web
    Toolkit](https://www.chainguard.dev/unchained/the-archiving-of-the-gorilla-web-toolkit-a-tale-of-two-software-security-risks)
    (Go, 2022)
3.  [minimist](https://twitter.com/ljharb/status/1579610392414007299?lang=en)
    (npm, 2022)

**Actions:**

1.  Check indicators for project liveliness and health.

    However, note that little activity can also be a sign of maturity.
    Projects that are considered feature-complete and mature will see
    less activity than projects under active development, and still
    receive timely patches in case of problems.

    Example indicators:

    - Recent issue and commit activity means the project is active.
    - A high ratio of issues opened by external contributors indicates
      that the project is active.
    - Activity from corporate affiliated accounts that indicate that the
      project can have reliable backing and support.
    - Activity from reputable accounts indicates that the repository is
      well-maintained.
    - The repository has frequent releases indicating a commitment to
      maintaining and supporting the codebase.

2.  Search for information on a project's maintenance or support
    strategy, e.g., the presence and dates of long-term support (LTS)
    versions.

    The Spring project is a great example for documenting [support time
    frames](https://spring.io/projects/spring-boot#support).

3.  Check the project page to see whether its has been archived, or
    whether there are any explicit statements regarding the project's
    maintenance status.

**References:**

1.  OWASP Top 10:2021 [A06:2021 - Vulnerable and Outdated
    Components](../Top10/A06_2021-Vulnerable_and_Outdated_Components/index.html)
2.  [Bus factor](https://en.wikipedia.org/wiki/Bus_factor)
3.  Common Weakness Enumeration (CWE) [CWE-1104: Use of Unmaintained
    Third Party
    Components](https://cwe.mitre.org/data/definitions/1104.html)
4.  [CWE-1329: Reliance on Component That is Not
    Updateable](https://cwe.mitre.org/data/definitions/1329.html)
5.  [Adoptoposs](https://github.com/adoptoposs/adoptoposs)
6.  [Jazzband](https://jazzband.co/)

------------------------------------------------------------------------

## OSS-RISK-5 : Outdated software {#oss-risk-5--outdated-software}

**Description:**

A project may use an old, outdated version of the component (though
newer versions exist).

Falling too much behind the latest releases of a dependency can make it
difficult to perform timely updates in emergency situations, e.g., when
a vulnerability is disclosed for the version in use. Old releases may
also not receive the same level of security assessment as recent
versions, esp. whether they are affected by vulnerabilities. If a new
version is syntactically or semantically incompatible with the current
version in use, application developers may require significant
update/migration efforts to resolve the incompatibility.

**Examples:**

1.  [Spring Boot support time
    frames](https://spring.io/projects/spring-boot#support)
2.  Vulnerabilities affecting Apache Tomcat are ["not checked against
    the 8.0.x branch and will not be
    fixed"](https://tomcat.apache.org/security-8.html)

**Actions:**

1.  Make dependency updates recurring backlog items
2.  Automate the discovery and suggestion of updates, e.g. through
    merge/pull requests
3.  Detect the introduction or breaking changes through change impact
    analysis tools

**References:**

1.  OWASP Top 10:2021 [A06:2021 - Vulnerable and Outdated
    Components](../Top10/A06_2021-Vulnerable_and_Outdated_Components/index.html)
2.  Tools to check for the availability of new versions:
    - [Versions Maven
      Plugin](https://www.mojohaus.org/versions/versions-maven-plugin/index.html)
3.  Tools to detect breaking changes:
    - [AexPy](https://github.com/StardustDL/aexpy)

------------------------------------------------------------------------

## OSS-RISK-6 : Untracked Dependencies {#oss-risk-6--untracked-dependencies}

**Description:**

Project developers may not be aware of a dependency on a component at
all, e.g., because it is not part of an upstream component's SBOM,
because SCA tools are not run or do not detect it, or because the
dependency is not established using a package manager.

Flying under the radar, the respective component cannot be checked or
monitored for any of the other deficiencies.

**Examples:**

1.  Incomplete SBOMs received for upstream components or produced by SCA
    tools
2.  Inclusion of 3rd-party code in a managed (tracked) dependency, e.g.
    - code snippets
    - source code files (copied as-is into the dependency's sources,
      also called "vendored")
    - compiled code (e.g., platform-specific binaries or Java
      archives/class files, also called rebundling)
3.  Dependencies not established through the manifest files of package
    managers like PIP or Maven, e.g. manual or scripted installation
    through brew or apt-get
4.  IDE plugins, build scripts, test dependencies or other developer
    tools, though not included in the dependent software itself, still
    pose security and operational risks

**Actions:**

1.  Evaluate and compare SCA tools regarding their capability to produce
    accurate bills of materials, both at coarse-granular level (e.g.,
    dependencies declared with help of package management tools likes
    Maven or npm) and fine-granular level (e.g., artifacts like single
    files included "out of band", i.e., without using package managers).

**References:**

1.  OWASP Software Component Versification Standard (SCVS) [V1 Inventory
    and V2 Software Bills of
    Materials](https://owasp-scvs.gitbook.io/scvs/v1-inventory)
2.  Research on rebundling
    - Seth Larson: [Patching the libwebp vulnerability across the Python
      ecosystem](https://sethmlarson.dev/security-developer-in-residence-weekly-report-16)
      (2023)
    - J Rack, et al.: [Jack-in-the-box: An Empirical Study of JavaScript
      Bundling on the Web and its Security
      Implications](https://publications.cispa.saarland/4036/1/Bundlers_Study_Submission-camera-ready.pdf)
      (2023)
    - A Dann, et al.: [Identifying Challenges for OSS Vulnerability
      Scanners - A Study & Test
      Suite](https://www.bodden.de/pubs/dph+21identifying.pdf) (2021)
3.  Anand Sawant: [Dependency Resolution in Python: Beware The Phantom
    Dependency](https://www.endorlabs.com/learn/dependency-resolution-in-python-beware-the-phantom-dependency)
    (2023)

------------------------------------------------------------------------

## OSS-RISK-7 : License and Regulatory Risk {#oss-risk-7--license-and-regulatory-risk}

**Description:**

A component or project may not have a license at all, one that is
incompatible with the intended use by a downstream consumer, or one
whose requirements are not or cannot be met by a downstream user.

A component may also violate license terms independent from downstream
use, e.g., if it is licensed as GPL but includes files licensed under
the original (4-clause) BSD license.

A component may also conflict with legal and regulatory requirements,
e.g., related to FedRAMP certification or export control.

It is important to use components in compliance with their license
terms. The absence of a license or non-compliant use can result in
copyright or license infringements, which the copyright holder can take
legal action against.

The violation of legal and regulatory requirements can constrain or
hamper addressing certain verticals or markets.

**Examples:**

1.  [Free Software Foundation, Inc. v. Cisco Systems,
    Inc.](https://www.fsf.org/licensing/complaint-2008-12-11.pdf) (2008)

**Actions:**

1.  Identify acceptable licenses for the intended use of the component
    in the software under development.

    This should consider, for example, how the component is linked, the
    software's deployment model (cloud, on-premise/device) and the
    intended distribution scheme.

2.  Comply with requirements stated in the open source licenses.

3.  Avoid components without license.

4.  Scrutinize component files for multiple and/or incompatible
    licenses.

**References:**

1.  [OSI Approved Licenses](https://opensource.org/licenses/)
2.  [SPDX License List](https://spdx.org/licenses/)
3.  [REUSE](https://reuse.software/)
4.  [Various Licenses and Comments about
    Them](https://www.gnu.org/licenses/license-list.en.html)
5.  [Fossology](https://www.fossology.org/)

------------------------------------------------------------------------

## OSS-RISK-8 : Immature-Software {#oss-risk-8--immature-software}

**Description:**

An open source project may not apply development best-practices, e.g.,
not use a standard versioning scheme, have no regression test suite, no
development or review guidelines or no documentation. As a result, a
component may not work reliably or securely (in the sense of having
security weaknesses that result in exploitable vulnerabilities).

The dependency on an immature component or project comes with
operational risks. The dependent software may not work as expected and
result in runtime reliability issues, or its use may be overly complex
and expensive for the dependent software development organization.

For example, a component or project may lack documentation, may not use
or comply with an established versioning scheme (which can result in
breaking changes during component updates), or may not have a test suite
to discover regressions introduced through pull/merge requests. Such
cases can increase the effort of developers depending on such
components.

**Examples:**

- None

**Actions:**

1.  Check quality indicators and whether a project follows development
    best-practices.

    Example indicators:

    - The project includes test code.
    - Displaying the Code Coverage badge means that the repository is
      using code coverage tools in its development process.
    - The repository includes documentation making it easier to
      understand and use.
    - The repository uses CI and a high fraction of commits pass the CI
      checks which is a sign of good code quality.
    - When a repository contains binary files it is harder to analyze
      and assess its functionality and risks.

2.  A proxy for checking project maturity may also be the number of
    downstream dependents.

**References:**

1.  [OpenSSF Best Practices Badge
    Program](https://www.bestpractices.dev/en)

------------------------------------------------------------------------

## OSS-RISK-9 : Unapproved Change (Mutable) {#oss-risk-9--unapproved-change-mutable}

**Description:**

A component may change without developers being able to notice, review
or approve such changes, e.g., because the download link points to an
unversioned resource, because a versioned resource has been modified or
tampered with or due to an insecure data transfer.

Using components that are not guaranteed to be identical when downloaded
at different points in time are primarily a security risk. Attacks such
as on the Codecov Bash Uploader demonstrate the risk of piping
downloaded scripts directly to bash, without checking their integrity
beforehand. Mutable components also threaten the stability and
reproducibility of software builds.

**Examples:**

1.  References to non-versioned shell scripts in CI/CD pipelines
    - [Codecov bash uploader](https://about.codecov.io/security-update/)
      (2021)
2.  References to Git repositories without commit identifier
3.  Insecure HTTP links to package registries
    - [CVE-2021-26291](https://nvd.nist.gov/vuln/detail/CVE-2021-26291)
      in Apache Maven (2022)

**Actions:**

1.  Use resource identifiers providing guarantees (or at least some
    degree of assurance) to always point to the same, immutable
    artifact.
2.  Verify digests or signatures after component download and before
    installation/use
3.  Use secure protocols for connection/distribution to avoid MITM
    attacks

**References:**

1.  SLSA [Immutable
    Reference](https://slsa.dev/spec/v0.1/requirements#immutable-reference)
2.  [CWE-829: Inclusion of Functionality from Untrusted Control
    Sphere](https://cwe.mitre.org/data/definitions/829.html)
3.  [CWE-830: Inclusion of Web Functionality from an Untrusted
    Source](https://cwe.mitre.org/data/definitions/830.html)
4.  OWASP Top 10:2021 [A08:2021 - Software and Data Integrity
    Failures](../Top10/A08_2021-Software_and_Data_Integrity_Failures/index.html)

------------------------------------------------------------------------

## OSS-RISK-10 : Under/over-sized Dependency {#oss-risk-10--underover-sized-dependency}

**Description:**

A component may provide very little functionality (e.g. npm micro
packages) or a lot of functionality (of which only a fraction may be
used).

Very small components, e.g. ones containing few lines of code only, are
subject to the same supply chain risks as large ones, e.g. account
take-over, malicious pull requests or CI/CD vulnerabilities, for
comparably little functionality. In other words, in exchange for very
few lines of code used, the consumer's security becomes dependent on the
upstream project's security and development posture.

Very large components, on the other hand, may have accumulated many
features that are not needed in standard use-cases, but contribute to
the component's attack surface. Additionally, such unused features may
also bring in additional, unused dependencies (bloated dependencies).

**Examples:**

1.  [Apache Log4j](https://logging.apache.org/log4j/2.x/)

    Included functionality to download and execute arbitrary Java
    classes from remote servers, which eventually led to
    [Log4Shell](https://en.wikipedia.org/wiki/Log4Shell).

2.  [Left-pad](https://www.theregister.com/2016/03/23/npm_left_pad_chaos/)
    (npm, 2016)

    Contained 11 lines of code to pad strings. Its removal from npm
    broke the builds of numerous downstream consumers.

**Actions:**

1.  Become aware of unused component capabilities, esp. if they use
    critical (security sensitive) APIs such as to establish network
    connections.

    Evaluate possibilities to disable unused capabilities, or move to
    smaller alternative open source components with fewer capabilities.

2.  Become aware of micro packages, and consider redeveloping their
    functionality internally.

**References:**

1.  Definition: [Feature
    creep](https://en.wikipedia.org/wiki/Feature_creep)
2.  Tools to uncover the use of security sensitive APIs:
    - Google [Capslock](https://github.com/google/capslock) for Go
    - Microsoft [Application
      Inspector](https://github.com/microsoft/ApplicationInspector) for
      various programming languages
    - Rahman et al.: [Less Is More](https://arxiv.org/pdf/2408.02846): A
      Mixed-Methods Study on Security-Sensitive API Calls in Java for
      Better Dependency Selection
:::
:::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-open-source-software-top-10/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-open-source-software-top-10){.github-button
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

### Top 10 Open Source Software Risks

-  Incubator Project
- Project type: Documentation
- Audience: Builder Defender
- Licensed under [CC BY-SA
  4.0](https://creativecommons.org/licenses/by-sa/4.0/legalcode.en)
- Current version: v0.1

### Social Links

- [Share on
  X](https://twitter.com/intent/tweet?url=https://owasp.org/www-project-open-source-software-top-10/&text=Check%20out%20the%20OWASP%20Top%2010%20for%20Open%20Source%20Software%20project:%20)
- [Share on
  LinkedIn](https://www.linkedin.com/sharing/share-offsite/?url=https://owasp.org/www-project-open-source-software-top-10/)

### Code Repository

- [GitHub](https://github.com/OWASP/www-project-open-source-software-top-10)

### Change Log

- 29 Feb 2024: Released
  [v0.1](https://github.com/OWASP/www-project-open-source-software-top-10/releases/v0.1)

### Leaders

- [Varun
  Badhwar](../cdn-cgi/l/email-protection.html#1f697e6d6a71317d7e7b77687e6d5f70687e6c6f31706d78)
  ([LinkedIn](https://www.linkedin.com/in/vbadhwar/))
- [George
  Apostolopoulos](../cdn-cgi/l/email-protection.html#f196949e839694b1949f959e83df9098)
  ([LinkedIn](https://www.linkedin.com/in/george-apostolopoulos-2336a8/))
- [Henrik
  Plate](../cdn-cgi/l/email-protection.html#cda5a8a3bfa4a6e3bda1acb9a88da2baacbebde3a2bfaa)
  ([LinkedIn](https://www.linkedin.com/in/henrikplate/))

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
