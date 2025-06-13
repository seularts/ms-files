:::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Scope and Definitions](#div-scope){#scope-link .tab-link role="tab"
  aria-selected="false" aria-controls="scope"}
- [Use Case Scenarios](#div-usecases){#usecases-link .tab-link
  role="tab" aria-selected="false" aria-controls="usecases"}
- [Ontology](#div-ontology){#ontology-link .tab-link role="tab"
  aria-selected="false" aria-controls="ontology"}
- [Bibliography](#div-bibliography){#bibliography-link .tab-link
  role="tab" aria-selected="false" aria-controls="bibliography"}
- [FAQs](#div-faqs){#faqs-link .tab-link role="tab"
  aria-selected="false" aria-controls="faqs"}
- [Acknowledgements and
  Sponsors](#div-acknowledgements){#acknowledgements-link .tab-link
  role="tab" aria-selected="false" aria-controls="acknowledgements"}
- [Road Map and Getting Involved](#div-roadmap){#roadmap-link .tab-link
  role="tab" aria-selected="false" aria-controls="roadmap"}

# OWASP Automated Threats to Web Applications {#owasp-automated-threats-to-web-applications .page-title}

::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
[![OWASP
Lab](https://img.shields.io/badge/owasp-lab%20project-yellow.svg)](../projects/index.html)

![OWASP automated threats mind
amp](assets/images/automated-threats-header.jpg)

The OWASP Automated Threats to Web Applications Project completed a
review of reports, academic and other papers, news stories and
vulnerability taxonomies/listings to identify, name and classify these
scenarios -- automated by software causing a divergence from accepted
behavior producing one or more undesirable effects on a web application,
but excluding tool-based exploitation of single-issue vulnerabilities.
The initial objective was to produce an ontology providing a common
language for developers, architects, operators, business owners,
security engineers, purchasers and suppliers/ vendors, to facilitate
clear communication and help tackle the issues. The project also
identifies symptoms, mitigations and controls in this problem area. The
project team monitor changes and possibel additions to keep the handbook
updated. Like all OWASP outputs, everything is free and published using
an open source license.

## Description

Web applications are subjected to unwanted automated usage -- day in,
day out. Often these events relate to misuse of inherent valid
functionality, rather than the attempted exploitation of unmitigated
vulnerabilities. Also, excessive misuse is commonly mistakenly reported
as application denial-of-service (DoS) like HTTP-flooding, when in fact
the DoS is a side-effect instead of the primary intent. Frequently these
have sector-specific names. Most of these problems seen regularly by web
application owners are not listed in any OWASP Top Ten or other top
issue list. Furthermore, they are not enumerated or defined adequately
in existing dictionaries. These factors have contributed to inadequate
visibility, and an inconsistency in naming such threats, with a
consequent lack of clarity in attempts to address the issues.

Without sharing a common language between devops, architects, business
owners, security engineers, purchasers and suppliers/vendors, everyone
has to make extra effort to communicate clearly. Misunderstandings can
be costly. The adverse impacts affect the privacy and security of
individuals as well as the security of the applications and related
system components.

## Automated Threats

The list of threat events, defined more fully in the [OWASP Automated
Threat
Handbook](https://github.com/OWASP/www-project-automated-threats-to-web-applications/tree/master/assets/files/EN),
is alphabetically:

- [OAT-020 Account
  Aggregation](assets/oats/EN/OAT-020_Account_Aggregation.html)
- [OAT-019 Account
  Creation](assets/oats/EN/OAT-019_Account_Creation.html)
- [OAT-003 Ad Fraud](assets/oats/EN/OAT-003_Ad_Fraud.html)
- [OAT-009 CAPTCHA Defeat](assets/oats/EN/OAT-009_CAPTCHA_Defeat.html)
- [OAT-010 Card Cracking](assets/oats/EN/OAT-010_Card_Cracking.html)
- [OAT-001 Carding](assets/oats/EN/OAT-001_Carding.html)
- [OAT-012 Cashing Out](assets/oats/EN/OAT-012_Cashing_Out.html)
- [OAT-007 Credential
  Cracking](assets/oats/EN/OAT-007_Credential_Cracking.html)
- [OAT-008 Credential
  Stuffing](assets/oats/EN/OAT-008_Credential_Stuffing.html)
- [OAT-021 Denial of
  Inventory](assets/oats/EN/OAT-021_Denial_of_Inventory.html)
- [OAT-015 Denial of
  Service](assets/oats/EN/OAT-015_Denial_of_Service.html)
- [OAT-006 Expediting](assets/oats/EN/OAT-006_Expediting.html)
- [OAT-004 Fingerprinting](assets/oats/EN/OAT-004_Fingerprinting.html)
- [OAT-018 Footprinting](assets/oats/EN/OAT-018_Footprinting.html)
- [OAT-005 Scalping](assets/oats/EN/OAT-005_Scalping.html)
- [OAT-011 Scraping](assets/oats/EN/OAT-011_Scraping.html)
- [OAT-016 Skewing](assets/oats/EN/OAT-016_Skewing.html)
- [OAT-013 Sniping](assets/oats/EN/OAT-013_Sniping.html)
- [OAT-017 Spamming](assets/oats/EN/OAT-017_Spamming.html)
- [OAT-002 Token Cracking](assets/oats/EN/OAT-002_Token_Cracking.html)
- [OAT-014 Vulnerability
  Scanning](assets/oats/EN/OAT-014_Vulnerability_Scanning.html)

Not sure which is which? Use the [threat identification
chart](assets/files/oat-ontology-decision-chart.pdf) in conjunction with
the [full
handbook](https://github.com/OWASP/www-project-automated-threats-to-web-applications/tree/master/assets/files/EN).

## Licensing

All the materials are free to use. They are licensed under the [Creative
Commons Attribution-ShareAlike 3.0
license](http://creativecommons.org/licenses/by-sa/3.0/), so you can
copy, distribute and transmit the work, and you can adapt it, and use it
commercially, but all provided that you attribute the work and if you
alter, transform, or build upon this work, you may distribute the
resulting work only under the same or similar license to this one.

© OWASP Foundation
:::

::: {#sec-scope .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Scope and Definitions

### Scope

The aim was to create a listing of vendor-neutral and technology
agnostic terms that describe real-world automated threats to web
applications, at a level of abstraction that application owners can
relate to. These terms are threat events to web applications undertaken
using automated actions.

The focus is on abuse of functionality - misuse of inherent
functionality and related design flaws, some of which are also referred
to as business logic flaws. There is almost no focus on implementation
bugs. It is not that the latter are not the target for attacks, but
there is much more knowledge published in that area with a greater
agreement on terminology. All the scenarios identified must require the
web to exist for the threat to be materialised. Many of the scenarios
have impacts upon the organisation that owns or operates web
applications, but some scenarios have impacts more focused on
individuals or other bodies. An attack that can be achieved without the
web is out of scope.

### Definitions

#### Automated Threats to Web Applications

Threat events to web applications undertaken using automated actions.

An attack that can be achieved without the web is out of scope.

### Glossary

#### Action

An act taken against an asset by a threat agent. Requires first that
contact occurs between the asset and threat agent (Ref 1)

#### Application

Software that performs a business process i.e. not system software

A software program hosted by an information system (Ref 2)

#### Application layer

"Layer 7" in the OSI model (Ref 3) and "application layer" in the TCP/IP
model (Ref 4)

#### Threat

Anything that is capable of acting in a manner resulting in harm to an
asset and/or organization; for example, acts of God (weather, geological
events, etc.); malicious actors; errors; failures (Ref 1)

#### Threat Agent

Any agent (e.g., object, substance, human, etc.) that is capable of
acting against an asset in a manner that can result in harm (Ref 1)

#### Threat Event

Occurs when a threat agent acts against an asset (Ref 1)

#### Web

The World Wide Web (WWW, or simply Web) is an information space in which
the items of interest, referred to as resources, are identified by
global identifiers called Uniform Resource Identifiers (URI) (Ref 5)

The first three specifications for Web technologies defined URLs, HTTP,
and HTML (Ref 6)

#### Web application

An application delivered over the web

\
\

Glossary references:

1.  [Risk Taxonomy, Technical Standard, The Open Group,
    2009](http://pubs.opengroup.org/onlinepubs/9699919899/toc.pdf)
2.  [NISTIR 7298 rev 2,
    NIST](http://nvlpubs.nist.gov/nistpubs/ir/2013/NIST.IR.7298r2.pdf)
3.  [OSI model, Wikipedia](https://en.wikipedia.org/wiki/OSI_model)
4.  [TCP/IP model,
    Wikipedia](https://en.wikipedia.org/wiki/Internet_protocol_suite)
5.  [Architecture of the World Wide Web, Volume One,
    W3C](http://www.w3.org/TR/webarch/)
6.  [Help and FAQ, W3C](http://www.w3.org/Help/)
:::

::: {#sec-usecases .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Use Case Scenarios

The following scenarios and organisation names are completely
fictitious.

### Defining application development security requirements

Cinnaminta SpA intends to build and launch a new multi-lingual and
multi-currency ecommerce website. The development will be outsourced and
Cinnaminta has been working on the functional design document. Among
many other requirements, the application security specification requires
that the website must not include any vulnerabilities identified in PCI
DSS v3.1 Requirement 6.5, nor any other vulnerabilities that could
affect the protection of payment cardholder data. Cinnaminta specifies
that the website's payment functions must not be susceptible to the
threat events **OAT-001 Carding** or **OAT-010 Card Cracking** as
defined in the **OWASP Automated Threat Handbook**. In addition, the
application must interact with the company's existing fraud detection
system to counter **OAT-012 Cashing Out**. The requirements are
specified in terms of these threat events, rather than particular
product or service categories. Development houses responding to the call
for bids use the ontology to focus their answers to these aspects
appropriately.

### Sharing intelligence within a sector

Unlimited Innovations Inc develops and supports patient-facing software
solutions to a range of healthcare providers, many of which participate
in the National Health Service Cyber Intelligence Sharing Center
(NHS-CISC). Unlimited Innovations already builds continuous monitoring
capabilities into its software and decides to provide an optional
enhancement so that customers could choose to share their misuse event
data with each other, to benefit from the combined threat intelligence.
Rather than sharing large quantities of low-level data, Unlimited
Innovations aggregates information and broadcasts validated and
categorised threat data amongst the participating organisations.
Automation attacks are classified according to the threat events defined
in the **OWASP Automated Threat Handbook** so that each receiving party
understands the nature of the threat. Even organisations that do not
want to take part in this information sharing can benefit, since their
own categorised information is made available to internal business
management in the form of an easy-to-comprehend monitoring dashboard.
The information gathered can also be fed into their other business
information management systems to help improve patient service.

### Exchanging threat data between CERTs

National Computer Emergency Response Teams (CERTs) recognise that
sharing of local information can contribute to worldwide prevention of
cyber attacks. Despite advances in cooperation between CERTs, anything
to increase continuity and interoperability, such as standards for data
exchange, is encouraged. CERT Zog is concerned about the sparsity of
application-specific data it receives, and also the classification of
that data. It has a particular concern about attacks and breaches that
affect sectors defined in Zog's 2015 national cyber security strategy.
CERT Zog and its neighbour CERT Tarset agree to tag threat events using
the **OWASP Automated Threat Handbook** in order to add greater context
to existing solutions being used for threat data exchange between them.
The programme also collects sector metadata, so that all organisations
within these can benefit from the centralised intelligence.

### Enhancing application penetration test findings

Specialist application security penetration testing firm Cherak
Industries Pte Ltd works primarily for financial services companies in
the banking and insurance sectors, and is looking to expand its business
throughout Asia. Cherak has some innovative pen test result reporting
systems which integrate with client software fault and vulnerability
tracking systems, and it actively looks for methods to provide
additional value to its clients. Cherak has identified that pen test
clients would benefit from help to in understanding the effects of
combinations of vulnerabilities, especially design flaws, and has
decided to utilise the **OWASP Automated Threat Handbook** to define and
explain the automation-related threats. The individual vulnerabilities
were scored as normal using CVSSv2 and v3, the matching CWEs identified,
and mitigations in place documented. In addition, Cherak uses the threat
events defined in the **OWASP Automated Threat Handbook** to help create
a new section in the executive summary that explains how combinations of
the issues found could lead to automation threats and the possible
technical and business impacts. For example, an assessment for one
client had identified weaknesses in authentication so that there is a
risk of **OAT-008 Credential Stuffing**. The defined identifier was
provided to the client, so its technical staff could refer to additional
information on the OWASP website.

### Specifying service acquisition needs

Falstone Paradise Inc is concerned about malicious use of their
portfolio of hotel and resort websites. The majority of the websites use
a shared application platform, but there are some unique applications
and a large number of other micro-sites, some of which use generic
content management systems such as Wordpress and Drupal. Falstone
Paradise has identified that its IT operations team are spending too
much time dealing with the effects of automated misuse, such as cleaning
up data, resetting customer accounts and providing extra capacity during
attacks. Furthermore, the unwanted automation is also causing some
instabilities leading to negative feedback from customers. Therefore
Falstone Paradise decides to go out to the security marketplace to
identify, assess and select products or services that might help address
these automation issues for all its websites. Their buying team works
with their information technology colleagues to write the detailed
requirements in an Invitation to Tender (ITT) document. This describes
the types of attacks its web applications are receiving, their frequency
of occurrence and their magnitudes. These are defined according to the
**OWASP Automated Threat Handbook**, so that vendors do not
misunderstand the requirements, and each vendor's offering can be
assessed against the particular automation threat events of concern.

### Characterising vendor services

Better Best Ltd has developed an innovative technology to help gaming
companies defend against a range of automated threats that can otherwise
permit cheating and distortion of the game, leading to disruption for
normal players. The solution can be deployed on premises, but is also
available in the cloud as a service. But Better Best is finding
difficulty explaining its solution in the market place, especially since
it does not fit into any conventional product category. Better Best
decide to use the terminology and threat events listed in the **OWASP
Automated Threat Handbook** to define their product's capabilities. They
hope this will provide some clarity about their offering, and also
demonstrate how their product can be used to replace more than one other
conventional security device. Additionally, Better Best writes a white
paper describing how their product has been successfully used by one of
their reference customers Hollybush Challenge Games to protect against
**OAT-006 Expediting**, **OAT-005 Scalping**, **OAT-016 Skewing** and
**OAT-013 Sniping**.
:::

::: {#sec-ontology .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Ontology

### Introduction

The A-Z list of automated threat events and summary descriptions,
defined in full in the [OWASP Automated Threat
Handbook](https://github.com/OWASP/www-project-automated-threats-to-web-applications/tree/master/assets/files/EN),
is:

  Identifier                                                      OAT Name                 Summary Defining Characteristics
  --------------------------------------------------------------- ------------------------ ---------------------------------------------------------------------------------------------------------------------------
  [OAT-020](assets/oats/EN/OAT-020_Account_Aggregation.html)      Account Aggregation      Use by an intermediary application that collects together multiple accounts and interacts on their behalf
  [OAT-019](assets/oats/EN/OAT-019_Account_Creation.html)         Account Creation         Create multiple accounts for subsequent misuse
  [OAT-003](assets/oats/EN/OAT-003_Ad_Fraud.html)                 Ad Fraud                 False clicks and fraudulent display of web-placed advertisements
  [OAT-009](assets/oats/EN/OAT-009_CAPTCHA_Defeat.html)           CAPTCHA Defeat           Solve anti-automation tests
  [OAT-010](assets/oats/EN/OAT-010_Card_Cracking.html)            Card Cracking            Identify missing start/expiry dates and security codes for stolen payment card data by trying different values
  [OAT-001](assets/oats/EN/OAT-001_Carding.html)                  Carding                  Multiple payment authorisation attempts used to verify the validity of bulk stolen payment card data
  [OAT-012](assets/oats/EN/OAT-012_Cashing_Out.html)              Cashing Out              Buy goods or obtain cash utilising validated stolen payment card or other user account data
  [OAT-007](assets/oats/EN/OAT-007_Credential_Cracking.html)      Credential Cracking      Identify valid login credentials by trying different values for usernames and/or passwords
  [OAT-008](assets/oats/EN/OAT-008_Credential_Stuffing.html)      Credential Stuffing      Mass log in attempts used to verify the validity of stolen username/password pairs
  [OAT-021](assets/oats/EN/OAT-021_Denial_of_Inventory.html)      Denial of Inventory      Deplete goods or services stock without ever completing the purchase or committing to the transaction
  [OAT-015](assets/oats/EN/OAT-015_Denial_of_Service.html)        Denial of Service        Target resources of the application and database servers, or individual user accounts, to achieve denial of service (DoS)
  [OAT-006](assets/oats/EN/OAT-006_Expediting.html)               Expediting               Perform actions to hasten progress of usually slow, tedious or time-consuming actions
  [OAT-004](assets/oats/EN/OAT-004_Fingerprinting.html)           Fingerprinting           Elicit information about the supporting software and framework types and versions
  [OAT-018](assets/oats/EN/OAT-018_Footprinting.html)             Footprinting             Probe and explore application to identify its constituents and properties
  [OAT-005](assets/oats/EN/OAT-005_Scalping.html)                 Scalping                 Obtain limited-availability and/or preferred goods/services by unfair methods
  [OAT-011](assets/oats/EN/OAT-011_Scraping.html)                 Scraping                 Collect application content and/or other data for use elsewhere
  [OAT-016](assets/oats/EN/OAT-016_Skewing.html)                  Skewing                  Repeated link clicks, page requests or form submissions intended to alter some metric
  [OAT-013](assets/oats/EN/OAT-013_Sniping.html)                  Sniping                  Last minute bid or offer for goods or services
  [OAT-017](assets/oats/EN/OAT-017_Spamming.html)                 Spamming                 Malicious or questionable information addition that appears in public or private content, databases or user messages
  [OAT-002](assets/oats/EN/OAT-002_Token_Cracking.html)           Token Cracking           Mass enumeration of coupon numbers, voucher codes, discount tokens, etc
  [OAT-014](assets/oats/EN/OAT-014_Vulnerability_Scanning.html)   Vulnerability Scanning   Crawl and fuzz application to identify weaknesses and possible vulnerabilities
                                                                                            

### Comparison with other dictionaries, taxonomies and lists

#### [Common Attack Pattern Enumeration and Classification](https://capec.mitre.org/) (CAPEC)

![Venn diagram showing OWASP Autoamted Threats (OATs) fromCAPEC point of
view](assets/images/Ontology-chart-capec-wiki.png)

CAPEC is a dictionary and classification taxonomy of known attacks on
software. Its primary classification structures are:

- [Domains of
  attack](https://capec.mitre.org/data/definitions/3000.html) (3000) -
  Social Engineering (403), [Supply
  Chain](https://capec.mitre.org/data/definitions/437.html) (437),
  Communications (512),
  [Software](https://capec.mitre.org/data/definitions/513.html) (513),
  Physical Security (514), Hardware (515)
- Mechanism of Attack (1000) - Gather Information (118), Deplete
  Resources (119), Injection (152), Deceptive Interactions (156),
  Manipulate Timing and State (172), Abuse of Functionality (210),
  Probabilistic Techniques (223), Exploitation of Authentication (225),
  Exploitation of Authorization (232), Manipulate Data Structures (255),
  Manipulate Resources (262), Analyze Target (281), Gain Physical Access
  (436), Malicious Code Execution (525), Alter System Components (526),
  Manipulate System Users (527)

#### [WASC Threat Classification](http://projects.webappsec.org/w/page/13246978/Threat%20Classification)

![Venn diagram showing OWASP Autoamted Threats (OATs) from WASC point of
view](assets/images/Ontology-chart-wasc-wiki.png)

The WASC Threat Classification classifies weaknesses and attacks that
can lead to the compromise of a website, its data, or its users.

#### [OWASP WASC Web Hacking Incidents Database Project](https://wiki.owasp.org/index.php/OWASP_WASC_Web_Hacking_Incidents_Database_Project) (WHID)

WHID classifies publicly known incidents using:

- attack methods e.g. ARP spoofing, abuse of functionality, account
  compromise, administration error, automation, backdoor, banking
  trojan, brute force, clickjacking, code injection, content injection,
  content spoofing, credential/session prediction, cross site request
  forgery (CSRF), cross-site scripting (XSS), denial of service,
  directory traversal, domain hijacking, DNS hijacking, forceful
  browsing, HTTP response splitting, hidden parameter manipulation,
  hosting malicious code, information leakage, insufficient
  authentication, known vulnerability, local file inclusion (LFI),
  malvertising, malware, malware injection, mass assignment,
  misconfiguration, OS commanding, parameter manipulation, path
  traversal, phishing, predictable resource location, process
  automation, redirection, remote file inclusion (RFI), rogue 3rd party
  app, scaping, search engine poisoning, shell injection, social
  engineering, stolen credentials, SQL injection, unintentional
  information disclosure, weak password recovery validation, worm
- weakness e.g. abuse of functionality, application misconfiguration,
  directory indexing, improper filesystem permissions, improper input
  handling, improper output handling, information leakage, insecure
  indexing, insufficient anti-automation, insufficient authentication,
  insufficient authorization, insufficient entropy, insufficient
  password recovery, insufficient process validation, insufficient
  session expiration, insufficient transport layer protection,
  misconfiguration, predictable resource location, weak password
- outcome e.g. account hijacking, account takeover, botnet
  participation, chaos, credit card leakage, data loss, defacement, DDoS
  attacks, DNS hijacking, DNS redirection, disinformation, disclosure
  only, downtime, extortion, fraud, information warfare, leakage of
  information, link spam, loss of sales, malware distribution, monetary
  loss, phishing, planting of malware, service disruption, session
  hijacking, spam, spam links, stolen credentials, worm Plus
  other/various/unknown.
:::

::: {#sec-bibliography .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Bibliography

The following academic, open source, commercial and news sources were
used in the research on automated threats to web applications. OWASP is
a worldwide not-for-profit charitable organization focused on improving
the security of software. We operate under a vendor neutral policy and
we do not endorse products or services.

- 10 years of Application Security, Denyall
  http://www.denyall.com/resources/whitepapers/?aliId=3438442
- 2012 Payment Card Threat Report
  https://www.securitymetrics.com/static/resources/orange/2012%20Payment%20Card%20Threat%20Report%20copy.pdf
- 2014 Bot Traffic Report: Just the Droids You were Looking for
  http://www.incapsula.com/blog/bot-traffic-report-2014.html
- 3 Types of 'Return Fraud' to Monitor this Holiday Season
  http://www.practicalecommerce.com/articles/3168-3-Types-of-%E2%80%98Return-Fraud-to-Monitor-this-Holiday-Season
- 7 Ways Bots Hurt Your Website, Distil Networks
  http://www.distilnetworks.com/7-ways-bots-hurt-website-whitepaper/
- Abusing HTML 5 Structured Client-side Storage 2008
  http://packetstorm.wowhacker.com/papers/general/html5whitepaper.pdf
- Acquiring Experience with Ontology and Vocabularies, Walt Melo, Risa
  Mayan and Jean Stanford, 2011
  http://www.omg.org/news/meetings/workshops/SOA-HC/presentations-2011/13_SC-6_Melo_Stanford_Mayan.pdf
- An Anatomy of a SQL Injection Attack Hacker Intelligence Initiative
  Imperva
  http://www.imperva.com/docs/HII_An_Anatomy_of_a_SQL_Injection_Attack_SQLi.pdf
- The Anatomy of Clickbot.A
  https://www.usenix.org/legacy/event/hotbots07/tech/full_papers/daswani/daswani.pdf
- Anatomy of comment spam Hacker Intelligence Initiative Imperva
  http://www.imperva.com/docs/HII_Anatomy_of_Comment_Spam.pdf
- Anti-Automation Monitoring and Prevention 2015
  https://www.clerkendweller.uk/2015/1/29/AntiAutomation-Monitoring-and-Prevention
- Anti-DDoS Solution for Internet Corporation
  http://www.nsfocus.com/uploadfile/Solution/NSFOCUS%20Anti-DDoS%20Solution%20for%20Internet%20Corporation.pdf
- Anti-Fraud Principles and Proposed Taxonomy Sep 2014
  http://www.iab.net/media/file/IAB_Anti_Fraud_Principles_and_Taxonomy.pdf
- Apache Security Ivan Ristic
- Application Security Desk Reference, OWASP
  https://www.owasp.org/index.php/Category:OWASP_ASDR_Project
- Application Security Guide For CISOs, OWASP, 2013
  https://www.owasp.org/index.php/File:Owasp-ciso-guide.pdf
- AppSensor, OWASP
  https://www.owasp.org/index.php/OWASP_AppSensor_Project
- Attack & Defense Labs http://www.andlabs.org/html5.html
- Attack categories OWASP
  https://www.owasp.org/index.php/Category:Attack
- Attack Trees, Schneier, Dr. Dobb's Journal, December 1999
  https://www.schneier.com/paper-attacktrees-ddj-ft.html
- Attacking with HTML5 2010
  https://media.blackhat.com/bh-ad-10/Kuppan/Blackhat-AD-2010-Kuppan-Attacking-with-HTML5-wp.pdf
- Automated attacks Hacker Intelligence Initiative Imperva
  http://www.imperva.com/docs/HII_Automation_of_Attacks.pdf
- Avoiding the Top 10 Software Security Design Flaws
  http://cybersecurity.ieee.org/images/files/images/pdf/CybersecurityInitiative-online.pdf
- Bad Bots On The Rise Dec 2014
  http://www.darkreading.com/informationweek-home/bad-bots-on-the-rise/d/d-id/1318276
- Banking Botnets Persist Despite Takedowns, Dell SecureWorks, 2015
  http://www.secureworks.com/cyber-threat-intelligence/threats/banking-botnets-persist-despite-takedowns/
- The Barracuda Web Application Firewall: XML Firewall
  https://www.barracuda.com/assets/docs/White_Papers/Barracuda_Web_Application_Firewall_WP_XML_Firewall.pdf
- Blocking Brute Force Attacks
  http://www.cs.virginia.edu/\~csadmin/gen_support/brute_force.php
- Bot Traffic Growing Problem for Digital Oct 2014
  http://www.netnewscheck.com/article/36537/bot-traffic-growing-problem-for-digital
- BotoPedia Incapsula http://www.botopedia.org/
- Boy in the Browser Imperva
  http://www.imperva.com/DefenseCenter/ThreatAdvisories/Boy_in_the_Browser
- Business Logic Attacks - Bots and BATs, Eldad Chai, 2009
  http://www.owasp.org/images/9/96/AppSecEU09_BusinessLogicAttacks_EldadChai.ppt
- Bypassing Client Application Protection Techniques
  http://www.securiteam.com/securityreviews/6S0030ABPE.html
- A CAPTCHA in the Rye Hacker Intelligence Initiative Imperva
  http://www.imperva.com/docs/HII_a_CAPTCHA_in_the_Rye.pdf
- Characterizing Large Scale Click fraud
  http://cseweb.ucsd.edu/\~voelker/pubs/za-ccs14.pdf
- Charter Addition Proposal: "Trusted Code" for the Web
  https://lists.w3.org/Archives/Public/public-webappsec/2015Mar/0150.html
- A cheesy Apache / IIS DoS vuln (+a question)
  http://www.securityfocus.com/archive/1/456339/30/0/threaded
- China's Man-on-the-Side Attack on GitHub
  http://www.netresec.com/?page=Blog&month=2015-03&post=China%27s-Man-on-the-Side-Attack-on-GitHub
- The CISO Survey and Report, OWASP, 2013
  https://www.owasp.org/index.php/File:Owasp-ciso-report-2013-1.0.pdf
- Common Attack Pattern Enumeration and Classification (CAPEC), Mitre
  https://capec.mitre.org/
- Common Cyber Attacks: Reducing the Impact CERT-UK
  https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/400106/Common_Cyber_Attacks-Reducing_The_Impact.pdf
- Corporate espionage -- the internet's new growth industry
  http://www.itproportal.com/2015/03/19/corporate-espionage-internets-new-growth-industry/
- CSA Top Threats to Cloud Computing
  https://cloudsecurityalliance.org/topthreats/csathreats.v1.0.pdf
- CSRF vulnerability in GMail service
  http://seclists.org/fulldisclosure/2009/Mar/29
- CWE/SANS Top 25 Most Dangerous Software Errors, 2011
  http://cwe.mitre.org/top25/
- Cyber Fraud - Tactics Techniques and Procedures
  http://www.crcpress.com/product/isbn/9781420091274
- Cybercrime Report: Q1 2015, ThreatMetrix, 2015
  http://info.threatmetrix.com/WP-2015Q1CybercrimeReport_WP-LP.html
- Data Breach Investigations Report (DBIR), 2014
  http://www.verizonenterprise.com/DBIR/2014/
- Data Breach Investigations Report (DBIR), 2015
  http://www.verizonenterprise.com/DBIR/2015/
- Data Breaches Fuel Login Attacks Akamai Feb 2015
  http://www.stateoftheinternet.com/downloads/pdfs/2014-state-of-the-internet-threat-advisory-public-data-breaches-fuel-login-attacks.pdf
- Data Scraping Wikipedia http://en.wikipedia.org/wiki/Data_scraping
- DDoS Quick Guide
  https://www.us-cert.gov/sites/default/files/publications/DDoS%20Quick%20Guide.pdf
- DDoS Threat Landscape Report, 2013-2014
  http://lp.incapsula.com/rs/incapsulainc/images/2013-14_ddos_threat_landscape.pdf
- Defending Against an Internet-based Attack on the Physical World
  http://avirubin.com/scripted.attacks.pdf
- Defending Against Application-Based DDoS Attacks with the Barracuda
  Web Application Firewall
  https://www.barracuda.com/assets/docs/White_Papers/Barracuda_Web_Application_Firewall_WP_Defending%20*Against*%20Application-Based\_%20DDoS\_%20Attacks.pdf
- Demystifying HTML 5 Attacks
  http://resources.infosecinstitute.com/demystifying-html-5-attacks/
- Denial of Service Attacks: A Comprehensive Guide to Trends Techniques
  and Technologies Hacker Intelligence Initiative Imperva
  http://www.imperva.com/docs/HII_Denial_of_Service_Attacks-Trends_Techniques_and_Technologies.pdf
- Detecting and Blocking Site Scraping Attacks Imperva
  http://www.imperva.com/docs/WP_Detecting_and_Blocking_Site_Scraping_Attacks.pdf
- Detecting Automation of Twitter Accounts: Are you a human cyborg or a
  bot? http://www.cs.wm.edu/\~hnw/paper/tdsc12b.pdf
- Detecting Malice Robert "RSnake" Hansen 2009
  http://www.detectmalice.com/
- Directive 2002/58/EC of the European Parliament and of the Council of
  12 July 2002 concerning the processing of personal data and the
  protection of privacy in the electronic communications sector
  (Directive on privacy and electronic communications)
  http://eur-lex.europa.eu/legal-content/EN/TXT/?qid=1414072277428&uri=CELEX:32002L0058
- Directive 95/46/EC of the European Parliament and of the Council of 24
  October 1995 on the protection of individuals with regard to the
  processing of personal data and on the free movement of such data
  http://eur-lex.europa.eu/legal-content/en/ALL/?uri=CELEX:31995L0046
- Distributed Denial-of-Service (DDoS) Cyber-Attacks Risk Mitigation and
  Additional Resources Federal Financial Institutions Examination
  Council
  http://www.ffiec.gov/press/PDF/FFIEC%20DDoS%20Joint%20Statement.pdf
- Do Evil - The Business of Social Media Bots Forbes
  http://www.forbes.com/sites/lutzfinger/2015/02/17/do-evil-the-business-of-social-media-bots/
- DoS and DDoS Glossary of Terms prolexic
  http://www.prolexic.com/knowledge-center-dos-and-ddos-glossary.html#layer-7-ddos-attack
- E-commerce Malware Trustwave
  https://gsr.trustwave.com/topics/placeholder-topic/e-commerce-malware/
- Exploiting Software, G. Hoglund and G. McGraw, Addison-Wesley, 2004
- Five Trends to Track in E-Commerce Fraud, ThreatMetrix, 2013
  http://info.threatmetrix.com/rs/threatmetrix/images/Five_Trends_eCommerce_Fraud_WP.pdf
- Hacker builds cheatbot for hit app Trivia Crack
  http://www.theregister.co.uk/2015/03/26/hacker_builds_trivia_crack_cheat_app/
- Has Walmart opened itself up to "Denial of inventory" attacks?
  https://arstechnica.com/business/2012/05/has-walmart-opened-itself-up-to-denial-of-inventory-attacks/
- How Hoarder Bots Steal sales from Online Retailers
  https://www.internetretailer.com/mobile/2016/12/16/how-hoarder-bots-steal-sales-online-retailers
- - How to Defend Against DDoS Attacks - Strategies for the Network
    Transport and Application Layers Prolexic
    http://www.prolexic.com/kcresources/white-paper/strategies-for-the-network-transport-and-application-layers-412/Strategies_for_the_Network_Transport_and_Application_Layers_Prolexic_White_Paper_A4_082412.pdf
- How to Defend Online Travel Websites in the Era of Site Scraping,
  Distil Networks
  http://www.distilnetworks.com/defend-online-travel-websites-era-site-scraping-download/
- How to Shop for Free Online - Security Analysis of
  Cashier-as-a-Service Based Web Stores
  http://research.microsoft.com/pubs/145858/caas-oakland-final.pdf
- HTML5 Overview A look at HTML5 Attack Scenarios Trend Micro 2011
  http://www.trendmicro.com/cloud-content/us/pdfs/security-intelligence/reports/rpt_html5-attack-scenarios.pdf
- HTML5 Top 10 Threats Stealth Attacks and Silent Exploits 2012
  https://media.blackhat.com/bh-eu-12/shah/bh-eu-12-Shah_HTML5_Top_10-WP.pdf
- HTML5 web security 2011
  http://media.hacking-lab.com/hlnews/HTML5_Web_Security_v1.0.pdf
- HTTPPOST - Slow POST Wong Onn Chee OWASP AppSec DC 2010
  https://www.owasp.org/images/4/43/Layer_7_DDOS.pdf
- If you've got \@British_Airways account may make sense to change your
  password. Just had all my Avios cleared out!
  https://twitter.com/suttonnick/status/581556027948195840/photo/1
- Internet Security Threat Report, Volume 19, 2014
  http://www.symantec.com/content/en/us/enterprise/other_resources/b-istr_main_report_v19_21291018.en-us.pdf
- An Investigation into the Detection and Mitigation of Denial of
  Service (DoS) Attacks http://www.springer.com/gb/book/9788132202769
- Is Your Data Center Ready for Today's DDoS Threats? DDoS attack types
  protection methods and testing your detection and mitigation defenses
  http://www.fortinet.com/sites/default/files/whitepapers/WP-DDoS-Testing.pdf
- Joomla Reflection DDoS-for-Hire Akamai Feb 2015
  http://www.stateoftheinternet.com/downloads/pdfs/2015-state-of-the-internet-threat-advisory-joomla-reflection-attack-ddos-for-hire.pdf
- Layer 7 DDOS -- Blocking HTTP Flood Attacks
  http://blog.sucuri.net/2014/02/layer-7-ddos-blocking-http-flood-attacks.html
- Lenovo Superfish put smut on my system' -- class-action lawsuit The
  Register
  http://www.theregister.co.uk/2015/02/23/lenovo_superfish_class_action_lawsuit/
- List of Attack Vectors Relative Vulnerability Rating TECAPI
  http://www.tecapi.com/public/relative-vulnerability-rating-gui.jsp#
- Man in the Browser
  http://scisweb.ulster.ac.uk/\~kevin/IJACI-Vol4No1-maninbrowser.pdf
- Man in the Browser Attack
  https://www.owasp.org/index.php/Man-in-the-browser_attack
- Mapping and Measuring Cybercrime, Oxford Internet Institute
  http://www.oii.ox.ac.uk/publications/FD18.pdf
- Massive Changes in the Criminal Landscape Europol 2015
  https://www.europol.europa.eu/content/massive-changes-criminal-landscape
- Matching Attack Patterns to Security Vulnerabilities in
  Software-Intensive System Designs
  http://collaboration.csc.ncsu.edu/laurie/Papers/ICSE_Final_MCG_LW.pdf
- Mitigating DDoS Attacks with F5 Technology F5
  https://f5.com/resources/white-papers/mitigating-ddos-attacks-with-f5-technology
- Mitigating the DoS/DDosS Threat, Radware, 2012
  http://www.radware.com/PleaseRegister.aspx?returnUrl=6442452061
- Modern Web Attacks, Sophos, 2007
  http://www.sophos.com/en-us/why-sophos/our-people/technical-papers/modern-web-attacks.aspx
- ModSecurity Advanced Topic of the Week: Mitigating Slow HTTP DoS
  Attacks
  https://www.trustwave.com/Resources/SpiderLabs-Blog/(Updated)-ModSecurity-Advanced-Topic-of-the-Week--Mitigating-Slow-HTTP-DoS-Attacks/
- Most common attacks on web applications
  https://ipsec.pl/web-application-security/most-common-attacks-web-applications.html
- Multi-dimensional Vulnerability Hierarchies Daniel Miessler
  https://danielmiessler.com/study/multi-dimensional-vulnerability-hierarchies/
- New Wave of DDoS Attacks Launched BankInfoSecurity.com Mar 2013
  http://www.bankinfosecurity.com/new-wave-ddos-attacks-launched-a-5584/op-1
- NOMAD: Toward Non-Invasive Moving Target Defense Against Web Bots
  http://faculty.cs.tamu.edu/guofei/paper/NOMAD_CNS13.pdf
- Online Ad Fraud Exposed: Advertisers Losing \$6.3 Billion To \$10
  Billion Per Year Sep 2014
  http://www.darkreading.com/analytics/threat-intelligence/online-ad-fraud-exposed-advertisers-losing-\$63-billion-to-\$10-billion-per-year/d/d-id/1317979
- Online Data Companies versus Bots: The Fight is on for Control of
  Online Data, Distil Networks
  http://www.distilnetworks.com/online-data-companies-vs-bots-download/
- Optimal Airline Ticket Purchasing Using Automated User-Guided Feature
  Selection http://ijcai.org/papers13/Papers/IJCAI13-032.pdf
- Payment Checkout Flaws and Bugs 2014
  https://www.clerkendweller.uk/2014/11/4/Payment-Checkout-Flaws-and-Bugs
- PCI Compliance Report 2015 Verizon
  http://www.verizonenterprise.com/pcireport/2015/
- Pixel Perfect Timing Attacks with HTML5 2013
  http://www.contextis.com/services/research/white-papers/pixel-perfect-timing-attacks-html5/
- Polymorphism as a Defense for Automated Attack of Websites
  http://link.springer.com/chapter/10.1007%2F978-3-319-07536-5_30
- Preventing Web Scraping: Best Practice
  https://creativedigitalideas.files.wordpress.com/2014/11/best-practice-to-prevent-web-scraping.pdf
- Profile: Automated Credit Card Fraud
  http://old.honeynet.org/papers/profiles/cc-fraud.pdf
- Protecting Against Web Floods, Radware
  http://www.radware.com/PleaseRegister.aspx?returnUrl=6442452968
- Q4 2014 State of the Internet Security Report prolexic
  http://www.stateoftheinternet.com/downloads/pdfs/2014-internet-security-report-q4.pdf
- Reflection injection
  http://cybersecurity.ieee.org/images/files/images/pdf/CybersecurityInitiative-online.pdf
- A Report on taxonomy and evaluation of existing inventories,
  ENISAhttp://ecrime-project.eu/wp-content/uploads/2015/02/E-Crime-Deliverable-2-1-20141128_FINAL.pdf
- Reporting Intellectual Property Crime: A Guide for Victims of
  Copyright Infringement, Trademark Counterfeiting, and Trade Secret
  Theft, Dept of Justice
  http://www.justice.gov/criminal/cybercrime/docs/ip-victim-guide-and-checklist-march-2013.pdf
- SANS Top 20 Critical Controls
  https://www.sans.org/critical-security-controls/
- Securing Websites, Sophos, 2011
  http://www.sophos.com/en-us/why-sophos/our-people/technical-papers/securing-websites.aspx
- Security Insights: Defending Against Automated Threats
  http://www.securityweek.com/security-insights-defending-against-automated-threats
- Server side DDoS Imperva
  http://www.imperva.com/DefenseCenter/ThreatAdvisories/DDOS_Attack_Method_Payload_05182010
- Slow Read Denial of Service attack
  https://code.google.com/p/slowhttptest/wiki/SlowReadTest
- Slow-Read DoS Attack
  https://www.trustwave.com/Resources/SpiderLabs-Blog/ModSecurity-Advanced-Topic-of-the-Week--Mitigation-of--Slow-Read--Denial-of-Service-Attack/
- Slowloris HTTP DoS http://ha.ckers.org/slowloris/
- So what are the "most critical" application flaws? On new OWASP Top 10
  https://ipsec.pl/application-security/2013/so-what-are-most-critical-application-flaws-new-owasp-top-10.html
- Social Media Bots Offer Phony Friends and Real Profit NY Times
  http://www.nytimes.com/2014/11/20/fashion/social-media-bots-offer-phony-friends-and-real-profit.html?\_r=1
- Software Vulnerability Analysis, Krsul, 1998
  http://www.krsul.org/ivan/articles/main.pdf
- Sophos Security Threat Report
  http://blogs.sophos.com/2014/12/11/our-top-10-predictions-for-security-threats-in-2015-and-beyond/
- SpoofedMe Social Login Attack Discovered by IBM X-Force Researchers
  http://securityintelligence.com/spoofedme-social-login-attack-discovered-by-ibm-x-force-researchers/#.VSuiEhPSngM
- State of Software Security Report, Volume 5, Veracode, 2013
  https://info.veracode.com/state-of-software-security-report-volume5.html
- Stopping Automated Attack Tools
  http://www.technicalinfo.net/papers/StoppingAutomatedAttackTools.html
- Taxonomy on Online Game Security
  http://www.math.snu.ac.kr/\~jhcheon/publications/2004/Taxonomy%20on%20online%20game%20security_EL.pdf
- A Taxonomy of Computer Program Security Flaws, with Examples, Landwehr
  https://cwe.mitre.org/documents/sources/ATaxonomyofComputerProgramSecurityFlawswithExamples%5BLandwehr93%5D.pdf
- A Taxonomy of Security Faults in the UNIX Operating System, Aslam,
  1995
  https://cwe.mitre.org/documents/sources/ATaxonomyofSecurityFaultsintheUNIXOperatingSystem%5BAslam95%5D.pdf
- Testing Guide, v4, OWASP, 2014
  https://www.owasp.org/images/5/52/OWASP_Testing_Guide_v4.pdf
- The Bot Baseline: Fraud in Digital Advertising
  https://s3.amazonaws.com/whiteops-public/WO-ANA-Baseline-Study-of-Bot-Fraud.pdf
- The Internet Organised Crime Threat Assessment (iOCTA) 2014
  https://www.europol.europa.eu/content/internet-organised-crime-threat-assesment-iocta
- The Notorious Nine Cloud Computing Top Threats in 2013 CSA
  https://downloads.cloudsecurityalliance.org/initiatives/top_threats/The_Notorious_Nine_Cloud_Computing_Top_Threats_in_2013.pdf
- The Risks of Content Management Systems, IBM, 2015
  https://portal.sec.ibm.com/mss/html/en_US/support_resources/pdf/CMS_Threats_MSS_Threat_Report.pdf
- The Spy in the Sandbox -- Practical Cache Attacks in Javascript
  http://iss.oy.ne.ro/SpyInTheSandbox.pdf
- Thousands of Hacked Uber Accounts Selling on Dark Web for \$1
  http://thehackernews.com/2015/03/thousands-of-hacked-uber-accounts_30.html?m=1
- Threat Intelligence Quarterly, IBM, 1Q 2015
  https://www.ibm.com/services/forms/signup.do?source=swg-WW_Security_Organic&S_PKG=ov33510&S_TACT=C327017W&dynform=18101
- Threat Modeling: Designing for Security, Adam Shostack, Wiley, April
  2014 http://eu.wiley.com/WileyCDA/WileyTitle/productCd-1118809998.html
- Threats and Mitigations: A Guide to Multi-Layered Web Security - eBook
  Prolexic
  http://www.prolexic.com/knowledge-center/prolexic-download/guide-multi-layered-web-security-ebook.pdf
- Trapping Unknown Malware in a Context Web, Sophos
  http://www.sophos.com/en-us/medialibrary/PDFs/technical%20papers/HuqSzabo-VB2013.pdf?la=en.pdf
- Trustwave Global Security Report 2014
  https://www2.trustwave.com/GSR2014.html?utm_source=redirect&utm_medium=web&utm_campaign=GSR2014
- TurboTax's Anti-Fraud Efforts Under Scrutiny
  http://krebsonsecurity.com/2015/02/turbotaxs-anti-fraud-efforts-under-scrutiny/
- Two Security Vulnerabilities in the Spring Framework's MVC pdf
  (from 2008)
  http://blog.diniscruz.com/2011/07/two-security-vulnerabilities-in-spring.html
- The Underground Economy of Spam: A Botmaster's Perspective of
  Coordinating Large-Scale Spam Campaigns
  http://static.usenix.org/events/leet11/tech/full_papers/Stone-Gross.pdf
- Understanding Web Bots and How They Hurt Your Business Encapsula
  http://www.slideshare.net/Incapsula/understanding-web-bots-and-how-they-hurt-your-business
- Use of A Taxonomy of Security Faults, Taimur Aslam, Ivan Krsul and
  Eugene H Spafford, 1996
  http://docs.lib.purdue.edu/cgi/viewcontent.cgi?article=2304&context=cstech
- The WASC Threat Classification v2.0
  http://projects.webappsec.org/w/page/13246978/Threat%20Classification
- Warhol Worms: The Potential for Very Fast Internet Plagues
  http://www.iwar.org.uk/comsec/resources/worms/warhol-worm.htm
- Web Application Attack Report #5 Imperva
  http://www.imperva.com/docs/HII_Web_Application_Attack_Report_Ed5.pdf
- Web Application Defender's Cookbook: Battling Hackers and Protecting
  Users, Ryan Barnett, Wiley, December 2012
  http://eu.wiley.com/WileyCDA/WileyTitle/productCd-1118362187.html
- Web Attacks in the Wild Corsaire
  https://www.owasp.org/images/a/a7/Web_attacks_in_the_wild\_-\_ap.pdf
- Web Automation Friend or Foe?
  https://www.owasp.org/images/5/58/OWASP_Israel\_-*May_2009*-*Ofer_Shezaf*-\_Automation_Attacks.pdf
- Web Spambot Detection Based on Web Navigation Behaviour
  http://pedramhayati.com/papers/Web_Spambot_Detection_Based_on_Web_Usage_Behaviour.pdf
- Website Security Statistics Report, 2014
  http://info.whitehatsec.com/rs/whitehatsecurity/images/statsreport2014-20140410.pdf
- What is Zeus?
  http://www.sophos.com/medialibrary/pdfs/technical%20papers/sophos%20what%20is%20zeus%20tp.pdf
- When Web 2.0 Attacks! Understanding Ajax Flash and other highly
  interactive web technologies...
  https://www.owasp.org/images/f/fc/When_Web_2.0*Attacks*-\_Understanding_Security_Implications_of_Highly_Interactive_Technologies-Rafal_Los.pdf
- Where have all of our Passwords Gone? Gartner 2015
  http://blogs.gartner.com/avivah-litan/2015/01/22/where-have-all-our-passwords-gone/
- WS-Attacks.org http://www.ws-attacks.org/index.php/Main_Page
:::

::: {#sec-faqs .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Frequently Asked Questions

### When will it be updaated next?

A new edition is in progress and will be published in April-May 2025.

### What do you mean by "web", "application" and "automated threat"?

See the definitions in the project's [glossary](index.html#div-scope).

### What is an "ontology"?

An ontology is a set of types, properties, and relationship. These
together define a subject description language. This particular ontology
is meant to represent what automated threats real world owners observe
affecting their web applications in usual operations.

### Isn't this another bug (vulnerability) list?

No, none of the named automated threat events are implementation bugs -
they relate to abuse of functionality using automated means.

### But is it an OWASP Top N List?

Again no, it's an ontology which currently contains 21 items but there
may be more identified in the future. Also it is not an ordered list
(like OWASP Top N lists) - the OAT identification numbers were randomly
assigned, so the list is often written in alphabetical order to
emphasize this.

### I thought "so and so" already did that?

We found that it did not exist. While many threats are mentioned in the
sources researched, there was no overall list or definitions. We found
the automated threat events tended to all be in a small number of
definied items from Mitre CAPEC and WASC Threat Classification. If you
know of other automated threat lists/taxonomies/ontologies, please share
them.

### What is an "oat"?

It is our abbreviation for OWASP Automated Threat (OAT).

### I am confused and don't know which OAT my problem is - how do I identify it?

In 2017 we created a [threat identification
chart](assets/files/oat-ontology-decision-chart.pdf) to help identify
the correct OAT, which can then be confirmed by reading the full
description in the
[handbook](https://github.com/OWASP/www-project-automated-threats-to-web-applications/tree/master/assets/files/EN).
The short summaries are important explanations of each OAT name.

## How can I help?

Please join our [Google
Group](https://groups.google.com/a/owasp.org/forum/#!forum/automated-threats-project),
send ideas, contribute clarifications, corrections and improvement, and
let other people know about the project and its handbook.
:::

::: {#sec-acknowledgements .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Acknowledgements and Sponsors

### Contributors

- Sumit Agarwal
- Jason Chan
- Mark Hall
- Omri Iluz
- José Santos Martins Pereira
- Andrew van der Stock
- Roland Weber
- [Colin
  Watson](../cdn-cgi/l/email-protection.html#fe9d91929790d0899f8a8d9190be91899f8d8ed0918c99)
- [Tin
  Zaw](../cdn-cgi/l/email-protection.html#a0d4c9ce8edac1d7e0cfd7c1d3d08ecfd2c7)

Additionally other professional colleagues and website owners and
operators who provided feedback.

### Reviewers

- Igor Andriushchenko
- Gabriel Mendez Justiniano
- Matt Tesauro

### Sponsors

All OWASP Projects are run and developed by volunteers and rely on
personal donations and sponsorship to continue their development. OWASP
does not endorse or recommend commercial products or services, allowing
our community to remain vendor neutral with the collective wisdom of the
best minds in software security worldwide. This project has received the
sponsorship part of their Corporate OWASP membership fees from Verizon
Digital Media Services in 2016 and Distil Networks in 2017, which has
already contributed to the v1.2 production design costs, and will also
be utilised to help promote knowledge of the project.

\

![Verizon Digital Media
logo](assets/images/Verizon_Digital_Medial_Logo.jpg)

\
\

![Distil Networks logo](assets/images/Distil-flat-logo-2.png)

\
:::

::: {#sec-roadmap .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Road Map and Getting Involved

We want to keep the Automated Threat Handbook Updated. As of spring
2025, we are updating the CAPEC and OWASP mappings and undertaking a
review to identify mappings to [Open Common Requirement Enumeration
(Open CRE)](https://www.opencre.org/).

A new edition will be published in April-May 2025.

Can you help? The project is looking for information on the prevalence
and types of automated threats seen by web application owners in the
real world. This will be used to refine and organise the information
gathered from research papers, whitepapers, security reports and
industry news. Please use the project's [Google
Group](https://groups.google.com/a/owasp.org/forum/#!forum/automated-threats-project)
to keep up-to-date with what's going on, and to contribute your ideas,
feedback, and experience:

To share information confidentially, you can email the project leaders
directly: [Tin
Zaw](../cdn-cgi/l/email-protection.html#2c58454202564d5b6c435b4d5f5c02435e4b)
and [Colin
Watson](../cdn-cgi/l/email-protection.html#3754585b5e591940564344585977584056444719584550).
:::
:::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-automated-threats-to-web-applications/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-automated-threats-to-web-applications){.github-button
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

### Quick Links

- [Download the free handbook as a
  PDF](https://github.com/OWASP/www-project-automated-threats-to-web-applications/tree/master/assets/files/EN)
  or [buy a print
  copy](http://www.lulu.com/shop/owasp-foundation/automated-threat-handbook/paperback/product-23540699.html)

### What Is This?

- Information and resources to help web application owners defend
  against automated threats

### What Isn't It?

- Not another vulnerability list
- Not an OWASP Top N List
- Not threat modelling
- Not attack trees
- Not non web
- Not non application

### Project Objective

This project brings together research and analysis of real world
automated attacks against web applications, to produce documentation to
assist operators defend against these threats. Sector-specific guidance
will be available.

### Project Information

- [Lab Project]{style="font-size:1.0em;padding-left:12px;"}
- [Documentation]{style="font-size:1.0em;padding-left:12px;"}
- [Builder]{style="font-size:1.0em;padding-left:12px;"}
- [Defender]{style="font-size:1.0em;padding-left:12px;"}

### Presentation

- [![Title slide of
  presentation](assets/images/automatedthreats-presentation-small.jpg)](assets/files/Bots-AppSecUSA2017-Project-Summit.pptx)

### In Print

- [![Cover image of the OWASP Automated Threat
  Handbook](assets/images/automatedThreatHandbook_small.jpg)](http://www.lulu.com/shop/owasp-foundation/automated-threat-handbook/paperback/product-23540699.html)
- The Automated Threat Handbook can be purchased at cost as a
  [print-on-demand
  book](http://www.lulu.com/shop/owasp-foundation/automated-threat-handbook/paperback/product-23540699.html).

### License

- [![CC BY-SA
  3.0](../../licensebuttons.net/l/by-sa/3.0/80x15.png)](http://creativecommons.org/licenses/by-sa/3.0/)

### Leaders

- [Tin
  Zaw](../cdn-cgi/l/email-protection.html#04706d6a2a7e6573446b736577742a6b7663)
- [Colin
  Watson](../cdn-cgi/l/email-protection.html#b1d2deddd8df9fc6d0c5c2dedff1dec6d0c2c19fdec3d6)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::::::
