:::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Rules](#div-rules){#rules-link .tab-link role="tab"
  aria-selected="false" aria-controls="rules"}
- [Online Version](#div-online){#online-link .tab-link role="tab"
  aria-selected="false" aria-controls="online"}
- [Printed Cards](#div-printed){#printed-link .tab-link role="tab"
  aria-selected="false" aria-controls="printed"}
- [Media](#div-media){#media-link .tab-link role="tab"
  aria-selected="false" aria-controls="media"}
- [Contribute](#div-contribute){#contribute-link .tab-link role="tab"
  aria-selected="false" aria-controls="contribute"}

# OWASP Cumulus {#owasp-cumulus .page-title}

::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
[⤓
Download](https://github.com/OWASP/cumulus/releases/latest){.cta-button
.green style="float:right"}

# *Threat modeling the clouds*

![Cumulus Cards](assets/images/cards.svg)

Cumulus is the easy way to bring security into cloud and devOps teams.

As a variant of the card game Elevation of Privilege it follows the idea
to threat model a system via gamification. This lightweight and
low-barrier approach helps you find threats to your devOps or cloud
project and teaches the developers a security oriented mindset.

Find the latest release
[here](https://github.com/OWASP/cumulus/releases/latest).

## Threat Modeling

The idea of threat modeling via serious games goes back to the card game
[Elevation of
Privilege](https://shostack.org/games/elevation-of-privilege) by [Adam
Shostack](https://github.com/adamshostack). The basic idea is to bring
the developers on a table and get them start discussing the security of
their system. For this, a card game serves as a guide through a
catalogue of threats. It is designed to be low-barrier and naturally
embeddable within agile development processes.

While the original game approaches security in general and another
variant, Cornucopia by the OWASP Foundation, targets (web) application
security in particular, we had the feeling that the specific needs of
devOps team working in cloud environments have been missing. Cumulus
seeks to fill this gap and provides a custom card deck with threats to
cloud systems.

Threats are classified into the categories (which are also the suits in
this game):

  Category            
  ------------------ -----------------------------------------------
  Access & Secrets   Threats related to IAM and secrets management
  Delivery           Build and ship software, and its supply chain
  Recovery           Backup and restore
  Monitoring         Logs, alerts and traceability
  Resources          Threats on resources and their configuration

This game does explicitly **not** try to replace Elevation of Privilege
or Cornucopia. It should rather be seen as part of a triplet of threat
modeling card decks, reflecting different aspects of modern software
development projects.

## Acknowledgements

Cumulus was started at and it heavily supported by [TNG Technology
Consulting](https://www.tngtech.com/en/index.html).

The original and wonderful idea of conducting threat modeling via
serious games goes back to [Adam
Shostack](https://github.com/adamshostack), working for Microsoft at
that time. He invented the game [Elevation of
Privilege](https://shostack.org/games/elevation-of-privilege) which is
the blue print for Cumulus.

Another great game following Elevation of Privilege's approach to threat
modeling is [Cornucopia](../www-project-cornucopia/index.html) developed
by the [OWASP Foundation](../index.html).

Both card games are great tools to help development teams increase the
security of the system they are building.

However, we felt the need for a threat modeling card game targeting
devOps/cloud projects in particular. Out of this idea, Cumulus arose.

## Versioning

The card deck follows [semantic versioning](https://semver.org/).
Version changes mean:

- *patch version*: Non-semantic changes: layout, typos, minor
  re-wordings, ...
- *minor version*: Semantic changes: rephrasings, additional cards...
- *major version*: Substantial semantic changes: new categories, ...

## Licensing

The card game (including the threat formulations and the released PDF)
files are distributed under
[CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/). When
distributing this game, mentioning [TNG Technology
Consulting](https://www.tngtech.com/en/index.html) is highly
appreciated.
:::

::: {#sec-rules .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Rules of the game

Cumulus ist trick-taking card game, similar to spades.

The objective is to collect as many points as possible, either by taking
a trick or by finding threats. At the end of the game the winner is the
player with the most points.

In preparation of the game a system model, e.g. an architectural
overview, is generated. Ideally, this is in the form of a data flow
diagram, but in the end every overview which is understood by the
players is fine. Additionally, the players agree on a starting suit,
i.e. a threat category.

After distributing the cards amongst the players, the game starts. The
first dealer is the player holding the lowest card in the starting suit.
The dealer plays a card in the starting suit. Each of the other players
has to follow the suit during that round. If that is not possible, the
player can choose any card on hand. The winner of the round takes the
trick and is the one who played the highest value card in the round's
suit or the highest trump card.

Trumps are cards from the suit **access & secrets**.

The winner then receives a point, starts a new round and chooses the new
suit. Each time a new card is played, all players are asked to think
about whether that particular threat, mentioned on the current card,
applies to their system in some form. If a threat is found (and the team
agrees that this is a topic to look at), it is written down and the
finder receives an extra point.

As Cumulus shares the same rules as Elevation of Privilege and
Cornucopia, you can find alternative explanations of the rules
[here](../www-project-cornucopia/index.html) or [here, chapter
2](http://download.microsoft.com/download/F/A/E/FAE1434F-6D22-4581-9804-8B60C04354E4/EoP_Whitepaper.pdf)

Also, Cornucopia has a wonderful explanation of the rules as a [Video on
YouTube](https://www.youtube.com/watch?app=desktop&v=XXTPXozIHow&ab_channel=OWASPFoundation).
:::

::: {#sec-online .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Online Version

We also maintain an online version of Cumulus, which you can easily host
yourselves. It can be found at

<https://github.com/tng/elevation-of-privilege>
:::

::: {#sec-printed .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Printed Cards

Printed versions of the cards are available at [Agile
Stationary](https://agilestationery.com/collections/threat-modeling).

If you want to print them yourselves, the
[download](https://github.com/OWASP/cumulus/releases/latest) also
contains printer-friendly versions.
:::

::: {#sec-media .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Cumulus in Media

- 2025-05-29: Cumulus was presented at the OWASP Global AppSec
  Conference in Barcelona:
  [Slides](assets/pdf/20250529_OWASPGlobalAppSec_Cumulus.pdf)
- 2025-05-20: [Threat Modeling Connect
  Spieleabend](https://lu.ma/njsexjws):
  [Slides](assets/pdf/20250520_TMC-DACH.pdf) *(in German)*
- 2025-03-25: Interview about Cumulus in the [Medical Device
  Cybersecurity Podcast](https://youtu.be/aMpIgmX9WZQ).
- 2023-12-14: The c't magazine features an article about DevOps security
  and Cumulus:
  - [IT-Sicherheit: Eine Security-Einführung für
    DevOps-Teams](https://heise.de/-9573277) (German, behind paywall)
- 2023-04-06: Cumulus appears in [Adam Shostack's
  blog](https://shostack.org/blog/cumulus-threat-model-thursday/)
:::

::: {#sec-contribute .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Contribute

Contributions to Cumulus are very much appreciated. In the end, this
card deck is intended to be a community project. It should change and
evolve in the same pace as cloud technologies and their particular
security requirements change.

### Review and discuss

Feedback, reviews and other opinions are very welcome. This card game is
only as helpful as its threats are relevant. Let's work together to
constantly improve the cards!

The best way is to simply create an
[issue](https://github.com/OWASP/cumulus/issues) to start a discussion.
But you can also reach out to the project leads.

### Contribute to the cards

Changes to the threat formulations are welcome as pull requests to
[cards.tex](https://github.com/OWASP/cumulus/blob/main/cards.tex).

### Contribute to documentation

When writing the threats we tried to condense each security issue into a
single sentence. Although a sufficiently general (but maybe also vague)
formulation can foster discussions, it can also hinder beginners to
understand the threats. We would love to provide further explanations
and examples to the cards.

Help (in the form of formulating explanations or giving real-world
examples) are very much appreciated. Just contact the project leads.
:::
:::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-cumulus/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-cumulus){.github-button
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

### Cumulus Information

-  Lab Project

#### Classification

- [Documentation]{style="font-size:1.0em;padding-left:12px;"}

#### Audience

- [Builder]{style="font-size:1.0em;padding-left:12px;"}
- [Defender]{style="font-size:1.0em;padding-left:12px;"}

### Downloads

- [Download](https://github.com/OWASP/cumulus/releases/latest)

### Code Repository

- [GitHub](https://github.com/OWASP/cumulus)

### Change Log

- [Changes](https://github.com/OWASP/cumulus/releases)

### License

- [![CC BY
  4.0](../../licensebuttons.net/l/by/4.0/80x15.png)](https://creativecommons.org/licenses/by/4.0/)

### Supporters

- [![TNG Technology
  Consulting](assets/images/TNG_Logo.svg)](https://www.tngtech.com/en/index.html)

### Leaders

- [Christoph
  Niehoff](../cdn-cgi/l/email-protection.html#600308120913140f10084e0e0905080f0606200f170113104e0f1207)
- [Benjamin
  Goose](../cdn-cgi/l/email-protection.html#f69493989c979b9f98d89199998593b69981978586d8998491)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::::
