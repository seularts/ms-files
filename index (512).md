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

[ A04 Insecure Design ]{.md-ellipsis} []{.md-nav__icon .md-icon} [[ A04
Insecure Design ]{.md-ellipsis}](index.html){.md-nav__link
.md-nav__link--active}

[]{.md-nav__icon .md-icon} Table of contents

- [[ Factors ]{.md-ellipsis}](#factors){.md-nav__link}
- [[ Overview ]{.md-ellipsis}](#overview){.md-nav__link}
- [[ Description ]{.md-ellipsis}](#description){.md-nav__link}
  - [[ Requirements and Resource Management
    ]{.md-ellipsis}](#requirements-and-resource-management){.md-nav__link}
  - [[ Secure Design ]{.md-ellipsis}](#secure-design){.md-nav__link}
  - [[ Secure Development Lifecycle
    ]{.md-ellipsis}](#secure-development-lifecycle){.md-nav__link}
- [[ How to Prevent ]{.md-ellipsis}](#how-to-prevent){.md-nav__link}
- [[ Example Attack Scenarios
  ]{.md-ellipsis}](#example-attack-scenarios){.md-nav__link}
- [[ References ]{.md-ellipsis}](#references){.md-nav__link}
- [[ List of Mapped CWEs
  ]{.md-ellipsis}](#list-of-mapped-cwes){.md-nav__link}

[[ A05 Security Misconfiguration
]{.md-ellipsis}](../A05_2021-Security_Misconfiguration/index.html){.md-nav__link}

[[ A06 Vulnerable and Outdated Components
]{.md-ellipsis}](../A06_2021-Vulnerable_and_Outdated_Components/index.html){.md-nav__link}

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
  - [[ Requirements and Resource Management
    ]{.md-ellipsis}](#requirements-and-resource-management){.md-nav__link}
  - [[ Secure Design ]{.md-ellipsis}](#secure-design){.md-nav__link}
  - [[ Secure Development Lifecycle
    ]{.md-ellipsis}](#secure-development-lifecycle){.md-nav__link}
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
# A04:2021 -- Insecure Design ![icon](../assets/TOP_10_Icons_Final_Insecure_Design.png){align="right" style="height:80px;width:80px"} {#a042021-insecure-design}

## Factors

   CWEs Mapped   Max Incidence Rate   Avg Incidence Rate   Avg Weighted Exploit   Avg Weighted Impact   Max Coverage   Avg Coverage   Total Occurrences   Total CVEs
  ------------- -------------------- -------------------- ---------------------- --------------------- -------------- -------------- ------------------- ------------
       40              24.19%               3.00%                  6.46                  6.78              77.25%         42.51%           262,407          2,691

## Overview

A new category for 2021 focuses on risks related to design and
architectural flaws, with a call for more use of threat modeling, secure
design patterns, and reference architectures. As a community we need to
move beyond \"shift-left\" in the coding space to pre-code activities
that are critical for the principles of Secure by Design. Notable Common
Weakness Enumerations (CWEs) include *CWE-209: Generation of Error
Message Containing Sensitive Information*, *CWE-256: Unprotected Storage
of Credentials*, *CWE-501: Trust Boundary Violation*, and *CWE-522:
Insufficiently Protected Credentials*.

## Description

Insecure design is a broad category representing different weaknesses,
expressed as "missing or ineffective control design." Insecure design is
not the source for all other Top 10 risk categories. There is a
difference between insecure design and insecure implementation. We
differentiate between design flaws and implementation defects for a
reason, they have different root causes and remediation. A secure design
can still have implementation defects leading to vulnerabilities that
may be exploited. An insecure design cannot be fixed by a perfect
implementation as by definition, needed security controls were never
created to defend against specific attacks. One of the factors that
contribute to insecure design is the lack of business risk profiling
inherent in the software or system being developed, and thus the failure
to determine what level of security design is required.

### Requirements and Resource Management

Collect and negotiate the business requirements for an application with
the business, including the protection requirements concerning
confidentiality, integrity, availability, and authenticity of all data
assets and the expected business logic. Take into account how exposed
your application will be and if you need segregation of tenants
(additionally to access control). Compile the technical requirements,
including functional and non-functional security requirements. Plan and
negotiate the budget covering all design, build, testing, and operation,
including security activities.

### Secure Design

Secure design is a culture and methodology that constantly evaluates
threats and ensures that code is robustly designed and tested to prevent
known attack methods. Threat modeling should be integrated into
refinement sessions (or similar activities); look for changes in data
flows and access control or other security controls. In the user story
development determine the correct flow and failure states, ensure they
are well understood and agreed upon by responsible and impacted parties.
Analyze assumptions and conditions for expected and failure flows,
ensure they are still accurate and desirable. Determine how to validate
the assumptions and enforce conditions needed for proper behaviors.
Ensure the results are documented in the user story. Learn from mistakes
and offer positive incentives to promote improvements. Secure design is
neither an add-on nor a tool that you can add to software.

### Secure Development Lifecycle

Secure software requires a secure development lifecycle, some form of
secure design pattern, paved road methodology, secured component
library, tooling, and threat modeling. Reach out for your security
specialists at the beginning of a software project throughout the whole
project and maintenance of your software. Consider leveraging the [OWASP
Software Assurance Maturity Model (SAMM)](https://owaspsamm.org/) to
help structure your secure software development efforts.

## How to Prevent

- Establish and use a secure development lifecycle with AppSec
  professionals to help evaluate and design security and privacy-related
  controls

- Establish and use a library of secure design patterns or paved road
  ready to use components

- Use threat modeling for critical authentication, access control,
  business logic, and key flows

- Integrate security language and controls into user stories

- Integrate plausibility checks at each tier of your application (from
  frontend to backend)

- Write unit and integration tests to validate that all critical flows
  are resistant to the threat model. Compile use-cases *and*
  misuse-cases for each tier of your application.

- Segregate tier layers on the system and network layers depending on
  the exposure and protection needs

- Segregate tenants robustly by design throughout all tiers

- Limit resource consumption by user or service

## Example Attack Scenarios

**Scenario #1:** A credential recovery workflow might include "questions
and answers," which is prohibited by NIST 800-63b, the OWASP ASVS, and
the OWASP Top 10. Questions and answers cannot be trusted as evidence of
identity as more than one person can know the answers, which is why they
are prohibited. Such code should be removed and replaced with a more
secure design.

**Scenario #2:** A cinema chain allows group booking discounts and has a
maximum of fifteen attendees before requiring a deposit. Attackers could
threat model this flow and test if they could book six hundred seats and
all cinemas at once in a few requests, causing a massive loss of income.

**Scenario #3:** A retail chain's e-commerce website does not have
protection against bots run by scalpers buying high-end video cards to
resell auction websites. This creates terrible publicity for the video
card makers and retail chain owners and enduring bad blood with
enthusiasts who cannot obtain these cards at any price. Careful anti-bot
design and domain logic rules, such as purchases made within a few
seconds of availability, might identify inauthentic purchases and
rejected such transactions.

## References

- [OWASP Cheat Sheet: Secure Design
  Principles](https://cheatsheetseries.owasp.org/cheatsheets/Secure_Product_Design_Cheat_Sheet.html)

- [OWASP SAMM: Design:Security
  Architecture](https://owaspsamm.org/model/design/security-architecture/)

- [OWASP SAMM: Design:Threat
  Assessment](https://owaspsamm.org/model/design/threat-assessment/)

- [NIST -- Guidelines on Minimum Standards for Developer Verification of
  Software](https://www.nist.gov/publications/guidelines-minimum-standards-developer-verification-software)

- [The Threat Modeling Manifesto](https://threatmodelingmanifesto.org/)

- [Awesome Threat
  Modeling](https://github.com/hysnsec/awesome-threat-modelling)

## List of Mapped CWEs

[CWE-73 External Control of File Name or
Path](https://cwe.mitre.org/data/definitions/73.html)

[CWE-183 Permissive List of Allowed
Inputs](https://cwe.mitre.org/data/definitions/183.html)

[CWE-209 Generation of Error Message Containing Sensitive
Information](https://cwe.mitre.org/data/definitions/209.html)

[CWE-213 Exposure of Sensitive Information Due to Incompatible
Policies](https://cwe.mitre.org/data/definitions/213.html)

[CWE-235 Improper Handling of Extra
Parameters](https://cwe.mitre.org/data/definitions/235.html)

[CWE-256 Unprotected Storage of
Credentials](https://cwe.mitre.org/data/definitions/256.html)

[CWE-257 Storing Passwords in a Recoverable
Format](https://cwe.mitre.org/data/definitions/257.html)

[CWE-266 Incorrect Privilege
Assignment](https://cwe.mitre.org/data/definitions/266.html)

[CWE-269 Improper Privilege
Management](https://cwe.mitre.org/data/definitions/269.html)

[CWE-280 Improper Handling of Insufficient Permissions or
Privileges](https://cwe.mitre.org/data/definitions/280.html)

[CWE-311 Missing Encryption of Sensitive
Data](https://cwe.mitre.org/data/definitions/311.html)

[CWE-312 Cleartext Storage of Sensitive
Information](https://cwe.mitre.org/data/definitions/312.html)

[CWE-313 Cleartext Storage in a File or on
Disk](https://cwe.mitre.org/data/definitions/313.html)

[CWE-316 Cleartext Storage of Sensitive Information in
Memory](https://cwe.mitre.org/data/definitions/316.html)

[CWE-419 Unprotected Primary
Channel](https://cwe.mitre.org/data/definitions/419.html)

[CWE-430 Deployment of Wrong
Handler](https://cwe.mitre.org/data/definitions/430.html)

[CWE-434 Unrestricted Upload of File with Dangerous
Type](https://cwe.mitre.org/data/definitions/434.html)

[CWE-444 Inconsistent Interpretation of HTTP Requests (\'HTTP Request
Smuggling\')](https://cwe.mitre.org/data/definitions/444.html)

[CWE-451 User Interface (UI) Misrepresentation of Critical
Information](https://cwe.mitre.org/data/definitions/451.html)

[CWE-472 External Control of Assumed-Immutable Web
Parameter](https://cwe.mitre.org/data/definitions/472.html)

[CWE-501 Trust Boundary
Violation](https://cwe.mitre.org/data/definitions/501.html)

[CWE-522 Insufficiently Protected
Credentials](https://cwe.mitre.org/data/definitions/522.html)

[CWE-525 Use of Web Browser Cache Containing Sensitive
Information](https://cwe.mitre.org/data/definitions/525.html)

[CWE-539 Use of Persistent Cookies Containing Sensitive
Information](https://cwe.mitre.org/data/definitions/539.html)

[CWE-579 J2EE Bad Practices: Non-serializable Object Stored in
Session](https://cwe.mitre.org/data/definitions/579.html)

[CWE-598 Use of GET Request Method With Sensitive Query
Strings](https://cwe.mitre.org/data/definitions/598.html)

[CWE-602 Client-Side Enforcement of Server-Side
Security](https://cwe.mitre.org/data/definitions/602.html)

[CWE-642 External Control of Critical State
Data](https://cwe.mitre.org/data/definitions/642.html)

[CWE-646 Reliance on File Name or Extension of Externally-Supplied
File](https://cwe.mitre.org/data/definitions/646.html)

[CWE-650 Trusting HTTP Permission Methods on the Server
Side](https://cwe.mitre.org/data/definitions/650.html)

[CWE-653 Insufficient
Compartmentalization](https://cwe.mitre.org/data/definitions/653.html)

[CWE-656 Reliance on Security Through
Obscurity](https://cwe.mitre.org/data/definitions/656.html)

[CWE-657 Violation of Secure Design
Principles](https://cwe.mitre.org/data/definitions/657.html)

[CWE-799 Improper Control of Interaction
Frequency](https://cwe.mitre.org/data/definitions/799.html)

[CWE-807 Reliance on Untrusted Inputs in a Security
Decision](https://cwe.mitre.org/data/definitions/807.html)

[CWE-840 Business Logic
Errors](https://cwe.mitre.org/data/definitions/840.html)

[CWE-841 Improper Enforcement of Behavioral
Workflow](https://cwe.mitre.org/data/definitions/841.html)

[CWE-927 Use of Implicit Intent for Sensitive
Communication](https://cwe.mitre.org/data/definitions/927.html)

[CWE-1021 Improper Restriction of Rendered UI Layers or
Frames](https://cwe.mitre.org/data/definitions/1021.html)

[CWE-1173 Improper Use of Validation
Framework](https://cwe.mitre.org/data/definitions/1173.html)
:::
:::::::::::::
::::::::::::::
