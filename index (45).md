::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [How to Play](#div-play){#play-link .tab-link role="tab"
  aria-selected="false" aria-controls="play"}
- [Web Applications Edition](#div-webapplications){#webapplications-link
  .tab-link role="tab" aria-selected="false"
  aria-controls="webapplications"}
- [Mobile Apps Edition](#div-mobileapps){#mobileapps-link .tab-link
  role="tab" aria-selected="false" aria-controls="mobileapps"}
- [FAQs](#div-faqs){#faqs-link .tab-link role="tab"
  aria-selected="false" aria-controls="faqs"}
- [Acknowledgements](#div-acknowledgements){#acknowledgements-link
  .tab-link role="tab" aria-selected="false"
  aria-controls="acknowledgements"}
- [Road Map and Getting Involved](#div-roadmap){#roadmap-link .tab-link
  role="tab" aria-selected="false" aria-controls="roadmap"}

# OWASP Snakes And Ladders {#owasp-snakes-and-ladders .page-title}

:::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
[![OWASP
Lab](https://img.shields.io/badge/owasp-lab%20project-yellow.svg)](../projects/index.html)
[![Twitter
Follow](https://img.shields.io/twitter/follow/OWASPSnakesWeb?style=social)](https://twitter.com/OWASPSnakesWeb)
[![Twitter
Follow](https://img.shields.io/twitter/follow/OWASPSnakesMob?style=social)](https://twitter.com/OWASPSnakesMob)

![OWASP Snakes and ladders
sheet](assets/images/Snakes_and_ladders-header.png)

Snakes and Ladders is an educational project. It uses gamification to
promote awareness of application security controls and risks, and in
particular knowledge of other OWASP documents and tools.

## Editions

*[Web Applications](index.html#div-webapplications)*

In the board game for web applications, the virtuous behaviours
(ladders) are secure coding practices (from [OWASP Proactive Controls
Project](http://top10proactive.owasp.org/) 2014-2024) and the vices
(snakes) are application security risks (from [OWASP Top Ten
Project](../www-project-top-ten/index.html) 2013-2021).

*[Mobile Apps](index.html#div-mobileapps)*

The identical board game for mobile apps uses mobile controls (from the
[Mobile Security Project](../www-project-mobile-security.html) top ten
controls 2013) as the virtuous behaviours and mobile risks (the top ten
mobile risks 2014 from the same project) as the vices.

## Background

This board game was created to use as an ice-breaker in application
security training, but it potentially has wider appeal simply as a
promotional hand-out, and maybe also more usefully as learning materials
for younger coders. To cover all of that, we use the phrase:

\"OWASP Snakes and Ladders is meant to be used by software programmers,
big and small\"

The game is quite lightweight, and does not have the same rigour or
depth as the card game Cornucopia, but it is meant to be just some fun
with some learning attached.

Print-ready PDFs have been published - these are poster sized A2
(international ISO 216 [paper
size](https://en.wikipedia.org/wiki/Paper_size) 420×594mm, approximately
16.5×23.4in, with 3mm bleed and printers' marks). But the original files
are in Adobe Illustrator, so these are also available for anyone to use
and improve upon. We recommend playing using a real die and counters
(markers), but you can cut out and make these from the paper sheet
itself if you have scissor and glue skills.

We hope it may be of use in any upcoming office party, celebration,
festival, seasonal event, application security awareness or training
exercise. Or just to help spread the word about controls and risks at
work, at college or at school. If you are training anyone about the
OWASP Top Ten, OWASP Proactive Controls or the OWASP Mobile projects,
please consider giving each attendee a printed copy of the game as a
take away.

## Licensing

OWASP Snakes and Ladders is free to use. It is licensed under the
[Creative Commons Attribution-ShareAlike 3.0
license](http://creativecommons.org/licenses/by-sa/3.0/), so you can
copy, distribute and transmit the work, and you can adapt it, and use it
commercially, but all provided that you attribute the work and if you
alter, transform, or build upon this work, you may distribute the
resulting work only under the same or similar license to this one.

© OWASP Foundation

## Other Security Gamification

If you are interested in using gaming for security, also see [OWASP
Cornucopia](../www-project-cornucopia/index.html), [Elevation of
Privilege: The Threat Modeling
Game](http://www.microsoft.com/security/sdl/adopt/eop.aspx), [Security
Cards](http://securitycards.cs.washington.edu/) from the University of
Washington, the commercial card game
[Control-Alt-Hack](http://www.controlalthack.com/)
([presentation](http://media.blackhat.com/bh-us-12/Briefings/Kohno/BH_US_12_Kohno_Control_Alt_Hack_Slides.pdf)),
and web application security training tools incorporating gamification
such as [OWASP Hackademic Challenges
Project](../www-project-hackademic-challenges.html), [OWASP Security
Shepherd](../www-project-security-shepherd/index.html) and [ITSEC
Games](http://itsecgames.blogspot.co.uk/).

Additionally, Adam Shostack maintains a list of tabletop security games
and related resources at [security
games](http://adam.shostack.org/games.html).
:::

::: {#sec-play .section .page-body .tab-hidden}

------------------------------------------------------------------------

## How to Play

Snakes and Ladders is a popular board game, with [ancient
provenance](https://en.wikipedia.org/wiki/Snakes_and_Ladders) imported
into [Great Britain from
Asia](http://sandradodd.com/game/snakesandladders) in the 19th century.
The original game showed the effects of good and evil, or virtues and
vices. This OWASP game is a poster-sized print-your-own paper sheet with
the game board on it. Just get some players together with a die and
counters. The virtues are application security controls, and the vices
are risks.

- The game is for 2-6 players.
- Firstly print the sheet out, get a six-sided die and some counters
  (markers).
- Give each player a coloured counter (marker). To begin, each player
  should throw the die to determine who plays first; the highest can
  lead.
- Put all the players' counters onto the first square labelled "Start
  1".
- In turn, each player rolls the die and moves their counter by the
  number of squares indicated on the die. At the end of the move, if a
  player's counter is at the bottom end of a ladder, the counter must be
  moved up the ladder to the square at its higher end. Conversely, if
  the player's counter is located at the mouth of a snake, the counter
  must be moved down to the end of the snake's tail.
- As a better alternative to enhance learning, either require the
  participants to discuss the risk/control when a player reaches each
  square, or only allow players to climb up a ladder after a quest about
  the control (e.g. simply describing the control, explain the risk (one
  example) the named control addresses and how the control (one example)
  could help prevent the named it
- The first player to reach "100" at the top left wins. Give a prize.
:::

::: {#sec-webapplications .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Web Applications Edition

OWASP Snakes and Ladders - Web Applications was the first edition
created. The objective is to raise awareness of the security controls
that every web application should have, but link that with the much more
widely known Top Ten Risks. The virtuous behaviours (ladders) are secure
coding practices (from [OWASP Proactive Controls
project](http://top10proactive.owasp.org/) 2014-2018) and the vices
(snakes) are application security risks (from [OWASP Top Ten
Project](../www-project-top-ten/index.html) 2013-2017).

![Overview image of the DE version of OWASP Snakes and
Ladders](assets/images/Osn-poster-web-de.jpg)

## Current Releases

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Language Code: Name / Title / Current Version                                                           Example Square
  ------------------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------------------
  [BR: Português                                                                                          [![BR](assets/images/Osn-webapp-BR.png)](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/BR)
  Brasileiro](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/BR)\   
  \                                                                                                       
  Serpentes e Escadas Aplicativos da Web\                                                                 
  \                                                                                                       

  [DE: Deutsch](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/DE)\ [![DE](assets/images/Osn-webapp-DE.png)](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/DE)
  \                                                                                                       
  Schlangen und Leitern Web Anwendungen\                                                                  
  \                                                                                                       

  [EN: English](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/EN)\ [![EN](assets/images/Osn-webapp-EN.png)](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/EN)
  \                                                                                                       
  Snakes and Ladders Web Applications\                                                                    
  \                                                                                                       
  v1.20                                                                                                   

  [ES: Español](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/ES)\ [![ES](assets/images/Osn-webapp-ES.png)](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/ES)
  \                                                                                                       
  Serpientes y Escaleras Aplicaciones Web\                                                                
  \                                                                                                       

  [FR:                                                                                                    [![FR](assets/images/Osn-webapp-FR.png)](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/FR)
  Français](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/FR)\     
  \                                                                                                       
  Serpents et Échelles Application Web\                                                                   
  \                                                                                                       

  [JA: 日本語](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/JA)\  [![JA](assets/images/Osn-webapp-JA.png)](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/JA)
  \                                                                                                       
  蛇とはしご ウェブアプリケーション\                                                                      
  \                                                                                                       

  [TR: Türkçe](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/TR)\  [![TR](assets/images/Osn-webapp-TR.png)](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/TR)
  \                                                                                                       
  Yılanlar ve Merdivenler Web Uygulamaları\                                                               
  \                                                                                                       

  [ZH: 中文](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/ZH)\    [![ZH](assets/images/Osn-webapp-ZH.png)](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/ZH)
  \                                                                                                       
  蛇梯棋 WEB应用程序\                                                                                     
  \                                                                                                       
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Note that some languages choose not to change the EN text for risk and
control names.

Source: [Adobe Illustrator
file](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web)

### Tabletop Simulator

A digital version (of the English release) is [available on Steam
Workshop](https://steamcommunity.com/sharedfiles/filedetails/?id=1969196030).
It can be played with 2-6 players online. While [the game itself is a
free community
download](https://steamcommunity.com/sharedfiles/filedetails/?id=1969196030),
all players must have [Tabletop
Simulator](https://store.steampowered.com/app/286160/Tabletop_Simulator/)
in their Steam library.

![](https://steamuserimages-a.akamaihd.net/ugc/772864662280754056/4284CB1CC51DC1676BC02CD71EF9B3E3B5E1FDAB/)

## Colour Scheme 'Classic'

![One row slice of the board showing the colours in
use](assets/images/Snakes_and_ladders_webapp-mini-banner.png)

This edition uses simple primary colours, like many versions that can be
seen in pictures of Snakes and Ladders games. The colours used in
'Classic' are:

- Green
- Yellow
- White
- Red
- Blue

The start square (1) is yellow and the final square (100) is red.
:::

::: {#sec-mobileapps .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Mobile Apps Edition

OWASP Snakes and Ladders - Mobile Apps was created after working out the
idea and design for the web application version of the board game. It
seemed easy to replicate the idea since the OWASP Mobile Project lists
both security controls and risks. The virtuous behaviours (ladders) are
mobile controls (from the Mobile Security Project Top Ten Controls 2013)
and the vices (snakes) are mobile risks (from the Top Ten Mobile Risks
2014).

![Overview image of the JA version of OWASP Snakes and
Ladders](assets/images/Osn-poster-mob-ja.jpg)

## Current Releases {#current-releases}

  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Language Code: Name / Title / Current Version                                                        Example Square
  ---------------------------------------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------------------
  [EN:                                                                                                 [![EN](assets/images/Osn-mobapp-EN.png)](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/mob/EN)
  English](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/mob/EN)\   
  \                                                                                                    
  Snakes and Ladders Mobile Apps                                                                       

  [JA:                                                                                                 [![JA](assets/images/Osn-mobapp-JA.png)](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/mob/JA)
  日本語](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/mob/JA)\    
  \                                                                                                    
  蛇とはしご モバイルアプリ版                                                                          
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Source: [Adobe Illustrator
file](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/mob)

### Tabletop Simulator {#tabletop-simulator}

A digital version (of the English release) is [available on Steam
Workshop](https://steamcommunity.com/sharedfiles/filedetails/?id=1970691216).
It can be played with 2-6 players online. While [the game itself is a
free community
download](https://steamcommunity.com/sharedfiles/filedetails/?id=1970691216),
all players must have [Tabletop
Simulator](https://store.steampowered.com/app/286160/Tabletop_Simulator/)
in their Steam library.

![](https://steamuserimages-a.akamaihd.net/ugc/770613072982577283/419067818E622DA505DCDD2FFF7BE20AD6BEB630/)

## Colour Scheme 'Farringdon'

![One row slice of the board showing the colours in
use](assets/images/Snakes_and_ladders_mobapp-mini-banner.png)

Other people's versions of Snakes and Ladders [use a wide variety of
designs and colour
schemes](https://duckduckgo.com/?q=snakes+and+ladders+board+game&t=h_&iax=images&ia=images).
Thus to make a complete contrast to the edition for web applications,
the colours used are the designatory colours of the underground and
mainline train services that run through Colin Watson's local station at
Farringdon in Clerkenwell, London EC1. The colours in 'Farringdon' are:

- Purple (future ~~Crossrail~~ Elizabeth)
- Yellow (Circle)
- White (Thameslink)
- Maroon (Metropolitan)
- Pink (Hammersmith & City)

You can see these colours on tube maps and station signage. The start
square (1) is yellow and the final square (100) is maroon.
:::

::: {#sec-faqs .section .page-body .tab-hidden}

------------------------------------------------------------------------

## FAQs

### Why Snakes & Ladders? {#why-snakes--ladders}

The OWASP Top 10 is the most well known document, but OWASP has many
other resources which provide better approaches for secure application
development. In particular, there are some "top 10 controls" lists, and
I wanted to highlight those. Creating a board game that features both
risks and controls is a simple way to compare and contrast these
aspects.

Players do not need to know either the risks or controls on the lists,
since they are just the decoration to what is otherwise standard Snakes
& Ladders. But as players land on assigned squares, this can be used to
discuss the risks and controls they are labelled with.

Also, after undertaking some due diligence, it was noted that since
Snakes & Ladders is such an ancient game it is not anyone's intellectual
property and many others have already created thousands of different
designs and versions. Other games would not meet this requirement.

### How was the game created?

By hard work! Each list of risks and controls contains ten items, so the
rough layout of snakes and ladder starting and end points was sketched
out on paper, as shown for web applications on the right. Instructional
text was written.

The concept was then converted into a layered Adobe Illustrator file,
and the text and graphics added. This design went through a number of
iterations to ensure it was legible and appealing. The PDF was exported
and both the PDF and AI files added to the project page. When
translations were provided, these were added as separate text layers in
the source Illustrator file, and then new files uploaded again to the
project.

Once Web Applications Snakes & Ladders was complete, the file was
duplicated and edited for Mobile Apps. This has different risks,
controls and arrangement of snakes and ladders. It also has its own
colour scheme.

### How can I participate in your project?

All you have to do is make the Project Leader aware of your available
time to contribute to the project. It is also important to let the
Leader know how you would like to contribute and pitch in to help the
project meet its goals and milestones. There are many different ways you
can contribute to an OWASP Project, but communication with the leads is
key. Please see the road map and getting involved section

### If I am not a programmer can I participate in your project?

Yes, you can certainly participate in the project if you are not a
programmer or technical. The project needs different skills and
expertise and different times during its development. Currently, we are
looking for users, translators and people to promote the project.
:::

::: {#sec-acknowledgements .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Acknowledgements

### Volunteers

Snakes and Ladders is developed, maintained, updated and promoted by a
worldwide team of volunteers. The contributors to date have been:

- Ziyahan Albeniz
- Kembolle Amilkar
- Katy Anton
- Manuel Lopez Arredondo
- Fabio Cerullo
- Álan Carlos B. Eufrázio
- Tobias Gondrom
- Martin Haslinger
- Yongliang He
- Manfred Hofmeier
- Björn Kimminich
- Cédric Messeguer
- Takanori Nakanowatari
- Marcos Vinícius Nunes de Arruda
- Riotaro Okada
- Gabriel Pedro S. Peres
- Alison S. Ribeiro
- Ivy Zhang
- Colin Watson

### Others

The project leaders and contributors to the referenced controls and
risks:

- [OWASP Proactive
  Controls](https://www2.owasp.org/www-project-proactive-controls)
- [OWASP Top Ten](https://www2.owasp.org/www-project-top-ten)
- [OWASP Mobile Security](../www-project-mobile-security.html)

OWASP staff for helping to set up the project and support its ongoing
activities.
:::

::: {#sec-roadmap .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Road Map and Getting Involved

Involvement in the development and promotion of Snakes and Ladders is
actively encouraged! You do not have to be a security expert in order to
contribute. Some of the ways you can help are listed below.

Recently completed:

- Update web applications edition to Proactive Controls 2018
- Translate into other languages
- Migration of project to new OWASP website

The ongoing priorities are:

- Update as other referenced projects updated (e.g. Top Ten)

Other ideas are:

- Promote use of Snakes and Ladders
- Develop other boards

### Localisation

Are you fluent in another language? Can you help translate Snakes and
Ladders into that language?

The project is on
[Crowdin](https://crowdin.com/project/owasp-snakes-and-ladders).

### Use and Promote the Board Game

Please help raise awareness of Snakes and Ladders:

Use the game with your colleagues, friends, families, students and
children Create video about how to play the game Develop a multi-user
mobile app or web application to play the game

### Feedback

Please use the [Snakes and Ladders Project Google
Group](https://groups.google.com/a/owasp.org/forum/#!forum/snakes-and-ladders-project)
for feedback:

- How did you use it?
- What is people's reaction?
- What do like?
- What don't you like?
- What doesn't make sense?
- How could the guidance be improved?
- What other boards would you like to see?

### Create a Board

Do you have an idea for your own application security Snakes and Ladders
board? Please contribute your ideas via the mailing list.
:::
::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-snakes-and-ladders/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-snakes-and-ladders){.github-button
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

### Quick Downloads

- [Web Applications](index.html#div-webapplications):
- [BR](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/BR),
  [DE](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/DE),
  [EN](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/EN),
  [ES](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/ES),
  [FR](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/FR),
  [JA](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/JA),
  [TR](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/TR),
  [ZH](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/web/ZH)
- [Mobile Apps](index.html#div-mobileapps):
- [EN](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/mob/EN),
  [JA](https://github.com/OWASP/www-project-snakes-and-ladders/tree/master/assets/files/mob/JA)

### What is This?

- Snakes and Ladders is a popular board game, with [ancient
  provenance](https://en.wikipedia.org/wiki/Snakes_and_Ladders) imported
  into [Great Britain from
  Asia](http://sandradodd.com/game/snakesandladders) in the 19th
  century. The original game showed the effects of good and evil, or
  virtues and vices. This OWASP game is a poster-sized *print-your-own*
  paper sheet with the game board on it. Just get some players together
  with a die and counters. The virtues are application security
  controls, and the vices are risks.

### Project Information

- [Lab Project]{style="font-size:1.0em;padding-left:12px;"}
- [Documentation]{style="font-size:1.0em;padding-left:12px;"}
- [Builder]{style="font-size:1.0em;padding-left:12px;"}
- [Defender]{style="font-size:1.0em;padding-left:12px;"}

### Twitter

- ![Picture of a die and two markers on an OWASP Snakes and Ladders
  sheet](assets/images/OWASPSnakesWeb-profile-small.jpg)

- Follow two mock games running on Twitter:

- [\@OWASPSnakesWeb](https://twitter.com/OWASPSnakesWeb)

- [\@OWASPSnakesMob](https://twitter.com/OWASPSnakesMob)

### License

- [![CC BY-SA
  3.0](../../licensebuttons.net/l/by-sa/3.0/80x15.png)](http://creativecommons.org/licenses/by-sa/3.0/)

### Leaders

- [Katy
  Anton](../cdn-cgi/l/email-protection.html#177c76636e39767963787957786076646739786570)
- [Colin
  Watson](../cdn-cgi/l/email-protection.html#35565a595c5b1b425441465a5b755a425446451b5a4752)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::
