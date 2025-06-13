::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [News](#div-news){#news-link .tab-link role="tab"
  aria-selected="false" aria-controls="news"}
- [Features and Collaboration](#div-features){#features-link .tab-link
  role="tab" aria-selected="false" aria-controls="features"}

# OWASP Seraphimdroid {#owasp-seraphimdroid .page-title}

:::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::::::: {#sec-main .section .page-body}
## Mission:

To create, as a community, an open platform for education and protection
of Android users against privacy and security threats.

## Project

OWASP Seraphimdroid is a privacy and security protection app for Android
devices. It enables users to protect their devices against malicious
software (viruses, trojans, worms, etc.), phishing SMS, MMS messages,
execution of dangerous USSD codes, theft and loosing. Also, it enables
user to protect their privacy and to control the usage of applications
and services via various kinds of locks.

OWASP Seraphimdroid has two aims:

- To protect user's privacy and secure the device against malicious
  features that may cost user money
- To educate user about threats and risks for their privacy, privacy of
  their data and security of their device.

:::::: iframe
::: {#player}
:::

:::: player-unavailable
# A apărut o eroare. {#a-apărut-o-eroare. .message}

::: submessage
Nu se poate executa JavaScript.
:::
::::
::::::

![OWASP SEraphimdroid
screenshot](../images/thumb/2/23/OWASPSeraphimdroid.png/200px-OWASPSeraphimdroid.html)

## Deeper introduction

Android users face many threats and risks. Since modern mobile devices
are almost all the time exposed to the internet and other types of
mobile networks, they are more exposed to the attacks. From the open
WiFi networks that can be spoofed to the Trojan malware applications on
the app stores, threats are everywhere around. Many of the attacks are
successful because users are not aware of the risks and threats. They
may act naive and expose themselves to the attacks even more. These
attacks may lead to the identity theft, money theft, losing privacy or
they devices may start acting as part of the botnet network.

In order to prevent attacks on the users, this project aims to develop a
set of guidelines and application that will ensure that users are using
their devices in a secure manner. Project is and always will remain open
for everyone to participate and all project deliverables will be free
and open source.

Project development is done on GitHub:
https://github.com/nikolamilosevic86/owasp-seraphimdroid

Release of OWASP Seraphimdroid is available on Google Play:
https://play.google.com/store/apps/details?id=org.owasp.seraphimdroid

## Description

The aim of this project is to research all threats and risks for users
of Android operating system. We want to develop, as a community an free
and open source security and privacy protection application and a set of
security guideline for Android users. The project tend to be research
oriented and we are willing to innovate in Android security field using
machine learning, heuristics and other innovative techniques in order to
protect our users, their privacy and money. The project is community
driven and everyone is open to participate. The main aim of OWASP
SeraphimDroid application should keep user data and money safe.

So far the main features include:

- Permission scanner. Permission scanner will show you the list of all
  installed application and the permission they are using. Also app will
  describe potential malicious use of certain permissions. Seraphimdroid
  is using machine learning in order to predict whether application
  might be malicious (be a virus, Trojan, worm, rootkit, etc) or not and
  will notify the user.
- Application and service locker. With OWASP Seraphimdroid, user may
  lock access to certain or to all of your applications and system
  services (WiFi, network, BlueTooth) with password
- Install lock. This feature can lock all installing and uninstalling
  action on your device. Great for parental control.
- Outgoing call and SMS blocker. This feature will allow user to perform
  normally outgoing calls and SMS, but it will block outgoing calls and
  inform about outgoing SMS performed by trojan applications.
- Geo-fencing. This feature allows user to set a location range where
  the device should be. If the device exits the range it may set up
  alarm or start sending messages to the defined number with its
  location.
- Remote location. If user lost your phone, he is able to send SMS with
  a defined secret code as a content and his phone and it will reply
  with the location coordinates of the device.
- Remote lock and lock
- Network and CPU monitoring

## Licencing

GNU GPL v3 License (allows commercial use, but requires that
modifications to your code stay open source, thus prohibiting
proprietary forks of your project)
:::::::

::: {#sec-news .section .page-body .tab-hidden}

------------------------------------------------------------------------

## News

- (05.11.2019) We have participated this year in Google Summer of Code.
  The work done on dynamic malware analysis and anomaly detection on the
  device using deep learning is described in the following paper:
  <https://arxiv.org/ftp/arxiv/papers/1910/1910.10660.pdf>
- (15.3.2017) We published a part of our machine learning methodology in
  Elsevier's scientific publication: Milosevic, Nikola, Ali
  Dehghantanha, and Kim-Kwang Raymond Choo. "Machine learning aided
  Android malware classification." Computers & Electrical Engineering
  (2017).
  <http://www.sciencedirect.com/science/article/pii/S0045790617303087>
- (09.1.2017) OWASP Seraphimdroid was promoted to Lab project
- (28.8.2016) New version (v2.0) of OWASP Seraphimdroid is released on
  Google play store. Blog post about new features can be [read
  here](http://inspiratron.org/blog/2015/09/08/new-version-of-owasp-seraphimdroid-v2-0-is-published/)
- (10.7.2015) OWASP Seraphimdroid is participating at OWASP Summer Code
  Sprint 2015
- (2.10.2014) OWASP Seraphimdroid was featured on a front page and
  interview with a project leader was published in Libre!, Serbian
  online magazine about open source. Issue 29 of the Libre! magazine,
  where the interview was published can be [seen
  here](https://libre.lugons.org/index.php/broj-29/)
- (5.9.2014) The first release of OWASP Seaphimdroid was released on
  Google play. Blog post about features can be [read
  here](http://inspiratron.org/blog/2014/10/06/owasp-seraphimdroid-android-security-published/)
- (1.6.2014) OWASP Searaphimdroid participates on [Google Summer of
  Code](https://www.google-melange.com/archive/gsoc/2014/orgs/owasp/projects/furquan.html)
- (2.2.2014) Article about malicious use of Android permissions was
  published by Digital Forensics magazine. This paper was a result of
  research conducted on OWASP Seraphimdroid project. Article can be
  viewed [here](http://inspiratron.org/AndroidSecurity.pdf)
:::

::: {#sec-features .section .page-body .tab-hidden}

------------------------------------------------------------------------

**OWASP Seraphimdroid encourages students and University lecturers to
contribute to the projects. We would like to encourage any BSc, 3rd year
or master project ideas that would improve Seraphimdroid app. Project
leaders are willing to co-supervise these projects. Please contact us if
you are interested. At the end of the page are listed some of the
potential project ideas, but we encourage you to send us your ideas as
well.**

## Behavioral malware and intrusion analysis

### Brief Explanation:

OWASP Seraphimdroid is an Android mobile app which already has a
capability to statically analyze malware using machine learning (weka
toolkit) relying on permissions. However, this is usually not enough and
we intend to improve this with behavioral analysis. There are a number
of paper in scientific literature describing how to detect malware and
intrusions by dynamically analyzing its behavior (system calls, battery
consumption, etc.). The idea of this project is to find the best
approach that can be implemented on the device and implement it. \*\*

### Expected Results:

- Reviewing scientific literature and find feasible approach we can take
- Implement and possibly improve the approach in Seraphimdroid
- Test the model and provide controls to switch algorithm on or off and
  possibly fine tune it \*Documenting approach as a technical report

### Knowledge Prerequisites:

- Java
- Android
- CSV, XML
- Basic knowledge and interest in machine learning

### Mentors:

- Nikola Milosevic - OWASP Seraphimdroid Project Leader

## Framework for plugin development

### Brief Explanation:

OWASP Seraphimdroid is well rounded security and privacy app, however,
it lacks some components community can provide. We would like to provide
community the way to develop plugins that can add features to OWASP
Seraphimdroid app. However, the way of integrating external components
into Android app may be challenge. The way of presenting GUI and
integration between processes need to be examined and developed.

### Expected Results:

- Examining the way of integrating third party apps through some
  provided API to OWASP Seraphimdroid
- Providing GUI integration with third party components
- Develop at least one test plugin
- Document the development process and API

### Knowledge Prerequisites:

- Java
- Android
- CSV, XML

### Mentors:

- Nikola Milosevic - OWASP Seraphimdroid Project Leader
:::
::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-seraphimdroid/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-seraphimdroid){.github-button
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

### What is OWASP SeraphimDroid?

- Free and open source project
- Android security and privacy protection app
- Educational platform (planned)
- OWASP SeraphimDroid provides:
  - Documentation on how Android permissions can be misused
  - Security guide for Android users
  - Security Android application
  - Application that keeps user secure and teaches him about risks

### Classifications

- Project type: Builders, Defenders
- Project level: Lab
- OWASP Code project

### Mailing list

[Mailing
list](https://lists.owasp.org/mailman/listinfo/owasp_seraphimdroid_project)

### Downloads and Documentation

- [Code
  repository](https://github.com/nikolamilosevic86/owasp-seraphimdroid)

Documents and publications:

- [User guide and
  Documentation](http://inspiratron.org/OWASPSeraphimdroid/SeraphimdroidDocumentation.pdf)
- [Article about android permissions, published by Digital Forensics
  magazine](http://inspiratron.org/AndroidSecurity.pdf)
- [Article describing deep learning based dynamic malware analysis and
  anomaly
  detection](https://arxiv.org/ftp/arxiv/papers/1910/1910.10660.pdf)

### Leaders

- [Nikola
  Milosevic](../cdn-cgi/l/email-protection.html#157b7c7e7a79743b787c797a6670637c76557a627466653b7a6772)
- [Kartik
  Kohli](../cdn-cgi/l/email-protection.html#ff949e8d8b9694d19490979396bf90889e8c8fd1908d98)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::
