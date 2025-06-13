:::::::::::::::::::::::::::: main-wrapper
- [Main](#div-main){#main-link .tab-link .current role="tab"
  aria-selected="true" aria-controls="main"}
- [Use](#div-use){#use-link .tab-link role="tab" aria-selected="false"
  aria-controls="use"}
- [News](#div-news){#news-link .tab-link role="tab"
  aria-selected="false" aria-controls="news"}
- [Related Projects](#div-related){#related-link .tab-link role="tab"
  aria-selected="false" aria-controls="related"}
- [Roadmap](#div-roadmap){#roadmap-link .tab-link role="tab"
  aria-selected="false" aria-controls="roadmap"}

# OWASP Java HTML Sanitizer {#owasp-java-html-sanitizer .page-title}

::::::::::::::::::::: {#main .page-body .tab role="tabpanel" aria-labelledby="main-link" tabindex="0"}
::: {#sec-main .section .page-body}
## What is this?

The OWASP HTML Sanitizer Projects provides Java based HTML sanitization
of untrusted HTML!

## About

The OWASP HTML Sanitizer is a fast and easy to configure HTML Sanitizer
written in Java which lets you include HTML authored by third-parties in
your web application while protecting against XSS. The existing
dependencies are on guava and JSR 305. The other jars are only needed by
the test suite. The JSR 305 dependency is a compile-only dependency,
only needed for annotations. This code was written with security best
practices in mind, has an extensive test suite, and has undergone
adversarial security review. A great place to get started using the
OWASP Java HTML Sanitizer is here:
<https://github.com/OWASP/java-html-sanitizer/blob/master/docs/getting_started.md>.

## Benefits

- Very easy to use. It allows for simple programmatic POSITIVE policy
  configuration (see below). No XML config.
- Actively maintained by Mike Samuel from Google's AppSec team!
- Passing 95+% of AntiSamy's unit tests plus many more.
- This is code from the Caja project that was donated by Google. It is
  rather high performance and low memory utilization.
- Java 1.5+
- Provides 4X the speed of
  [AntiSamy](../www-project-antisamy/index.html) sanitization in DOM
  mode and 2X the speed of AntiSamy in SAX mode.

## Questions

- **How was this project tested?** This code was written with security
  best practices in mind, has an extensive test suite, and has undergone
  [adversarial security
  review](https://github.com/OWASP/java-html-sanitizer/blob/master/docs/attack_review_ground_rules.md).
- **How is this project deployed?** This project is best deployed
  through
  [Maven](https://github.com/OWASP/java-html-sanitizer/blob/master/docs/getting_started.md)

## Licensing

The OWASP HTML Sanitizer is free to use and is dual licensed under the
[Apache 2 License](http://www.apache.org/licenses/LICENSE-2.0) and the
[New BSD License](http://opensource.org/licenses/BSD-3-Clause)..
:::

::: {#sec-example .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Example

Put whatever you like here: news, screenshots, features, supporters, or
remove this file and don't use tabs at all.
:::

::::::::::::::: {#sec-use .section .page-body .tab-hidden}

------------------------------------------------------------------------

## How to Use

The project is available at [OWASP HTML Sanitizer : Maven
Central](https://search.maven.org/#search%7Cga%7C1%7Cowasp%20html%20sanitizer)

## Creating a HTML Policy

### 1. Use prepackaged policies {#1-use-prepackaged-policies}

You can view basic prepackaged policies for links, tables, integers,
images at:
<https://github.com/OWASP/java-html-sanitizer/blob/master/src/main/java/org/owasp/html/Sanitizers.java>.

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
`PolicyFactory policy = Sanitizers.FORMATTING.and(Sanitizers.LINKS);`
`String safeHTML = policy.sanitize(untrustedHTML);`
```
:::
::::

### 2. Configure own policy {#2-configure-own-policy}

Check the tests on how to configure your own policy at:
<https://github.com/OWASP/java-html-sanitizer/blob/master/src/test/java/org/owasp/html/HtmlPolicyBuilderTest.java>

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
`PolicyFactory policy = new HtmlPolicyBuilder()`
`   .allowElements("a")`
`   .allowUrlProtocols("https")`
`   .allowAttributes("href").onElements("a")`
`   .requireRelNofollowOnLinks()`
`   .build();`
`String safeHTML = policy.sanitize(untrustedHTML);`
```
:::
::::

### 3. Define custom policies {#3-define-custom-policies}

You can write custom policies :

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
`PolicyFactory policy = new HtmlPolicyBuilder()`
`   .allowElements("p")`
`   .allowElements(`
`       new ElementPolicy() {`
`         public String apply(String elementName, List`<String>` attrs) {`
`           attrs.add("class");`
`           attrs.add("header-" + elementName);`
`           return "div";`
    `         }`
`       }, "h1", "h2", "h3", "h4", "h5", "h6"))`
`   .build();`
`String safeHTML = policy.sanitize(untrustedHTML);`
```
:::
::::

Please note that the elements "a", "font", "img", "input" and "span"
need to be explicitly whitelisted using the \`allowWithoutAttributes()\`
method if you want them to be allowed through the filter when these
elements do not include any attributes.

### 4. Use ebay / slashdot policies {#4-use-ebay--slashdot-policies}

You can also use the default
"[ebay](https://github.com/OWASP/java-html-sanitizer/blob/master/src/main/java/org/owasp/html/examples/EbayPolicyExample.java)"
and "slashdot" policies.

The [Slashdot
policy](https://github.com/OWASP/java-html-sanitizer/blob/master/src/main/java/org/owasp/html/examples/SlashdotPolicyExample.java)
allows the following tags ("a", "p", "div", "i", "b", "em",
"blockquote", "tt", "strong"n "br", "ul", "ol", "li") and only certain
attributes. This policy also allows for the custom slashdot tags,"quote"
and "ecode".

### CSS Sanitization

CSS sanitization is challenging.

We disallow position:sticky and position:fixed so that client code can
use a position:relative;overflow:hidden to contain self-styling
sanitized snippets. Embedders of sanitized content do have to
consistently do that and make sure that contributed content is clearly
demarcated.

Most CSS attacks require a payload to specify selectors which the
sanitizer should not allow. Unproxied images do allow tracking and, by
positioning below the fold, can track whether a user scrolls down.
Embedders do need to use URL rewriting if they allow background styling
and use sensible Referrer-Policy and related headers.

That said, even if care is taken, CSS has a large attack surface, so not
using it puts you in a safer place.

### Inline/Embedded Images

Inline images use the data URI scheme to embed images directly within
web pages. The following describes how to allow inline images in an HTML
Sanitizer policy.

1\) Add the "data" protocol do your whitelist. Se example [how to add
"data"
protocol.](https://www.javadoc.io/doc/com.googlecode.owasp-java-html-sanitizer/owasp-java-html-sanitizer/20160628.1/org/owasp/html/HtmlPolicyBuilder.html#allowUrlProtocols-java.lang.String...-)

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
`.allowUrlProtocols("data")`
```
:::
::::

2\) You can then allow an attribute with an extra check thus

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
`.allowAttributes("src")`
`.matching(...)`
`.onElements("img")`
```
:::
::::

3\) There are a number of things you can do in the matching part such as
allow the following instead of just allowing data.

4\) Since allowUrlProtocols("data") allows data URLs anywhere data URLs
are allowed, you might want to also add a matcher to any other URL
attributes that reject anything with a colon that does not start with
http: or https: or mailto:

:::: {.language-plaintext .highlighter-rouge}
::: highlight
``` highlight
`.allowAttributes("href")`
`.matching(...)`
`.onElements("a")`
```
:::
::::
:::::::::::::::

::: {#sec-news .section .page-body .tab-hidden}

------------------------------------------------------------------------

## News and Events

- \[18 Oct 2021\] v20211018.2 Released - addresses issue with \<select\>
  elements
- \[10 Sep 2020\] Migrate OWASP wiki page
- \[20 Feb 2018\] Update 20180219.1 - addresses iOS/MacOS "text bomb"
- \[28 June 2016\] v20160628.1 Released
- \[14 Apr 2016\] v20160413.1 Released
- \[1 May 2015\] Move to GitHub
- \[2 July 2014\] v239 Released
- \[3 Mar 2014\] v226 Released
- \[5 Feb 2014\] New Wiki
- \[4 Sept 2013\] v209 Released
:::

::: {#sec-related .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Related Projects

- [OWASP JSON Sanitizer](../www-project-json-sanitizer/index.html)
- [OWASP Java Encoder Project](../www-project-java-encoder/index.html)
- [OWASP Dependency Check](../www-project-dependency-check/index.html)
:::

::: {#sec-roadmap .section .page-body .tab-hidden}

------------------------------------------------------------------------

## Roadmap

- Maintaining a fully featured HTML sanitizer is a lot of work. We
  intend to continue to handle community questions and bug reports in a
  very timely manner.
- There are no plans for major new features other than supporting
  incoming requests for advanced sanitization such as additional HTML5
  support.
:::
:::::::::::::::::::::

------------------------------------------------------------------------

::: repo
:::

::: github-buttons
[Watch](https://github.com/owasp/www-project-java-html-sanitizer/subscription){.github-button
icon="octicon-eye" data-size="large" show-count="true"
aria-label="Watch on GitHub"}
[Star](https://github.com/owasp/www-project-java-html-sanitizer){.github-button
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

- [Lab Project]{style="font-size:1.0em;padding-left:12px;"}

  ### Classification

- [ Code Project ]{style="font-size:1.0em;padding-left:12px;"}

  #### Audience

- [Builder]{style="font-size:1.0em;padding-left:12px;"}

- [Defender]{style="font-size:1.0em;padding-left:12px;"}

### Code Repository

- [OWASP HTML Sanitizer at
  GitHub](https://github.com/owasp/java-html-sanitizer)

### Change Log

- For recent release notes, please visit the [changelog on
  GitHub](https://github.com/OWASP/java-html-sanitizer/blob/master/change_log.md).

### Leaders

- [Mike
  Samuel](../cdn-cgi/l/email-protection.html#2d404446485e4c405848416d4a404c4441034e4240)
- [Jim
  Manico](../cdn-cgi/l/email-protection.html#325f535b5e465d08585b5f1c5f535c5b515d725d455341421c5d4055)

:::: owasp-sidebar-bottom
### Upcoming OWASP Global Events

::: {#global-event-div}
:::
::::
::::::
::::::::::::::::::::::::::::
