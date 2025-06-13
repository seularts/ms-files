::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Past Events](#div-pastevents){#pastevents-link .tab-link role="tab"
  aria-selected="false" aria-controls="pastevents"}

# OWASP Salt Lake City {#owasp-salt-lake-city .page-title}

:::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
## Welcome

Welcome to the OWASP Salt Lake City Chapter (aka your local appsec
support group). We try to meet most months and we plan to alternate
between virtual and in person meetings.

- Join us at our upcoming chapter meetings (RSVP for upcoming events
  through our [meetup page](https://meetup.com/owasp-slc/))
- Chat with us on
  [Slack](https://join.slack.com/t/wasatchappsec/shared_invite/zt-1wgxnyqpt-FgwaUExorcc3o5gbdpFdhw)
- Follow us on Twitter

## Upcoming Event(s)

- February's event will probably be virtual, date and topic TBD

## Recent Events

### January 22, 2025

- Met at HealthEquity's Draper office
- Talked about Tanya Janca's Alice and Bob Learn Application Security
  book
- Should threat models require approval? By whom?
- How does Tanya's advice that devs not use the first result from
  StackExchange (since it is probably the least secure) change, if at
  all, with recent developments in AI for code generation?

### September 26, 2024

- Met at Aumni's Cottonwood Heights office
- Talked about SDLC
- How do you move fast without breaking things
- You can only fix security bugs as fast as you can release
- Talked about passing the torch to new group leaders

### May 29, 2024

- Met at Murray Park
- Talked about AI helping us to automate our AppSec jobs by assisting us
  in performing code reviews or threat modeling.
- Challenges of getting deterministic results that are accurate.
- Small Language Models (see Louis Barrett's talk from LASCON).

### April 25, 2024

- Met at HealthEquity's office
- We talked about the book Nine Lies About Work and how it can relate to
  AppSec and working with Security Champions and Developers.
- Talked about doing "Bug of the Month" to help raise awareness.
- Thinking about Lie #8, we discussed how developers love solving
  problems so try to leverage that for your AppSec program.

### March 20th, 2024

- Virtual meet up
- We talked about using HMACs in various situations vs other solutions
- We also talked about envelop encryption and using it to encrypt
  specific fields in a database

## Participation

The Open Web Application Security Project (OWASP) is a nonprofit
foundation that works to improve the security of software. All of our
projects ,tools, documents, forums, and chapters are free and open to
anyone interested in improving application security.

Chapters are led by local leaders in accordance with the [Chapter Leader
Handbook](https://owasp.org/www-policy/rules-of-procedure/chapter-handbook).
Financial contributions should only be made online using the authorized
online donation button. To be a SPEAKER at ANY OWASP Chapter in the
world simply review the [speaker
agreement](https://owasp.org/www-policy/speaker-agreement) and then
contact the local chapter leader with details of what OWASP Project,
independent research, or related software security topic you would like
to present.

Everyone is welcome and encouraged to participate in our
[Projects](https://owasp.org/projects), [Local
Chapters](https://owasp.org/chapters),
[Events](https://owasp.org/events), [Online
Groups](https://groups.google.com/a/owasp.com/){target="_blank"}, and
[Community Slack Channel](https://owasp.slack.com/){target="_blank"}. We
especially encourage diversity in all our initiatives. OWASP is a
fantastic place to learn about application security, to network, and
even to build your reputation as an expert. We also encourage you to be
[become a member](https://owasp.org/membership) or consider a
[donation](https://owasp.org/donate) to support our ongoing work.
:::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

Put whatever you like here: news, screenshots, features, supporters, or
remove this file and don't use tabs at all.
:::

::: {#sec-pastevents .section .page-body .tab-hidden}

------------------------------------------------------------------------

# Past Events

See all [recent events in
MeetUp](https://www.meetup.com/owasp-slc/events/past/).

## September 21st, 2023

- In person at Weave in Lehi
- Seth Law presented on Modern vs Old 5k00l AppSec
- Some key points were
  - Ware report from 1970 and how many of the same issues (usually with
    different names) still exist today
  - AppSec is not a "point solution" in that you can't just implement a
    SAST/DAST tool and think it is solved

## August 30th, 2023

- Virtual
- Testing with Nuclei - Justin
- Risk assessments and threat modeling - Mark

## May 25th, 2023

- in person (park)
- Book Club: Discuss Project Zero Trust ([goodreads
  link](https://www.goodreads.com/book/show/60659055-project-zero-trust))

## April 27th, 2023 - virtual

- Mike McCabe spoke to us about Terraform and Infrastructure as Code
  security

## March 30th, 2023 - In person at Salt Lake County building

- How to Measure Anything in CyberSecurity
- How do you calculate the likelihood of an incident occuring?
- Use the Monte Carlo method to understand annual loss expectancy
- https://docs.google.com/spreadsheets/d/1if1MTESnwY31_Qm4MfPnUZrl4GtP0toRG8xS2OZIXfQ/edit?usp=sharing
- You need to cater your presentation to your audience; some folks like
  critical/high/medium/low classifications, some might want \$ amounts
  like annual loss expectancy

## February 23rd, 2023 - virtual

- Talked mainly about metrics
  - How do you show value to your leadership (finding bugs earlier in
    SDLC and fixing them quicker; show value in \$ of saved engineer
    time, customer happiness)
  - Mentioned Doug Hubbard's (the author) book on How to Measure
    Anything in Cybersecurity
  - Success stories

## January 24th, 2023 - In person at HealthEquity

- HealthEquity hosted an onsite meet-up in Draper.
- We discussed third party scripts and how to secure them:
  - Discussed use of SRI for versioned scripts and how a CSP offers
    partial protection for dynamic scripts that can't be protected via
    SRI (primarily by preventing an attacker from including scripts from
    domains not allowed on the CSP).
  - Some script vendors are so big (e.g., Google) that if they were
    compromised, your company probably wouldn't be in the news even from
    the downstream impact, but if your script vendor is smaller and your
    data is sensitive, you could be the headline.
  - Limiting these types of risky scripts to less-used pages or only
    loading them when the user wants to use the functionality could help
    limit impact.
  - Other potential solutions include scanning the scripts (before as a
    preventive solution or even after as a detective solution \[Seth had
    a solution along these lines\]), using iframes, and/or using a tool
    like feroot.

## August 25, 2022 - Tokens

- Talked about all the various kinds of tokens in use in web
  applications; used to primarily be session cookies, but now there are
  refresh, access, JWT, bearer, self-contained tokens and more.
- Talked about maintaining the controls of immediately logging out users
  and logging out any other sessions of a particular account when their
  password is changed. This is trickier in a microservices architecture
  that relies on self-contained and non-revokable access tokens to be
  performant. Solutions include managing expectations by telling
  partners and penetration testers that your access tokens will stay
  alive up to 5-10 minutes (or whatever you set their expiration to be)
  even after the session is destroyed. Also talked about setting up a
  revoked list that would have to be disseminated to all microservices
  in some way (list should be short if it is only users who click the
  log out button or other user sessions when a user changes their
  password and the list can be purged once the tokens expire naturally
  anyway).

## February 22, 2022 - Mobile App Pen testing

- It's getting harder (to jailbreak and analyze)
- [Pentesting iOS without a
  jailbreak](https://medium.com/securing/pentesting-ios-apps-without-jailbreak-91809d23f64e)
- Many vulnerabilities are actually with the APIs mobile apps utilize
- [Proxyman.io](https://proxyman.io/)

## Thursday, January 12

- Developer Training
- Round Table Discussion

## November 22nd and talked about:

- OWASP's new [Top 10](https://owasp.org/Top10/) 2021
- OWASP Top 10 is almost entirely categories now with SSRF the last Top
  10 that sounds like a single vulnerability; most are collections of
  dozens of CWEs
- XSS is now part of the broad injection category, but in some ways, a
  lot of these could be linked into even broader categories in the same
  way; there's a lot of overlap as illustrated by a [venn
  diagram](https://www.owasptopten.org/thedata) that was shared, but it
  was for the 2017 Top 10
- Lots of company's use OWASP Top 10 for training
- Top 10 can also be used for threat modeling/checklists or as a way to
  check tool/process coverage (e.g., does tool X find OWASP Top 10 A??)

## September 29, 2021

- Career progression in AppSec (from entry level up to technical tracks
  and management),
- How participating in conferences and events (e.g., CTF) can help entry
  level candidates,
- Impostor syndrom is common in this industry and we all often have to
  look things up or refresh our memory or learn something new,
- How technical leaders provide value by "scaling their services"
  (helping others be more effective).
:::
::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-chapter-salt-lake-city/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-chapter-salt-lake-city){.github-button
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

### Chapter Information

- Salt Lake City Metro Area

### Social Links

- [Meetup](https://www.meetup.com/owasp-slc/)
- [Slack](https://join.slack.com/t/wasatchappsec/shared_invite/zt-1wgxnyqpt-FgwaUExorcc3o5gbdpFdhw)
- Twitter
- [\@sethlaw](https://twitter.com/sethlaw)

### Leaders

- [Seth
  Law](https://owasp.org/cdn-cgi/l/email-protection#3c4f59485412505d4b7c534b5d4f4c12534e5b)
- [Cameron
  White](https://owasp.org/www-chapter-salt-lake-city/cameron.white@owasp.org)
- [Steve
  Christiaens](https://owasp.org/cdn-cgi/l/email-protection#26555243504308454e544f55524f4743485566495147555608495441)
- [Jason
  Wood](https://owasp.org/cdn-cgi/l/email-protection#7d171c0e1213530a1212193d120a1c0e0d53120f1a)
- [Doug
  Hubbard](https://owasp.org/cdn-cgi/l/email-protection#a7c3c8d2c089cfd2c5c5c6d5c3e7c8d0c6d4d789c8d5c0)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::
