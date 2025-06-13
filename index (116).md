:::::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Overview](#div-overview){#overview-link .tab-link role="tab"
  aria-selected="false" aria-controls="overview"}
- [News](#div-news){#news-link .tab-link role="tab"
  aria-selected="false" aria-controls="news"}
- [Challenges](#div-challenges){#challenges-link .tab-link role="tab"
  aria-selected="false" aria-controls="challenges"}
- [Learning](#div-learning){#learning-link .tab-link role="tab"
  aria-selected="false" aria-controls="learning"}
- [CTF](#div-ctf){#ctf-link .tab-link role="tab" aria-selected="false"
  aria-controls="ctf"}
- [Ecosystem](#div-ecosystem){#ecosystem-link .tab-link role="tab"
  aria-selected="false" aria-controls="ecosystem"}
- [Supporters](#div-supporters){#supporters-link .tab-link role="tab"
  aria-selected="false" aria-controls="supporters"}

# OWASP Juice Shop {#owasp-juice-shop .page-title}

::::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![Juice Shop
Logo](../../raw.githubusercontent.com/juice-shop/juice-shop/develop/frontend/src/assets/public/images/JuiceShop_Logo_100px.png)

[![OWASP
Flagship](https://img.shields.io/badge/owasp-flagship%20project-48A646.svg)](../projects/index.html#div-flagships)
[![GitHub
release](https://img.shields.io/github/release/juice-shop/juice-shop.svg)](https://github.com/juice-shop/juice-shop/releases/latest)
[![GitHub
stars](https://img.shields.io/github/stars/juice-shop/juice-shop.svg?label=GitHub%20%E2%98%85&style=flat)](https://github.com/juice-shop/juice-shop/stargazers)
[![Twitter
Follow](https://img.shields.io/twitter/follow/owasp_juiceshop.svg?style=social&label=Follow)](https://twitter.com/owasp_juiceshop)

[![OpenSSF Best
Practices](https://www.bestpractices.dev/projects/223/badge)](https://www.bestpractices.dev/projects/223)
[![Contributor
Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](https://github.com/juice-shop/juice-shop/blob/master/CODE_OF_CONDUCT.md)

OWASP Juice Shop is probably the most modern and sophisticated insecure
web application! It can be used in security trainings, awareness demos,
CTFs and as a guinea pig for security tools! Juice Shop encompasses
vulnerabilities from the entire [OWASP Top
Ten](../www-project-top-ten/index.html) along with many other security
flaws found in real-world applications!

![Slideshow](../../raw.githubusercontent.com/juice-shop/juice-shop/master/screenshots/slideshow.gif)

## Description

Juice Shop is written in Node.js, Express and Angular. It was the first
application written entirely in JavaScript listed in the [OWASP VWA
Directory](../www-project-vulnerable-web-applications-directory/index.html).

The application contains a vast number of hacking challenges of varying
difficulty where the user is supposed to exploit the underlying
vulnerabilities. The hacking progress is tracked on a score board.
Finding this score board is actually one of the (easy) challenges!

Apart from the hacker and awareness training use case, pentesting
proxies or security scanners can use Juice Shop as a "guinea
pig"-application to check how well their tools cope with
JavaScript-heavy application frontends and REST APIs.

*Translating "dump" or "useless outfit" into German yields "Saftladen"
which can be reverse-translated word by word into "juice shop". Hence
the project name. That the initials "JS" match with those of
"JavaScript" was purely coincidental!*

## Testimonials

> [The most trustworthy online shop out
> there.](https://twitter.com/dschadow/status/706781693504589824) (
> [\@dschadow](https://github.com/dschadow)) --- [The best juice shop on
> the whole
> internet!](https://twitter.com/shehackspurple/status/907335357775085568)
> ( [\@shehackspurple](https://twitter.com/shehackspurple)) ---
> [Actually the most bug-free vulnerable application in
> existence!](https://youtu.be/TXAztSpYpvE?t=26m35s) (
> [\@vanderaj](https://twitter.com/vanderaj)) --- [First you 😂😂then
> you 😢](https://twitter.com/kramse/status/1073168529405472768) (
> [\@kramse](https://twitter.com/kramse)) --- [But this doesn't have
> anything to do with
> juice.](https://twitter.com/coderPatros/status/1199268774626488320) (
> [\@coderPatros' wife](https://twitter.com/coderPatros))

## Contributors

[![GitHub
contributors](https://img.shields.io/github/contributors/juice-shop/juice-shop.svg)](https://github.com/juice-shop/juice-shop/graphs/contributors)
[![Crowdin](https://d322cqt584bo4o.cloudfront.net/owasp-juice-shop/localized.svg)](https://crowdin.com/project/owasp-juice-shop)

The OWASP Juice Shop has been created by [Björn
Kimminich](../cdn-cgi/l/email-protection.html#debcb4b1bbacb0f0b5b7b3b3b7b0b7bdb69eb1a9bfadaef0b1acb9)
and is developed, maintained and translated by a [team of
volunteers](https://github.com/juice-shop/juice-shop/blob/master/HALL_OF_FAME.md).
A [live update of the project
contributors](https://github.com/juice-shop/juice-shop/graphs/contributors)
is found here.

## Licensing

[![license](https://img.shields.io/github/license/juice-shop/juice-shop.svg)](https://github.com/juice-shop/juice-shop/blob/master/LICENSE)

This program is free software: You can redistribute it and/or modify it
under the terms of the [MIT
License](https://github.com/juice-shop/juice-shop/blob/master/LICENSE).
OWASP Juice Shop and any contributions are Copyright © by Bjoern
Kimminich & the OWASP Juice Shop contributors 2014-2025.
:::

::: {#sec-overview .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Main Selling Points

- **Free and Open source**: Licensed under the [MIT
  license](https://github.com/juice-shop/juice-shop/blob/master/LICENSE)
  with no hidden costs or caveats
- **Easy-to-install**: Choose between [node.js](http://nodejs.org/),
  [Docker](https://www.docker.com/) and
  [Vagrant](https://www.vagrantup.com/downloads.html) to run on
  Windows/Mac/Linux as well as all major cloud providers
- **Self-contained**: Additional dependencies are
  [pre-packaged](https://github.com/juice-shop/juice-shop/releases/latest)
  or will be resolved and downloaded automatically
- **Beginner-friendly**: [Hacking
  Instructor](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_hacking_instructor)
  scripts with optional [tutorial
  mode](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_tutorial_mode)
  guide newcomers through several challenges while explaining the
  underlying vulnerabilities
- **Gamification**: The application [notifies you on solved
  challenges](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_success_notifications)
  and keeps track of successfully exploited vulnerabilities on a [Score
  Board](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_the_score_board)
- **Self-healing**: [Wiped clean and repopulated from
  scratch](https://pwning.owasp-juice.shop/companion-guide/latest/part1/running.html#_self_healing_feature)
  on every server startup while [automatically persisting progress in
  your
  browser](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_automatic_saving_and_restoring_hacking_progress)
  or via [manual local
  backup](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_manual_progress_and_settings_backup)
- **Re-branding**: [Fully
  customizable](https://pwning.owasp-juice.shop/companion-guide/latest/part4/customization.html)
  in business context and look & feel to your own corporate or customer
  requirements
- **CTF-support**: Challenge notifications optionally contain a flag
  code for your own [Capture-The-Flag
  events](https://pwning.owasp-juice.shop/companion-guide/latest/part4/ctf.html)
- **Coding Challenges**: Over 20 hacking challenges come with an
  additional [Coding
  Challenge](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_coding_challenges)
  where finding and fixing the responsible code flaw can be trained
- **Interoperability**: Integrate with your own training systems via
  [WebHook](https://pwning.owasp-juice.shop/companion-guide/latest/part4/integration.html#_challenge_solution_webhook),
  monitor the [extensive
  metrics](https://pwning.owasp-juice.shop/companion-guide/latest/part4/monitoring.html)
  or consume challenge information directly via
  [API](https://pwning.owasp-juice.shop/companion-guide/latest/part4/integration.html#_challenges_api)
  or [file
  import](https://pwning.owasp-juice.shop/companion-guide/latest/part4/integration.html#_challenge_declaration_file)

## Screenshots

![Screenshot
1](../../raw.githubusercontent.com/juice-shop/juice-shop/master/screenshots/screenshot01.png)\
\
![Screenshot
2](../../raw.githubusercontent.com/juice-shop/juice-shop/master/screenshots/screenshot02.png)\
\
![Screenshot
3](../../raw.githubusercontent.com/juice-shop/juice-shop/master/screenshots/screenshot03.png)\
\
![Screenshot
4](../../raw.githubusercontent.com/juice-shop/juice-shop/master/screenshots/screenshot04.png)\
\
![Screenshot
5](../../raw.githubusercontent.com/juice-shop/juice-shop/master/screenshots/screenshot05.png)

## Application Architecture

![Architecture
diagram](../../raw.githubusercontent.com/juice-shop/pwning-juice-shop/master/docs/modules/ROOT/assets/images/introduction/architecture-diagram.png)
:::

::: {#sec-news .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Latest Releases

[![GitHub
release](https://img.shields.io/github/release/juice-shop/juice-shop.svg)](https://github.com/juice-shop/juice-shop/releases/latest)
[![GitHub
release](https://img.shields.io/github/downloads/juice-shop/juice-shop/total.svg)](https://github.com/juice-shop/juice-shop/releases/latest)
[![SourceForge](https://img.shields.io/sourceforge/dm/juice-shop?label=sourceforge%20downloads)](https://sourceforge.net/projects/juice-shop/)
[![SourceForge](https://img.shields.io/sourceforge/dt/juice-shop?label=sourceforge%20downloads)](https://sourceforge.net/projects/juice-shop/)
[![Docker
Pulls](https://img.shields.io/docker/pulls/bkimminich/juice-shop.svg)](https://hub.docker.com/r/bkimminich/juice-shop)

- 2025-04-22T22:13:33Z: juice-shop [`v17.3.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop/releases/tag/v17.3.0)
- 2025-03-14T21:04:32Z: juice-shop [`v17.2.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop/releases/tag/v17.2.0)
- 2024-09-09T16:06:22Z: juice-shop [`v17.1.1`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop/releases/tag/v17.1.1)
- 2024-08-05T15:07:20Z: juice-shop [`v17.1.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop/releases/tag/v17.1.0)
- 2024-05-24T21:08:54Z: juice-shop [`v17.0.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop/releases/tag/v17.0.0)
- 2024-04-22T13:36:03Z: juice-shop [`v16.0.1`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop/releases/tag/v16.0.1)
- 2023-12-19T15:35:41Z: juice-shop [`v16.0.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop/releases/tag/v16.0.0)
- 2023-11-03T20:11:03Z: juice-shop [`v15.3.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop/releases/tag/v15.3.0)
- 2023-10-03T21:17:58Z: juice-shop [`v15.2.1`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop/releases/tag/v15.2.1)
- 2023-09-22T16:37:04Z: juice-shop [`v15.2.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop/releases/tag/v15.2.0)
- 2023-09-08T13:03:29Z: juice-shop [`v15.1.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop/releases/tag/v15.1.0)
- 2023-05-19T23:00:51Z: juice-shop [`v15.0.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop/releases/tag/v15.0.0)

### CTF Extension

[![GitHub
release](https://img.shields.io/github/release/juice-shop/juice-shop-ctf.svg)](https://github.com/juice-shop/juice-shop-ctf/releases/latest)
[![npm](https://img.shields.io/npm/dm/juice-shop-ctf-cli.svg)](https://www.npmjs.com/package/juice-shop-ctf-cli)
[![npm](https://img.shields.io/npm/dt/juice-shop-ctf-cli.svg)](https://www.npmjs.com/package/juice-shop-ctf-cli)
[![Docker
Pulls](https://img.shields.io/docker/pulls/bkimminich/juice-shop-ctf.svg)](https://hub.docker.com/r/bkimminich/juice-shop-ctf)

- 2025-02-18T11:19:13Z: juice-shop-ctf [`v11.1.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop-ctf/releases/tag/v11.1.0)
- 2024-10-25T14:30:28Z: juice-shop-ctf [`v11.0.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop-ctf/releases/tag/v11.0.0)
- 2023-10-11T22:23:15Z: juice-shop-ctf [`v10.0.1`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop-ctf/releases/tag/v10.0.1)
- 2023-09-01T10:31:42Z: juice-shop-ctf [`v10.0.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop-ctf/releases/tag/v10.0.0)
- 2022-08-23T16:13:55Z: juice-shop-ctf [`v9.1.2`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop-ctf/releases/tag/v9.1.2)
- 2022-08-03T04:31:18Z: juice-shop-ctf [`v9.1.1`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/juice-shop-ctf/releases/tag/v9.1.1)

### MultiJuicer

[![GitHub
release](https://img.shields.io/github/release/juice-shop/multi-juicer.svg)](https://github.com/juice-shop/juice-shop-ctf/releases/latest)

- 2025-04-30T09:15:52Z: multi-juicer [`v8.2.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/multi-juicer/releases/tag/v8.2.0)
- 2025-03-15T18:57:18Z: multi-juicer [`v8.1.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/multi-juicer/releases/tag/v8.1.0)
- 2025-03-05T18:29:42Z: multi-juicer [`v8.0.5`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/multi-juicer/releases/tag/v8.0.5)
- 2025-02-27T13:10:39Z: multi-juicer [`v8.0.4`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/multi-juicer/releases/tag/v8.0.4)
- 2025-02-25T19:43:35Z: multi-juicer [`v8.0.3`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/multi-juicer/releases/tag/v8.0.3)
- 2025-02-07T14:54:23Z: multi-juicer [`v8.0.2`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/multi-juicer/releases/tag/v8.0.2)
- 2025-01-07T18:42:57Z: multi-juicer [`v8.0.1`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/multi-juicer/releases/tag/v8.0.1)
- 2024-12-28T13:51:39Z: multi-juicer [`v8.0.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/multi-juicer/releases/tag/v8.0.0)
- 2024-10-06T00:25:23Z: multi-juicer [`v7.3.2`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/multi-juicer/releases/tag/v7.3.2)
- 2024-09-19T13:26:34Z: multi-juicer [`v7.3.1`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/multi-juicer/releases/tag/v7.3.1)
- 2024-09-10T09:40:37Z: multi-juicer [`v7.3.0`{.language-plaintext
  .highlighter-rouge}](https://github.com/juice-shop/multi-juicer/releases/tag/v7.3.0)

## Roadmap

![GitHub issues
by-label](https://img.shields.io/github/issues/juice-shop/juice-shop/help%20wanted.svg)
![GitHub issues
by-label](https://img.shields.io/github/issues/juice-shop/juice-shop/good%20first%20issue.svg)

- Auction off up to ten [unique anniversary NFT
  artworks](https://opensea.io/collection/juice-shop-10th-anniversary){target="_blank"}
  to true Juice Shop fans

- Update to the [newest Angular
  Version](https://github.com/juice-shop/juice-shop/issues/2538){target="_blank"}

- Pay back other accumulated technical debt and harmonize codebase
  overall

- Bring [overall test
  coverage](https://codeclimate.com/github/juice-shop/juice-shop){target="_blank"}
  back over 90%+
:::

::: {#sec-challenges .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Challenge Categories

The vulnerabilities found in the OWASP Juice Shop are categorized into
several different classes. Most of them cover different risk or
vulnerability types from well-known lists or documents, such as [OWASP
Top 10](../www-project-top-ten/index.html), [OWASP
ASVS](../www-project-application-security-verification-standard/index.html),
[OWASP Automated Threat
Handbook](../www-project-automated-threats-to-web-applications/index.html)
and [OWASP API Security Top 10](../www-project-api-security/index.html)
or MITRE's [Common Weakness Enumeration](https://cwe.mitre.org/).

+--------------------------------+----+--------------------------------+
| Category                       | \# | Challenges                     |
+================================+====+================================+
| Broken Access Control          | 11 | [Admin Section, CSRF, Easter   |
|                                |    | Egg, Five-Star Feedback,       |
|                                |    | Forged Feedback, Forged        |
|                                |    | Review, Manipulate Basket,     |
|                                |    | Product Tampering, SSRF, View  |
|                                |    | Basket, Web3 Sandbox]{.small}  |
+--------------------------------+----+--------------------------------+
| Broken Anti Automation         | 4  | [CAPTCHA Bypass, Extra         |
|                                |    | Language, Multiple Likes,      |
|                                |    | Reset Morty\'s                 |
|                                |    | Password]{.small}              |
+--------------------------------+----+--------------------------------+
| Broken Authentication          | 9  | [Bjoern\'s Favorite Pet,       |
|                                |    | Change Bender\'s Password,     |
|                                |    | GDPR Data Erasure, Login       |
|                                |    | Bjoern, Password Strength,     |
|                                |    | Reset Bender\'s Password,      |
|                                |    | Reset Bjoern\'s Password,      |
|                                |    | Reset Jim\'s Password, Two     |
|                                |    | Factor Authentication]{.small} |
+--------------------------------+----+--------------------------------+
| Cryptographic Issues           | 5  | [Forged Coupon, Imaginary      |
|                                |    | Challenge, Nested Easter Egg,  |
|                                |    | Premium Paywall, Weird         |
|                                |    | Crypto]{.small}                |
+--------------------------------+----+--------------------------------+
| Improper Input Validation      | 12 | [Admin Registration, Deluxe    |
|                                |    | Fraud, Empty User              |
|                                |    | Registration, Expired Coupon,  |
|                                |    | Mint the Honey Pot, Missing    |
|                                |    | Encoding, Payback Time, Poison |
|                                |    | Null Byte, Repetitive          |
|                                |    | Registration, Upload Size,     |
|                                |    | Upload Type, Zero              |
|                                |    | Stars]{.small}                 |
+--------------------------------+----+--------------------------------+
| Injection                      | 11 | [Christmas Special, Database   |
|                                |    | Schema, Ephemeral Accountant,  |
|                                |    | Login Admin, Login Bender,     |
|                                |    | Login Jim, NoSQL DoS, NoSQL    |
|                                |    | Exfiltration, NoSQL            |
|                                |    | Manipulation, SSTi, User       |
|                                |    | Credentials]{.small}           |
+--------------------------------+----+--------------------------------+
| Insecure Deserialization       | 3  | [Blocked RCE DoS, Memory Bomb, |
|                                |    | Successful RCE DoS]{.small}    |
+--------------------------------+----+--------------------------------+
| Miscellaneous                  | 7  | [Bully Chatbot, Mass Dispel,   |
|                                |    | Privacy Policy, Score Board,   |
|                                |    | Security Advisory, Security    |
|                                |    | Policy, Wallet                 |
|                                |    | Depletion]{.small}             |
+--------------------------------+----+--------------------------------+
| Security Misconfiguration      | 4  | [Cross-Site Imaging,           |
|                                |    | Deprecated Interface, Error    |
|                                |    | Handling, Login Support        |
|                                |    | Team]{.small}                  |
+--------------------------------+----+--------------------------------+
| Security through Obscurity     | 3  | [Blockchain Hype, Privacy      |
|                                |    | Policy Inspection,             |
|                                |    | Steganography]{.small}         |
+--------------------------------+----+--------------------------------+
| Sensitive Data Exposure        | 18 | [Access Log, Confidential      |
|                                |    | Document, Email Leak, Exposed  |
|                                |    | Metrics, Exposed credentials,  |
|                                |    | Forgotten Developer Backup,    |
|                                |    | Forgotten Sales Backup, GDPR   |
|                                |    | Data Theft, Leaked Access      |
|                                |    | Logs, Leaked Unsafe Product,   |
|                                |    | Login Amy, Login MC            |
|                                |    | SafeSearch, Meta Geo Stalking, |
|                                |    | Misplaced Signature File, NFT  |
|                                |    | Takeover, Reset Uvogin\'s      |
|                                |    | Password, Retrieve Blueprint,  |
|                                |    | Visual Geo Stalking]{.small}   |
+--------------------------------+----+--------------------------------+
| Unvalidated Redirects          | 2  | [Allowlist Bypass, Outdated    |
|                                |    | Allowlist]{.small}             |
+--------------------------------+----+--------------------------------+
| Vulnerable Components          | 9  | [Arbitrary File Write, Forged  |
|                                |    | Signed JWT, Frontend           |
|                                |    | Typosquatting, Kill Chatbot,   |
|                                |    | Legacy Typosquatting, Local    |
|                                |    | File Read, Supply Chain        |
|                                |    | Attack, Unsigned JWT,          |
|                                |    | Vulnerable Library]{.small}    |
+--------------------------------+----+--------------------------------+
| XSS                            | 9  | [API-only XSS, Bonus Payload,  |
|                                |    | CSP Bypass, Client-side XSS    |
|                                |    | Protection, DOM XSS,           |
|                                |    | HTTP-Header XSS, Reflected     |
|                                |    | XSS, Server-side XSS           |
|                                |    | Protection, Video XSS]{.small} |
+--------------------------------+----+--------------------------------+
| XXE                            | 2  | [XXE Data Access, XXE          |
|                                |    | DoS]{.small}                   |
+--------------------------------+----+--------------------------------+
| **Total Σ**                    | 109                                 |
+--------------------------------+-------------------------------------+

## Challenge Tags

Tags do not represent vulnerability categories but serve as additional
meta information for challenges. They mark certain commonalities or
special types of challenges - like those lacking seriousness or ones
that probably need some scripting/automation etc.

  Tag                \#   Challenges
  ------------------ ---- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Brute Force        6    [Bully Chatbot, CAPTCHA Bypass, Extra Language, Login Support Team, Password Strength, Reset Morty\'s Password]{.small}
  Code Analysis      10   [Blockchain Hype, Forged Coupon, Imaginary Challenge, Kill Chatbot, Login Bjoern, Login Support Team, Outdated Allowlist, SSRF, SSTi, Score Board]{.small}
  Contraption        9    [Blockchain Hype, Cross-Site Imaging, Deprecated Interface, Easter Egg, Forgotten Developer Backup, Forgotten Sales Backup, Misplaced Signature File, NFT Takeover, SSTi]{.small}
  Danger Zone        17   [API-only XSS, Arbitrary File Write, Blocked RCE DoS, CSP Bypass, Client-side XSS Protection, HTTP-Header XSS, Local File Read, Memory Bomb, NoSQL DoS, NoSQL Exfiltration, Reflected XSS, SSTi, Server-side XSS Protection, Successful RCE DoS, Video XSS, XXE Data Access, XXE DoS]{.small}
  Good Practice      4    [Exposed Metrics, Misplaced Signature File, Privacy Policy, Security Policy]{.small}
  Good for Demos     13   [Admin Section, Confidential Document, DOM XSS, Easter Egg, Forged Coupon, Forgotten Developer Backup, Login Admin, NFT Takeover, Nested Easter Egg, Privacy Policy, Privacy Policy Inspection, Reflected XSS, View Basket]{.small}
  Internet Traffic   2    [Mint the Honey Pot, Wallet Depletion]{.small}
  OSINT              15   [Bjoern\'s Favorite Pet, Leaked Access Logs, Leaked Unsafe Product, Local File Read, Login Amy, Login MC SafeSearch, Meta Geo Stalking, Reset Bender\'s Password, Reset Bjoern\'s Password, Reset Jim\'s Password, Reset Morty\'s Password, Reset Uvogin\'s Password, Supply Chain Attack, Visual Geo Stalking, Vulnerable Library]{.small}
  Prerequisite       6    [Allowlist Bypass, Arbitrary File Write, Deprecated Interface, Error Handling, Forgotten Developer Backup, Poison Null Byte]{.small}
  Shenanigans        11   [Bonus Payload, Bully Chatbot, Easter Egg, Imaginary Challenge, Leaked Unsafe Product, Login MC SafeSearch, Missing Encoding, Nested Easter Egg, Premium Paywall, Privacy Policy Inspection, Steganography]{.small}
  Tutorial           11   [Bonus Payload, DOM XSS, Forged Feedback, Login Admin, Login Bender, Login Jim, Password Strength, Privacy Policy, Reflected XSS, Score Board, View Basket]{.small}
  Web3               5    [Blockchain Hype, Mint the Honey Pot, NFT Takeover, Wallet Depletion, Web3 Sandbox]{.small}
:::

::: {#sec-learning .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Hacking Instructor Tutorials

![Juicy
Bot](../../raw.githubusercontent.com/juice-shop/juice-shop/master/frontend/src/assets/public/images/JuicyBot_MedicalMask.png)

Click on a link in the table below to launch a [step-by-step
tutorial](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_hacking_instructor)
for that particular challenge on our public
[https://demo.owasp-juice.shop](https://demo.owasp-juice.shop/)
instance. If you are entirely new to the Juice Shop, we recommend doing
them in the listed order. With the (optional) [Tutorial
Mode](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_tutorial_mode)
you can even enforce that the 13 tutorial challenges have to be
performed gradually in order to unlock the other 96 challenges.

  Challenge                                                                                                                    Category                  Difficulty
  ---------------------------------------------------------------------------------------------------------------------------- ------------------------- ------------
  [Score Board](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Score%20Board){target="_blank"}                   Miscellaneous             ⭐
  [DOM XSS](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=DOM%20XSS){target="_blank"}                           XSS                       ⭐
  [Bonus Payload](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Bonus%20Payload){target="_blank"}               XSS                       ⭐
  [Privacy Policy](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Privacy%20Policy){target="_blank"}             Miscellaneous             ⭐
  [Reflected XSS](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Reflected%20XSS){target="_blank"}               XSS                       ⭐⭐
  [Exposed credentials](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Exposed%20credentials){target="_blank"}   Sensitive Data Exposure   ⭐⭐
  [Login Admin](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Login%20Admin){target="_blank"}                   Injection                 ⭐⭐
  [Admin Section](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Admin%20Section){target="_blank"}               Broken Access Control     ⭐⭐
  [Password Strength](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Password%20Strength){target="_blank"}       Broken Authentication     ⭐⭐
  [View Basket](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=View%20Basket){target="_blank"}                   Broken Access Control     ⭐⭐
  [Forged Feedback](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Forged%20Feedback){target="_blank"}           Broken Access Control     ⭐⭐⭐
  [Login Jim](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Login%20Jim){target="_blank"}                       Injection                 ⭐⭐⭐
  [Login Bender](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Login%20Bender){target="_blank"}                 Injection                 ⭐⭐⭐
  [Coding Challenges](https://demo.owasp-juice.shop/#/hacking-instructor?challenge=Coding%20Challenges){target="_blank"}       n/a                       n/a

## Coding Challenges

For 31 challenges an additional [coding
challenge](https://pwning.owasp-juice.shop/companion-guide/latest/part1/challenges.html#_coding_challenges)
is available. In their "Find It" phase they teach spotting
vulnerabilities in the actual codebase of the Juice Shop. In the "Fix
It" phase the user then chooses the most appropriate fix from a list.
Solve any of the hacking challenges below to enable a button on the
Score Board that launches the corresponding coding challenge:\
\

+--------------------------------+----+--------------------------------+
| Category                       | \# | Challenges                     |
+================================+====+================================+
| Broken Access Control          | 4  | [Admin Section, Forged Review, |
|                                |    | Product Tampering, Web3        |
|                                |    | Sandbox]{.small}               |
+--------------------------------+----+--------------------------------+
| Broken Anti Automation         | 1  | [Reset Morty\'s                |
|                                |    | Password]{.small}              |
+--------------------------------+----+--------------------------------+
| Broken Authentication          | 5  | [Bjoern\'s Favorite Pet,       |
|                                |    | Password Strength, Reset       |
|                                |    | Bender\'s Password, Reset      |
|                                |    | Bjoern\'s Password, Reset      |
|                                |    | Jim\'s Password]{.small}       |
+--------------------------------+----+--------------------------------+
| Improper Input Validation      | 2  | [Admin Registration, Mint the  |
|                                |    | Honey Pot]{.small}             |
+--------------------------------+----+--------------------------------+
| Injection                      | 6  | [Database Schema, Login Admin, |
|                                |    | Login Bender, Login Jim, NoSQL |
|                                |    | Manipulation, User             |
|                                |    | Credentials]{.small}           |
+--------------------------------+----+--------------------------------+
| Miscellaneous                  | 2  | [Score Board, Wallet           |
|                                |    | Depletion]{.small}             |
+--------------------------------+----+--------------------------------+
| Security through Obscurity     | 1  | [Blockchain Hype]{.small}      |
+--------------------------------+----+--------------------------------+
| Sensitive Data Exposure        | 5  | [Access Log, Confidential      |
|                                |    | Document, Exposed Metrics, NFT |
|                                |    | Takeover, Reset Uvogin\'s      |
|                                |    | Password]{.small}              |
+--------------------------------+----+--------------------------------+
| Unvalidated Redirects          | 2  | [Allowlist Bypass, Outdated    |
|                                |    | Allowlist]{.small}             |
+--------------------------------+----+--------------------------------+
| XSS                            | 3  | [API-only XSS, Bonus Payload,  |
|                                |    | DOM XSS]{.small}               |
+--------------------------------+----+--------------------------------+
| **Total Σ**                    | 31                                  |
+--------------------------------+-------------------------------------+

## Mitigation Links

For many solved challenges links to mitigation techniques are presented
on the Score Board by offering a link to a corresponding [OWASP Cheat
Sheet](https://cheatsheetseries.owasp.org/) explaining how to avoid that
kind of vulnerability in the first place. The following cheat sheets are
referred to by OWASP Juice Shop as mitigation links:

- [[Authentication Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Authorization Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Choosing and Using Security Questions Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Choosing_and_Using_Security_Questions_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Credential Stuffing Prevention Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Credential_Stuffing_Prevention_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Cross-Site Request Forgery Prevention Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Cross Site Scripting Prevention Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Cryptographic Storage Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Cryptographic_Storage_Cheat_Sheet.html){target="_blank"}]{.small}
- [[DOM based XSS Prevention Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/DOM_based_XSS_Prevention_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Denial of Service Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Denial_of_Service_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Error Handling Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Error_Handling_Cheat_Sheet.html){target="_blank"}]{.small}
- [[File Upload Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Forgot Password Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Forgot_Password_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Injection Prevention Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Injection_Prevention_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Input Validation Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Input_Validation_Cheat_Sheet.html){target="_blank"}]{.small}
- [[JSON Web Token for Java Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/JSON_Web_Token_for_Java_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Key Management Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Key_Management_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Logging Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Logging_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Mass Assignment Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Mass_Assignment_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Multifactor Authentication Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Multifactor_Authentication_Cheat_Sheet.html){target="_blank"}]{.small}
- [[REST Security Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/REST_Security_Cheat_Sheet.html){target="_blank"}]{.small}
- [[SQL Injection Prevention Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Server Side Request Forgery Prevention Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Server_Side_Request_Forgery_Prevention_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Unvalidated Redirects and Forwards Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html){target="_blank"}]{.small}
- [[User Privacy Protection Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/User_Privacy_Protection_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Vulnerability Disclosure Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Vulnerability_Disclosure_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Vulnerable Dependency Management Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Vulnerable_Dependency_Management_Cheat_Sheet.html){target="_blank"}]{.small}
- [[Web Service Security Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Web_Service_Security_Cheat_Sheet.html){target="_blank"}]{.small}
- [[XML External Entity Prevention Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/XML_External_Entity_Prevention_Cheat_Sheet.html){target="_blank"}]{.small}
- [[XS Leaks Cheat
  Sheet](https://cheatsheetseries.owasp.org/cheatsheets/XS_Leaks_Cheat_Sheet.html){target="_blank"}]{.small}
:::

::: {#sec-ctf .section .page-body .tab-hidden}

------------------------------------------------------------------------

## CTF Extension {#ctf-extension}

![Juice Shop CTF
Logo](../../raw.githubusercontent.com/juice-shop/juice-shop-ctf/master/images/JuiceShopCTF_Logo_100px.png)

[![GitHub
release](https://img.shields.io/github/release/juice-shop/juice-shop-ctf.svg)](https://github.com/juice-shop/juice-shop-ctf/releases/latest)
[![GitHub
stars](https://img.shields.io/github/stars/juice-shop/juice-shop-ctf.svg?label=GitHub%20%E2%98%85&style=flat)](https://github.com/juice-shop/juice-shop-ctf)

The Node package [`juice-shop-ctf-cli`{.language-plaintext
.highlighter-rouge}](https://www.npmjs.com/package/juice-shop-ctf-cli)
helps you to prepare [Capture the
Flag](https://en.wikipedia.org/wiki/Capture_the_flag#Computer_security)
events with the OWASP Juice Shop challenges for different popular CTF
frameworks. This interactive utility allows you to populate a CTF game
server in a matter of minutes.

![Juice Shop CLI in
Powershell](../../raw.githubusercontent.com/juice-shop/juice-shop-ctf/master/images/juice-shop-ctf-cli.png)

### Supported CTF Frameworks

The following open source CTF frameworks are supported by
`juice-shop-ctf-cli`{.language-plaintext .highlighter-rouge}:

- [CTFd](https://github.com/CTFd/CTFd)
- [FBCTF](https://github.com/facebook/fbctf)
- [RootTheBox](https://github.com/moloch--/RootTheBox)
:::

::::: {#sec-ecosystem .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Official Companion Guide

[![Write Goodreads
Review](https://img.shields.io/badge/goodreads-write%20review-47129532.svg)](https://www.goodreads.com/review/edit/47129532)

[Pwning OWASP Juice Shop](https://leanpub.com/juice-shop) is the
official companion guide for this project. It will give you a complete
overview of the vulnerabilities found in the application including hints
how to spot and exploit them. In the appendix you will even find
complete step-by-step solutions to every challenge.

[![Pwning OWASP Juice Shop
cover](../../raw.githubusercontent.com/juice-shop/pwning-juice-shop/master/docs/modules/ROOT/assets/images/cover.jpg){width="250"}](https://leanpub.com/juice-shop)
[![Pwning OWASP Juice Shop back
cover](../../raw.githubusercontent.com/juice-shop/pwning-juice-shop/master/docs/modules/ROOT/assets/images/introduction/back.jpg){width="250"}](https://leanpub.com/juice-shop)

The ebook is published under [CC BY-NC-ND
4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/) and is
online-readable **for free** at
[https://pwning.owasp-juice.shop](https://pwning.owasp-juice.shop/). The
latest officially released edition is also available **for free** at
<https://leanpub.com/juice-shop> in PDF, Kindle and ePub format.

## Official Multi User Platform

[![MultiJuicer
Logo](../../raw.githubusercontent.com/juice-shop/multi-juicer/master/images/multijuicer-with-text.png)](https://github.com/juice-shop/multi-juicer)

Multi User Juice Shop Platform to run separate Juice Shop instances for
training or CTF participants on a central Kubernetes cluster.
[MultiJuicer](https://github.com/juice-shop/multi-juicer) comes with a
built-in leader board and its own dedicated Juice Balancer for instance
isolation.

## Official Jingle

Official [OWASP Juice Shop
Jingle](https://soundcloud.com/braimee/owasp-juice-shop-jingle) written
and performed by [Brian Johnson](https://github.com/braimee)

:::: iframe
::: {#widget .widget .g-background-default .g-shadow-inset style="height:100%"}
:::
::::

## Endorsed Open Source Projects

  Project                                       Description
  --------------------------------------------- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  <https://github.com/wurstbrot/shake-logger>   Demo to show the dangers of XSS holes combined with bad Content Security Policy using Harlem Shake and a Keylogger against the Juice Shop ([📺YouTube](https://youtu.be/Msi52Kicb-w))

*The tools listed above are provided by third parties outside the OWASP
Juice Shop project scope. For support or feature requests please use the
support channels or issue trackers mentioned by these projects.*
:::::

::: {#sec-supporters .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Project Supporters

> You can attribute your donation to the OWASP Juice Shop project by
> using [this
> link](../donate/indexf7e4.html?reponame=www-project-juice-shop&title=OWASP+Juice+Shop)
> or the green "Donate"-button while on any tab of the Juice Shop
> project page!

### Top Supporters

[![Your company
name](assets/images/yourlogo_logo.png)](index.html#div-supporters)

[[*In order to be recognized as a "Top Supporter" a company must have
donated \$1000 or more a) to OWASP while attributing it to Juice Shop or
b) as a restricted gift to OWASP Juice Shop in the last 12
months.*]{.small}]{.small}

#### All Corporate Supporters

- [secuvera](https://www.secuvera.de/)^(2018/2019/2023)^
- [mindsetters OG](https://www.mindsetters.com/)^(2023)^
- [Heyhack](https://heyhack.com/)^(2022)^
- [Schutzwerk](https://www.schutzwerk.com/)^(2022)^
- [New Work
  SE](https://www.new-work.se/en/about-new-work-se)^(2019/2021)^
- [RandoriSec](https://randorisec.fr/)^(2021)^
- [Wild West Hackin' Fest](https://wildwesthackinfest.com/)^(2020)^
- [Denim Group](http://www.denimgroup.com/)^(2018-2019)^
- [PlexTrac](https://plextrac.com/)^(2019)^
- [Silpion](https://silpion.de/)^(2019)^
- [iteratec](https://www.iteratec.de/)^(2017)^
- [eSailors](https://www.esailors.de/)^(2016)^
- [XING](https://corporate.xing.com/en/about-xing/security/)^(2016)^

#### All Individual Supporters

- Björn Kimminich

- Jeroen Willemsen

- Soron Foster

- Bendik Mjaaland

- Timo Pagel

- Benjamin Pfänder

- Kevin Chung

- Brian Johnson

- Omar Santos

- Merlyn Albery

- Alper Basaran

- Jediah Logiodice

- Kenyo Kaneda

- Ian Sexton

- [\[email protected\]](../cdn-cgi/l/email-protection.html){.__cf_email__
  cfemail="0c7e6d756b6d6b6263623e3c3e394c6b616d6560226f6361"}

- *You want to appear on this list?* [Donate to OWASP here!
  🤲](../donate/indexf7e4.html?reponame=www-project-juice-shop&title=OWASP+Juice+Shop)

#### All Corporate-sponsored Code Contributions

- [#1221](https://github.com/juice-shop/juice-shop/pull/1221),
  [#1356](https://github.com/juice-shop/juice-shop/pull/1356):
  [Panasonic Information Systems Company
  Europe](https://application.job.panasonic.eu/data/ruP0pHQvHrGZJKvL/rc.php?nav=jobsearch&custval12=ite&lang=EN&custval11=PBSEU_GER)^(2019-2020)^

[[*In order to be recognized as a "Corporate-sponsored Code
Contribution" an official written confirmation of waiving all IP to the
contributed code must be formally submitted to the OWASP
Foundation.*]{.small}]{.small}

#### LeanPub Royalties

[![Pwning OWASP Juice
Shop](../../raw.githubusercontent.com/juice-shop/pwning-juice-shop/master/docs/modules/ROOT/assets/images/cover.jpg){width="250"}](https://leanpub.com/juice-shop)

\$1,251.68 of royalties from [Björn Kimminich](https://kimminich.de/)'s
eBook have been donated to the project between 09/2017 and 07/2019.

#### MultiJuicer Maintenance

MultiJuicer was originally developed (and is still maintained primarily)
by [iteratec](https://www.iteratec.com/en/). It became an official part
of the OWASP Juice Shop project 05/2023.

![iteratec](assets/images/iteratec-logo.png)

------------------------------------------------------------------------

*The OWASP Foundation is very grateful for the support by the
individuals and organizations listed. However, please note, the OWASP
Foundation is strictly vendor neutral and does not endorse any of its
supporters.*
:::
:::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/bkimminich/juice-shop/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/bkimminich/juice-shop){.github-button
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

-  [Flagship Project]{style="font-size: 1.3em;"}

#### Classification

-  Tool

#### Audience

-  Builder
-  Breaker
-  Defender

### Installation

- [From Source](https://github.com/juice-shop/juice-shop#from-sources)
- Packaged
  ([GitHub](https://github.com/juice-shop/juice-shop/releases/)/[SourceForge](https://sourceforge.net/projects/juice-shop/files/))
- [Docker Image](https://hub.docker.com/r/bkimminich/juice-shop)

### Sources

- [GitHub](https://github.com/juice-shop/juice-shop)
- [CTF Extension (GitHub)](https://github.com/juice-shop/juice-shop-ctf)
- [MultiJuicer (GitHub)](https://github.com/juice-shop/multi-juicer)
- [Crowdin I18N](https://crowdin.com/project/owasp-juice-shop)

### Documentation

- [Online Demo](https://juice-shop.herokuapp.com/)
- [Introduction Slides](https://juice-shop.github.io/juice-shop)
- Companion Guide
  ([LeanPub](https://leanpub.com/juice-shop)/[Online](https://pwning.owasp-juice.shop/))

### Community

- Chat
  ([Gitter](https://gitter.im/bkimminich/juice-shop)/[Matrix](https://matrix.to/#/#bkimminich_juice-shop:gitter.im))
- [Subreddit](https://www.reddit.com/r/owasp_juiceshop)
- [Slack Channel](https://owasp.slack.com/messages/project-juiceshop)
  ([Self-registration](../slack/invite.html))
- [Google
  Group](https://groups.google.com/a/owasp.org/forum/#!forum/juice-shop-project)

### Statistics

- [Daily Project Stats](https://stats.owasp-juice.shop/)

### Social Media

- [BlueSky](https://bsky.app/profile/owasp-juice.shop)
- [Twitter/X](https://twitter.com/owasp_juiceshop)
- [Mastodon](https://fosstodon.org/@owasp_juiceshop){rel="me"}
- [Facebook](https://www.facebook.com/owasp.juiceshop)
- [YouTube](https://www.youtube.com/channel/UCjkQ1Y-bxYAqwwD1SyQpBvw/playlists)

### Merchandise

- [OpenSea](https://opensea.io/collection/juice-shop)
- [StickerYou](https://www.stickeryou.com/products/owasp-juice-shop/794)
- SpreadShirt
  ([US](https://shop.spreadshirt.com/juiceshop)/[DE](https://shop.spreadshirt.de/juiceshop))

### Leaders

- [Bjoern
  Kimminich](../cdn-cgi/l/email-protection.html#d9bbb3b6bcabb7f7b2b0b4b4b0b7b0bab199b6aeb8aaa9f7b6abbe)
- [Jannik
  Hollenbach](../cdn-cgi/l/email-protection.html#a8c2c9c6c6c1c386c0c7c4c4cdc6cac9cbc0e8c7dfc9dbd886c7dacf)

![Bjoern\'s GitHub
stats](https://github-readme-stats.vercel.app/api?username=bkimminich&show_icons=true)
![Jannik\'s GitHub
stats](https://github-readme-stats.vercel.app/api?username=J12934&show_icons=true)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::::::::
