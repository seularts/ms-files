::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Acknowledgments](#div-acknowledgments){#acknowledgments-link
  .tab-link role="tab" aria-selected="false"
  aria-controls="acknowledgments"}
- [Join](#div-join){#join-link .tab-link role="tab"
  aria-selected="false" aria-controls="join"}
- [News](#div-news){#news-link .tab-link role="tab"
  aria-selected="false" aria-controls="news"}
- [RoadMap](#div-roadmap){#roadmap-link .tab-link role="tab"
  aria-selected="false" aria-controls="roadmap"}
- [Translations](#div-translations){#translations-link .tab-link
  role="tab" aria-selected="false" aria-controls="translations"}

# OWASP API Security Project {#owasp-api-security-project .page-title}

:::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
:::: {#sec-main .section .page-body}
::: alert
Check out the new [OWASP API Security Top 10
2023](../API-Security/editions/2023/en/0x00-header/index.html) !
:::

## What is API Security?

A foundational element of innovation in today's app-driven world is the
API. From banks, retail and transportation to IoT, autonomous vehicles
and smart cities, APIs are a critical part of modern mobile, SaaS and
web applications and can be found in customer-facing, partner-facing and
internal applications. By nature, APIs expose application logic and
sensitive data such as Personally Identifiable Information (PII) and
because of this have increasingly become a target for attackers. Without
secure APIs, rapid innovation would be impossible.

API Security focuses on strategies and solutions to understand and
mitigate the unique vulnerabilities and security risks of Application
Programming Interfaces (APIs).

## API Security Top 10 2023

Here is a sneak peek of the 2023 version:

- **[API1:2023 - Broken Object Level
  Authorization](../API-Security/editions/2023/en/0xa1-broken-object-level-authorization/index.html)**

  APIs tend to expose endpoints that handle object identifiers, creating
  a wide attack surface of Object Level Access Control issues. Object
  level authorization checks should be considered in every function that
  accesses a data source using an ID from the user. [Continue
  reading](../API-Security/editions/2023/en/0xa1-broken-object-level-authorization/index.html).

- **[API2:2023 - Broken
  Authentication](../API-Security/editions/2023/en/0xa2-broken-authentication/index.html)**

  Authentication mechanisms are often implemented incorrectly, allowing
  attackers to compromise authentication tokens or to exploit
  implementation flaws to assume other user's identities temporarily or
  permanently. Compromising a system's ability to identify the
  client/user, compromises API security overall. [Continue
  reading](../API-Security/editions/2023/en/0xa2-broken-authentication/index.html).

- **[API3:2023 - Broken Object Property Level
  Authorization](../API-Security/editions/2023/en/0xa3-broken-object-property-level-authorization/index.html)**

  This category combines [API3:2019 Excessive Data
  Exposure](../API-Security/editions/2019/en/0xa3-excessive-data-exposure/index.html)
  and [API6:2019 - Mass
  Assignment](../API-Security/editions/2019/en/0xa6-mass-assignment/index.html),
  focusing on the root cause: the lack of or improper authorization
  validation at the object property level. This leads to information
  exposure or manipulation by unauthorized parties. [Continue
  reading](../API-Security/editions/2023/en/0xa3-broken-object-property-level-authorization/index.html).

- **[API4:2023 - Unrestricted Resource
  Consumption](../API-Security/editions/2023/en/0xa4-unrestricted-resource-consumption/index.html)**

  Satisfying API requests requires resources such as network bandwidth,
  CPU, memory, and storage. Other resources such as emails/SMS/phone
  calls or biometrics validation are made available by service providers
  via API integrations, and paid for per request. Successful attacks can
  lead to Denial of Service or an increase of operational costs.
  [Continue
  reading](../API-Security/editions/2023/en/0xa4-unrestricted-resource-consumption/index.html).

- **[API5:2023 - Broken Function Level
  Authorization](../API-Security/editions/2023/en/0xa5-broken-function-level-authorization/index.html)**

  Complex access control policies with different hierarchies, groups,
  and roles, and an unclear separation between administrative and
  regular functions, tend to lead to authorization flaws. By exploiting
  these issues, attackers can gain access to other users' resources
  and/or administrative functions. [Continue
  reading](../API-Security/editions/2023/en/0xa5-broken-function-level-authorization/index.html).

- **[API6:2023 - Unrestricted Access to Sensitive Business
  Flows](../API-Security/editions/2023/en/0xa6-unrestricted-access-to-sensitive-business-flows/index.html)**

  APIs vulnerable to this risk expose a business flow - such as buying a
  ticket, or posting a comment - without compensating for how the
  functionality could harm the business if used excessively in an
  automated manner. This doesn't necessarily come from implementation
  bugs. [Continue
  reading](../API-Security/editions/2023/en/0xa6-unrestricted-access-to-sensitive-business-flows/index.html).

- **[API7:2023 - Server Side Request
  Forgery](../API-Security/editions/2023/en/0xa7-server-side-request-forgery/index.html)**

  Server-Side Request Forgery (SSRF) flaws can occur when an API is
  fetching a remote resource without validating the user-supplied URI.
  This enables an attacker to coerce the application to send a crafted
  request to an unexpected destination, even when protected by a
  firewall or a VPN. [Continue
  reading](../API-Security/editions/2023/en/0xa7-server-side-request-forgery/index.html).

- **[API8:2023 - Security
  Misconfiguration](../API-Security/editions/2023/en/0xa8-security-misconfiguration/index.html)**

  APIs and the systems supporting them typically contain complex
  configurations, meant to make the APIs more customizable. Software and
  DevOps engineers can miss these configurations, or don't follow
  security best practices when it comes to configuration, opening the
  door for different types of attacks. [Continue
  reading](../API-Security/editions/2023/en/0xa8-security-misconfiguration/index.html).

- **[API9:2023 - Improper Inventory
  Management](../API-Security/editions/2023/en/0xa9-improper-inventory-management/index.html)**

  APIs tend to expose more endpoints than traditional web applications,
  making proper and updated documentation highly important. A proper
  inventory of hosts and deployed API versions also are important to
  mitigate issues such as deprecated API versions and exposed debug
  endpoints. [Continue
  reading](../API-Security/editions/2023/en/0xa9-improper-inventory-management/index.html).

- **[API10:2023 - Unsafe Consumption of
  APIs](../API-Security/editions/2023/en/0xaa-unsafe-consumption-of-apis/index.html)**

  Developers tend to trust data received from third-party APIs more than
  user input, and so tend to adopt weaker security standards. In order
  to compromise APIs, attackers go after integrated third-party services
  instead of trying to compromise the target API directly. [Continue
  reading](../API-Security/editions/2023/en/0xaa-unsafe-consumption-of-apis/index.html).

## Licensing

**The OWASP API Security Project documents are free to use!**

The OWASP API Security Project is licensed under the [Creative Commons
Attribution-ShareAlike 4.0
license](https://creativecommons.org/licenses/by-sa/4.0/), so you can
copy, distribute and transmit the work, and you can adapt it, and use it
commercially, but all provided that you attribute the work and if you
alter, transform, or build upon this work, you may distribute the
resulting work only under the same or similar license to this one.
::::

::: {#sec-acknowledgments .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Founders

- [Erez Yalon](https://www.owasp.org/index.php/User:ErezYalon)
- [Inon Shkedy](https://www.owasp.org/index.php/User:Inon)

## Leaders

- [Erez Yalon](https://www.owasp.org/index.php/User:ErezYalon)
- [Inon Shkedy](https://www.owasp.org/index.php/User:Inon)
- [Paulo Silva](https://www.owasp.org/index.php/User:PauloASilva)

## 2023 Sponsors {#2023-sponsors}

![Cequence
Security](assets/images/sponsors/cequence-security.png){height="96px"}

![Checkmarx](assets/images/sponsors/checkmarx.png){height="96px"}

![Equixly](assets/images/sponsors/equixly.png){height="96px"}

![Impart Security](assets/images/sponsors/impart.png){height="96px"}

![Salt Security](assets/images/sponsors/salt.png){height="96px"}

![Traceable](assets/images/sponsors/traceable.png){height="96px"}

## 2023 Contributors {#2023-contributors}

247arjun, abunuwas, Alissa Knight, Arik Atar, aymenfurter, Corey J.
Ball, cyn8, d0znpp, Dan Gordon, donge, Dor Tumarkin, faizzaidi, gavjl,
guybensimhon, Inês Martins, Isabelle Mauny, Ivan Novikov, jmanico, Juan
Pablo, k7jto, LaurentCB, llegaz, Maxim Zavodchik, MrPRogers,
planetlevel, rahulk22, Roey Eliyahu, Roshan Piyush, securitylevelup,
sudeshgadewar123, Tatsuya-hasegawa, tebbers, vanderaj, wenz, xplo1t-sec,
Yaniv Balmas, ynvb

## 2019 Contributors {#2019-contributors}

007divyachawla, Abid Khan, Adam Fisher, anotherik, bkimminich,
caseysoftware, Chris Westphal, dsopas, DSotnikov, emilva, ErezYalon,
flascelles, Guillaume Benats, IgorSasovets, Inonshk, JonnySchnittger,
jmanico, jmdx, Keith Casey, kozmic, LauraRosePorter, Matthieu Estrade,
nathanawmk, PauloASilva, pentagramz, philippederyck, pleothaud, r00ter,
Raj kumar, Sagar Popat, Stephen Gates, thomaskonrad, xycloops123,
Raphael Hagi, Eduardo Bellis, Bruno Barbosa
:::

::: {#sec-join .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Google Group

Join the discussion on the [OWASP API Security Project Google
group](https://groups.google.com/a/owasp.org/d/forum/api-security-project).

This is the best place to introduce yourself, ask questions, suggest and
discuss any topic that is relevant to the project.

## GitHub Discussions

You can also use [GitHub
Discussions](https://github.com/OWASP/API-Security/discussions) as a
place to connect with other community members, asking questions or
sharing ideas.

## GitHub

The project is maintained in the [OWASP API Security Project
repo](https://github.com/OWASP/API-Security).

**The latest changes are under the [`develop`{.language-plaintext
.highlighter-rouge}
branch](https://github.com/OWASP/API-Security/tree/develop)**.

Feel free to open or solve an
[issue](https://github.com/OWASP/API-Security/issues).

Ready to contribute directly into the repo? Great! Just make sure you
read the [How to Contribute
guide](https://github.com/OWASP/API-Security/blob/master/CONTRIBUTING.md).
:::

::: {#sec-news .section .page-body .tab-hidden}

------------------------------------------------------------------------

- **Jun 28th, 2024**

  OWASP API Security Project - Past Present and Future @ OWASP Global
  AppSec Lisbon 2024
  ([YouTube](https://www.youtube.com/watch?v=hn4mgTu5izg))

- **Jun 3rd, 2024**

  [OWASP API Security Top 10 2023 French
  translation](../API-Security/editions/2023/fr/0x00-header/index.html)
  release.

- **Jun 5th, 2023**

  [OWASP API Security Top 10
  2023](../API-Security/editions/2023/en/0x00-header/index.html) stable
  version was publicly released.

- **Feb 14, 2023**

  [OWASP API Security Top 10 2023 Release
  Candidate](announcements/2023/02/api-top10-2023rc.html) is now
  available.

- **Aug 30, 2022**

  [OWASP API Security Top 10 2022 call for
  data](announcements/cfd/2022/index.html) is open.

- **Oct 30, 2020**

  [GraphQL Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/GraphQL_Cheat_Sheet.html)
  release. A truly community effort whose [log and contributors list are
  available at
  GitHub](https://github.com/OWASP/CheatSheetSeries/pull/434).

- **Apr 4, 2020**

  [OWASP API Security Top 10 2019 pt-PT
  translation](https://github.com/OWASP/API-Security/raw/master/2019/pt-pt/dist/owasp-api-security-top-10.pdf)
  release.

- **Mar 27, 2020**

  [OWASP API Security Top 10 2019 pt-BR
  translation](https://github.com/OWASP/API-Security/raw/master/2019/pt-br/dist/owasp-api-security-top-10-pt-br.pdf)
  release.

- **Dec 26, 2019**

  OWASP API Security Top 10 2019 stable version release.

- **Sep 30, 2019**

  The RC of API Security Top-10 List was published during [OWASP Global
  AppSec Amsterdam](https://ams.globalappsec.org/) ([slide
  deck](https://github.com/OWASP/www-project-api-security/raw/master/assets/presentations/api-security-top10-rc-global-appsec-ams.pdf))

- **Sep 13, 2019**

  The RC of API Security Top-10 List was published during [OWASP Global
  AppSec DC](https://dc.globalappsec.org/) ([slide
  deck](https://github.com/OWASP/www-project-api-security/raw/master/assets/presentations/api-security-top10.pdf))

- **May 30, 2019**

  The API Security Project was Kicked-Off during [OWASP Global AppSec
  Tel Aviv](https://telaviv.appsecglobal.org/) ([slide
  deck](https://github.com/OWASP/www-project-api-security/raw/master/assets/presentations/owasp-api-security-project-kick-off.pdf))
:::

::: {#sec-roadmap .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Planned Projects

- API Security Top 10
- API Security Cheat Sheet
- crAPI - **C**ompletely **R**idiculous **API**, an intentionally
  vulnerable API project)

## Roadmap

![Roadmap](assets/images/roadmap.png)
:::

::: {#sec-translations .section .page-body .tab-hidden}

------------------------------------------------------------------------

## OWASP API Security Top 10 2023

- [Bahasa
  (Indonesian)](../API-Security/editions/2023/id/0x00-header/index.html)

  [Faiz Ahmed Zaidi](https://github.com/faizzaidi)

- [French](../API-Security/editions/2023/fr/0x00-header/index.html)

  [Aurélien
  Troncy](https://www.linkedin.com/in/aurélien-troncy-214075229/),
  [Laurent Legaz](https://github.com/llegaz)

- [Persian](../API-Security/editions/2023/fa/0x00-header/index.html)

  [Alireza
  Mostame](https://www.linkedin.com/in/alireza-mostame-29970b242),
  [Maryam Javadi
  Hoseini](https://www.linkedin.com/in/maryam-javadi-353b1744/),
  [Mohammad Reza Ismaeli Taba](https://www.linkedin.com/in/rezataba),
  [RNPG](https://www.linkedin.com/company/raspina-net-pars/){rel="nofollow"}

- [Português
  (Portugal)](../API-Security/editions/2023/pt-pt/0x00-header/index.html)

  [Rui Silva](https://www.linkedin.com/in/rspro/)

## OWASP API Security Top 10 2019

- [Arabic](../API-Security/editions/2019/ar/0x00-header/index.html)
  (also available in
  [PDF](../API-Security/editions/2019/ar/dist/owasp-api-security-top-10-ar.pdf),
  [ODT](../API-Security/editions/2019/ar/dist/owasp-api-security-top-10-ar.odt))

  [Malek Aldossary](https://twitter.com/malajab), [Sabri
  Hassanyah](https://twitter.com/kingsabri), [Mostafa
  Alaqsm](https://twitter.com/malaqsm), [Fahad
  Alduraibi](https://twitter.com/fahad_alduraibi), [Thamer
  Alshammeri](https://twitter.com/t44t_), [Mohammed
  Alsuhaymi](https://twitter.com/msuhaymi)

- [French](../API-Security/editions/2019/fr/0x00-header/index.html)
  (also available in
  [PDF](../API-Security/editions/2019/fr/dist/owasp-api-security-top-10.pdf),
  [ODT](../API-Security/editions/2019/fr/dist/owasp-api-security-top-10.odt))

  [Fred](https://github.com/datakime), [Laurent
  Legaz](https://github.com/llegaz)

- [German](../API-Security/editions/2019/de/0x00-header/index.html)
  (also available in
  [PDF](../API-Security/editions/2019/de/dist/owasp-api-security-top-10.pdf),
  [ODT](../API-Security/editions/2019/de/dist/owasp-api-security-top-10.odt))

  [Moritz Gruber](https://www.linkedin.com/in/moritz-gruber-734a43199/),
  [Nick Lorenz](https://www.linkedin.com/in/nick-lorenz-16b211222/),
  [Steffen Thamm](https://www.linkedin.com/in/steffen-thamm-a8341a27b/),
  [Tim B.](https://www.linkedin.com/in/domai-tb/)

- [Greek](../API-Security/editions/2019/el-gr/0x00-header/index.html)
  ([PDF](../API-Security/editions/2019/el-gr/dist/owasp-api-security-top-10.pdf),
  [ODT](../API-Security/editions/2019/el-gr/dist/owasp-api-security-top-10.odt))

  [Athanasios Emmanouilidis](https://www.linkedin.com/in/athanasiosem/),
  [Apostolos
  Giannakidis](https://www.linkedin.com/in/giannakidisapostolos/)

- [Persian](../API-Security/editions/2019/fa/0x00-header/index.html)
  (also available in
  [PDF](../API-Security/editions/2019/fa/dist/owasp-api-security-top-10.pdf),
  [ODT](../API-Security/editions/2019/fa/dist/owasp-api-security-top-10.odt))

  [Alireza
  Mostame](https://www.linkedin.com/in/alireza-mostame-29970b242),
  [Mohammad Reza Ismaeli Taba](https://www.linkedin.com/in/rezataba),
  [Amirmahdi
  Nowbakht](https://www.linkedin.com/in/amirmahdi-nowbakht-3b8865200),
  [RNPG](https://www.linkedin.com/company/raspina-net-pars/){rel="nofollow"}

- [Portuguese
  (Brazil)](../API-Security/editions/2019/pt-BR/0x00-header/index.html)
  (also available in
  [PDF](../API-Security/editions/2019/pt-BR/dist/owasp-api-security-top-10-pt-br.pdf),
  [ODT](../API-Security/editions/2019/pt-BR/dist/owasp-api-security-top-10-pt-br.odt))

  [Raphael Hagi](https://www.linkedin.com/in/raphael-hagi/), [Eduardo
  Bellis](https://www.linkedin.com/in/eduardo-bellis-92482534/), [Bruno
  Barbosa](https://www.linkedin.com/in/bbarbosa85/)

- [Portuguese
  (Portugal)](../API-Security/editions/2019/pt-pt/0x00-header/index.html)
  (also available in
  [PDF](../API-Security/editions/2019/pt-pt/dist/owasp-api-security-top-10.pdf),
  [ODT](../API-Security/editions/2019/pt-pt/dist/owasp-api-security-top-10.odt))

  [Paulo A. Silva](https://www.linkedin.com/in/devpauloasilva/), [Rui
  Silva](https://www.linkedin.com/in/rspro/)

- [Russian](../API-Security/editions/2019/ru/0x00-header/index.html)
  (also available in
  [PDF](../API-Security/editions/2019/ru/dist/owasp-api-security-top-10.pdf),
  [ODT](../API-Security/editions/2019/ru/dist/owasp-api-security-top-10.odt))

  [Eugene Rojavski](https://twitter.com/eugenerojavski),
  [act1on3](https://twitter.com/act1on3), keni0k
:::
::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/OWASP/API-Security/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/OWASP/API-Security){.github-button
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

### API Security Information

[ ]{.fa-stack .fa-2x title="Production Project"} ![Documentation
Project](https://raw.githubusercontent.com/OWASP/www--site-theme/master/assets/images/common/owasp_documentation_project.svg?sanitize=true)

Builders Breakers Defenders

[![CC BY-SA
4.0](assets/images/by-sa.svg){width="175px"}](http://creativecommons.org/licenses/by-sa/4.0/)

### Downloads or Social Links

- [API Security Top 10
  2023](../API-Security/editions/2023/en/0x00-header/index.html)
- [API Security Top 10
  2019](../API-Security/editions/2019/en/0x00-header/index.html)
  ([PDF](../API-Security/editions/2019/en/dist/owasp-api-security-top-10.pdf))
- [GraphQL Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/GraphQL_Cheat_Sheet.html)
- [GitHub
  Discussions](https://github.com/OWASP/API-Security/discussions)
- [Mailing
  List](https://groups.google.com/a/owasp.org/d/forum/api-security-project)

### Code Repository

- [GitHub](https://github.com/OWASP/API-Security)

### Leaders {#leaders}

- [Erez
  Yalon](../cdn-cgi/l/email-protection.html#0a6f786f7024736b6665644a657d6b797a2465786d)
- [Inon
  Shkedy](../cdn-cgi/l/email-protection.html#a0c9cecfce8ed3c8cbc5c4d9e0cfd7c1d3d08ecfd2c7)
- [Paulo
  Silva](../cdn-cgi/l/email-protection.html#abdbcadec7c485d8c2c7ddcaebc4dccad8db85c4d9cc)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::
