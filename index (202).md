::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [How do I get
  started?](#div-how_do_i_get_started){#how_do_i_get_started-link
  .tab-link role="tab" aria-selected="false"
  aria-controls="how_do_i_get_started"}
- [Related Projects](#div-related_projects){#related_projects-link
  .tab-link role="tab" aria-selected="false"
  aria-controls="related_projects"}

# OWASP AntiSamy {#owasp-antisamy .page-title}

:::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
[![OWASP
Lab](https://img.shields.io/badge/owasp-lab%20project-yellow)](https://www.owasp.org/projects)
[![GitHub
release](https://img.shields.io/github/release/nahsra/antisamy.svg)](https://github.com/nahsra/antisamy/releases/latest)

## OWASP AntiSamy {#owasp-antisamy}

AntiSamy was originally authored by Arshan Dabirsiaghi
(arshan.dabirsiaghi \[at\] gmail.com) of Contrast Security with help
from Jason Li (jason.li \[at\] owasp.org) and is currently maintained by
Dave Wichers (dave.wichers \[at\] owasp.org) and Sebastian Passaro
(sebastian.passaro \[at\] owasp.org).

### Description

The OWASP AntiSamy project is a few things. Technically, it is an API
for ensuring user-supplied HTML/CSS is in compliance within an
application's rules. Another way of saying that could be: It's an API
that helps you make sure that clients don't supply malicious cargo code
in the HTML they supply for their profile, comments, etc., that get
persisted on the server. The term "malicious code" in regards to web
applications usually means "JavaScript." Cascading Stylesheets are only
considered malicious when they invoke the JavaScript engine. However,
there are many situations where "normal" HTML and CSS can be used in a
malicious manner. So we take care of that too.

Philosophically, AntiSamy is a departure from contemporary security
mechanisms. Generally, the security mechanism and user have a
communication that is virtually one way, for good reason. Letting the
potential attacker know details about the validation is considered
unwise as it allows the attacker to "learn" and "recon" the mechanism
for weaknesses. These types of information leaks can also hurt in ways
you don't expect. A login mechanism that tells the user, "Username
invalid" leaks the fact that a user by that name does not exist. A user
could use a dictionary or phone book or both to remotely come up with a
list of valid usernames. Using this information, an attacker could
launch a brute force attack or massive account lock denial-of-service.
We get that.

Unfortunately, that's just not very usable in this situation. Typical
Internet users are largely pretty bad when it comes to writing HTML/CSS,
so where do they get their HTML from? Usually they copy it from
somewhere out on the web. Simply rejecting their input without any clue
as to why is jolting and annoying. Annoyed users go somewhere else to do
their social networking.

The OWASP licensing policy allows OWASP projects to be released under
any [approved open source
license](https://www.opensource.org/licenses/alphabetical). Under these
guidelines, AntiSamy is distributed under a [BSD
license](https://opensource.org/licenses/BSD-3-Clause).

### What is AntiSamy?

OWASP AntiSamy provides:

[This
page](https://github.com/nahsra/antisamy/wiki/AntiSamy-Core-Features)
shows a big-picture comparison between the versions. Since it's an
unfunded open source project, the ports can't be expected to mirror
functionality exactly. If there's something a port is missing -- let us
know, and we'll try to accommodate, or write a patch!

### Presentations

From OWASP & WASC AppSec U.S. 2007 Conference (San Jose, CA): AntiSamy:
[Picking a Fight with XSS
(ppt)](assets/files/OWASP-WASCAppSec2007SanJose_AntiSamy.ppt) - by
Arshan Dabirsiaghi - AntiSamy project lead

From OWASP AppSec Europe 2008 (Ghent, Belgium): [The OWASP AntiSamy
project (ppt)](assets/files/AppSecEU08-AntiSamy.ppt) - by Jason Li -
AntiSamy project contributor

From OWASP AppSec India 2008 (Delhi, India): [Validating Rich User
Content (ppt)](assets/files/AppSecIN08-ValidatingRichUserContent.ppt) -
by Jason Li - AntiSamy project contributor

From Shmoocon 2009 (Washington, DC): AntiSamy - [Picking a Fight with
XSS (pptx)](https://slideplayer.com/slide/4360528/) - by Arshan
Dabirsiaghi - AntiSamy project lead

### News and Events

\[3 July 2021\] Please update AntiSamy to 1.6.4 or later to avoid
CVE-2021-35043, CVE-2017-14735, and CVE-2016-10006.

\[10 Apr 2022\] Please update AntiSamy to 1.6.7 or later to additionally
avoid CVE-2022-28367 and CVE-2022-29577

We always recommend using the latest available release to not only
eliminate direct vulnerabilities, but any vulnerabilities in
dependencies that have been upgraded.
:::

::: {#sec-how_do_i_get_started .section .page-body .tab-hidden}

------------------------------------------------------------------------

There are 4 steps in the process of integrating AntiSamy. Each step is
detailed in the next section, but the high level overview follows:

1.  Download AntiSamy from Maven
2.  Choose one of the standard policy files that matches as close to the
    functionality you need:
    - antisamy-tinymce-X.X.X.xml
    - antisamy-slashdot-X.X.X.xml
    - antisamy-ebay-X.X.X.xml
    - antisamy-myspace-X.X.X.xml
    - antisamy-anythinggoes-X.X.X.xml
3.  Tailor the policy file according to your site's rules
4.  Call the API from the code

## Stage 1 - Downloading AntiSamy

First, add the dependency from Maven:

``` XML
  <dependency>
    <groupId>org.owasp.antisamy</groupId>
    <projectId>antisamy</projectId>
  </dependency>
```

## Stage 2 - Choosing a base policy file

Chances are that your site's use case for AntiSamy is at least roughly
comparable to one of the predefined policy files. They each represent a
"typical" scenario for allowing users to provide HTML (and possibly CSS)
formatting information. Let's look into the different policy files:

1\) antisamy-slashdot.xml

[Slashdot](https://slashdot.org/) is a techie news site that allows
users to respond anonymously to news posts with very limited HTML
markup. Now, Slashdot is not only one of the coolest sites around, it's
also one that's been subject to many different successful attacks. Even
more unfortunate is the fact that most of the attacks led users to the
infamous goatse.cx picture (please don't go look it up). The rules for
Slashdot are fairly strict: users can only submit the following HTML
tags and no CSS: `<b>`{.language-plaintext .highlighter-rouge},
`<u>`{.language-plaintext .highlighter-rouge}, `<i>`{.language-plaintext
.highlighter-rouge}, `<a>`{.language-plaintext .highlighter-rouge},
`<blockquote>`{.language-plaintext .highlighter-rouge}.

Accordingly, we've built a policy file that allows fairly similar
functionality. All text-formatting tags that operate directly on the
font, color or emphasis have been allowed.

2\) antisamy-ebay.xml

[eBay](https://www.ebay.com/) is the most popular online auction site in
the universe, as far as I can tell. It is a public site so anyone is
allowed to post listings with rich HTML content. It's not surprising
that given the attractiveness of eBay as a target that it has been
subject to a few complex XSS attacks. Listings are allowed to contain
much more rich content than, say, Slashdot- so it's attack surface is
considerably larger. The following tags appear to be accepted by eBay
(they don't publish rules): `<a>`{.language-plaintext
.highlighter-rouge}, `...`{.language-plaintext .highlighter-rouge}

3\) antisamy-myspace.xml

[MySpace](https://myspace.com/) was, at the time this project was born,
arguably the most popular social networking site. Users were allowed to
submit pretty much all HTML and CSS they want - as long as it doesn't
contain JavaScript. MySpace was using a word blacklist to validate
users' HTML, which is why they were subject to the infamous Samy worm:
[Article: The MySpace Worm that Changed the Internet
Forever](https://www.vice.com/en_us/article/wnjwb4/the-myspace-worm-that-changed-the-internet-forever)
and another [In Samy's own words](https://samy.pl/myspace/). The Samy
worm, which used fragmentation attacks combined with a word that should
have been blacklisted (eval) - was the inspiration for the project.

4\) antisamy-anythinggoes.xml

I don't know of a possible use case for this policy file. If you wanted
to allow every single valid HTML and CSS element (but without JavaScript
or blatant CSS-related phishing attacks), you can use this policy file.
Not even MySpace was *this* crazy. However, it does serve as a good
reference because it contains base rules for every element, so you can
use it as a knowledge base when using tailoring the other policy files.

## Stage 3 - Tailoring the policy file

Smaller organizations may want to deploy AntiSamy in a default
configuration, but it's equally likely that a site may want to have
strict, business-driven rules for what users can allow. The discussion
that decides the tailoring should also consider attack surface - which
grows in relative proportion to the policy file.

You may also want to enable/modify some "directives", which are
basically advanced user options. [This
page](https://github.com/nahsra/antisamy/wiki/AntiSamy-Directives) tells
you what the directives are and which versions support them.

## Stage 4 - Calling the AntiSamy API

Using AntiSamy is easy. Here is an example of invoking AntiSamy with a
policy file:

``` Java
import org.owasp.validator.html.*;

Policy policy = Policy.getInstance(POLICY_FILE_LOCATION);

AntiSamy as = new AntiSamy();
CleanResults cr = as.scan(dirtyInput, policy);

MyUserDAO.storeUserProfile(cr.getCleanHTML()); // some custom function
```

There are a few ways to create a Policy object. The
`getInstance()`{.language-plaintext .highlighter-rouge} method can take
any of the following:

- a String filename
- a File object
- an InputStream

Policy files can also be referenced by filename by passing a second
argument to the AntiSamy:scan() method as the following examples show:

``` Java
AntiSamy as = new AntiSamy();
CleanResults cr = as.scan(dirtyInput, policyFilePath);
```

Finally, policy files can also be referenced by File objects directly in
the second parameter:

``` Java
AntiSamy as = new AntiSamy();
CleanResults cr = as.scan(dirtyInput, new File(policyFilePath));
```

## Stage 5 - Analyzing CleanResults

The CleanResults object provides a lot of useful stuff.

``` Java
getErrorMessages() - a list of String error messages
getCleanHTML() - the clean, safe HTML output
getCleanXMLDocumentFragment() - the clean, safe XMLDocumentFragment which is reflected in getCleanHTML()
getScanTime() - returns the scan time in seconds
```
:::

::: {#sec-related_projects .section .page-body .tab-hidden}

------------------------------------------------------------------------

The following ports of AntiSamy are known to exist:

## Grails

Daniel Bower created a [Grails
plugin](https://github.com/danieldbower/grails-sanitizer) for AntiSamy.
No updates since 2015 however.

2 related projects built on top of the OWASP ESAPI for Java library
(which uses AntiSamy for Java under the hood) are:

- [grails-xss-sanitizer](https://github.com/rpalcolea/grails-xss-sanitizer) -
  This supports Grails 3 and is a port of the following:
- [XssSanitizer](https://github.com/tonyzampogna/XssSanitizer) -
  Supports Grails 2

## .NET

A new (2020+) .NET port of AntiSamy is available at the [OWASP AntiSamy
.NET project](https://github.com/spassarop/antisamy-dotnet/). This
version of AntiSamy is looking for a few good developers to help make it
feature-synchronized with the Java version.

If it doesn't suit your needs, consider [Microsoft's AntiXSS
library](https://archive.codeplex.com/?p=wpl). However, this library is
now end of life too. Microsoft states: "In .NET 4.0 a version of AntiXSS
was included in the framework and could be enabled via configuration. In
ASP.NET v5 a white list based encoder will be the only encoder."

## Python

A port of AntiSamy to Python was attempted, but has been abandoned since
2010. Michael Coates suggests you check out project [Bleach
instead](https://pypi.org/project/bleach/).

## PHP

Although a PHP version was initially planned, we now suggest
[HTMLPurifier](http://htmlpurifier.org/) for safe rich input validation
for PHP applications.
:::
::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-antisamy/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-antisamy){.github-button
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

[![OWASP 20th
Anniversary](../www-project-juice-shop/assets/images/OWASP%2020th%20Anniversary.jpg)](https://20thanniversary.owasp.org/)

### Project Information

- [Builder]{style="font-size:1.0em;padding-left:12px;"}
- [Defender]{style="font-size:1.0em;padding-left:12px;"}

### Code Repository

- [Source code](https://github.com/nahsra/antisamy)

### Downloads

- [Git clone URL](https://github.com/nahsra/antisamy.git)

### Contacts

- [Report an issue](https://github.com/nahsra/antisamy/issues)
- [Contributing](https://github.com/nahsra/antisamy/blob/main/README.md#contributing-to-antisamy)

### Licensing

- [BSD-3-Clause](https://opensource.org/licenses/BSD-3-Clause)

### Leaders

- [Dave
  Wichers](../cdn-cgi/l/email-protection.html#8ce8edfae9a2fbe5efe4e9feffcce3fbedfffca2e3feeb)
  (Maintainer)
- [Sebastian
  Passaro](../cdn-cgi/l/email-protection.html#354650575446415c545b1b4554464654475a755a425446451b5a4752)
  (Maintainer)
- Arshan Dabirsiaghi (Project Lead)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
:::::::::::::
