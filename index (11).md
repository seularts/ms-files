::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [FAQ](#div-faq){#faq-link .tab-link role="tab" aria-selected="false"
  aria-controls="faq"}
- [How To Contribute](#div-example){#example-link .tab-link role="tab"
  aria-selected="false" aria-controls="example"}

# OWASP Web Hacking Incident Database {#owasp-web-hacking-incident-database .page-title}

:::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
## OWASP/WASC Web Hacking Incidents Database (WHID) Project

WHID is a project dedicated to maintaining a list of publicly
referenceable web applications related security incidents.

![Mapping](assets/images/whid-logo.jpg)

## Description

WHID's goal is to serve as a tool for raising awareness of the web
application security problem and provide information for statistical
analysis of web applications security incidents. The database is unique
in tracking **only media reported security incidents that can be
associated with a web application security vulnerability**. While the
[OWASP Top Ten](../www-project-top-ten/index.html) focuses on
***vulnerability prevalence*** WHID provides complimentary data the
**types of vulnerabilities that are actively being exploited by threat
actors**.
:::

::: {#sec-faq .section .page-body .tab-hidden}

------------------------------------------------------------------------

## What incidents are included in WHID?

WHID only tracks media reported security incidents that can be
associated with a negative impact to a public web application (such as
downtime, data leakage, planting of malware, etc...). We also try to
limit the database only to targeted attacks, though the distinction
between targeted and non-targeted attacks is grey.

The database does not include known vulnerabilities in web based
applications, an area well covered by other databases such as
[CVE](https://www.cve.org/). WHID does not include incidents in which
web site were breached using operating system or network layer
vulnerabilities.

We also consider most web site defacements as non targeted attacks and
we do not include them in the database. We will, however, include
defacements of high profile websites. For information about web site
defacements refer to [zone-h](https://zone-h.org/archive).

As those criteria are somewhat subjective, we welcome comments on the
inclusion or exclusion of publicized security breaches.

## Were there only few dozen web hacks last year?

The criteria for inclusion into WHID as mentioned above is a bit strict.
The goal is to list only incidents that are related to web application
layer compromises by threat actors. The goal is to show that application
layer security is a risk that cannot be ignored regardless of the
perceived value of the website.

Keep in mind, that while there are countless website hacks, the vast
majority are not reported. Even for those reported most of the time it
is difficult to tell how exactly they occurred (attack methods).

Specifically addressing the defacement incidents reported in zone-h,
bear in mind that in nearly all of these incidents there is no public
information on the way in which they were carried. Additionally, many
defacements are not targeted and are the result of a wide scan for
vulnerable sites and therefore we do not normally include defacements in
WHID.

## Why can't I find a well known incident in WHID?

The reason is probably that the incident did not occur due to a web
application vulnerability, or there was not direct impact (outcome). For
example probably the most well known information security breach ever,
the CardSystems incident was added only in April 2006, nearly a year
after it was initially publicized. While we always suspected that it was
a web hack and industry rumors hinted that, no public information
regarding the way in which the hack was done was available until April
2006. Actually the CardSystems incident was brought in previous versions
of this FAQ as an example of an incident that we would like to add to
WHID but cannot. For other hacks such information is not available and
may not become available in the future.

## How reliable are the incidents reported in WHID?

The data collected is NOT reported directly to OWASP/WASC but is rather
collected from public sources, mostly technical media, mailing list post
and researchers advisories. As a result the reliability of the reported
information depends on the source. Since the source (or sources) is
included with each entry, the reader can assess its reliability
independently. We do however assess the source before including an
incident in the database and if for whatever reason something we added
to the database is found to be erroneous, we remove it, though this has
ever happened to date.

For media reported incidents, we're trusting that the reporter or news
outlet verified the information. For mailing list reported incidents and
research advisories, these issues are normally quickly confirmed our
refuted by other subscribers or by the offended vendor. In case of doubt
evaluate the level of information provided in the disclosure and the
publishing history of the researcher.

## Breach vs. Disclosure {#breach-vs-disclosure}

WHID includes "breaches" but not "disclosures". Breaches are incidents
in which a web site was compromised, while disclosures are incidents in
which a researcher published a vulnerability in a web site. In other
words, breaches are incidents in which we know bad guys took advantage
of a vulnerability, while disclosures are incidents in which whitehat
hackers disclose the vulnerability details. WHID is focused on
compromises by real threat actors.

## The "Unknown" Attack Method

Some of the incident attack methods are classified as "Unknown". You may
wonder why were these incidents included in the list, as there is no way
to know that the hacker exploited a web application vulnerability. In
some cases the public information available indicates that the incident
exploited a web application vulnerability, and in others we deducted
from the available information. This important inclusion criteria for
WHID is a negative impact to a web application or its data. Attack
Method and Application Weakness may be listed as Unknown if those
details are not available.
:::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## How can I contribute?

You can help make WHID better. You don't need to invest a lot of time:

- If you encounter a new Web incident, use the [WHID Submittal
  Form](https://docs.google.com/forms/d/e/1FAIpQLSdRxE1DqOsgKf_nMNwtb2vY3EBRKsBgc0-sBzVdj5zud0HwEQ/viewform?embedded=true&formkey=dHktV0FmWGMyTDZPbkZtOEJXNzhPbXc6MQ&pli=1)
- As we speak English we miss alot in non English speaking countries so
  we are especially looking for non English sources. As long as they can
  be translated using Google translate of a similar service, we can
  include it.
- If you want to contribute more, become a WHID editor. Send an e-mail
  to the project leaders with a few words (and preferably a link) about
  yourself and sign up to this site. We will activate your account and
  enable you to edit incidents. We need you to: add past incidents.
:::
::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-web-hacking-incident-database/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-web-hacking-incident-database){.github-button
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

### Web Hacking Incident Database Information

- [Incubator Project](#)
- [Type of Project](#)
- [Documentation]{style="font-size:1.0em;padding-left:12px;"}
- [Builder]{style="font-size:1.0em;padding-left:12px;"}
- [Defender]{style="font-size:1.0em;padding-left:12px;"}

### Downloads

- [Download](https://docs.google.com/spreadsheets/d/1xZPAw1uCdLqDz8F_Vz57DRvCNJTcCnPgtG7P-yeloUc/edit?usp=sharing)

### Social

- [Twitter](https://twitter.com/OWASPWHID)

### Code Repository

- [repo](https://github.com/OWASP/owasp-whid)

### Change Log

- [changes](#)

### Leaders

- [Ryan
  Barnett](../cdn-cgi/l/email-protection.html#eb99928a85c5898a99858e9f9fab849c8a989bc584998c)
- [4ng3l
  hacker](../cdn-cgi/l/email-protection.html#596d373e6a3531383a323c2b193e34383035773a3634)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::
