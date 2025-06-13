::::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Overview](#div-overview){#overview-link .tab-link role="tab"
  aria-selected="false" aria-controls="overview"}
- [CTF](#div-ctf){#ctf-link .tab-link role="tab" aria-selected="false"
  aria-controls="ctf"}
- [webdesktop](#div-webdesktop){#webdesktop-link .tab-link role="tab"
  aria-selected="false" aria-controls="webdesktop"}
- [passwords](#div-passwords){#passwords-link .tab-link role="tab"
  aria-selected="false" aria-controls="passwords"}

# OWASP WrongSecrets {#owasp-wrongsecrets .page-title}

:::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::: {#sec-main .section .page-body}
![logo by Ben de Haan](assets/images/icon.png){width="100px"}

[![Github
Stars](https://img.shields.io/github/stars/OWASP/wrongsecrets?label=Stars%20WrongSecrets&style=social)](https://github.com/OWASP/wrongsecrets/stargazers)
[![OWASP Production
Project](https://img.shields.io/badge/OWASP-production%20project-48A646.svg)](../projects/index.html)
[![Release
version](https://img.shields.io/github/v/release/OWASP/wrongsecrets)](https://github.com/OWASP/wrongsecrets/releases/latest)
[![OpenSSF Best
Practices](https://bestpractices.coreinfrastructure.org/projects/7024/badge)](https://bestpractices.coreinfrastructure.org/projects/7024)
[![Docker
pulls](https://img.shields.io/docker/pulls/jeroenwillemsen/wrongsecrets.svg)](https://hub.docker.com/r/jeroenwillemsen/wrongsecrets)
[![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=Want%20to%20dive%20into%20secrets%20management%20and%20do%20some%20hunting?%20try%20this&url=https://github.com/OWASP/wrongsecrets&hashtags=secretsmanagement,secrets,hunting,p0wnableapp,OWASP,WrongSecrets)
[![](https://img.shields.io/badge/-MASTODON-%232B90D9?style=for-the-badge&logo=mastodon&logoColor=white){width="86"}](https://tootpick.org/#text=Want%20to%20dive%20into%20secrets%20management%20and%20do%20some%20hunting?%20try%20this%0A%0Ahttps://github.com/OWASP/wrongsecrets%20%23secretsmanagement,%20%23secrets,%20%23hunting,%20%23p0wnableapp,%20%23OWASP,%20%23WrongSecrets)

OWASP WrongSecrets is the first Secrets Management-focused
vulnerable/p0wnable app! It can be used as a stand-alone game, as part
of security trainings, awareness demos, as a test environment for secret
detection tools, and bad practice detection tooling. It even has a
supporting CTF platform to play the game in a larger group.

Want to give it a shot? Go to [our demo environment running on
Heroku](https://www.wrongsecrets.com/).

![Image](../../raw.githubusercontent.com/OWASP/wrongsecrets/master/images/screenshot.png)

## Description

WrongSecrets is based on Java, Docker, Terraform, and a bit of scripting
fun. It contains more than 50 exercises with various wrongly stored or
misconfigured secrets - which you need to find. Finding these secrets
will

- Help you to look for secrets being misconfigured at your own
  environment, or target environments for bug bounties.
- Help you to re-evaluate your own secrets management practices as well.

## Want to play?

There are multiple ways on how you can play/work with OWASP
WrongSecrets. Want to play locally? Try

:::: {.language-sh .highlighter-rouge}
::: highlight
``` highlight
docker run -p 8080:8080  jeroenwillemsen/wrongsecrets:latest-no-vault
```
:::
::::

Otherwise, try one of the following online environments:

- [Online demo env
  (Heroku)](https://wrongsecrets.herokuapp.com/ "Online demo on a Heroku Dyno")
- [Online CTF demo
  (Heroku)](https://wrongsecrets-ctf.herokuapp.com/ "Online CTF demo on a Heroku Dyno")

Or try to deploy it using free services:

[![Deploy to
Render](https://render.com/images/deploy-to-render-button.svg)](https://render.com/deploy?repo=https://github.com/OWASP/wrongsecrets)

[![Deploy on
Railway](assets/images/railway-button.svg)](https://railway.app/new/template/7pnwRj)

## Contributors

[![GitHub contributors
WrongSecrets](https://img.shields.io/github/contributors/OWASP/Wrongsecrets?label=Contributors%20WrongSecrets)](https://github.com/OWASP/wrongsecrets/graphs/contributors)
[![GitHub contributors
WrongSecrets-ctf-party](https://img.shields.io/github/contributors/OWASP/Wrongsecrets-ctf-party?label=Contributors%20WrongSecrets-ctf-party)](https://github.com/OWASP/wrongsecrets-ctf-party/graphs/contributors)
[![GitHub contributors
WrongSecrets-binaries](https://img.shields.io/github/contributors/OWASP/Wrongsecrets-binaries?label=Contributors%20WrongSecrets-binaries)](https://github.com/OWASP/wrongsecrets-binaries/graphs/contributors)

Leaders:

- [Ben de Haan \@bendehaan](https://www.github.com/bendehaan)
- [Jeroen Willemsen \@commjoen](https://www.github.com/commjoen)

Top contributors:

- [Jannik Hollenbach \@J12934](https://www.github.com/J12934)
- [Puneeth Y \@puneeth072003](https://www.github.com/puneeth072003)
- [Joss Sparkes \@RemakingEden](https://www.github.com/RemakingEden)

Contributors:

- [Nanne Baars \@nbaars](https://www.github.com/nbaars)
- [Marcin Nowak \@drnow4u](https://www.github.com/drnow4u)
- [Rodolfo Neves \@roddas](https://www.github.com/roddas)
- [Osama Magdy \@osamamagdy](https://www.github.com/osamamagdy)
- [Pastekitoo \@Pastekitoo](https://www.github.com/Pastekitoo)
- [Shubham Patel
  \@Shubham-Patel07](https://www.github.com/Shubham-Patel07)
- [za \@za](https://www.github.com/za)
- [Divyanshu Dev \@Novice-expert](https://www.github.com/Novice-expert)
- [Tibor Hercz \@tiborhercz](https://www.github.com/tiborhercz)
- [Chris Elbring Jr. \@neatzsche](https://www.github.com/neatzsche)
- [Adarsh A \@adarsh-a-tw](https://www.github.com/adarsh-a-tw)
- [Diamond Rivero \@diamant3](https://www.github.com/diamant3)
- [Norbert Wolniak \@nwolniak](https://www.github.com/nwolniak)
- [Filip Chyla \@fchyla](https://www.github.com/fchyla)
- [Dmitry Litosh \@Dlitosh](https://www.github.com/Dlitosh)
- [Vineeth Jagadeesh \@djvinnie](https://www.github.com/djvinnie)
- [Mahaputra Ilham Awal
  \@mahaputrailhamawal](https://www.github.com/mahaputrailhamawal)
- [Turjo Chowdhury \@turjoc120](https://www.github.com/turjoc120)
- [SndR \@SndR85](https://www.github.com/SndR85)
- [Josh Grossman \@tghosth](https://www.github.com/tghosth)
- [alphasec \@alphasecio](https://www.github.com/alphasecio)
- [CaduRoriz \@CaduRoriz](https://www.github.com/CaduRoriz)
- [Madhu Akula \@madhuakula](https://www.github.com/madhuakula)
- [Mike Woudenberg
  \@mikewoudenberg](https://www.github.com/mikewoudenberg)
- [Spyros \@northdpole](https://www.github.com/northdpole)
- [RubenAtBinx \@RubenAtBinx](https://www.github.com/RubenAtBinx)
- [Alex Bender \@alex-bender](https://www.github.com/alex-bender)
- [Danny Lloyd \@dannylloyd](https://www.github.com/dannylloyd)
- [Nicolas Humblot \@nhumblot](https://www.github.com/nhumblot)
- [Rick M \@kingthorin](https://www.github.com/kingthorin)
- [Shlomo Zalman Heigh \@szh](https://www.github.com/szh)
- [Fern \@f3rn0s](https://www.github.com/f3rn0s)
- [Jeff Tong \@Wind010](https://www.github.com/Wind010)

Testers:

- [Dave van Stein \@davevs](https://www.github.com/davevs)
- [Marcin Nowak \@drnow4u](https://www.github.com/drnow4u)
- [Marc Chang Sing Pang \@mchangsp](https://www.github.com/mchangsp)
- [Vineeth Jagadeesh \@djvinnie](https://www.github.com/djvinnie)

Special thanks:

- [Madhu Akula \@madhuakula
  \@madhuakula](https://www.github.com/madhuakula)
- [Nanne Baars \@nbaars \@nbaars](https://www.github.com/nbaars)
- [Björn Kimminich \@bkimminich](https://www.github.com/bkimminich)
- [Dan Gora \@devsecops](https://www.github.com/devsecops)
- [Xiaolu Dai \@saragluna](https://www.github.com/saragluna)
- [Jonathan Giles \@jonathanGiles](https://www.github.com/jonathanGiles)

### Sponsorships

We would like to thank the following parties for helping us out:

[![gitguardian_logo.png](assets/images/gitguardian_logo.jpg)](https://blog.gitguardian.com/gitguardian-is-proud-sponsor-of-owasp/)

[GitGuardian](https://blog.gitguardian.com/gitguardian-is-proud-sponsor-of-owasp/)
for their sponsorship which allows us to pay the bills for our
cloud-accounts.

[![jetbrains_logo.png](assets/images/jetbrains_logo.png)](https://www.jetbrains.com/)

[Jetbrains](https://www.jetbrains.com/) for licensing an instance of
Intellij IDEA Ultimate edition to the project leads. We could not have
been this fast with the development without it!

[![docker_logo.png](assets/images/docker_logo.png)](https://www.docker.com/)

[Docker](https://www.docker.com/) for granting us their Docker Open
Source Sponsored program.

[![1password_logo.png](assets/images/1password_logo.png)](https://github.com/1Password/1password-teams-open-source/pull/552)

[1Password](https://github.com/1Password/1password-teams-open-source/pull/552)
for granting us an open source license to 1Password for the secret
detection testbed.

[![AWS Open Source](assets/images/aws.svg.png)](https://aws.amazon.com/)

[AWS](https://aws.amazon.com/) for granting us AWS Open Source credits
which we use to test our project and the [Wrongsecrets CTF
Party](https://github.com/OWASP/wrongsecrets-ctf-party) setup on AWS.

#### Individual supporters

- Jeroen Willemsen

- *You want to appear on this list?* [Donate to OWASP here!
  🤲](../donate/indexb1e6.html?reponame=www-project-wrongsecrets&title=OWASP+wrongsecrets)

## Licensing

[![license](https://img.shields.io/github/license/OWASP/wrongsecrets.svg)](https://github.com/OWASP/wrongsecrets/blob/master/LICENSE)

This program is free software: You can redistribute it and/or modify it
under the terms of the [AGPLv3
License](https://github.com/OWASP/wrongsecrets/blob/master/LICENSE).
OWASP WrongSecrets and any contributions are Copyright © by Jeroen
Willemsen & the OWASP WrongSecrets contributors 2020-2025.

## Want to help out?

You can help us in many ways:

- Star us on github: [Star Wrongsecrets on
  Github](https://github.com/OWASP/WrongSecrets){.github-button
  color-scheme="no-preference: light; light: light; dark: light;"
  data-size="large" show-count="true"
  aria-label="Star OWASP/WrongSecrets on GitHub"}
- Promote us using
  [![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=Want%20to%20dive%20into%20secrets%20management%20and%20do%20some%20hunting?%20try%20this&url=https://github.com/OWASP/wrongsecrets&hashtags=secretsmanagement,secrets,hunting,p0wnableapp,OWASP,WrongSecrets)
  [![](https://img.shields.io/badge/-MASTODON-%232B90D9?style=for-the-badge&logo=mastodon&logoColor=white){width="86"}](https://tootpick.org/#text=Want%20to%20dive%20into%20secrets%20management%20and%20do%20some%20hunting?%20try%20this%0A%0Ahttps://github.com/OWASP/wrongsecrets%20%23secretsmanagement,%20%23secrets,%20%23hunting,%20%23p0wnableapp,%20%23OWASP,%20%23WrongSecrets).
- Promote us with a Blog, Vlog, Podcast, or presentation on a
  conference. Or use our materials to organize a CTF! If you do, let us
  know, so we can list your event or publication here on the webiste.
- Work with us on the project! Take a look at the [Readme of the
  project](https://github.com/OWASP/wrongsecrets), [How to
  contribute](https://github.com/OWASP/wrongsecrets/blob/master/CONTRIBUTING.md),
  and the [Github Issues](https://github.com/OWASP/wrongsecrets/issues).
  If you want to contribute to an issue: make sure it is not yet
  assigned to someone, comment on it with your intention, and then we
  can assign it to you.
- [Sponsor our
  project](../donate/indexb1e6.html?reponame=www-project-wrongsecrets&title=OWASP+wrongsecrets)!
  We will use the money for covering our cloud costs (building &
  maintaining the project in 3 clouds costs money). And soon we hope to
  be able to buy you some stickers if you do ;-).

## Presentations about OWASP WrongSecrets

The project has been promoted at:

- [AllDayDevOps: Our secrets management journey from Code to
  Vault](https://www.alldaydevops.com/addo-speakers/jeroen-willemsen)
- [Conf42 DevSecOps 2021: Secrets-management: challenges from code to
  cloud](https://www.youtube.com/watch?v=EsMS7gOBrY4)
- [Club Cloud 2021: Securing your secrets in the
  cloud](https://youtu.be/lXMRTP5eg9Q)
- [OWASP Dutch Chapter Meetup: Our Secrets Management Journey: From Code
  to Vault](https://www.youtube.com/watch?v=qR6JCkZgOlY)
- [Open Security Summit: OWASP Wrong Secrets: project goals, under the
  hood, and where do we go from
  here?](https://www.youtube.com/watch?v=EYkjgGuhOYw)
- [WrongSecrets demo - How not to store secrets with the project founder
  Jeroen Willemsen](https://www.youtube.com/watch?v=nqzxpgvLEv4&t=709s)
- [Security Journey: Jeroen Willemsen and Ben de Haan - Dirty little
  secrets](https://www.youtube.com/watch?v=0HGPnQAYFNY)
- [Meetup OWASP Bay Area: OWASP WrongSecrets: how to NOT mange your
  secrets](https://www.youtube.com/watch?v=oRUPVhp1Bfw)
- [Code to Cloud Virtual Summit: Learn How to (Not) Use Secrets with
  OWASP
  WrongSecrets!](https://start.paloaltonetworks.com/code-to-cloud-summit.html)
- [Teqnation 2022 Utrecht](https://teqnation.com/timetable-2022/)
- [Devops Pro Europe: Introducing OWASP WrongSecrets: How You Should NOT
  Handle Your Secrets](https://devopspro.lt/Jeroen-Willemsen/)
- [OWASP Virtual Appsec Europe 2022: OWASP WrongSecrets: We have a
  secret for
  Everyone!](https://whova.com/web/GKSmlhCK%2FWzBY2c8qqJ+p7kNcnjsUQAQJ+yBsjLrbOo%3D/Agenda)
- [Tweakers Developers Summit: OWASP WrongSecrets - waar je je
  applicatiegeheimen (niet) moet
  neerzetten](https://tweakers.net/partners/devsummit2022/1684/bendehaan/)
- [OWASP Frankfurt #55 In-Person Event: Cloud Secrets,Cyber-Crime &
  Threat Modeling: Can't you keep a secret? Learn Secrets Management
  with OWASP WrongSecrets by Dan Gora, OWASP
  Frankfurt](https://www.meetup.com/nl-NL/it-security-stammtisch-frankfurt-owasp-u-w/events/286925136/)
- OWASP Hamburg Stammtich
- [DevSecOps Days 2022 Washington DC (Virtual): Learn How To (Not) Use
  Secrets With OWASP Wrong
  Secrets!](https://resources.sei.cmu.edu/library/asset-view.cfm?assetid=887917)
  and [see the Youtube recording
  here](https://www.youtube.com/watch?v=bYDnMYkRUN0)
- [AllDayDevOps - Learn how to (not) use secrets with OWASP
  WrongSecrets!](https://www.alldaydevops.com/addo-speakers/jeroen-willemsen)
- [Azure Cloud Security Group - Can't You Keep a Secret ? Cloud Native
  Secrets Management with OWASP Wrong
  Secrets](https://www.youtube.com/watch?v=Aafvip8XGDI)
- [Azure Cloud Security Meetup: Cloud-Native Secrets Management with
  OWASP WrongSecrets by Dan
  Gora](https://www.youtube.com/watch?v=Aafvip8XGDI&t=2505s)
- [OWASP Benelux Days 2022 - CTF
  Kickoff](https://www.owaspbenelux.eu/program/conference#Jeroen-Willemsen-and-Ben-De-Haan)
  with actual [CTF info](https://www.owaspbenelux.eu/program/ctf)
- [WeHackPurple: Don't make the same mistakes we did: How you can do
  secrets management better with OWASP
  WrongSecrets](https://community.wehackpurple.com/events/dont-make-the-same-mistakes-we-did-how-you-can-do-secrets-management-better-with-owasp-wrongsecrets)
- [Open Security Summit: OWASP WrongSecrets a journey into secrets
  management](https://open-security-summit.org/sessions/2024/mini-summits/jan/governance/owasp-wrongsecrets-a-journey-into-secret-management-failures/)
- [Open Security Summit: OWASP WrongSecrets: Define the future
  challenges
  togeter](https://open-security-summit.org/sessions/2024/mini-summits/jan/governance/owasp-wrongsecrets-define-the-future-challenges-together/)
- [Cyberwisecon: OWASP WrongSecrets: How We Keep on Growing Our Open
  Source
  Project](https://events.pinetool.ai/3152/#sessions/102169?referrer%5Bpathname%5D=%2Fsessions&referrer%5Bsearch%5D=&referrer%5Btitle%5D=Sessions)
- [NLUUG: How to (not) Use Secrets with OWASP
  WrongSecrets](https://nluug.nl/evenementen/nluug/voorjaarsconferentie-2024/talks/ben-de-haan-jeroen-willemsen-how-to-not-use-secrets-with-owasp-wrongsecrets/)
  [recording from From
  2:13](https://www.youtube.com/live/iJGV-SP1vRw?si=PE1rUH-py0GIvkuv)
- [ADDO: OWASP WrongSecrets: How We Keep on Growing Our Open Source
  Project](https://event.alldaydevops.com/event/registration/websitePage:04030226-24b8-49ac-9c30-5671087b28ec?_gl=1*1r8zqhp*_gcl_au*MTkyNDMzMzAxOS4xNzI1NTI1OTY4&session=f7080cbc-c775-4c3d-8c6b-c6cca2158a74)
- [OWASP Spotlight Series
  WrongSecrets](https://www.youtube.com/watch?v=inSkNPLDlWo)
- Coverage on youtube: [walkthrough by sec
  right](https://youtu.be/tSQATLTuSqQ?si=DwCnQ4FlQQALGVfZ)
- Various Blogs: [A blog by
  Gitguardian](https://blog.gitguardian.com/gitguardian-is-proud-sponsor-of-owasp/),
  [Another blog by
  Gitguardian](https://blog.gitguardian.com/a-beginners-guide-to-owasp/),
  [Blogs by the author(s)](https://dev.to/commjoen), [A blog by
  Okteto](https://www.okteto.com/blog/practice-secrets-management-in-kubernetes-with-owasp-wrongsecrets-and-okteto/),
  [A blog by
  Nec](https://jpn.nec.com/cybersecurity/blog/230707/index.html), [A
  blog from
  vineeth.dj](https://medium.com/@vineeth.dj/owasp-wrongsecrets-writeup-24ad3460be0a).
- Various Podcasts: [Application Security Podcast: Jeroen Willemsen &
  Ben de Haan -- Dirty little
  secrets](https://appsecpodcast.securityjourney.com/1730684/9864567-jeroen-willemsen-and-ben-de-haan-dirty-little-secrets),
  [Devsec for scale: Secrets Management Pt
  1](https://www.youtube.com/watch?v=dxgXUQZgUnI), [Devsec for scale:
  Secrets Management Pt 2](https://www.youtube.com/watch?v=_gY0T9vIl4E),
  [Devsec for scale: Secrets Management Pt
  3](https://www.youtube.com/watch?v=vtUk2bc34AY).

We would like to thank many people that have given a shoutout or a share
about this project! Thank you for your forum-posts, blogs, and more!
:::::

::: {#sec-overview .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Overview

The application can best be run as a [Docker
container](https://hub.docker.com/r/jeroenwillemsen/wrongsecrets) as
part of a K8s cluster. Some challenges are unique to specific public
clouds (AWS, GCP, and Azure only for now).

![overview](assets/images/layerswithchallenges.png)

The overview above nicely shows which technologies are mostly used to
build up the full application. Consult the [GitHub repo
readme](https://github.com/OWASP/wrongsecrets) for more information.
:::

::: {#sec-ctf .section .page-body .tab-hidden}

------------------------------------------------------------------------

## CTF

### With just OWASP WrongSecrets

We support playing CTFs with OWASP WrongSecrets! Want to know more? Have
a look at [the Git repo
README](https://github.com/OWASP/wrongsecrets#ctf) and [the additional
CTF
documentation](https://github.com/OWASP/wrongsecrets/blob/master/ctf-instructions.md)

### With OWASP WrongSecrets-CTF-Party

[![Github
Stars](https://img.shields.io/github/stars/OWASP/wrongsecrets-ctf-party?label=Stars%20wrongsecrets-ctf-party&style=social)](https://github.com/OWASP/wrongsecrets-ctf-party/stargazers)
[![Docker
pulls](https://img.shields.io/docker/pulls/jeroenwillemsen/wrongsecrets-balancer.svg)](https://img.shields.io/docker/pulls/jeroenwillemsen/wrongsecrets-balancer.svg).

Want to play OWASP WrongSecrets in a large group in CTF mode, but not go
over all the hassle of setting up local copies of OWASP WrongSecrets?
Here is [OWASP WrongSecrets CTF
Party](https://github.com/OWASP/wrongsecrets-ctf-party)! This is a fork
of [OWASP MultiJuicer](https://github.com/iteratec/multi-juicer), which
is adapted to become a dynamic multi-tenant setup for doing a CTF
together!

Note that we:

- have a [Webtop](https://docs.linuxserver.io/images/docker-webtop)
  integrated for each player
- have a WrongSecrets instance integrated for each player
- A working admin interface which can restart both or delete both (by
  deleting the full namespace)
- It can cleanup old & unused namespaces automatically.

You can currently play [OWASP WrongSecrets CTF
Party](https://github.com/OWASP/wrongsecrets-ctf-party) using:

- Any k8s setup that allows you to have multiple namespaces (including
  Minikube), by leveraging our [helm
  charts](../wrongsecrets-ctf-party/index.html).
- AWS, Azure, and GCP by using terraform which is part of the repo.

## Special thanks

Special thanks to [\@commjoen](https://github.com/commjoen),
[\@madhuakula](https://github.com/madhuakula),
[\@bendehaan](https://github.com/bendehaan), and
[\@mikewoudenberg](https://github.com/mikewoudenberg), and
[\@osamamagdy](https://github.com/osamamagdy) for making this port a
reality!
:::

::::: {#sec-webdesktop .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Wrongsecrets Desktop

[![Docker
pulls](https://img.shields.io/docker/pulls/jeroenwillemsen/wrongsecrets-desktop?label=docker%20pulls%20wrongsecrets-desktop)](https://hub.docker.com/r/jeroenwillemsen/wrongsecrets-desktop)[![Docker
pulls](https://img.shields.io/docker/pulls/jeroenwillemsen/wrongsecrets-desktop-k8s?label=docker%20pulls%20wrongsecrets-desktop-k8s)](https://hub.docker.com/r/jeroenwillemsen/wrongsecrets-desktop-k8s)

Want to try out the secrets-hunting, but don't want to install all the
recommended tools? Try to use our [WrongSecrets
desktop](https://hub.docker.com/r/jeroenwillemsen/wrongsecrets-desktop).

![WrongSecrets
desktopt](assets/images/wrongsecrets-desktop.png){width="300px"}

You can run all the tools and a desktop environment in a container by
doing the following:

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
docker run -p 3000:3000 jeroenwillemsen/wrongsecrets-desktop:latest
```
:::
::::

and open a browser at [http://localhost:3000](http://localhost:3000/).
Want to know more? Checkout the [Readme at the WrongSecrets github
repo](https://github.com/OWASP/wrongsecrets#want-to-play-but-are-not-allowed-to-install-the-tools).
:::::

::: {#sec-passwords .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Creating Passwords

You can create various types of passwords. OWASP WrongSecrets has quite
a few of them as an example. There are complex passwords, which you can
easily create with tools like OpenSSL and/or password managers. There
are short passphrases, which you can easily remember There are longer
passphrases with a more extensive set of words involved.

### Complex passwords

Complex passwords can be easily generated securely using tools like
OpenSSL (using `openssl rand 20 -base64`{.language-plaintext
.highlighter-rouge}) or a password manager. For instance, the generation
of challenge 31's password. The password (SGF2ZSBhIG5pY2UgZGF5) was
obtained using random information generated through OpenSSL.

Of course, we need to reference the [(in)famous XKCD on this
topic](https://xkcd.com/936/).

### Short passphrases

Short passphrases uses short combinations of words. These are easy to
think of and easy to remember. The solution to challenge0 is a good
example here. Here a short passphrase(The first answer) is used as a
solution.

### Longer passphrases

In other challenges we packed longer passphrases, which are still easy
to remember, but do have a lot more entropy to them.

## References

NIST Digital Identity Guidelines:
https://pages.nist.gov/800-63-3/sp800-63b.html OWASP Authentication
cheatsheet:
https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html
:::
::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-wrongsecrets/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-wrongsecrets){.github-button
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

-  Production Project

#### Classification

-  Tool

#### Audience

-  Builder
-  Breaker
-  Defender

### Getting Started

- [WrongSecrets Github
  repo](https://github.com/OWASP/wrongsecrets "Github Repository")
- [Online demo env
  (Heroku)](https://wrongsecrets.herokuapp.com/ "Online demo on a Heroku Dyno")
- [Sometimes Online CTF demo
  (Heroku)](https://wrongsecrets-ctf.herokuapp.com/ "Online demo on a Heroku Dyno, which is not always up")
- [Online demo (Render.io
  free)](https://wrongsecrets.onrender.com/ "Online demo on a free Render.io instance")
- [Get Latest
  Docker](https://hub.docker.com/r/jeroenwillemsen/wrongsecrets "WrongSecrets docker container")
- [Get Latest WrongSecrets
  Desktop](https://hub.docker.com/r/jeroenwillemsen/wrongsecrets-desktop "WrongSecrets-desktop docker container")
- [Download
  Releases](https://github.com/OWASP/wrongsecrets/releases "WrongSecrets releases")

### Socials and Support

- [Slack
  Channel](https://owasp.slack.com/messages/project-wrongsecrets "OWASP Slack")([Self-registration](../slack/invite.html "Get yourself invited to OWASP Slack"))
- [Twitter
  Jeroen](https://twitter.com/commjoenie "Twitter Jeroen Willemsen")
- [Twitter Ben](https://twitter.com/BJFdeHaan "Twitter Ben de Haan")

### Code Repository

- [Github
  repo](https://github.com/OWASP/wrongsecrets "Github Repository")
- [Github repo
  binaries](https://github.com/OWASP/wrongsecrets-binaries "Github Repository for the binary challenges")
- [Github CTF party
  repo](https://github.com/OWASP/wrongsecrets-ctf-party "Github Repository for WrongSecrets CTF Party")

### Getting Involved

- [Code of
  Conduct](https://github.com/OWASP/wrongsecrets/blob/master/CODE_OF_CONDUCT.md)
- [Contributing to the
  project](https://github.com/OWASP/wrongsecrets/blob/master/CONTRIBUTING.md)

### Sponsoring

- [Sponsor the
  project](../donate/indexb1e6.html?reponame=www-project-wrongsecrets&title=OWASP+wrongsecrets)

### Leaders

- [Jeroen
  Willemsen](../cdn-cgi/l/email-protection.html#a3c9c6d1ccc6cd8dd4cacfcfc6ced0c6cde3ccd4c2d0d38dccd1c4)
  ([\@commjoenie](https://twitter.com/commjoenie "Twitter Jeroen Willemsen"))
- [Ben de
  Haan](../cdn-cgi/l/email-protection.html#2a484f44044e4f424b4b446a455d4b595a0445584d)
  ([\@BJFdeHaan](https://twitter.com/BJFdeHaan "Twitter Ben de Haan"))

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::::
