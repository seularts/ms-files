::::::::::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Goals](#div-goals){#goals-link .tab-link role="tab"
  aria-selected="false" aria-controls="goals"}
- [Lessons](#div-lessons){#lessons-link .tab-link role="tab"
  aria-selected="false" aria-controls="lessons"}
- [Start](#div-start){#start-link .tab-link role="tab"
  aria-selected="false" aria-controls="start"}
- [WebWolf](#div-webwolf){#webwolf-link .tab-link role="tab"
  aria-selected="false" aria-controls="webwolf"}

# OWASP WebGoat {#owasp-webgoat .page-title}

:::::::::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
![WebGoat
Loge](../../raw.githubusercontent.com/WebGoat/WebGoat/main/src/main/resources/lessons/challenges/images/webgoat2.png)

[![GitHub
release](https://img.shields.io/github/v/release/WebGoat/WebGoat.svg)](https://github.com/WebGoat/WebGoat/releases/latest)

## Learn the hack - Stop the attack

WebGoat is a deliberately insecure application that allows interested
developers just like you to test vulnerabilities commonly found in
Java-based applications that use common and popular open source
components.

## Description

Web application security is difficult to learn and practice. Not many
people have full blown web applications like online book stores or
online banks that can be used to scan for vulnerabilities. In addition,
security professionals frequently need to test tools against a platform
known to be vulnerable to ensure that they perform as advertised. All of
this needs to happen in a safe and legal environment.

Even if your intentions are good, we believe you should never attempt to
find vulnerabilities without permission. The primary goal of the WebGoat
project is simple: create a de-facto interactive teaching environment
for web application security. In the future, the project team hopes to
extend WebGoat into becoming a security benchmarking platform and a
Java-based Web site Honeypot.

**WARNING 1:** *While running this program your machine will be
extremely vulnerable to attack. You should disconnect from the Internet
while using this program.* WebGoat's default configuration binds to
localhost to minimize the exposure.

**WARNING 2:** *This program is for educational purposes only. If you
attempt these techniques without authorization, you are very likely to
get caught. If you are caught engaging in unauthorized hacking, most
companies will fire you. Claiming that you were doing security research
will not work as that is the first thing that all hackers claim.*
:::

::: {#sec-goals .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Goals

Web application security is difficult to learn and practice. Not many
people have full blown web applications like online book stores or
online banks that can be used to scan for vulnerabilities. In addition,
security professionals frequently need to test tools against a platform
known to be vulnerable to ensure that they perform as advertised. All of
this needs to happen in a safe and legal environment.

Even if your intentions are good, we believe you should never attempt to
find vulnerabilities without permission. The primary goal of the WebGoat
project is simple: create a de-facto interactive teaching environment
for web application security. In the future, the project team hopes to
extend WebGoat into becoming a security benchmarking platform and a
Java-based Web site Honeypot.

## Learn in three steps

### ![](assets/images/teach.png){width="8%" heigth="8%"}Explain the vulnerability

![](../../webgoat.github.io/WebGoat/img/portfolio/lesson.html)

Teaching is now a first class citizen of WebGoat, we explain the
vulnerability. Instead of 'just hacking' we now focus on explaining from
the beginning what for example a SQL injection is.

### ![](assets/images/assignment.png){width="8%" heigth="8%"}Learn by doing

During the explanation of a vulnerability we build assignments which
will help you understand how it works.

![](../../webgoat.github.io/WebGoat/img/portfolio/assignment-example.html)

### ![](assets/images/mitigation.png){width="8%" heigth="8%"}Explain mitigation

At the end of each lesson you will receive an overview of possible
mitigations which will help you during your development work.

![](../../webgoat.github.io/WebGoat/img/portfolio/mitigation-example.html)
:::

::: {#sec-lessons .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Lessons

WebGoat contains lesson for almost all OWASP Top 10 vulnerabilities and
more...

![](assets/images/lesson-overview.png)

### Future lessons

The following lessons are on our wish list:

- Lesson about cryptography (in progress)
- Lesson about path traversal (in progress)
- Session management
- More password reset lessons
- etc

See our [Github page](https://github.com/WebGoat/WebGoat/issues) for
more information.
:::

::::::::::::: {#sec-start .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Getting started

### 1. Run using Docker {#1-run-using-docker}

Already have a browser and ZAP and/or Burp installed on your machine in
this case you can run the WebGoat image directly using Docker.

Every release is also published on
[DockerHub](https://hub.docker.com/r/webgoat/webgoat).

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
docker run -it -p 127.0.0.1:8080:8080 -p 127.0.0.1:9090:9090 webgoat/webgoat
```
:::
::::

If you want to reuse the container, give it a name:

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
docker run --name webgoat -it -p 127.0.0.1:8080:8080 -p 127.0.0.1:9090:9090 webgoat/webgoat
```
:::
::::

As long as you don't remove the container you can use:

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
docker start webgoat
```
:::
::::

This way, you can start where you left off. If you remove the container,
you need to use `docker run`{.language-plaintext .highlighter-rouge}
again.

### 2. Run using Docker with complete Linux Desktop {#2-run-using-docker-with-complete-linux-desktop}

Instead of installing tools locally we have a complete Docker image
based on running a desktop in your browser. This way you only have to
run a Docker image which will give you the best user experience.

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
docker run -p 127.0.0.1:3000:3000 webgoat/webgoat-desktop
```
:::
::::

### 3. Standalone {#3-standalone}

Download the latest WebGoat release from
<https://github.com/WebGoat/WebGoat/releases>

:::: {.language-shell .highlighter-rouge}
::: highlight
``` highlight
java -Dfile.encoding=UTF-8 -Dwebgoat.port=8080 -Dwebwolf.port=9090 -jar webgoat-2023.5.jar
```
:::
::::

Click the link in the log to start WebGoat.
:::::::::::::

::: {#sec-webwolf .section .page-body .tab-hidden}

------------------------------------------------------------------------

![](assets/images/wolf-enabled.png){width="8%" heigth="8%"
align="right"}\

## WebWolf the small helper

WebWolf is a separate web application which simulates an attackers
machine. It makes it possible for us to make a clear distinction between
what takes place on the attacked website and the actions you need to do
as an "attacker". WebWolf was introduced after a couple of workshops
where we received feedback that there was no clear distinction between
what was part of the "attackers" role and what was part of the "users"
role on the website. The following items are supported in WebWolf:

### Host a file

Upload a file needed to be downloaded during an assignment

![](assets/images/files.png "Uploading and serving a file")

### E-mail client

WebWolf serves a mail client with which we can easily simulate sending
an e-mail.

![](assets/images/mailbox.png "Integrated e-mail client")

### Landing page for incoming requests

WebWolf can serve as a landing page to which you can make a call from
inside an assignment, giving you as the attacker information about the
complete request. Think of it as a very simple form of
`netcat`{.language-plaintext .highlighter-rouge}.

![](assets/images/requests.png)

## Running

### 1. Docker {#1-docker}

If you started the Docker image, WebWolf is already running. Please
point your browser to: http://localhost:9090/WebWolf

### 2. Standalone {#2-standalone}

If you want to use the standalone version, you will need to download the
jar file and start it:

``` Shell
java -jar webwolf-<<version>>.jar [--server.port=9090] [--server.address=localhost]
```

By default, WebWolf starts on port 9090 with
`--server.port`{.language-plaintext .highlighter-rouge} you can specify
a different port. With `server.address`{.language-plaintext
.highlighter-rouge} you can bind it to a different address (default
localhost)
:::
::::::::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-webgoat/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-webgoat){.github-button
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

### Downloads

- [Standalone jars](https://github.com/WebGoat/WebGoat/releases)
- [Docker Image](https://hub.docker.com/r/webgoat/webgoat)

### Code Repository

- [Source code](https://github.com/WebGoat/WebGoat)

### Helping the Goat!

- [Report an issue](https://github.com/WebGoat/WebGoat/issues)
- [Contributing to
  WebGoat](https://github.com/WebGoat/WebGoat/wiki/Contributing-to-WebGoat)
- [Forking WebGoat in
  GitHub](https://github.com/WebGoat/WebGoat/wiki/Forking-WebGoat-in-GitHub)
- [Solutions](https://github.com/WebGoat/WebGoat/wiki/Main-Exploits)

### Around the Web

- [Gitter](https://gitter.im/OWASPWebGoat/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
- [Mail](../cdn-cgi/l/email-protection.html#93bcbce4f6f1f4fcf2e7d3fce4f2e0e3bdfce1f4)
- [StackOverflow](https://stackoverflow.com/search?q=webgoat)
- [Twitter](https://twitter.com/OWASP_WebGoat)
- [Slack](https://owasp.slack.com/messages/#project-webgoat/)

#### Classification

-  Tool

#### Audience

-  Builder
-  Breaker
-  Defender

### Leaders

- [Nanne
  Baars](../cdn-cgi/l/email-protection.html#89a6a6e7e8e7e7eca7ebe8e8fbfac9e6fee8faf9a7e6fbee)
- [René
  Zubčević](../cdn-cgi/l/email-protection.html#705f5f02151e155e0a05121315061913301f071103005e1f0217)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::::::::::::::
