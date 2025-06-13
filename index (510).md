:::::::::::::: {.md-main role="main" md-component="main"}
::::::::::::: {.md-main__inner .md-grid}
:::::::: {.md-sidebar .md-sidebar--primary md-component="sidebar" md-type="navigation"}
::::::: md-sidebar__scrollwrap
:::::: md-sidebar__inner
[![logo](../assets/OWASP_Logo_Transp.png)](../index.html "OWASP Top 10:2021"){.md-nav__button
.md-logo aria-label="OWASP Top 10:2021" md-component="logo"} OWASP Top
10:2021

::::: md-nav__source
[](https://github.com/OWASP/Top10 "Go to repository"){.md-source
md-component="source"}

::: {.md-source__icon .md-icon}
![](data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdib3g9IjAgMCA0NDggNTEyIj48IS0tISBGb250IEF3ZXNvbWUgRnJlZSA2LjUuMSBieSBAZm9udGF3ZXNvbWUgLSBodHRwczovL2ZvbnRhd2Vzb21lLmNvbSBMaWNlbnNlIC0gaHR0cHM6Ly9mb250YXdlc29tZS5jb20vbGljZW5zZS9mcmVlIChJY29uczogQ0MgQlkgNC4wLCBGb250czogU0lMIE9GTCAxLjEsIENvZGU6IE1JVCBMaWNlbnNlKSBDb3B5cmlnaHQgMjAyMyBGb250aWNvbnMsIEluYy4tLT48cGF0aCBkPSJNNDM5LjU1IDIzNi4wNSAyNDQgNDAuNDVhMjguODcgMjguODcgMCAwIDAtNDAuODEgMGwtNDAuNjYgNDAuNjMgNTEuNTIgNTEuNTJjMjcuMDYtOS4xNCA1Mi42OCAxNi43NyA0My4zOSA0My42OGw0OS42NiA0OS42NmMzNC4yMy0xMS44IDYxLjE4IDMxIDM1LjQ3IDU2LjY5LTI2LjQ5IDI2LjQ5LTcwLjIxLTIuODctNTYtMzcuMzRMMjQwLjIyIDE5OXYxMjEuODVjMjUuMyAxMi41NCAyMi4yNiA0MS44NSA5LjA4IDU1YTM0LjM0IDM0LjM0IDAgMCAxLTQ4LjU1IDBjLTE3LjU3LTE3LjYtMTEuMDctNDYuOTEgMTEuMjUtNTZ2LTEyM2MtMjAuOC04LjUxLTI0LjYtMzAuNzQtMTguNjQtNDVMMTQyLjU3IDEwMSA4LjQ1IDIzNS4xNGEyOC44NiAyOC44NiAwIDAgMCAwIDQwLjgxbDE5NS42MSAxOTUuNmEyOC44NiAyOC44NiAwIDAgMCA0MC44IDBsMTk0LjY5LTE5NC42OWEyOC44NiAyOC44NiAwIDAgMCAwLTQwLjgxeiIgLz48L3N2Zz4=)
:::

::: md-source__repository
OWASP/Top10
:::
:::::

[[ Home ]{.md-ellipsis}](../index.html){.md-nav__link}

[[ Notice ]{.md-ellipsis}](../0x00-notice/index.html){.md-nav__link}

[[ Introduction
]{.md-ellipsis}](../A00_2021_Introduction/index.html){.md-nav__link}

[[ How to use the OWASP Top 10 as a standard
]{.md-ellipsis}](../A00_2021_How_to_use_the_OWASP_Top_10_as_a_standard/index.html){.md-nav__link}

[[ How to start an AppSec program with the OWASP Top 10
]{.md-ellipsis}](../A00_2021-How_to_start_an_AppSec_program_with_the_OWASP_Top_10/index.html){.md-nav__link}

[[ About OWASP
]{.md-ellipsis}](../A00-about-owasp/index.html){.md-nav__link}

[ Top 10:2021 List ]{.md-ellipsis} []{.md-nav__icon .md-icon}

[]{.md-nav__icon .md-icon} Top 10:2021 List

[[ A01 Broken Access Control
]{.md-ellipsis}](../A01_2021-Broken_Access_Control/index.html){.md-nav__link}

[[ A02 Cryptographic Failures
]{.md-ellipsis}](../A02_2021-Cryptographic_Failures/index.html){.md-nav__link}

[[ A03 Injection
]{.md-ellipsis}](../A03_2021-Injection/index.html){.md-nav__link}

