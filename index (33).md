:::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Related Top 10
  Projects](#div-related_projects){#related_projects-link .tab-link
  role="tab" aria-selected="false" aria-controls="related_projects"}

# OWASP Top 10 Client-Side Security Risks {#owasp-top-10-client-side-security-risks .page-title}

::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
## OWASP Top 10 Client-Side Security Risks {#owasp-top-10-client-side-security-risks}

Browser side applications are frequently a complex combination of custom
HTML, CSS, and JavaScript, leveraging numerous third-party libraries
that are both served by the custom application, and frequently
integrated with third-party services that supply their own custom code
and libraries into the same client-side application. All this runs in
the customer's browser in the wild, rather than on application owner
controlled, managed, and secured servers. Browser applications
frequently interact with numerous servers, not just the original server
hosting the server application and serving the core elements of the
client-side JavaScript application to the user's browser.

This results in numerous risks for client-side code that are very
different from the server-side applications. Therefore, the security of
the client-side web application code requires a dedicated Top 10. This
is similar to the [OWASP Mobile Top
10](../www-project-mobile-top-10/index.html) which is a dedicated Top 10
for mobile apps. Mobile apps are frequently the client-side of a web
app, where the server-side of the web app provides REST services to the
mobile app.

This project will focus on identifying and organizing a prioritized set
of security risks for client-side browser code (e.g., JavaScript, Web
Assembly, etc.).

## Candidate Top 10 Client-Side Security Risks

The current team has pulled together the following Candidates for the
OWASP Top 10 Client-side Security Risks. After a suitable comment period
on this list, we'll produce a complete draft Top 10 later in 2022 for
another round of comments. Like other OWASP Top 10s, we plan to produce
PDF, Wiki and/or GitBook versions of the final document so it can be
consumed in the format most helpful to the reader.

The following is the candidate list (subject to change based on feedback
of course):

**1. Broken Client-side Access Control**

Insufficient control of JavaScript access to client-side assets (data
and code), exfiltration of sensitive data, or manipulation of the DOM
for malicious purposes (to access those assets). Just like [OWASP Top
10: A01-2021 - Broken Access
Control](../Top10/A01_2021-Broken_Access_Control/index.html), but
focused on client-side code.

**2. [DOM-based XSS](../www-community/attacks/DOM_Based_XSS.html)**

Vulnerabilities that permit XSS attacks through DOM manipulation or
abuse.

**3. Sensitive Data Leakage**

Inability to detect/prevent digital trackers and pixels across a web
property to ensure national and international privacy laws are complied
with.

**4. Vulnerable and Outdated Components**

Lack of detection and updates to JavaScript libraries that are outdated
or contain known vulnerabilities. Just like [OWASP Top 10: A06-2021 -
Vulnerable and Outdated
Components](../Top10/A06_2021-Vulnerable_and_Outdated_Components/index.html),
but focused on client-side libraries.

**5. Lack of Third-party Origin Control**

Origin control allows the restriction of certain web assets or resources
by comparing the origin of the resource to the origin of the third-party
library. Without leveraging such controls, supply chain risk increases
due to inclusion of unknown or uncontrolled third-party code that has
access to data in the site's origin.

**6. JavaScript Drift**

Inability to detect changes at the asset and code level of JavaScript
used client-side. This includes the inability to detect behavioral
changes of this code to determine if the changes are potentially
malicious in nature. This is particularly important for third-party
libraries.

**7. Sensitive Data Stored Client-Side**

Storage of sensitive data like passwords, crypto secrets, API tokens, or
PII data in persistent client-side storage like LocalStorage, browser
cache, or transient storage like JavaScript variables in a data layer.

**8. Client-side Security Logging and Monitoring Failures**

Insufficient monitoring and detection of client-side changes and data
accesses, particularly failures and errors, in real-time as each page is
assembled and executed using both first-party and third-party code. Just
like [OWASP Top 10: A09-2021 - Security Logging and Monitoring
Failures](../Top10/A09_2021-Security_Logging_and_Monitoring_Failures/index.html),
but focused on client-side behavior.

**9. Not Using Standard Browser Security Controls**

Not using common standards-based security controls built into browsers
such as iframe sandboxes, and security headers like Content Security
Policy (CSP), subresource integrity, and many other standard security
features.

**10. Including Proprietary Information on the Client-Side**

Presence of sensitive business logic, developer comments, proprietary
algorithms, or system information contained in client-side code or
stored data.

## Providing Feedback

The best way to provide feedback is to join our Google Group listed to
the right, and then post feedback to the project. Or you can simply
email directly to the project leaders if you prefer to provide feedback
privately.
:::

::: {#sec-related_projects .section .page-body .tab-hidden}

------------------------------------------------------------------------

# OWASP Top 10 Projects

The Top 10 Client Side Security Risks Project is one of many
interrelated Top 10 projects at OWASP.

The other OWASP Top 10 projects that we are aware of are:

- [THE OWASP Top 10](../www-project-top-ten/index.html)
- [OWASP Serverless Top 10](../www-project-serverless-top-10/index.html)
- [OWASP Mobile Top 10](../www-project-mobile-top-10/index.html)
- [OWASP Top 10 Privacy
  Risks](../www-project-top-10-privacy-risks/index.html)
- [OWASP API Security Top 10](../www-project-api-security/index.html)
- [OWASP Docker Top 10](../www-project-docker-top-10/index.html)
:::
:::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-top-10-client-side-security-risks/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-top-10-client-side-security-risks){.github-button
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

-  Incubator Project

### Project Type

- [Documentation]{style="font-size:1.0em;padding-left:12px;"}

### Audience

- [Builder]{style="font-size:1.0em;padding-left:12px;"}
- [Defender]{style="font-size:1.0em;padding-left:12px;"}

### Community

- [Google
  Group](https://groups.google.com/a/owasp.org/forum/#!forum/top10-client-side-security-risks)

### Licensing

This document will be licensed under the [Creative Commons
Attribution-ShareAlike 4.0
license](https://creativecommons.org/licenses/by-sa/4.0/), so you can
copy, distribute and transmit the work, and you can adapt it, and use it
commercially, provided that you attribute the work and if you alter,
transform, or build upon this work, you may distribute the resulting
work only under the same or a similar license to this one.

### Leaders

- [Ivan
  Tsarynny](../cdn-cgi/l/email-protection.html#dcb5aabdb29cbab9aeb3b3a8f2bfb3b1)
  (Project Coleader)
- [Lavakumar
  Kuppan](../cdn-cgi/l/email-protection.html#761a170017360514190e045815191b)
  (Project Coleader)
- [Dave
  Wichers](../cdn-cgi/l/email-protection.html#3e5a5f485b1049575d565b4c4d7e51495f4d4e10514c59)
  (Contributor)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::
