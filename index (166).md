::::::::::::: main-wrapper
# OWASP Coraza Web Application Firewall {#owasp-coraza-web-application-firewall .page-title}

:::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::: {#sec-main .section .page-body}
![logo](assets/images/logo-coraza-mascot.png){height="100vh"
width="auto"}

[![OWASP Production
Project](https://img.shields.io/badge/owasp-production%20project-brightgreen)](index.html)

OWASP Coraza is a golang enterprise-grade Web Application Firewall
framework that supports Modsecurity's seclang language and is 100%
compatible with OWASP Core Ruleset.

Enrich your web application's security with powerful rules that
comprehensively enforce good cybersecurity behavior.

OWASP Coraza can be imported as a library or used with one of our
connectors like
[coraza-server](https://github.com/corazawaf/coraza-server) (GRPC and
SPOA), [coraza-caddy](https://github.com/corazawaf/coraza-caddy) (web
server, reverse proxy), [docker](#) (using connector).

## Try OWASP Coraza

Try OWASP Coraza using [OWASP Core Rule Set
Sandbox](#)https://coreruleset.org/docs/development/sandbox/ or the
[Coraza Playground](https://playground.coraza.io/).

:::: {.language-sh .highlighter-rouge}
::: highlight
``` highlight
curl -H "x-format-output: txt-matched-rules" \
 -H "x-backend: coraza-caddy" \
"https://sandbox.coreruleset.org/?search=<script>alert('CRS+Sandbox+Release')</script>"
```
:::
::::

## Take control of your applications

Control your requests and response before processing by your server or
your customer's browser by submitting the content to our 4 "phase
processors."

![Rule Phases](assets/images/execution_flow.png)

Parse multiple content types, like XML, JSON, Multipart, and urlencoded,
and don't miss anything. Coraza can transform all of this into easily
manageable variables.

Extend OWASP Coraza to achieve anything; our plugin framework allows you
to extend any capability, like operators, actions, directives, body
processors, and audit engines.

Don't miss anything; log everything you need in order to achieve
compliance and complete visibility of your applications.

## Communication channels

- [OWASP Slack](../slack/invite.html) #coraza
- [Github Discussions](https://github.com/corazawaf/coraza/discussions)
- [Monthly
  Meeting](https://github.com/corazawaf/coraza/issues?q=label%3Ameeting+)

## Documentation

We have [extensive documentation](https://coraza.io/) on integration,
directives supported and additional usage patterns.

## Licensing

OWASP Coraza Web Application Firewall is free to use. It is licensed
under the Apache Software License version 2 (ASLv2), so you can copy,
distribute and transmit the work, and you can adapt it and use it
commercially. Still, all provided that you attribute the work and if you
alter, transform, or build upon this work, you may distribute the
resulting work only under the same or similar license to this one.
:::::
::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-coraza-web-application-firewall/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-coraza-web-application-firewall){.github-button
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

### Coraza Web Application Firewall Information

- [OWASP Coraza WAF Website](https://www.coraza.io/)
-  Production Project
-  Defender
-  Code
- [Version
  3.3.3](https://github.com/corazawaf/coraza/releases/tag/v3.3.3)

### Downloads or Social Links

- [Download](https://github.com/corazawaf/coraza)
- [Meetup](#)

### Code Repository

- [GitHub](https://github.com/corazawaf/coraza)

### Change Log

- [See Releases](https://github.com/corazawaf/coraza/releases)

### Leaders

- [Juan Pablo
  Tosso](../cdn-cgi/l/email-protection.html#99f3ecf8f7b7e9f8fbf5f6edf6eaeaf6d9f6eef8eae9b7f6ebfe)
- [Felipe
  Zipitría](../cdn-cgi/l/email-protection.html#8debe8e1e4fde8a3f7e4fde4f9ffe4eccde2faecfefda3e2ffea)
- [José Carlos
  Chávez](../cdn-cgi/l/email-protection.html#dbb1b4a8beb8baa9b7b4a8f5b8b3baadbea19bb4acbaa8abf5b4a9bc)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::