[[ A04 Insecure Design
]{.md-ellipsis}](../A04_2021-Insecure_Design/index.html){.md-nav__link}

[[ A05 Security Misconfiguration
]{.md-ellipsis}](../A05_2021-Security_Misconfiguration/index.html){.md-nav__link}

[ A06 Vulnerable and Outdated Components ]{.md-ellipsis}
[]{.md-nav__icon .md-icon} [[ A06 Vulnerable and Outdated Components
]{.md-ellipsis}](index.html){.md-nav__link .md-nav__link--active}

[]{.md-nav__icon .md-icon} Table of contents

- [[ Factors ]{.md-ellipsis}](#factors){.md-nav__link}
- [[ Overview ]{.md-ellipsis}](#overview){.md-nav__link}
- [[ Description ]{.md-ellipsis}](#description){.md-nav__link}
- [[ How to Prevent ]{.md-ellipsis}](#how-to-prevent){.md-nav__link}
- [[ Example Attack Scenarios
  ]{.md-ellipsis}](#example-attack-scenarios){.md-nav__link}
- [[ References ]{.md-ellipsis}](#references){.md-nav__link}
- [[ List of Mapped CWEs
  ]{.md-ellipsis}](#list-of-mapped-cwes){.md-nav__link}

[[ A07 Identification and Authentication Failures
]{.md-ellipsis}](../A07_2021-Identification_and_Authentication_Failures/index.html){.md-nav__link}

[[ A08 Software and Data Integrity Failures
]{.md-ellipsis}](../A08_2021-Software_and_Data_Integrity_Failures/index.html){.md-nav__link}

[[ A09 Security Logging and Monitoring Failures
]{.md-ellipsis}](../A09_2021-Security_Logging_and_Monitoring_Failures/index.html){.md-nav__link}

[[ A10 Server Side Request Forgery (SSRF)
]{.md-ellipsis}](../A10_2021-Server-Side_Request_Forgery_(SSRF)/index.html){.md-nav__link}

[[ Next Steps
]{.md-ellipsis}](../A11_2021-Next_Steps/index.html){.md-nav__link}
::::::
:::::::
::::::::

::::: {.md-sidebar .md-sidebar--secondary md-component="sidebar" md-type="toc"}
:::: md-sidebar__scrollwrap
::: md-sidebar__inner
[]{.md-nav__icon .md-icon} Table of contents

- [[ Factors ]{.md-ellipsis}](#factors){.md-nav__link}
- [[ Overview ]{.md-ellipsis}](#overview){.md-nav__link}
- [[ Description ]{.md-ellipsis}](#description){.md-nav__link}
- [[ How to Prevent ]{.md-ellipsis}](#how-to-prevent){.md-nav__link}
- [[ Example Attack Scenarios
  ]{.md-ellipsis}](#example-attack-scenarios){.md-nav__link}
- [[ References ]{.md-ellipsis}](#references){.md-nav__link}
- [[ List of Mapped CWEs
  ]{.md-ellipsis}](#list-of-mapped-cwes){.md-nav__link}
:::
::::
:::::

::: {.md-content md-component="content"}
# A06:2021 -- Vulnerable and Outdated Components ![icon](../assets/TOP_10_Icons_Final_Vulnerable_Outdated_Components.png){align="right" style="height:80px;width:80px"} {#a062021-vulnerable-and-outdated-components}

## Factors

   CWEs Mapped   Max Incidence Rate   Avg Incidence Rate   Max Coverage   Avg Coverage   Avg Weighted Exploit   Avg Weighted Impact   Total Occurrences   Total CVEs
  ------------- -------------------- -------------------- -------------- -------------- ---------------------- --------------------- ------------------- ------------
        3              27.96%               8.77%             51.78%         22.47%              5.00                  5.00                30,457             0

## Overview

It was #2 from the Top 10 community survey but also had enough data to
make the Top 10 via data. Vulnerable Components are a known issue that
we struggle to test and assess risk and is the only category to not have
any Common Vulnerability and Exposures (CVEs) mapped to the included
CWEs, so a default exploits/impact weight of 5.0 is used. Notable CWEs
included are *CWE-1104: Use of Unmaintained Third-Party Components* and
the two CWEs from Top 10 2013 and 2017.

## Description

You are likely vulnerable:

- If you do not know the versions of all components you use (both
  client-side and server-side). This includes components you directly
  use as well as nested dependencies.

- If the software is vulnerable, unsupported, or out of date. This
  includes the OS, web/application server, database management system
  (DBMS), applications, APIs and all components, runtime environments,
  and libraries.

- If you do not scan for vulnerabilities regularly and subscribe to
  security bulletins related to the components you use.

- If you do not fix or upgrade the underlying platform, frameworks, and
  dependencies in a risk-based, timely fashion. This commonly happens in
  environments when patching is a monthly or quarterly task under change
  control, leaving organizations open to days or months of unnecessary
  exposure to fixed vulnerabilities.

- If software developers do not test the compatibility of updated,
  upgraded, or patched libraries.

- If you do not secure the components' configurations (see
  [A05:2021-Security
  Misconfiguration](../A05_2021-Security_Misconfiguration/index.html)).

## How to Prevent

There should be a patch management process in place to:

- Remove unused dependencies, unnecessary features, components, files,
  and documentation.

- Continuously inventory the versions of both client-side and
  server-side components (e.g., frameworks, libraries) and their
  dependencies using tools like versions, OWASP Dependency Check,
  retire.js, etc. Continuously monitor sources like Common Vulnerability
  and Exposures (CVE) and National Vulnerability Database (NVD) for
  vulnerabilities in the components. Use software composition analysis
  tools to automate the process. Subscribe to email alerts for security
  vulnerabilities related to components you use.

- Only obtain components from official sources over secure links. Prefer
  signed packages to reduce the chance of including a modified,
  malicious component (See A08:2021-Software and Data Integrity
  Failures).

- Monitor for libraries and components that are unmaintained or do not
  create security patches for older versions. If patching is not
  possible, consider deploying a virtual patch to monitor, detect, or
  protect against the discovered issue.

Every organization must ensure an ongoing plan for monitoring, triaging,
and applying updates or configuration changes for the lifetime of the
application or portfolio.

## Example Attack Scenarios

**Scenario #1:** Components typically run with the same privileges as
the application itself, so flaws in any component can result in serious
impact. Such flaws can be accidental (e.g., coding error) or intentional
(e.g., a backdoor in a component). Some example exploitable component
vulnerabilities discovered are:

- CVE-2017-5638, a Struts 2 remote code execution vulnerability that
  enables the execution of arbitrary code on the server, has been blamed
  for significant breaches.

- While the internet of things (IoT) is frequently difficult or
  impossible to patch, the importance of patching them can be great
  (e.g., biomedical devices).

There are automated tools to help attackers find unpatched or
misconfigured systems. For example, the Shodan IoT search engine can
help you find devices that still suffer from Heartbleed vulnerability
patched in April 2014.

## References

- [OWASP Application Security Verification Standard: V1 Architecture,
  design and threat
  modelling](../../www-project-application-security-verification-standard/index.html)

- [OWASP Dependency Check (for Java and .NET
  libraries)](../../www-project-dependency-check/index.html)

- [OWASP Testing Guide - Map Application Architecture
  (OTG-INFO-010)](../../www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/01-Information_Gathering/10-Map_Application_Architecture.html)

- [OWASP Virtual Patching Best
  Practices](../../www-community/Virtual_Patching_Best_Practices.html)

- [The Unfortunate Reality of Insecure
  Libraries](https://cdn2.hubspot.net/hub/203759/file-1100864196-pdf/docs/Contrast_-_Insecure_Libraries_2014.pdf)

- [MITRE Common Vulnerabilities and Exposures (CVE)
  search](https://www.cvedetails.com/version-search.php)

- [National Vulnerability Database (NVD)](https://nvd.nist.gov/)

- [Retire.js for detecting known vulnerable JavaScript
  libraries](https://github.com/retirejs/retire.js/)

- [GitHub Advisory Database](https://github.com/advisories)

- [Ruby Libraries Security Advisory Database and
  Tools](https://rubysec.com/)

- [SAFECode Software Integrity Controls
  \[PDF\]](https://safecode.org/publication/SAFECode_Software_Integrity_Controls0610.pdf)

## List of Mapped CWEs

[CWE-937 OWASP Top 10 2013: Using Components with Known
Vulnerabilities](https://cwe.mitre.org/data/definitions/937.html)

[CWE-1035 2017 Top 10 A9: Using Components with Known
Vulnerabilities](https://cwe.mitre.org/data/definitions/1035.html)

[CWE-1104 Use of Unmaintained Third Party
Components](https://cwe.mitre.org/data/definitions/1104.html)
:::
:::::::::::::
::::::::::::::
